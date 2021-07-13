---
title: 証券およびExchange委員会 (SEC) 規則 17a-4(f) 米国
description: 独立した評価会社は、Azure と Office 365 が SEC Rule 17a-4(f) レコードの保持と不変のストレージ要件を満たすのに役立つ可能性を検証しました。
keywords: Microsoft 365、コンプライアンス、サービス
localization_priority: None
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
ms.openlocfilehash: d92fc7b56d2c240588b90afad6a82264fde911c5
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384327"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>証券およびExchange委員会 (SEC) 規則 17a-4(f) 米国

## <a name="about-sec-rule-17a-4f"></a>SEC ルール 17a-4(f) について

米国[証券Exchange委員会 (SEC)](https://www.sec.gov/)は、米国連邦政府の独立機関であり、米国証券市場の主要な監督および規制当局です。 これは、連邦証券法に対する執行機関を制御し、新しい証券ルールを提案し、証券業界の市場規制を監督します。

SEC は、電子ストレージ メディア上の書籍やレコードを保持する規制対象エンティティに対して厳密かつ明示的な要件を定義します。 [17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3)と[17 CFR 240.17a-4](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64)を確立し、証券ブローカー-ディーラの保持期間を含むレコードキーピングを規制しました。 その [後、SEC](https://www.sec.gov/rules/interp/34-47806.htm) は 17 CFR 240.17a-4 段落 (f) を修正し、一定の条件が満たされている限り、書籍とレコードを電子ストレージ メディアに保持するために明示的に 2 つの解釈リリースを発行しました。

電子ストレージ システムは、必要な保持期間のレコードの変更または消去を防止する場合、これらの条件を満たします。 保持期間は、レコードの種類に基づいて 3 年から 6 年までさまざまで、最初の 2 年間は直ちにアクセシビリティが義務付けされます。 さらに、解釈リリースの 1 つは、ストレージ システムが、SUBPOENA、法的保持、または他のそのような要件に準拠するために、SEC で確立された保持期間を超えてレコードを保持できる必要があります。

## <a name="microsoft-and-sec-rule-17a-4f"></a>Microsoft および SEC ルール 17a-4(f)

世界で最も厳しく規制されている業界の 1 つを代表する金融サービスの顧客は、金融取引の保持や、消えられない変更不可の状態での関連する通信など、複雑な規定の対象となります。 最も前例として、電子ストレージ メディアで書籍やレコードを保持する規制対象に対する厳しい要件を規定する米国セキュリティおよび Exchange 委員会 (SEC) の規則 17a-4(f) があります。 保存されるレコードは、指定された保持期間の後まで変更または削除する機能を持つ改ざん防止である必要があります。

Microsoft Azureポリシー ロックStorageおよび保持ロック付き Microsoft Office 365 を使用した不変 Blob Microsoft Office 365 は、金融機関が SEC ルール 17a-4(f) の不変ストレージ要件を満たすのに役立ちます。

Azure および Office 365 SEC Rule 17a-4(f) への準拠を評価するために、Microsoft はレコード管理と情報ガバナンスを専門とする独立した評価会社である Cohasset Associates を保持しました。 結果のレポートでは、次の情報を確認できます。

- **Azure**: [SEC 17a-4(f)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)コンプライアンス評価: Microsoft Azure Storage 、 Cohasset は、時間ベースの BLOB を消去不可で書き換えできない (WORM) 形式で保持するために使用される場合、ポリシー ロック オプションを使用して [Azure Immutable Blob Storage](/azure/storage/blobs/storage-blob-immutable-storage)が SEC ルールの変更できないストレージ要件を満たしていることを検証しました。 各 BLOB (レコード) は、必要な保持期間が満了し、関連付けられた法的保持が解放されるまで、変更、上書き、または削除から保護されます。 機密性の高いワークロードを持つソフトウェア プロバイダーとパートナーは、レコード保持と不変ストレージの 1 つのショップ クラウド ソリューションとして Azure Immutable Blob Storage を利用できます。 金融機関は、コンプライアンスを維持しながら、これらの機能を利用して独自のアプリケーションを構築できます。
- **Microsoft 365**: SEC [17a-4(f)](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d)の要件に対して、Cohasset は Microsoft 365 に、ブローカー-ディーラを含む規制対象の顧客がレコード保持の SEC 要件に準拠する方法でデータを保存できるアーカイブ機能が含まれると検証しました。 メール、ボイスメールMicrosoft 365共有ドキュメント、インスタント メッセージ、サードパーティデータなど、さまざまなデータを保持するのに役立ちます。 特に、Microsoft 365 でのアーカイブを使用すると、ユーザーは、グローバルまたは詳細なメッセージング保持ポリシーを設定して、定義された期間以降のデータを書き換え不可の消去可能な形式で保存できます。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft のスコープ内クラウド プラットフォームと&サービス

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

### <a name="azure--sec-rule-17"></a>Azure & SEC ルール 17

[SEC 17a-4(f) & CFTC 1.31 (c-d) コンプライアンス評価のAzure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--sec-rule-17"></a>Office 365 & SEC ルール 17

[SEC 17a-4(f) コンプライアンス評価: Microsoft セキュリティ & コンプライアンス センター (SharePoint、OneDrive、Teams、Exchange、および Skype for Business](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=2dc92867-5f83-49d8-ad04-9e7295c9e40e&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

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

- [アーカイブ、Microsoft Office 365保持、およびルール 17a-4 でのアーカイブ](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
- [コンプライアンス Microsoft Financial Services](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [コンプライアンス プログラム Microsoft ビジネス クラウド サービスと金融サービス](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Azure における金融サービス コンプライアンス](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Azure 金融サービス クラウド リスク評価ツール](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office 365アイテム保持ポリシー](/office365/securitycompliance/retention-policies)
- [Microsoft Financial Services Community](https://techcommunity.microsoft.com/t5/financial-services/ct-p/FinancialServices)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
