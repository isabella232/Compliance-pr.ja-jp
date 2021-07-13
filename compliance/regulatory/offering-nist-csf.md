---
title: 国立標準技術研究所 (NIST) サイバーセキュリティ フレームワーク (CSF)
description: Microsoft Cloud Services は、国立標準技術研究所 (NIST) のサイバーセキュリティ フレームワーク (CSF) を満たしています。
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
ms.openlocfilehash: 9080474699eae7e65d8df86638a9250ec7127585
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385677"
---
# <a name="national-institute-of-standards-and-technology-nist-cybersecurity-framework-csf"></a>国立標準技術研究所 (NIST) サイバーセキュリティ フレームワーク (CSF)

## <a name="nist-csf-overview"></a>NIST CSF の概要

国立標準技術研究所 (NIST) は、組織がリスクを評価するのに役立つ測定基準とガイダンスを推進し、維持しています。 連邦ネットワークと重要なインフラストラクチャのサイバーセキュリティ強化に関するエグゼクティブ オーダー 13636 に対応して、NIST は 2014 年 2 月に重要なインフラストラクチャ サイバーセキュリティの向上のためのフレームワーク (FICIC) をリリースしました。

FICIC の主な優先事項は、企業がビジネス効率を高めながら、サイバーセキュリティ リスクを管理するための一連の標準とプラクティスを確立することでした。 NIST Framework は、政府機関と民間組織の両方に追加の規制要件を課さずに、サイバーセキュリティ リスクに対応します。

