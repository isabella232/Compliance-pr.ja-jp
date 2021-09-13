---
title: システムおよび組織管理 (SOC) 1 Type 2
description: Microsoft クラウド サービスが運用セキュリティに関するシステムおよび組織管理 (SOC) 1 Type 2 標準にどのように準拠しているかをご覧ください。
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
ms.openlocfilehash: 8c374ce340538e4030e0cd07a2bdbe0aa4f4615d
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59161167"
---
# <a name="system-and-organization-controls-soc-1-type-2"></a>システムおよび組織管理 (SOC) 1 Type 2

## <a name="soc-1-type-2-overview"></a>SOC 1 Type 2 の概要

サービス組織のシステムおよび組織管理 (SOC) は、米国公認会計士協会 (AICPA) によって作成された内部統制レポートです。 これらは、エンド ユーザーがアウトソーシングされたサービスに関連するリスクを評価および対処するために、サービス組織によって提供されるサービスを調査することを目的としています。

SOC 1 Type 2 認証は次のように実行されます。

- SSAE No. 18、認証基準: 明確化と認識。これには、AT-C セクション 320、*財務報告に対するユーザー エンティティの内部統制に関連するサービス組織での統制の調査に関する報告* (AICPA、専門基準) が含まれます。
- 財務報告に対するユーザー エンティティの内部統制に関連するサービス組織での統制の調査に関する SOC 1 報告 (AICPA ガイド)。

認証業務の基準 18 (SSAE 18) に関する AICPA ステートメントとは別に、Office 365 SOC 1 Type 2 監査は、保証業務に関する国際基準 No. に従って実施されます。 3402 (ISAE 3402)。 SOC 1 認証は SAS 70 に取って代わり、財務報告に対するユーザー エンティティの内部統制に関連するサービス組織での管理に関する報告に適しています。 Type 2 報告書には、指定された監視期間中に関連する管理目標を達成するための管理の有効性に関する監査人の意見が含まれています。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

対象となる Microsoft オンライン サービスは、Azure SOC 1 Type 2 認証レポートに示されています。

- Azure (詳細な分析情報については、[Microsoft Azure コンプライアンス サービス](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/)または Azure SOC 1 Type 2 認証レポートを参照してください)
- Azure DevOps (別の Azure DevOps SOC 1 Type 2 認証レポートを参照してください)
- Dynamics 365 (詳細な分析情報については、Azure SOC 1 Type 2 認証レポートを参照してください)
- Microsoft 365 Defender
- Microsoft Cloud App Security (MCAS)
- Microsoft Defender for Endpoint (以前の Microsoft Defender Advanced Threat Protection)
- Microsoft Defender for Identity (以前の Azure Advanced Threat Protection)
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

## <a name="azure-dynamics-365-and-soc-1"></a>Azure、Dynamics 365、および SOC 1

Azure、Dynamics 365、およびその他のオンライン サービス コンプライアンスの詳細については、[Azure SOC 1 サービス](/azure/compliance/offerings/offering-soc-1)を参照してください。

## <a name="office-365-and-soc-1"></a>Office 365 および SOC 1

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **商用** | コンプライアンス マネージャー、カスタマー ロックボックス、Delve、Exchange Online Protection、Exchange Online、Forms、Griffin、Identity Manager、Lockbox (Torus)、Microsoft Teams、MyAnalytics、Office 365 Customer Portal、Office 365 Microservices (Kaizala、ObjectStore、Sway、PowerPoint Online Document Service、Query Annotation Service、School Data Sync、Siphon、Speech、StaffHub、eXtensible Application Program を含むがこれらに限定されない)、Office Online、Office Services Infrastructure、OneDrive for Business、Planner、PowerApps、Power BI、Project Online、カスタマー キーによるサービスの暗号化、SharePoint Online、Skype for Business |
| **GCC** | Azure Active Directory、コンプライアンス マネージャー、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream |
| **GCC High** | Azure Active Directory、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business |
| **DoD** | Azure Active Directory、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power BI、SharePoint Online、Skype for Business |

### <a name="office-365-audit-reports"></a>Office 365 監査レポート

- [Office 365 Core - SSAE 18 SOC 1 報告書](https://aka.ms/o365SOC-1)
- ブリッジ レターおよびその他の監査報告書を参照する

必要に応じて SOC 1 および SOC 2 の認証レポートとブリッジ レターをダウンロードするには、Office 365 または Office 365 米国政府に既存のサブスクリプションまたは無料試用版アカウントが必要です。

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**Office 365 SOC レポートが発行される頻度はどれくらいですか?**

Office 365 およびその他のオンライン サービスの SOC レポートは、12 か月毎の実行間隔 (監査期間) に基づいており、半年ごとに新たな報告書が発行されます (期限は 3 月 31 日と 9 月 30 日)。 *ブリッジ レター* は四半期ごとに発行され、過去 3 か月間をカバーします。 たとえば、1 月のレターは 10 月 1 日から 12 月 31 日まで、4 月のレターは 1 月 1 日から 3 月 31 日まで、7 月のレターは 4 月 1 日から 6 月 30 日まで、10 月のレターは 7 月 1 日から 9 月 30 日までをカバーします。

**お客様は Office 365 SOC 1 Type 2 認証からどのように利益を得ることができますか?**

お客様は、Sarbanes-Oxley (SOX)、Federal Financial Institutions Examination Council (FFIEC)、グラム リーチ ブライリー法 (GLBA) など、独自の金融業界固有のコンプライアンス要件を追求する場合、Office 365 SOC 1 Type 2 認証を使用できます。

**ブリッジ レターを含む Office 365 SOC 監査文書はどこで入手できますか?**

監査文書へのリンクについては、監査レポートのセクションを参照してください。 ログインするには、Office 365 または Office 365 米国政府に既存のサブスクリプションまたは無料試用版アカウントが必要です。 監査証明書、評価レポート、およびその他の該当するドキュメントをダウンロードして、独自の規制要件に役立てることができます。

**記載されている例外に対する管理対応はどこで確認できますか?**

管理対応は、SOC 認証レポートの終わり近くにあります。 ドキュメントで「管理対応」を検索します。

**ユーザー エンティティの責任はどこで確認できますか?**

ユーザー エンティティの責任は、SOC 認証レポートの最後にあります。 ドキュメントで「ユーザー エンティティの責任」を検索します。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

### <a name="resources"></a>リソース

- [Service Trust Portal 監査レポート](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [SSAE No. 18、認証基準: 明確化と認識](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)
- [財務報告に対するユーザー エンティティの内部統制に関連するサービス組織での統制の調査に関する SOC 1 報告 (AICPA ガイド)](https://future.aicpa.org/cpe-learning/publication/reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-user-entities-internal-control-over-financial-reporting-soc-1-guide-OPL) (購入可能)
