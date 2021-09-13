---
title: データの入力がMicrosoft 365
description: 規制コンプライアンスMicrosoft 365内部ガバナンス要件、訴訟リスクに対処するために、データを検出可能な形式で保持する方法について説明します。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e17685c7d927ab8188abe1ef4dae4d2cdf0f3764
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160327"
---
# <a name="data-immutability-in-microsoft-365"></a>データの入力がMicrosoft 365

規制コンプライアンス、内部ガバナンス要件、または訴訟リスクでは、組織は電子メールと関連データを検出可能な形式で保持する必要があります。 システム内のすべてのデータは検出可能である必要があります。また、それらのデータのいずれも破棄または変更できません。 この業界標準の用語は"immutability" です。

一般的に、電子メール メッセージを別の読み取り専用の保存場所に移動することで、従来の使い方を変更できます。 このようなシステムは、メールボックス アイテムを検出のために保存する目的で使用しますが、通常の日常のワークフローから保持されたアイテムを削除することで、ユーザー エクスペリエンスに影響を与える場合があります。 IT 担当者の場合、この使い勝手の良い方法では、別のサーバーとストレージ インフラストラクチャの展開と継続的なメンテナンスが必要です。 検出は、メール システム外部のツールを使用して実行され、関連する展開とメンテナンスのコストが含まれます。

Microsoft 365 とそのサービスでのアーカイブの一元的な保持と保存ポリシー機能を使用すると、受信データ、内部データ、および送信データの多くのクラスを保持および保持できます。 保持されるデータには以下が含まれます。

- 受信メールと送信メールの通信データ
- メール フォームまたはオンラインド共有キュメントに含まれている帳簿や記録
- 会議出席依頼
- FAX
- インスタント メッセージ
- オンライン会議中に共有されたドキュメント
- ボイスメール

さらに、Microsoft は、サードパーティのデータキャプチャおよび管理ソリューション[](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc)との統合を通じて、他のソースからのデータのアーカイブを可能にするためのアドオン機能を開発しました。 サード パーティのデータをインポートした後、次のMicrosoft 365コンプライアンス機能をデータに適用できます。

- [訴訟ホールド](/microsoft-365/compliance/create-a-litigation-hold)
- [インプレースの電子情報開示と保持](/microsoft-365/compliance/manage-legal-investigations)
- [コンプライアンス検索](/microsoft-365/compliance/search-for-content)
- [インプレース アーカイブ](/microsoft-365/compliance/enable-archive-mailboxes)
- [メールボックスの監査](/microsoft-365/compliance/enable-mailbox-auditing)
- [アイテム保持ポリシー](/microsoft-365/compliance/retention-policies)

たとえば、メールボックスが訴訟ホールドに置かれると、サード パーティのデータが保持されます。 電子情報開示またはコンプライアンス検索を使用して、In-Placeデータを検索できます。 または、Microsoft データの場合と同様に、アーカイブポリシーと保持ポリシーをサードパーティのデータに適用できます。 サードパーティ のデータをアーカイブMicrosoft 365、組織が政府および規制ポリシーに準拠しつ付けるのに役立ちます。

ドキュメントのアーカイブMicrosoft 365は、証券Exchange委員会 (SEC) ルール 17a-4 に準拠したストレージを提供します。 Microsoft 365保持ポリシーと保存ポリシー (保存ロックを含む) を使用して、書き換え不可で消去できない形式で収集されたデータの永続的なファイルを保持します。

特に次のような場合です。

- 上記の保持ポリシーを使用して保存されたレコードはすべて、通常のユーザーのビューから専用の記憶域に保持されます。 承認されたユーザーのみがこれらのレコードにアクセスして検索できますが、変更または消去することはできません。
- 各アイテムのメタデータには、保持期間の計算で使用されるタイムスタンプが含まれます。 タイムスタンプは、新しいアイテムを受信または作成するときに適用され、メタデータから変更または削除することはできません。
- ユーザーは、Microsoft 365保持ポリシーを組み合わせ、アクションを保持して詳細な保持ポリシーを作成できます。 これらのポリシーは、保持されるアイテムの種類または場所と保存期間を定義します。
- 保持ロック機能を使用すると、ユーザーはポリシーを制限ポリシーにするかどうかを選択できます。 制限付きポリシーでは、保持ポリシーを削除、無効化、または変更する機能を誰もが持つことを禁止します。 つまり、保持ロックを有効にすると、無効にすることはできません。保持ポリシーによって収集された既存の保管担当者のデータが、保存期間中に上書き、変更、消去、または削除されるメカニズムは存在しません。 また、保持ロックによって設定された保持期間を短縮または減少できない場合があります。 ただし、上記に示したように、保存されたデータの保持を継続する法的要件がある場合は、長くすることができます。 保持ロックを使用すると、管理者や特定の制御アクセス権を持つユーザーも、設定を変更したり、保存されているデータを上書きまたは消去したりし、2003 年リリースの SEC ルール 17a-4 に記載されているガイダンスに従って Microsoft 365 にアーカイブを適用できます。

Microsoft 365 が規制上の義務を果たす上でどのように役立つのか(特にルール 17a-4 の要件に[](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf)関連して)理解するには、Exchange Online Archiving、SharePoint Online、OneDrive for Business、および Skype for Business をカバーするホワイトペーパーを参照してください。 また、ホワイトペーパーでは、SEC Rule 17a-4 の各要件に対する Microsoft 365 アーカイブ機能の詳細な分析を提供し、Microsoft 365 アーカイブによってこれらの要件を満たす方法を規制された顧客に示します。
