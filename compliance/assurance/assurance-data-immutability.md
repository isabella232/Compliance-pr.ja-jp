---
title: Microsoft 365 のデータの変更可能性
description: Microsoft 365 がデータを検出可能な形式で保持し、規制遵守、内部ガバナンス要件、および訴訟リスクに対処する方法について説明します。
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: da465b850a9216dd64f8e4d9e6450c6a17f7b26d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120666"
---
# <a name="data-immutability-in-microsoft-365"></a>Microsoft 365 のデータの変更可能性

規制コンプライアンス、内部ガバナンスの要件、または訴訟リスクでは、組織は電子メールと関連データを検出可能な形式で保持する必要があります。 システム内のすべてのデータは検出可能である必要があります。破棄または変更できません。 この業界標準の用語は"変更性" です。

一般的に、電子メール メッセージを別の読み取り専用の保存場所に移動することで、従来の変更を行う方法が機能します。 このようなシステムは、メールボックス アイテムを検出のために保持する目的で機能しますが、多くの場合、ユーザーエクスペリエンスに影響を与えるのは、保存されたアイテムを毎日のカスタム ワークフローから削除することで行います。 IT 担当者の場合、この変更を容易に行うには、個別のサーバーとストレージ インフラストラクチャの展開と継続的なメンテナンスが必要です。 検出は、メール システムの外部にあるツールを使用して実行され、関連する展開と保守のコストが含まれます。

Microsoft 365 とそのサービスでのアーカイブのインセット保持および保持ポリシー機能を使用すると、受信データ、内部データ、送信データの多くのクラスを保持および保持できます。 保持されるデータには以下が含まれます。

- 受信メールと送信メールの通信データ
- メール フォームまたはオンラインド共有キュメントに含まれている帳簿や記録
- 会議出席依頼
- FAX
- インスタント メッセージ
- オンライン会議中に共有されたドキュメント
- ボイスメール

さらに、Microsoft は、サードパーティのデータキャプチャおよび管理ソリューション[](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc)との統合を通じて、他のソースからのデータのアーカイブを可能にするためのアドオン機能を開発しました。 サード パーティのデータをインポートした後、次のデータを含む Microsoft 365 コンプライアンス機能をデータに適用できます。

- [訴訟ホールド](/microsoft-365/compliance/create-a-litigation-hold)
- [インプレースの電子情報開示と保持](/microsoft-365/compliance/manage-legal-investigations)
- [コンプライアンス検索](/microsoft-365/compliance/search-for-content)
- [インプレース アーカイブ](/microsoft-365/compliance/enable-archive-mailboxes)
- [メールボックスの監査](/microsoft-365/compliance/enable-mailbox-auditing)
- [アイテム保持ポリシー](/microsoft-365/compliance/retention-policies)

たとえば、メールボックスが訴訟ホールドの対象の場合、サード パーティのデータは保持されます。 電子情報開示またはコンプライアンス検索を使用して、In-Placeデータを検索できます。 また、Microsoft データの場合と同様に、アーカイブ ポリシーとアイテム保持ポリシーをサードパーティのデータに適用できます。 Microsoft 365 でサード パーティのデータをアーカイブすると、組織は政府や規制のポリシーに準拠しつながっています。

Microsoft 365 のアーカイブは、証券取引委員会 (SEC) 規則 17a-4 準拠のストレージを提供します。 Microsoft 365 は、インセット保持ポリシーと保持ロックを含む保持ポリシーを使用して、書き換えできない、消去できない形式で収集されたデータすべての永続ファイルを保持します。

具体的には次のとおりです。

- 上記のアイテム保持ポリシーを使用して保存されたレコードはすべて、通常のユーザーのビューから専用のストレージ領域に保持されます。 権限のあるユーザーのみがこれらのレコードにアクセスして検索できますが、それらのレコードを変更または消去することはできません。
- 各アイテムのメタデータには、保持期間の計算で使用されるタイムスタンプが含まれます。 タイムスタンプは、新しいアイテムを受信または作成するときに適用され、メタデータを変更または削除することはできません。
- Microsoft 365 のアーカイブを使用すると、ユーザーはさまざまなアイテム保持ポリシーを組み合わせてアクションを保持し、詳細なアイテム保持ポリシーを作成できます。 これらのポリシーは、保持されるアイテムの種類または場所、および保持期間を定義します。
- 保持ロック機能を使用すると、ユーザーはポリシーを制限ポリシーにするかどうかを選択できます。 制限の厳しいポリシーは、アイテム保持ポリシーを削除、無効化、または変更する機能をユーザーが持つことを禁止します。 つまり、保持ロックを有効にした後は無効にすることはできません。保持ポリシーによって収集された既存の保管担当者のデータが、保持期間中に上書き、変更、消去、または削除されるメカニズムは存在しません。 また、保持ロックによって設定された保持期間が短縮または短縮されない場合があります。 ただし、前に説明したように、保存されたデータの保持を継続する法的要件がある場合は、時間が長くなる場合があります。 保持ロックを使用すると、管理者や特定の制御アクセス権を持つユーザーも、設定を変更したり、保存されているデータを上書きまたは消去したりし、2003 年の SEC Rule 17a-4 リリースに記載されているガイダンスに従って Microsoft 365 にアーカイブを適用できます。

Microsoft 365 が規制上の義務を果たす上でどのように役立つのか、特にルール 17a-4[](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf)の要件に関して理解するには、Exchange Online Archiving、SharePoint Online、OneDrive for Business、Skype for Business に関するホワイトペーパーを参照してください。 また、ホワイトペーパーでは、SEC Rule 17a-4 の各要件に対する Microsoft 365 アーカイブ機能の詳細な分析を提供し、Microsoft 365 アーカイブを使用してこれらの要件を満たす方法を規制する方法について説明します。
