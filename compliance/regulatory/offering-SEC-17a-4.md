---
title: 証券およびExchange委員会 (SEC) 規則 17a-4(f) 米国
description: 独立した評価会社は、Azure と Office 365 が SEC Rule 17a-4(f) レコードの保持と不変のストレージ要件を満たすのに役立つ可能性を検証しました。
keywords: Microsoft 365、コンプライアンス、サービス
ms.localizationpriority: medium
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 50c44b6801e15af02bf4bfa4f4d46758b7a6c7a8
ms.sourcegitcommit: 70efe7749db2c6dd4ae0faa8ac22da6e87109c79
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/30/2021
ms.locfileid: "58707126"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>証券およびExchange委員会 (SEC) 規則 17a-4(f) 米国

## <a name="about-sec-rule-17a-4f"></a>SEC ルール 17a-4(f) について

米国[証券Exchange委員会 (SEC)](https://www.sec.gov/)は、米国連邦政府の独立機関であり、米国証券市場の主要な監督および規制当局です。 これは、連邦証券法に対する執行機関を制御し、新しい証券ルールを提案し、証券業界の市場規制を監督します。

SEC は、電子ストレージ メディア上の書籍やレコードを保持する規制対象エンティティに対して厳密かつ明示的な要件を定義します。 [17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3)と[17 CFR 240.17a-4](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64)を確立し、証券ブローカー-ディーラの保持期間を含むレコードキーピングを規制しました。 その [後、SEC](https://www.sec.gov/rules/interp/34-47806.htm) は 17 CFR 240.17a-4 段落 (f) を修正し、一定の条件が満たされている限り、書籍とレコードを電子ストレージ メディアに保持するために明示的に 2 つの解釈リリースを発行しました。

電子ストレージ システムは、必要な保持期間のレコードの変更または消去を防止する場合、これらの条件を満たします。 保持期間は、レコードの種類に基づいて 3 年から 6 年までさまざまで、最初の 2 年間は直ちにアクセシビリティが義務付けされます。 さらに、解釈リリースの 1 つは、ストレージ システムが、SUBPOENA、法的保持、または他のそのような要件に準拠するために、SEC で確立された保持期間を超えてレコードを保持できる必要があります。

## <a name="microsoft-and-sec-rule-17a-4f"></a>Microsoft および SEC ルール 17a-4(f)

世界で最も厳しく規制されている業界の 1 つを代表する金融サービスの顧客は、金融取引の保持や、消えられない変更不可の状態での関連する通信など、複雑な規定の対象となります。 最も前例として、電子ストレージ メディアで書籍やレコードを保持する規制対象に対する厳しい要件を規定する米国セキュリティおよび Exchange 委員会 (SEC) の規則 17a-4(f) があります。 保存されるレコードは、指定された保持期間の後まで変更または削除する機能を持つ改ざん防止である必要があります。

Microsoft Azureポリシー ロックStorageおよび保持ロック付き Microsoft Office 365 を使用した不変 Blob Microsoft Office 365 は、金融機関が SEC ルール 17a-4(f) の不変ストレージ要件を満たすのに役立ちます。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="independent-assessments"></a>独立した評価

Azure および Office 365 SEC Rule 17a-4(f) への準拠を評価するために、Microsoft はレコード管理と情報ガバナンスを専門とする独立した評価会社である Cohasset Associates を保持しました。

### <a name="azure"></a>Azure

[Azure BLOB ストレージの不変ストレージ](/azure/storage/blobs/storage-blob-immutable-storage) を使用すると、ユーザーは多くの (WORM) 状態を読み取った後に、ビジネスクリティカルなレコードを書き込みで保存できます。 この状態により、ユーザーが指定した間隔でデータを消去および変更できません。 保持期間の間は、BLOB を作成して読み取りできますが、変更または削除することはできません。 Azure 不変ストレージのこれらの機能は、お客様がレコード保持要件に対処するのに役立ちます。

Microsoft は、レコード管理と情報ガバナンスを専門とする独立したサードパーティの評価会社を保持し、SEC Rule 17a-4(f) 要件に準拠した Azure BLOB ストレージの不変ストレージを評価しました。 結果のレポート *[Cohasset Assessment: Microsoft Azure WORM Storage](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)* 利用できます。

*Azure Blobs* 機能の不変ストレージとロックされた時間ベースのポリシー オプションを持つ Azure Storageは、時間ベースの BLOB (レコード) を消去不可で書き換えできない形式で保持し、満たしているという評価者の意見です。 SEC ルール 17a-4(f)、FINRA [Rule 4511(c)](offering-FINRA-4511.md)の関連ストレージ要件、[および CFTC ルール 1.31(c)-(d)](offering-cftc-1-31-us.md)の原則に基づく要件を示します。

要求に応じて、Microsoft は、電子ストレージ メディアを使用する少なくとも *90* 日前に指定された審査機関に通知するために、SEC 17a-4(f)(2) 要件を満たすために必要な 90 日間のレターを提供します。 規則に記載されている通り、「メンバー、ブローカー、またはディーラは、選択したストレージ メディアが、この段落 (f)(2)に記載されている条件を満たす適切な専門知識を持つ、ストレージ メディアベンダーまたは他の第三者から独自の表現または 1 つを提供する必要があります。 Microsoft *Attestation* of Electronic Storage Media Services for SEC Rule 17a-4 を取得するには [](https://azure.microsoft.com/support/create-ticket/)[、Azure](https://azure.microsoft.com/support/plans/)サポート プランをお持ちのお客様が Azure portal でサポート チケットを作成し、SEC ルール 17a-4 の構成証明レターを要求できます。 このドキュメントでは、Microsoft は SEC 17a-4(f)(2) の要件に関連する保証を提供します。

### <a name="office-365"></a>Office 365

[SEC 17a-4(f)](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d)の要件に対して、Cohasset は Microsoft 365 にアーカイブ機能が含まれており、ブローカー販売店を含む規制対象のお客様が、レコード保持の SEC 要件に準拠する方法でデータを保存できると検証しました。 メール、ボイスメールMicrosoft 365共有ドキュメント、インスタント メッセージ、サードパーティデータなど、さまざまなデータを保持するのに役立ちます。 特に、Microsoft 365 でのアーカイブを使用すると、ユーザーは、グローバルまたは詳細なメッセージング保持ポリシーを設定して、定義された期間以降のデータを書き換え不可の消去可能な形式で保存できます。

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

### <a name="azure--sec-rule-17"></a>Azure & SEC ルール 17

- [SEC 17a-4(f) & CFTC 1.31 (c-d) コンプライアンス評価のAzure Storage](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)

Microsoft *Attestation of electronic Storage Media Services* SEC Rule 17a-4 [](https://azure.microsoft.com/support/create-ticket/)は、Azure サポートを使用してサポート チケットを作成することで [要求できます](https://azure.microsoft.com/support/plans/)。 この構成証明書では、Microsoft は、お客様が SEC 17a-4(f)(2) の要件を遵守するのに役立つ保証を提供します。

### <a name="office-365--sec-rule-17"></a>Office 365 & SEC ルール 17

- [SEC 17a-4(f) コンプライアンス評価: Microsoft セキュリティ & コンプライアンス センター (SharePoint、OneDrive、Teams、Exchange、および Skype for Business](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=2dc92867-5f83-49d8-ad04-9e7295c9e40e&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="how-to-implement"></a>実装方法

### <a name="financial-services-regulation"></a>金融サービス規制

クラウド コンピューティングおよび Microsoft オンライン サービスに関する米国の主要な規制原則のコンプライアンス マップ。 [詳細情報](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

### <a name="risk-assessment--compliance-guide"></a>リスク評価&コンプライアンス ガイド

Microsoft クラウド サービスのリスク評価と規制当局の通知のためのガバナンス モデルを作成します。 [詳細情報](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

### <a name="financial-use-cases"></a>財務上の使用例

ケースの概要、チュートリアル、その他のリソースを使用して、金融サービス用の Azure ソリューションを構築します。 [詳細情報](/azure/industry/financial/)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

## <a name="resources"></a>リソース

- [Azure コンプライアンスのドキュメント](/azure/compliance/)
- [Azure はコンプライアンスの世界を実現する](https://azure.microsoft.com/resources/azure-enables-a-world-of-compliance/)
- [証券およびExchange委員会](https://www.sec.gov/)(SEC) ルール[17a-4](https://www.sec.gov/rules/final/34-38245.txt)
- [Microsoft Cloud の金融サービス リソース](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Microsoft Cloud 金融サービスコンプライアンス プログラム](https://aka.ms/FSCP-Print)
- [クラウド コンピューティングの規制原則と Microsoft オンライン サービスのコンプライアンス マップ](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- [Microsoft Cloud の金融機関のリスク評価とコンプライアンス ガイド](https://azure.microsoft.com/resources/risk-assessment-and-compliance-guide-for-financial-institutions-in-the-microsoft-cloud-/)
- [金融サービス業界の使用例](/azure/industry/financial/)
- [アーカイブ、Microsoft Office 365保持、およびルール 17a-4 でのアーカイブ](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
