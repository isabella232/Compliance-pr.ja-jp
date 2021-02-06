---
title: Microsoft 365 での SharePoint と OneDrive のデータ復元
description: この記事では、Microsoft 365 の SharePoint と OneDrive のデータ復元の概要について説明します。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 26281e076ea2500a0a4071233b88c2a1f23fe9c5
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120456"
---
# <a name="sharepoint-and-onedrive-data-resiliency-in-microsoft-365"></a>Microsoft 365 での SharePoint と OneDrive のデータ復元

Microsoft 365 では、OneDrive は SharePoint ファイル プラットフォーム上に構築されています。 この記事では、SharePoint のみを使用して両方の製品を参照します。 この記事の内容は Microsoft 365 に関連し、コンシューマー サービスには適用されません。

SharePoint のコア コンテンツ ストレージを構成する主なアセットは 2 種類です。

- **メタデータ**: 各ファイルに関するメタデータは、Azure SQL Database に格納されます。 Azure SQLは、SharePoint が使用する完全なビジネス継続性のストーリーを提供します。詳細については、この記事の後半で説明します。
- **BLOB ストレージ**: SharePoint にアップロードされるユーザー コンテンツは、Azure Storage に格納されます。 SharePoint は、ユーザー コンテンツのほぼリアルタイムの重複と、本当にアクティブ/アクティブなシステムを保証するために、Azure Storage の上にカスタムの復元計画を構築しました。

データの回復性を確保するためのコントロールの完全なセットについては、詳細なセクションで説明します。

## <a name="blob-storage-resilience"></a>BLOB ストレージの復元

SharePoint には、Azure Storage に顧客データを保存するカスタムビルド ソリューションがあります。 すべてのファイルは、プライマリ データセンター リージョンとセカンダリ データセンター リージョンの両方に同時に書き込まれます。 いずれかの Azure 地域への書き込みを失敗すると、ファイルの保存は失敗します。 コンテンツが Azure Storage に書き込まれると、チェックサムはメタデータと別個に格納され、コミットされた書き込みを、今後のすべての読み取り中に SharePoint に送信される元のファイルと同じにするためのものとして使用されます。 この同じ手法をすべてのワークフローで使用して、発生する破損の伝達を防止します。 各地域内で、Azure Locally Redundant Storage (LRS) は高レベルの信頼性を提供します。 詳細については [、Azure Storage の冗長性に関する](/azure/storage/common/storage-redundancy-lrs) 記事を参照してください。

SharePoint はストレージAppend-Only使用します。 このプロセスにより、最初の保存後にファイルを変更したり破損したりすることはできませんが、製品内のバージョン管理を使用すると、以前のバージョンのファイル コンテンツを取得できます。

どちらのデータセンターの SharePoint 環境でも、両方の Azure リージョンのストレージ コンテナーにアクセスできます。 パフォーマンス上の理由から、同じローカル データセンター内のストレージ コンテナーが常に優先されます。ただし、目的のしきい値内に結果が表示されない読み取り要求には、データが常に使用可能なことを確認するためにリモート データセンターから要求されたコンテンツが同じになります。

## <a name="metadata-resilience"></a>メタデータの復元

SharePoint メタデータは、Azure Storage に格納されているコンテンツの場所とアクセス キーを格納するユーザー コンテンツへのアクセスにも重要です。 これらのデータベースは、広範なビジネス継続性SQL Azure SQL [に格納されます](/azure/sql-database/sql-database-business-continuity)。

