---
title: 連邦金融機関審査評議会 (FFIEC)
description: Microsoft は、金融サービスクライアントが連邦金融機関審査評議会 (FFIEC) の監査要件に準拠するのに役立ちます。
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
ms.openlocfilehash: 1830d0d61fe0787d7f8e8034af2e4ca64bdb0bc8
ms.sourcegitcommit: 01938022a292c07e98041dc6ae1312a1b8c617db
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "58261025"
---
# <a name="federal-financial-institutions-examination-council-ffiec"></a>連邦金融機関審査評議会 (FFIEC)

## <a name="ffiec-overview"></a>FFIEC の概要

連邦金融機関審査評議会 (FFIEC) は、米国の金融機関の米国連邦政府審査を担当する 5 つの銀行規制当局で構成される正式な機関間機関です。 FFIEC 審査官教育Office、FFIEC メンバー機関のフィールド審査官を対象とした IT 審査ハンドブックを発行しています。

[FFIEC 監査 IT 審査](https://ithandbook.ffiec.gov/it-booklets/audit.aspx)ハンドブックには、金融機関と TSP の両方の IT 監査プログラムの品質と有効性を評価するためのガイダンスが含まれている。 具体的には、独立した監査レポートの例として、米国公認会計士協会 (AICPA) の SOC 1、SOC 2、および SOC 3 の構成証明レポートに関する言及が含まれます。 ただし、FFIEC では、金融機関は、これらのレポートに含まれる情報だけに依存するのではなく [、FFIEC](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx)アウトソーシング テクノロジ サービス IT 審査ハンドブックで詳細に説明されている検証および監視手順も使用してください。

## <a name="microsoft-and-ffiec"></a>Microsoft および FFIEC

Microsoft Azure、Microsoft Power BI、Microsoft Office 365は、金融機関向けのクラウド サービスの提供という厳しい要件を満たして構築されています。 サポートの一環として、情報技術に関する FFIEC 監査要件と、FFIEC コンプライアンス義務を遵守する際に Azure SOC 構成証明を使用する機能に準拠するためのガイダンスを提供します。

金融機関のクライアントが Azure で FFIEC コンプライアンス要件を満たすのを支援するために、Microsoft は [FFIEC](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint)規制サービス ワークロード向け Azure Security and Compliance Blueprint を開発しました。 Azure クラウド サービスの使用に関するガイダンスと、FFIEC 要件とリスク評価ガイドラインに対する顧客のコンプライアンスに関する考慮事項について説明します。

FFIEC 要件の遵守をさらに支援するために、Microsoft クラウド サービスは、独立した CPA 会社によって作成された [SOC](offering-SOC.md) 構成証明レポートを提供します。 たとえば、SOC 1 Type 2 の構成証明は、SAS 70 を置き換えた AICPA SSAE 18 標準 (AT-C セクション 105 を参照) に基づいており、財務報告の特定のコントロールに関する報告に適しています。 SOC レポートには、指定された監視期間中に関連する制御目標を達成する際の Microsoft コントロールの有効性に関する監査者の意見が含まれます。 金融機関は、Azure、Power BI、および Office 365 に展開された資産に対する FFIEC 固有のコンプライアンス義務を追求する際に、この正式な監査を使用Office 365。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- Azure
- Intune
- Office 365 Office 365米国政府
- Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに搭載されているサービス)

## <a name="azure-dynamics-365-and-ffiec"></a>Azure、Dynamics 365、および FFIEC

Azure、Dynamics 365、その他のオンライン サービスコンプライアンスの詳細については [、「Azure FFIEC 製品」を参照してください](/azure/compliance/offerings/offering-ffiec-us)。

## <a name="office-365-and-ffiec"></a>Office 365および FFIEC

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **商用** | Azure Active Directory、Azure Information Protection、Bookings、Compliance Manager、Exchange Online、Exchange Online Protection、Forms、Kaizala、Microsoft Analytics、Microsoft Booking、Microsoft Defender for Office 365、Microsoft Graph、Microsoft Teams、Microsoft To-Do for Web、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 Cloud App Security、Office 365 Groups、Office 365 セキュリティ/コンプライアンス センター、Office 365 Video、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、StaffHub、Stream、Sway、Yammer Enterprise |
| **GCC** | Azure Active Directory、コンプライアンス マネージャー、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365 監査、レポート、証明書

SOC 構成証明Office 365を参照してください。

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**Microsoft コンプライアンスと SOC 標準を使用して、教育機関の FFIEC コンプライアンス義務を満たできますか?**

これらの義務を満たすために、Microsoft は前述の SOC 標準への準拠に関する詳細を提供します。 ただし、最終的には、サービスが教育機関に適用される特定の法律および規制に準拠するかどうかを判断する必要があります。 また、FFIEC は、「監査レポートまたはレビューのユーザーは、TSP の内部管理環境を検証するために、レポートに含まれる情報だけに依存しなき」と助言しています。 FFIEC IT 審査ハンドブックのアウトソーシング テクノロジ ブック[](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx)レットで詳しい説明に従って、他の検証および監視手順を使用する必要があります。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

### <a name="resources"></a>リソース

- [連邦金融機関審査評議会 (FFIEC)](https://www.ffiec.gov/)
- [米国におけるクラウド コンピューティングと規制原則のコンプライアンス マップ](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- [FFIEC 監査 IT 審査ハンドブック](https://ithandbook.ffiec.gov/it-booklets/audit.aspx)
- [FFIEC アウトソーシング テクノロジ サービス IT 審査ハンドブック](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx)

### <a name="other-microsoft-resources-for-financial-services"></a>金融サービス向けのその他の Microsoft リソース

- [Microsoft 金融サービス コンプライアンス プログラム](https://www.microsoft.com/download/details.aspx?id=55332)
- [Azure における金融サービス コンプライアンス](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Microsoft 法人向けクラウド サービスおよび金融サービス](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [クラウド コンピューティングの共同責任](https://aka.ms/sharedresponsibility)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
