---
title: システムおよび組織管理 (SOC) 2 Type 2
description: Microsoft クラウド サービスが運用セキュリティに関するシステムおよび組織管理 (SOC) 2 Type 2 標準にどのように準拠しているかをご覧ください。
keywords: Microsoft 365、コンプライアンス、サービス
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
ms.openlocfilehash: 99144f348b74ffa15752dbd9ec80ff8fbf17e538
ms.sourcegitcommit: 85b36ce8c79fb111980cc6462f2addb44a924065
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2021
ms.locfileid: "60678444"
---
# <a name="system-and-organization-controls-soc-2-type-2"></a>システムおよび組織管理 (SOC) 2 Type 2

## <a name="soc-2-type-2-overview"></a>SOC 2 Type 2 の概要

サービス組織のシステムおよび組織管理 (SOC) は、米国公認会計士協会 (AICPA) によって作成された内部統制レポートです。 これらは、エンド ユーザーがアウトソーシングされたサービスに関連するリスクを評価および対処するために、サービス組織によって提供されるサービスを調査することを目的としています。

SOC 2 Type 2 認証は次のように実行されます。

- SSAE No. 18、認証基準: 明確化と認識。これには、AT-C セクション 105、*すべての認証業務に共通の概念*、および AT-C セクション 205、*調査業務* (AICPA、専門基準) が含まれます。
- セキュリティ、可用性、処理の整合性、機密性、またはプライバシーに関連するサービス組織での統制の調査に関する SOC 2 報告 (AICPA ガイド)。
- TSP セクション 100、セキュリティ、可用性、処理の整合性、機密性、およびプライバシーに関する 2017 年のトラスト サービス基準 (AICPA、2017 年のトラスト サービス基準)。

さらに、Office 365 SOC 2 Type 2 認証レポートは、クラウド セキュリティ アライアンス (CSA) のクラウド コントロール マトリックス(CCM)、およびドイツ連邦情報セキュリティ局 (BSI) が作成したクラウド コンピューティング コンプライアンス基準カタログ (C5:2020) に記載されている要件に対応しています。

Office 365 SOC 2 認証は、評判の良い公認会計士事務所によって実施された厳格な独立した第三者監査に基づいています。 SOC 2 監査の終了時、監査人は SOC 2 Type 2 報告書で意見を述べます。報告書では、クラウド サービス プロバイダー (CSP) のシステムについて説明し、CSP による自身の制御の説明の正当性を評価します。 また、CSP の制御が適切に設計されているかどうか、指定した日付に実行されていたか、また、指定した期間に正常に運用されていたかも評価します。 Office 365 SOC 2 Type 2 報告書は、システムのセキュリティ、可用性、処理の整合性、機密性、およびプライバシーに関連しています。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

対象となる Microsoft オンライン サービスは、Azure SOC 2 Type 2 認証レポートに示されています。

- Azure (詳細な分析情報については、[Microsoft Azure コンプライアンス サービス](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/)または Azure SOC 2 Type 2 認証レポートを参照してください)
- Azure DevOps (別の [Azure DevOps SOC 2 Type 2 認証レポート](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)を参照してください)
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

## <a name="azure-dynamics-365-and-soc-2"></a>Azure、Dynamics 365、および SOC 2

Azure、Dynamics 365、およびその他のオンライン サービス コンプライアンスの詳細については、[Azure SOC 2 サービス](/azure/compliance/offerings/offering-soc-2)を参照してください。

## <a name="office-365-and-soc-2"></a>Office 365 および SOC 2

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **商用** | コンプライアンス マネージャー、カスタマー ロックボックス、Delve、Exchange Online Protection、Exchange Online、Forms、Griffin、Identity Manager、Lockbox (Torus)、Microsoft Teams、MyAnalytics、Office 365 Customer Portal、Office 365 Microservices (Kaizala、ObjectStore、Sway、PowerPoint Online Document Service、Query Annotation Service、School Data Sync、Siphon、Speech、StaffHub、eXtensible Application Program を含むが、これらに限定されない)、Office Online、Office Services Infrastructure、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、Project Online、カスタマー キーによるサービスの暗号化、SharePoint Online、Skype for Business |
| **GCC** | Azure Active Directory、コンプライアンス マネージャー、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream |
| **GCC High** | Azure Active Directory、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business |
| **DoD** | Azure Active Directory、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power BI、SharePoint Online、Skype for Business |