SharePoint は Azure SQL が提供するレプリケーション モデルを使用し、専用の自動化テクノロジを構築してフェールオーバーが必要かどうかを判断し、必要に応じて操作を開始します。 そのため、Azure の観点から見ると、"手動データベース フェールオーバー" カテゴリSQLされます。 データベースの回復性に関する Azure SQLの指標は、こちらから参照 [できます](/azure/azure-sql/database/business-continuity-high-availability-disaster-recover-hadr-overview#recover-a-database-to-the-existing-server)。

SharePoint は Azure SQLのバックアップ システムを使用して、Point in Time Restores (PITR) を最大 14 日間有効にしています。 PITR については、後のセクションで [詳しい説明を参照してください。](#deletion-backup-and-point-in-time-restore)

## <a name="automated-failover"></a>自動フェールオーバー

SharePoint では、場所固有のイベントが発生した場合のカスタマー エクスペリエンスへの影響を最小限に抑えるために、カスタムビルドの自動フェールオーバーを使用します。 特定のしきい値を超える単一または複数コンポーネントの障害を監視型の自動化が検出すると、問題のある環境からすべてのユーザーのアクティビティが自動的にリダイレクトされ、ウォーム セカンダリにリダイレクトされます。 フェールオーバーによって、メタデータとコンピューティング ストレージが新しいデータセンターから完全に提供されます。 BLOB ストレージは常に完全にアクティブ/アクティブで実行されるので、フェールオーバーに変更を行う必要はありません。 コンピューティング層は最も近い BLOB コンテナーを優先しますが、いつでもローカルとリモートの両方の BLOB ストレージの場所を使用して可用性を確保します。

SharePoint は、Azure フロント ドア サービスを使用して、Microsoft ネットワーク内部へのルーティングを提供します。 この構成により、DNS に依存しないフェールオーバー リダイレクトが可能で、ローカル コンピューターのキャッシュの影響が軽減されます。 ほとんどのフェールオーバー操作はエンド ユーザーに対して透過的です。 フェールオーバーがある場合、お客様はサービスへのアクセスを維持するために変更を加える必要がなされません。

## <a name="versioning-and-files-restore"></a>バージョン管理とファイルの復元

新しく作成されたドキュメント ライブラリの場合、SharePoint は、すべてのファイルで既定で 500 バージョンに設定され、必要に応じてより多くのバージョンを保持するように構成できます。 UI では、100 未満のバージョンを設定できますが、パブリック API を使用して、より少ないバージョンを格納するシステムを設定できます。 信頼性を高め、100 未満の値を指定すると、ユーザー アクティビティが不注意でデータを失う可能性があります。

バージョン管理の詳細については [、「SharePoint でのバージョン管理」を参照してください](/microsoft-365/community/versioning-basics-best-practices)。

ファイルの復元は、SharePoint のドキュメント ライブラリで過去 30 日間の任意の秒に "時間に戻る" 機能です。 このプロセスは、ランサムウェア、大量削除、破損、その他のイベントから回復するために使用できます。 この機能ではファイル バージョンが使用されます。したがって、既定のバージョンを減らすと、この復元の効果が低下します。

OneDrive と SharePoint の両方について、ファイル [の復元](https://support.office.com/article/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15) 機能 [について説明します](https://support.office.com/article/Restore-a-document-library-317791c3-8bd0-4dfd-8254-3ca90883d39a)。

## <a name="deletion-backup-and-point-in-time-restore"></a>削除、バックアップ、およびポイント イン タイムの復元

SharePoint から削除されたユーザー コンテンツは、次の削除フローを通過します。

削除されたアイテムは、一定の期間、ごみ箱に保持されます。 SharePoint の場合、保持期間は 93 日です。 元の場所からアイテムを削除すると開始されます。 サイトのごみ箱からアイテムを削除すると、サイト コレクションのごみ [箱に移動します](https://support.office.com/article/restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b)。 残りの 93 日間はそこに残り、完全に削除されます。 ごみ箱の使い方の詳細については、次のリンクを参照してください。

- [ごみ箱内のアイテムを復元する](https://support.office.com/article/Restore-items-in-the-Recycle-Bin-of-a-SharePoint-site-6df466b6-55f2-4898-8d6e-c0dff851a0be)
- [サイト コレクションのごみ箱から削除済みアイテムを復元します](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b)。

このプロセスは既定の削除フローであり、保持ポリシーやラベルは考慮されません。 詳細については [、「SharePoint と OneDrive の保持について」を参照してください](/microsoft-365/compliance/retention-policies-sharepoint)。

93 日間のリサイクル パイプラインが完了すると、メタデータと Blob ストレージに対して個別に削除が実行されます。 メタデータはデータベースから直ちに削除され、メタデータがバックアップから復元されていない限り、コンテンツは読み取り不能になります。 SharePoint は、メタデータの 14 日間分のバックアップを維持します。 これらのバックアップは、ほぼリアルタイムでローカルに作成され、この文書の時点で 5 分から[](/azure/sql-database/sql-database-automated-backups)10 分のスケジュールで、冗長な Azure Storage コンテナー内のストレージにプッシュされます。

Blob Storage コンテンツを削除する場合、SharePoint は Azure Blob Storage の回復可能な削除機能を利用して、偶発的または悪意のある削除から保護します。 この機能を使用すると、コンテンツが完全に削除される前に、合計 14 日間コンテンツを復元できます。

>[!Note]
>Microsoft アプリケーションは標準プロセスのごみ箱にコンテンツを送信しますが、SharePoint はごみ箱をスキップして直ちに削除を実行できる API を提供します。 アプリケーションを確認して、コンプライアンス上の理由で必要な場合にのみこれが行われるか確認します。

## <a name="integrity-checks"></a>整合性チェック

SharePoint はさまざまな方法を使用して、データ ライフサイクルのすべての段階で BLOB とメタデータの整合性を確保します。

- **メタデータに格納された** ファイル ハッシュ : ファイル全体のハッシュがファイル メタデータと一緒に格納され、すべての操作中にドキュメント レベルのデータ整合性が維持されます。
- **メタデータに格納された BLOB** ハッシュ : 各 BLOB アイテムは、暗号化されたコンテンツのハッシュを格納して、基になる Azure ストレージの破損から保護します。
- **データ整合性ジョブ**: 14 日ごとに、データベース内のアイテムを一覧表示し、それらのアイテムを Azure Storage のリストされた BLOB と照合することで、各サイトの整合性がスキャンされます。 このジョブは、不足しているストレージ BLOB を BLOB 参照として報告し、必要に応じて [Azure](/azure/storage/blobs/soft-delete-blob-overview) ストレージの回復可能な削除機能を使用してそれらの BLOB を取得できます。
