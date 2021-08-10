---
title: Exchange Server での GDPR 対応
description: 削除済みアイテムの保持期間やデータの自動収集など、オンプレミスの Exchange Server での GDPR の要件への対処方法について説明します。
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: MS-Compliance
ms.custom:
- seo-marvel-mar2020
- seo-marvel-apr2020
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: 8c3354405ae0e3b04abd4ec0181eadf1aba7d01496797e869b7d51e4defba472
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292984"
---
# <a name="gdpr-for-exchange-server"></a>Exchange Server での GDPR 対応

個人情報保護の一部として、次のことをお勧めします。

- Exchange Server の[保持タグおよびポリシー](https://technet.microsoft.com/library/dd297955(v=exchg.160).aspx)を使用して、電子メール ライフ サイクル ポリシーを実装します。
- [Information Rights Management](https://technet.microsoft.com/library/dd638140(v=exchg.160).aspx) を展開し、Exchange Server に保存されている情報にアクセスできるユーザーを制限します。
- サーバー上で [BitLocker 暗号化](https://blogs.technet.microsoft.com/exchange/2015/10/20/enabling-bitlocker-on-exchange-servers/)を有効にします。

## <a name="identifying-in-scope-content"></a>範囲内コンテンツの特定

Exchange では、エンド ユーザー生成のコンテンツ用に、メールボックスとパブリック フォルダーの 2 種類のプライマリ ストレージ リポジトリが使用されます。個々のユーザーのメールボックスに保存されるコンテンツは、そのユーザーに一意に関連付けられ、Exchange 内での既定のリポジトリを表します。ユーザー メールボックス内に保存されるデータには、Outlook、Outlook on the web (旧称 Outlook Web App)、Exchange ActiveSync、Skype for Business クライアント、および POP、IMAP または Exchange Web Services (EWS) を使用して Exchange サーバーに接続するサードパーティ ツールで作成されるコンテンツが含まれます。これらのアイテムの例としては、メッセージ、予定表アイテム (会議と予定)、連絡先、メモ、タスクなどがあります。個々のユーザーのメールボックスを削除すると、それぞれのメールボックスのコンテキストの中でユーザーが生成した、またはユーザーに直接送信されたコンテンツが削除されます。ユーザー メールボックスは、Exchange 管理センター (EAC) を使用することにより、または Exchange 管理シェルで [Remove-Mailbox](/powershell/module/exchange/remove-mailbox) コマンドレットを使用することによって削除できます。\
注: Remove-Mailbox コマンドレットの Permanent パラメーターは、慎重に使用してください。このオプションを使用すると、データが回復できなくなります。

Exchange には、共有メールボックスも提供されており、それにより 1 人以上のユーザーが、1 つの共通のメールボックス内に保存されているコンテンツにアクセスして送受信することができます。共有メールボックスは、単一アカウントには関連付けられない一意のエンティティです。むしろ、複数のユーザーに、共有メールボックス内のメール コンテンツの送信、受信、確認のためのアクセス権限が付与されます。共有メールボックスは、Exchange 管理センター、および通常のユーザーのメールボックスの管理に使用されるのと同じコマンドレットを使用して管理されます。メールボックスから個々のメッセージを削除することが必要な場合は、Exchange のバージョンに応じていくつかの異なるオプションがあります。Exchange Server 2010 および 2013 では、[Search-Mailbox](/powershell/module/exchange/search-mailbox) コマンドレットに DeleteContent パラメーターを指定することにより、メールボックスのメッセージを特定し、削除することができます。Exchange Server 2016 以降の場合は、[New-ComplianceSearch](https://technet.microsoft.com/library/ff459253(v=exchg.160).aspx) 機能を使用する必要があります。

パブリック フォルダーは、特定のユーザーに関連付けられていない共有ストレージ実装です。ユーザーには、コンテンツを生成するためのパブリック フォルダーへのアクセス権限が付与されます。パブリック フォルダーの実際の実装は、Exchange のバージョンに応じて異なります (Exchange Server 2010 では Exchange Server 2013 以降とは異なる実装が使用されます)。パブリック フォルダー内のコンテンツを管理するためのツールとしては、限られたものが存在しています。クライアント ツール (Outlook など) は、パブリック フォルダー内のコンテンツを管理するための主要なメカニズムです。パブリック フォルダーのオブジェクトを管理するためのコマンドレットがいくつかありますが、パブリック フォルダー内の個々のコンテンツ アイテムを管理するためのものではありません。パブリック フォルダー内の個々のアイテムを管理するには、Exchange Web Services (EWS) またはその他のサード パーティ ツールを利用するカスタム スクリプトが必要になることが少なくありません。

しばしば主要な要件は、ユーザーの個々のメール ボックスのコンテンツを管理することになります。この要件は、メールボックスを管理するために通常使用するグラフィック ツールまたはコマンドレット ベースのツールにより容易に対応できます。複数のメールボックスまたは複数のリソース タイプのコンテンツを処理することが必要な場合、対象のコンテンツを特定するための Exchange 内の望ましいメカニズムは[電子情報開示](https://technet.microsoft.com/library/dd298021(v=exchg.160).aspx)です。

## <a name="deleted-item-retention"></a>削除済みアイテムの保存期間

メールボックスから (メールボックス全体やパブリック フォルダー リソース自体ではなく) 個々のメッセージまたはアイテムを削除する場合、コンテンツは、メールボックス データベースまたはパブリック フォルダー データベースの DeletedItemRetention パラメーターの値に基づいて、回復可能な形で保持されています。既定値は 14 日間ですが、この値は、Exchange 管理者により設定可能です。

## <a name="removing-soft-deleted-and-disconnected-mailboxes"></a>論理削除されたメールボックスまたは切断されたメールボックスの削除

Exchange メールボックスが無効になっていたり、削除されていたり、データベース間で移動 (負荷分散の一部としてなど) していたりする場合、操作に応じてメールボックスは、無効、論理削除、または切断の状態になります。メールボックスがそれらの状態のうちのいずれかになっている間、Exchange は、メールボックス データベースで指定されている MailboxRetention パラメーターの現行値に基づいてメールボックス (そのコンテンツを含む) を保持します。既定値は 30 日間ですが、この値は Exchange 管理者によって構成可能です。[Remove-StoreMailbox](/powershell/module/exchange/remove-storemailbox) コマンドレットを使用することにより、保持期間が自然に終了する前に、メールボックスの全関連データを Exchange が永久的に削除 (パージ) するように強制することができます。

> [!IMPORTANT]
> Remove-StoreMailbox コマンドレットは、慎重に使用してください。ターゲット メールボックスのデータが失われ、回復不能な状態になります。 

## <a name="on-prem-to-cloud-migrations"></a>オンプレミスからクラウドへの移行

データを Exchange Server から Exchange Online に移行する間、Exchange 管理者により回復可能な形で移行データが元のオンプレミス Exchange Server 上に存在し続ける場合があります。既定では、このデータは 30 日以内にデータベースから自動的に削除されます (前述の「論理削除されたメールボックスまたは切断されたメールボックスの削除」セクションを参照してください)。

## <a name="automatic-data-collection-reported-to-microsoft-by-exchange-server"></a>Exchange Server により Microsoft にレポートされる自動データ収集

オンプレミス環境に展開される Exchange Server では、Microsoft に対する自動レポートやエンド ユーザー データ キャプチャの機能は、どんなタイプのものも提供されません。Windows オペレーティング システムで Watson クラッシュ ダンプ レポート機能が有効になっている Exchange Server は、クラッシュ レポートが生成された時点でのメモリの内容の一部を受け取ることがあります。
