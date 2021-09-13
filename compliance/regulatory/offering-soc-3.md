---
title: システムと組織管理 (SOC) 3
description: Microsoft クラウド サービスが運用セキュリティに関する「システムと組織管理 (SOC) 3 標準」にどのように準拠しているか説明します。
keywords: Microsoft 365、コンプライアンス、オファリング
ms.localizationpriority: high
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
ms.openlocfilehash: b3690ba79ba8adca1d01e4eda03831c431747d01
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59161116"
---
# <a name="system-and-organization-controls-soc-3"></a>システムと組織管理 (SOC) 3

## <a name="soc-3-overview"></a>SOC 3 の概要

サービス提供組織におけるシステムと組織管理 (SOC) は、米国公認会計士協会 (AICPA) によって作成された内部統制レポートです。 これらはサービス組織によって提供されるサービス内容を調査することを意図しています。従って、外注したサービスに関するリスクについて、エンドユーザーが評価し、対処できます。

*SOC 3 サービス組織のためのSOC: サービスの信頼基準についての一般向けのレポート* は、SOC 2 Type 2 注意喚起レポートの短い公開バージョンです。セキュリティ、可用性、処理の完全性、機密性またはプライバシーに関するサービス組織の管理について確実な認識を必要とするが、完全な SOC 2 レポートは必要ないユーザー向けです。 SOC 3 レポートは一般向けのレポートであるため、自由に配布できます。

SOC 3 レポートには、サービス組織の管理者により記述された、責任を持つことに対応した統制力の有効性を考慮した主張を含みます。それは適用可能なサービス信頼基準と、管理者の主張が公正に述べられているかどうかについてのサービス監査人の意見を元にしています。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft が提供範囲とするクラウド プラットフォームとサービス

Microsoft が提供範囲とするサービスは、「[Azure SOC 2 Type 2 認証レポート](offering-soc-2.md)」に示されています。

- Azure (詳細な分析情報については、[Microsoft Azure コンプライアンス オファリング](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/) または Azure SOC 2 Type 2 認証レポートを参照してください)
- Dynamics 365 (詳細な分析情報については、Azure SOC 2 Type 2 認証レポートを参照してください)
- Microsoft 365 Defender
- Microsoft Cloud App Security (MCAS)
- Microsoft Defender for Endpoint
- Microsoft Defender for Identity
- Microsoft Forms Pro (Azure Government の対象外)
- Microsoft Graph
- Microsoft Intune
- Microsoft マネージド デスクトップ (Azure Government の対象外)
- Microsoft Stream
- Microsoft 脅威エキスパート (Azure Government の対象外)
- Nomination Portal
- Office 365、Office 365 U.S. Government、Office 365 U.S. Government - High、Office 365 U.S. Government Defense
- Power Apps
- Power Automate
- Power BI
- Power Virtual Agents (Azure Government の対象外)
- Update Compliance (Azure Government の対象外)

## <a name="azure-dynamics-365-and-soc-3"></a>Azure、Dynamics 365、および SOC 3

Azure、Dynamics 365、およびその他のオンライン サービス コンプライアンスの詳細情報については、[Azure SOC 3 オファリング](/azure/compliance/offerings/offering-soc-3)を参照してください。

## <a name="office-365-and-soc-3"></a>Office 365 および SOC 3

### <a name="office-365-cloud-environments"></a>Office 365 クラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **商用** | コンプライアンス マネージャー、カスタマー ロックボックス、Delve、Exchange Online Protection、Exchange Online、Forms、Griffin、Identity Manager、Lockbox (Torus)、Microsoft Teams、MyAnalytics、Office 365 Customer Portal、Office 365 Microservices (Kaizala、ObjectStore、Sway、PowerPoint Online Document Service、Query Annotation Service、School Data Sync、Siphon、Speech、StaffHub、eXtensible Application Program を含むが、これらに限定されない)、Office Online、Office Services Infrastructure、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、Project Online、カスタマー キーによるサービスの暗号化、SharePoint Online、Skype for Business |
| **GCC** | Azure Active Directory、コンプライアンス マネージャー、Delve、Exchange Online、 
、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream |
| **GCC High** | Azure Active Directory、Exchange Online、Flow、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business |
| **DoD** | Azure Active Directory、Exchange Online、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power Automate、Power BI、SharePoint Online、Skype for Business |

### <a name="office-365-audit-reports"></a>Office 365 監査レポート

- [Office 365 Core - SSAE 18 SOC 3 レポート](https://aka.ms/o365SOC-3)
- [ブリッジ レターおよびその他の監査レポートを参照する](https://aka.ms/auditreports)

必要に応じて SOC 1 および SOC 2 の認証レポートと任意のブリッジ レターをダウンロードするには、Office 365 または Office 365 U.S. Government に既存のサブスクリプションまたは無料試用版アカウントが必要です。

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**Office 365 SOC レポートが発行される頻度はどれくらいですか?**

Office 365 およびその他のオンライン サービスの SOC レポートは、12 か月毎の実行間隔 (監査期間) に基づいており、半年ごとに新たな報告書が発行されます (期限は 3 月 31 日と 9 月 30 日)。 *ブリッジ レター* は四半期ごとに発行され、過去 3 か月間をカバーします。 たとえば、1 月のレターは 10 月 1 日から 12 月 31 日まで、4 月のレターは 1 月 1 日から 3 月 31 日まで、7 月のレターは 4 月 1 日から 6 月 30 日まで、10 月のレターは 7 月 1 日から 9 月 30 日までをカバーします。

**ブリッジ レターを含む Office 365 SOC 監査ドキュメントはどこで入手できますか?** 監査ドキュメントへのリンクについては、監査レポートのセクションを参照してください。 ログインするには、Office 365 または [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 U.S. Government に既存のサブスクリプションまたは無料試用版アカウントが必要です。 監査証明書、評価レポート、およびその他の該当するドキュメントをダウンロードして、独自の規制要件に役立てることができます。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

### <a name="resources"></a>リソース

- [Service Trust Portal 監査レポート](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [サービス組織のための AICPA SOC](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/socforserviceorganizations.html)
- [SSAE No. 18、認証基準: 明確化と再策定 (AICPA プロフェッショナル標準)](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)
- [セキュリティ、可用性、処理の完全性、機密性またはプライバシーに関わる、サービス組織の全般統制の検査に関する SOC 2 レポート (AICPA ガイド)](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL) (購入可能)
- [TSP セクション 100 (AICPA、2017 Trust Services Criteria)](https://www.aicpa.org/content/dam/aicpa/interestareas/frc/assuranceadvisoryservices/downloadabledocuments/trust-services-criteria.pdf)