### <a name="office-365-audit-reports"></a>Office 365 監査レポート

- [Office 365 Core - SSAE 18 SOC 2 報告書](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports)
- [Office 365 Microservices T1 – SSAE 18 SOC2 Type I 報告書](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e2dd6942-e70d-4222-8013-960514742f19&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports)
- [ブリッジ レターおよびその他の監査報告書を参照する](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports)

必要に応じて SOC 1 および SOC 2 の認証レポートとブリッジ レターをダウンロードするには、Office 365 または [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 米国政府に既存のサブスクリプションまたは無料試用版アカウントが必要です。

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**Office 365 SOC レポートが発行される頻度はどれくらいですか?**

Office 365 およびその他のオンライン サービスの SOC レポートは、12 か月毎の実行間隔 (監査期間) に基づいており、半年ごとに新たな報告書が発行されます (期限は 3 月 31 日と 9 月 30 日)。 *ブリッジ レター* は四半期ごとに発行され、過去 3 か月間をカバーします。 たとえば、1 月のレターは 10 月 1 日から 12 月 31 日まで、4 月のレターは 1 月 1 日から 3 月 31 日まで、7 月のレターは 4 月 1 日から 6 月 30 日まで、10 月のレターは 7 月 1 日から 9 月 30 日までをカバーします。

**ブリッジ レターを含む Office 365 SOC 監査ドキュメントはどこで入手できますか?**

監査文書へのリンクについては、監査レポートのセクションを参照してください。 ログインするには、Office 365 または [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 米国政府に既存のサブスクリプションまたは無料試用版アカウントが必要です。 監査証明書、評価レポート、およびその他の該当するドキュメントをダウンロードして、独自の規制要件に役立てることができます。

**クラウド セキュリティ アライアンス CCM 制御の実装の評価はどこにありますか?**

Office 365 SOC 2 Type 2 の監査は、米国公認会計士協会 (AICPA) のトラスト サービスの原則と基準に基づき、セキュリティ、可用性、機密性、プライバシー、および処理の整合性と、クラウド セキュリティ アライアンス (CSA) のクラウド コントロール マトリックス (CCM) の基準について評価します。 AICPA 基準と、CCM で規定されている要件の両方を満たすことが目的です。 Office 365 SOC 2 Type 2 監査には、CSA STAR 認証で要求される CCM 制御の評価が組み込まれています。 詳細については、Office 365 SOC 2 Type 2 認証レポートを参照してください。

**記載されている例外に対する管理対応はどこで確認できますか?**

管理対応は、SOC 認証レポートの終わり近くにあります。 ドキュメントで「管理対応」を検索します。

**ユーザー エンティティの責任はどこで確認できますか?**

ユーザー エンティティの責任は、SOC 認証レポートの最後にあります。 ドキュメントで「ユーザー エンティティの責任」を検索します。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

### <a name="resources"></a>リソース

- [Service Trust Portal 監査レポート](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [サービス組織のための AICPA SOC](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/socforserviceorganizations.html)
- [SSAE No. 18、認証基準: 明確化と再策定 (AICPA プロフェッショナル標準)](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)
- [セキュリティ、可用性、処理の完全性、機密性またはプライバシーに関わる、サービス組織の全般統制の検査に関する SOC 2 レポート (AICPA ガイド)](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL) (購入可能)
- [TSP セクション 100 (AICPA、2017 Trust Services Criteria)](https://www.aicpa.org/content/dam/aicpa/interestareas/frc/assuranceadvisoryservices/downloadabledocuments/trust-services-criteria.pdf)
