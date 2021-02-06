---
title: 米国証券取引委員会 (SEC) 規則 17a-4(f)
description: 独立した評価会社は、Azure および Office 365 が金融機関が SEC Rule 17a-4(f) レコード保持および不変ストレージ要件を満たすのに役立つ可能性を検証しました。
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
ms.openlocfilehash: f877bbec76cc0d760f2f908975b3818b88551829
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121206"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>米国証券取引委員会 (SEC) 規則 17a-4(f)

## <a name="about-sec-rule-17a-4f"></a>SEC 規則 17a-4(f) について

米国証券取引委員会 [(SEC)](https://www.sec.gov/) は、米国連邦政府の独立機関であり、米国証券市場の主要監督者および規制当局です。 連邦証券法に対する執行機関を務め、新しい証券規則を提案し、証券業界の市場規制を監督します。

SEC は、電子ストレージ メディアで書籍や記録を保持する規制対象エンティティに対して厳格かつ明示的な要件を定義しています。 証券ブローカー販売業者向けには、保持期間を含む記録保持期間を規制するために [、17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3) および [17 CFR 240.17a-4](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64) を設置しました。 その後 [、SEC](https://www.sec.gov/rules/interp/34-47806.htm) は 17 CFR 240.17a-4 段落 (f) を修正し、特定の条件が満たされている限り、書籍とレコードを電子ストレージ メディアに保持できる 2 つの解釈的なリリースを明示的に発行しました。

電子ストレージ システムは、必要な保持期間のレコードの変更または消去を防止する場合、これらの条件を満たします。 保持期間は、レコードの種類によって 3 ~ 6 年ごとに異なりますが、最初の 2 年間は直ちにアクセシビリティが義務付けされます。 さらに、解釈的なリリースの 1 つは、ストレージ システムが SUBPOENA、法的情報保留、その他の要件に準拠するために、SEC が確立した保持期間を超えてレコードを保持できる必要があります。

## <a name="microsoft-and-sec-rule-17a-4f"></a>Microsoft および SEC 規則 17a-4(f)

金融サービスのお客様は、世界で最も厳しく規制されている業界の 1 つであり、金融取引の保持や、消えられない変更できない状態での関連する通信など、複雑な規定の対象となります。 最も規定的な規則の 17a-4(f) は、電子ストレージ メディア上の書籍や記録の保持を選択する規制対象エンティティに対する厳しい要件を規定する米国セキュリティおよび Exchange 委員会 (SEC) の規則 17a-4(f) です。 保存されるレコードは、指定された保持期間が終了するまで変更または削除する機能を備えず、改ざん防止する必要があります。

ポリシー ロック付き Microsoft Azure 不変 Blob ストレージと保持ロック付き Microsoft Office 365 は、金融機関が SEC Rule 17a-4(f) の不変ストレージ要件を満たすのに役立ちます。

Azure および Office 365 の SEC Rule 17a-4(f) への準拠を評価するために、Microsoft はレコード管理と情報ガバナンスを専門とする独立した評価会社である Cohasset Associates を保持しました。 結果のレポートで、次の情報が表示されます。

- **Azure**: [SEC 17a-4(f) コンプライアンス評価: Microsoft Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)、Cohasset は、時間ベースの BLOB を消去不可で書き換えできない (WORM) 形式で保持するために使用される場合に、ポリシー ロック オプションを使用した Azure [Immutable Blob Storage](/azure/storage/blobs/storage-blob-immutable-storage) が SEC ルールの不変ストレージ要件を満たしていることを検証しました。 各 BLOB (レコード) は、必要な保持期間が終了し、関連する法的情報保留が解放されるまで、変更、上書き、または削除から保護されます。 機密性の高いワークロードを持つソフトウェア プロバイダーとパートナーは、レコードの保持と不変ストレージの 1 つのショップ クラウド ソリューションとして Azure 不変 Blob ストレージを利用できます。 金融機関は、コンプライアンスを維持しながら、これらの機能を活用して独自のアプリケーションを構築できます。
- **Microsoft 365**: [SEC 17a-4(f)](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) の要件に関して、Cohasset は、Microsoft 365 にアーカイブ機能が含まれており、ブローカー販売業者を含む規制対象のお客様がレコード保持のための SEC 要件に準拠する方法でデータを保存できると検証しました。 Microsoft 365 の保持機能は、電子メール、ボイスメール、共有ドキュメント、インスタント メッセージ、サード パーティデータなど、幅広いデータを保持するのに役立ちます。 特に、Microsoft 365 のアーカイブを使用すると、グローバルまたは詳細なメッセージング保持ポリシーを設定して、定義された期間以降のデータを書き換え不可で消去できない形式で保存できます。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

### <a name="azure--sec-rule-17"></a>Azure & SEC Rule 17

[SEC 17a-4(f) & CFTC 1.31 (c-d) Compliance Assessment of Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--sec-rule-17"></a>Office 365 & SEC Rule 17

[SEC 17a-4(f) コンプライアンス評価: Microsoft Security & Compliance Center with SharePoint, OneDrive, Teams, Exchange, and Skype for Business](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=9fa8349d-a0c9-47d9-93ad-472aa0fa44ec&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

## <a name="how-to-implement"></a>実装方法

### <a name="financial-services-regulation"></a>金融サービス規則

クラウド コンピューティングと Microsoft オンライン サービスに関する米国の主要な規制原則のコンプライアンス マップ。 [詳細情報](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

### <a name="risk-assessment--compliance-guide"></a>リスク評価&コンプライアンス ガイド

Microsoft クラウド サービスのリスク評価と規制当局への通知のためのガバナンス モデルを作成します。 [詳細情報](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

### <a name="financial-use-cases"></a>財務上の使用事例

金融サービス用の Azure ソリューションを構築するためのケースの概要、チュートリアル、その他のリソース。 [詳細情報](/azure/industry/financial/)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

## <a name="resources"></a>リソース

- [Microsoft Office 365 でのアーカイブ、データ保持、およびルール 17a-4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
- [コンプライアンス Microsoft Financial Services](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [コンプライアンス プログラム Microsoft ビジネス クラウド サービスと金融サービス](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Azure における金融サービス コンプライアンス](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Azure 金融サービス クラウド リスク評価ツール](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office 365 アイテム保持ポリシー](/office365/securitycompliance/retention-policies)
- [Microsoft 金融サービス コミュニティ](https://techcommunity.microsoft.com/t5/financial-services/ct-p/FinancialServices)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