FICIC は、NIST の重要なインフラストラクチャサイバーセキュリティを改善するフレームワークの付録 A に記載されている NIST SP 800-53 を含む、グローバルに認識されている標準を [参照しています](https://www.nist.gov/publications/framework-improving-critical-infrastructure-cybersecurity-version-11)。 FICIC フレームワーク内の各コントロールは、FedRAMP モデレート ベースライン内の対応する NIST 800-53 コントロールにマップされます。

## <a name="microsoft-and-the-nist-csf"></a>Microsoft と NIST CSF

NIST Cybersecurity Framework (CSF) は、サイバーセキュリティ関連のリスクを管理するための標準、ガイドライン、ベスト プラクティスで構成される自主的なフレームワークです。 Microsoft Cloud サービスは、独立したサードパーティの FedRAMP モデレートおよびハイ ベースライン監査を受け、FedRAMP 標準に従って認定されています。 また、セキュリティおよびプライバシー基準の開発および認定の主要組織である HITRUST が実施する検証済みの評価を通じて、Office 365 は NIST CSF で指定された目標に認定されています。

コンプライアンス スコアと Azure Security and Compliance Blueprint を使用して NIST サイバーセキュリティ フレームワークの展開を加速する方法について説明します。

- [NIST SP 800-53 R4 ブループリント サンプルの概要](/azure/governance/blueprints/samples/nist-sp-800-53-rev4/)
- [コンプライアンス スコアの NIST CSF 評価の詳細については、「Office 365」を参照してください。](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/New-NIST-CSF-and-CSA-CCM-assessments-available-in-Compliance/ba-p/218554)

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft のスコープ内クラウド プラットフォームと&サービス

- Azure Government
- Dynamics 365 for Government
- Office 365

## <a name="azure-dynamics-365-and-nist-csf"></a>Azure、Dynamics 365、および NIST CSF

Azure、Dynamics 365、その他のオンライン サービスのコンプライアンスの詳細については [、「Azure NIST CSF](/azure/compliance/offerings/offering-nist-csf)の提供」を参照してください。

## <a name="office-365-and-nist-csf"></a>Office 365 NIST CSF

### <a name="office-365-cloud-environments"></a>Office 365クラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365とスコープ内サービス

次の表を使用して、サービスとサブスクリプションOffice 365を決定します。

| **適用対象** | **スコープ内サービス** |
|:------------------|:----------------------|
| **Office 365** | アクティビティ フィード サービス、Bing サービス、Delve、Exchange Online、インテリジェント サービス、Microsoft Teams、Office 365 カスタマー ポータル、Office Online、Office サービス インフラストラクチャ、Office 利用状況レポート、OneDrive for Business、People Card、SharePoint Online、Skype for Business、Windows Ink |

### <a name="office-365-audit-cycle-and-certification"></a>Office 365監査サイクルと認定

NIST CSF 認定Office 365 2 年間有効です。

- [Office 365NIST CSF 認定書](https://aka.ms/O365NISTCSFcertification)

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**独立した評価者は、NIST CSF Office 365サポートしていることを検証しましたか?**

はい、Office 365 2019 年 7 月に HITRUST から[NIST CSF](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=2a472d92-7c3b-47e0-9ae7-0f539da31f42&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)認定書を取得しました。

**Microsoft Cloud Services は、フレームワークへの準拠を実証する方法を説明します。**

第三者が FedRAMP 認定のために作成した正式な監査レポートを使用して、Microsoft は、これらのレポートに示されている関連するコントロールが、重要なインフラストラクチャサイバーセキュリティを向上させる NIST Framework への準拠を示す方法を示します。 Microsoft によって実装された監査されたコントロールは、Microsoft の責任として識別された Azure、Office 365、および Dynamics 365 によって保存、処理、および送信されるデータの機密性、整合性、可用性を確保するために機能します。

**このイニシアチブへの準拠を維持するための Microsoft の責任は何ですか?**

FICIC への参加は任意です。 ただし、Microsoft は、Office 365オンライン サービス条項および該当するサービス レベル契約で定義されている条件を満たします。

**組織で Microsoft のコンプライアンスを使用できますか?**

はい。 FedRAMP 標準に対する独立したサード パーティのコンプライアンス レポートは、Microsoft が Microsoft Cloud Services のセキュリティとプライバシーを維持するために実装したコントロールの有効性を証明します。 Microsoft のお客様は、これらの関連レポートに記載されている監査されたコントロールを、独自の FedRAMP および NIST FICIC のリスク分析と資格の取り組みの一環として使用できます。

**米国政府が重要なインフラストラクチャと見なす組織**

ホームランドセキュリティ[](https://www.dhs.gov/critical-infrastructure-sectors)省によると、これらには、化学、商業施設、通信、重要な製造、ダム、防衛産業基盤、緊急サービス、エネルギー、金融サービス、食料と農業、政府機関、医療と公衆衛生、情報技術、核(リアクターの材料と廃棄物)、輸送システムと水(および廃水)の組織が含まれます。

**一部のOffice 365サービスが、この認定の対象ではない理由**

Microsoft は、他のクラウド サービス プロバイダーと比較して最も包括的なサービスを提供します。 地域や業界全体にわたる広範なコンプライアンスの提供に対応するために、市場の需要、顧客からのフィードバック、製品ライフサイクルに基づく保証の取り組みの範囲にサービスが含まれます。 特定のコンプライアンスサービスの現在の範囲にサービスが含まれていない場合、組織は、コンプライアンス義務に基づいてリスクを評価し、そのサービスでデータを処理する方法を決定する責任があります。 お客様からのフィードバックを継続的に収集し、規制当局や監査人と一緒に取り組み、お客様のセキュリティとコンプライアンスのニーズに合わせてコンプライアンス範囲を拡大します。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

### <a name="resources"></a>リソース

- [Microsoft Cloud Services の承認](https://marketplace.fedramp.gov/index.html#/products?status=Compliant&sort=productName)
- [Microsoft Cyber Offerings のマッピング: NIST サイバーセキュリティ フレームワーク (CSF)、CIS コントロール、ISO27001:2013、HITRUST CSF](https://go.microsoft.com/fwlink/p/?linkid=2074025)
- [重要なインフラストラクチャのサイバーセキュリティを改善するフレームワーク](https://www.nist.gov/publications/framework-improving-critical-infrastructure-cybersecurity-version-11)
- [連邦ネットワークと重要なインフラストラクチャのサイバーセキュリティ強化に関する大統領執行命令](https://www.whitehouse.gov/the-press-office/2017/05/11/presidential-executive-order-strengthening-cybersecurity-federal)
- [Microsoft Government クラウド](https://go.microsoft.com/fwlink/p/?linkid=2087246)
- [オンライン サービスの使用条件](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=31)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
