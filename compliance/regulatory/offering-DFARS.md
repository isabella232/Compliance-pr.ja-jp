---
title: 国防連邦取得規則の補足 (DFARS)
description: Microsoft Azure政府は、国防連邦取得規則 (DFARS) の要件をサポートしています。
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
ms.openlocfilehash: e190a98a475d6170e793e92e8052012048cc3d7f
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947901"
---
# <a name="defense-federal-acquisition-regulation-supplement-dfars"></a>国防連邦取得規則の補足 (DFARS)

## <a name="dfars-overview"></a>DFARS の概要

2016 年 10 月 21 日、国防総省 (DoD) は、防衛連邦取得規制補足 (DFARS) を修正し、情報システムが対象防御情報 (CDI) を処理、保存、または送信する防衛請負業者に対して保護およびサイバー インシデント報告義務を課す最終規則を発行しました。  
  
最後の DFARS 条項 252.204-7012 (保護対象防御情報とサイバー インシデント報告) では、サイバー インシデント報告要件とクラウド サービス プロバイダーの追加の考慮事項を含むセーフガードを指定します。 DFARS 252.204-7012 では、すべての DoD 請負業者と防衛産業基盤は、「できるだけ早く実用的だが、2017 年 12 月 31 日より早く」適切なセキュリティのために DFARS 要件に準拠する必要があります。

## <a name="microsoft-and-dfars"></a>Microsoft および DFARS

Microsoft Government Cloud Services は、米国の防衛産業基盤および防衛請負業者のお客様が、クラウド サービス プロバイダーに適用される 252.204-7012 の DFARS 条項に列挙されている DFARS 要件を満たすのに役立ちます。 防衛請負業者が契約で DFARS 条項 252.204-7012 に準拠する必要がある場合、Microsoft は Azure Government および Office 365 米国政府機関のクラウド サービス プロバイダーに適用される要件をサポートできます。 どちらのサービスも、L5 認定を通じて、お客様が DFARS 7012 条項に準拠するために必要な機能を国防総省セキュリティ要件ガイドに対するサポートを示しています。  

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

DoD 影響レベル 5 の対象サービス

- Azure および Azure Government
- Office 365米国政府と米国Office 365国防

## <a name="azure-dynamics-365-and-dfars"></a>Azure、Dynamics 365、DFARS

Azure、Dynamics 365、その他のオンライン サービスコンプライアンスの詳細については [、「Azure DFARS](/azure/compliance/offerings/offering-dfars)の提供」を参照してください。

## <a name="office-365-and-dfars"></a>Office 365 DFARS

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **GCC** | Azure Active Directory、コンプライアンス マネージャー、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream |
| **GCC High** | Azure Active Directory、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business |
| **DoD** | Azure Active Directory、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power BI、SharePoint Online、Skype for Business |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365 監査、レポート、証明書

- [Microsoft Cloud Services の承認](https://marketplace.fedramp.gov/index.html#/products?status=Compliant&sort=productName)
- [その他の監査レポートを見る](https://aka.ms/auditreports)

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**どの DFARS 要件が米国政府機関Office 365サポートされていますか?**

Office 365米国政府機関は、クラウド サービス プロバイダーに適用される 252.204-7012 の DFARS 条項に列挙されている DFARS 要件を、防衛産業基盤および防衛請負業者のお客様が満たします。

**独立した評価者は、米国Office 365が DFARS 要件をサポートしていることを検証しましたか?**

はい、サード パーティの評価組織は、Office 365 米国政府機関のクラウド サービス提供が DFARS 条項 252.204-7012 (未分類の管理技術情報の保護) の該当する要件を満たしていることを証明しています。

**管理された未分類情報 (CUI) と対象となる防御情報 (CDI) の関係は何ですか?**

CUI は、法律、規制、または政府全体のポリシーに従って制御を保護または普及する必要がある情報です。 [CUI レジストリは、](https://www.archives.gov/cui/registry/category-list.html)承認済みの CUI カテゴリとサブカテゴリを識別します。

CDI は、技術的な情報または他の情報 (CUI レジストリに記載されている) を制御し、保護または普及の制御が必要であり、次のいずれかです。

- 契約、タスクオーダー、または配信注文でマークされた、または他の方法で識別され、契約のパフォーマンスに関連して DoD によって、または DoD に代わって請負業者に提供される
- 契約のパフォーマンスをサポートするために、契約者によってまたは代理して収集、開発、受信、送信、使用、または保存される

**すべてのサービスMicrosoft Office 365は、DFARS 規制の下で「対象となる防御情報」に適用される「適切なセキュリティ」要件を満たしていますか?**

2016 年 10 月、国防総省 (DoD) は、情報システムを通じて 「対象となる防御情報」を処理、保存、または送信するすべての DoD 請負業者に適用される、国防連邦取得規制補足 (DFARS) 条項を実装する最終規則を公布しました。 このルールでは、このようなシステムは、NIST SP 800-171、非統合情報システムおよび[](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-171.pdf)組織における制御された未分類情報の保護、または DoD 契約担当者によって承認された「代替的だが、同様に効果的なセキュリティ対策」に記載されているセキュリティ要件を満たす必要があります。 また、DoD の請負業者が外部クラウド サービス プロバイダーを使用して、対象となる防御情報を処理、保存、または送信する場合、そのようなプロバイダーは FedRAMP モデレート ベースラインと同等のセキュリティ要件を満たす必要があります。

次のMicrosoft Office 365クラウド サービスは FedRAMP の中程度の承認を受け取り、DFARS Office 365 米国政府、および米国政府機関Office 365に十分です。

また、DoD の請負業者が「対象となる防御情報」の処理、保存、または送信に使用する可能性がある FedRAMP 認定の境界外の Microsoft 製品は、2017 年 12 月 31 日のコンプライアンス期限を満たす審査を受けています。 Microsoft は、DFARS 関連条項を満たすために、これらの内部および顧客向けサービスが NIST SP 800-171 または許容可能なセキュリティと同等に準拠する方法を文書化しています。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

### <a name="resources"></a>リソース

- [国防連邦取得規則の補足 (DFARS)](https://www.acq.osd.mil/dpap/dars/dfarspgi/current/index.html)
- [Microsoft Cloud for Government](https://enterprise.microsoft.com/industries/government/start-your-microsoft-cloud-for-government-trial-today)
- [オンライン サービスの使用条件](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=31)
- [制御された未分類情報 (CUI)](https://www.archives.gov/cui/registry/category-list)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
