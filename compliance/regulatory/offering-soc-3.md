---
title: システムと組織管理 (SOC) 3
description: Microsoft クラウド サービスが運用セキュリティに関する「システムと組織管理 (SOC) 3 標準」にどのように準拠しているか説明します。
keywords: Microsoft 365、コンプライアンス、オファリング
localization_priority: Priority
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
ms.openlocfilehash: 1d6f6b0a4c9bd3ebbccb90331a8cf17df7ff8928
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385769"
---
# <a name="system-and-organization-controls-soc-3"></a><span data-ttu-id="d9255-104">システムと組織管理 (SOC) 3</span><span class="sxs-lookup"><span data-stu-id="d9255-104">System and Organization Controls (SOC) 3</span></span>

## <a name="soc-3-overview"></a><span data-ttu-id="d9255-105">SOC 3 の概要</span><span class="sxs-lookup"><span data-stu-id="d9255-105">SOC 3 overview</span></span>

<span data-ttu-id="d9255-106">サービス提供組織におけるシステムと組織管理 (SOC) は、米国公認会計士協会 (AICPA) によって作成された内部統制レポートです。</span><span class="sxs-lookup"><span data-stu-id="d9255-106">System and Organization Controls (SOC) for Service Organizations are internal control reports created by the American Institute of Certified Public Accountants (AICPA).</span></span> <span data-ttu-id="d9255-107">これらはサービス組織によって提供されるサービス内容を調査することを意図しています。従って、外注したサービスに関するリスクについて、エンドユーザーが評価し、対処できます。</span><span class="sxs-lookup"><span data-stu-id="d9255-107">They are intended to examine services provided by a service organization so that end users can assess and address the risk associated with an outsourced service.</span></span>

<span data-ttu-id="d9255-108">*SOC 3 サービス組織のためのSOC: サービスの信頼基準についての一般向けのレポート* は、SOC 2 Type 2 注意喚起レポートの短い公開バージョンです。セキュリティ、可用性、処理の完全性、機密性またはプライバシーに関するサービス組織の管理について確実な認識を必要とするが、完全な SOC 2 レポートは必要ないユーザー向けです。</span><span class="sxs-lookup"><span data-stu-id="d9255-108">*SOC 3 SOC for Service Organizations: Trust Services Criteria for General Use Report* is a short, publicly facing version of the SOC 2 Type 2 attestation report for users who need assurances about service organization's controls relevant to Security, Availability, Processing Integrity, Confidentiality, or Privacy but do not need a full SOC 2 report.</span></span> <span data-ttu-id="d9255-109">SOC 3 レポートは一般向けのレポートであるため、自由に配布できます。</span><span class="sxs-lookup"><span data-stu-id="d9255-109">Because SOC 3 reports are general use reports, they can be freely distributed.</span></span>

<span data-ttu-id="d9255-110">SOC 3 レポートには、サービス組織の管理者により記述された、責任を持つことに対応した統制力の有効性を考慮した主張を含みます。それは適用可能なサービス信頼基準と、管理者の主張が公正に述べられているかどうかについてのサービス監査人の意見を元にしています。</span><span class="sxs-lookup"><span data-stu-id="d9255-110">A SOC 3 report contains a written assertion by service organization management regarding control effectiveness to achieve commitments based on the applicable trust services criteria, as well as service auditor's opinion on whether management's assertion is stated fairly.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="d9255-111">Microsoft が提供範囲とするクラウド プラットフォームとサービス</span><span class="sxs-lookup"><span data-stu-id="d9255-111">Microsoft in-scope cloud platforms & services</span></span>

<span data-ttu-id="d9255-112">Microsoft が提供範囲とするサービスは、「[Azure SOC 2 Type 2 認証レポート](offering-soc-2.md)」に示されています。</span><span class="sxs-lookup"><span data-stu-id="d9255-112">Microsoft in-scope services are shown in the Azure [SOC 2 Type 2 attestation](offering-soc-2.md) report.</span></span>

- <span data-ttu-id="d9255-113">Azure (詳細な分析情報については、[Microsoft Azure コンプライアンス オファリング](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/) または Azure SOC 2 Type 2 認証レポートを参照してください)</span><span class="sxs-lookup"><span data-stu-id="d9255-113">Azure (for detailed insight, see [Microsoft Azure Compliance Offerings](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/) or Azure SOC 2 Type 2 attestation report)</span></span>
- <span data-ttu-id="d9255-114">Dynamics 365 (詳細な分析情報については、Azure SOC 2 Type 2 認証レポートを参照してください)</span><span class="sxs-lookup"><span data-stu-id="d9255-114">Dynamics 365 (for detailed insight, see Azure SOC 2 Type 2 attestation report)</span></span>
- <span data-ttu-id="d9255-115">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d9255-115">Microsoft 365 Defender</span></span>
- <span data-ttu-id="d9255-116">Microsoft Cloud App Security (MCAS)</span><span class="sxs-lookup"><span data-stu-id="d9255-116">Microsoft Cloud App Security (MCAS)</span></span>
- <span data-ttu-id="d9255-117">Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="d9255-117">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="d9255-118">Microsoft Defender for Identity</span><span class="sxs-lookup"><span data-stu-id="d9255-118">Microsoft Defender for Identity</span></span>
- <span data-ttu-id="d9255-119">Microsoft Forms Pro (Azure Government の対象外)</span><span class="sxs-lookup"><span data-stu-id="d9255-119">Microsoft Forms Pro (not in scope for Azure Government)</span></span>
- <span data-ttu-id="d9255-120">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="d9255-120">Microsoft Graph</span></span>
- <span data-ttu-id="d9255-121">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="d9255-121">Microsoft Intune</span></span>
- <span data-ttu-id="d9255-122">Microsoft マネージド デスクトップ (Azure Government の対象外)</span><span class="sxs-lookup"><span data-stu-id="d9255-122">Microsoft Managed Desktop (not in scope for Azure Government)</span></span>
- <span data-ttu-id="d9255-123">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="d9255-123">Microsoft Stream</span></span>
- <span data-ttu-id="d9255-124">Microsoft 脅威エキスパート (Azure Government の対象外)</span><span class="sxs-lookup"><span data-stu-id="d9255-124">Microsoft Threat Experts (not in scope for Azure Government)</span></span>
- <span data-ttu-id="d9255-125">Nomination Portal</span><span class="sxs-lookup"><span data-stu-id="d9255-125">Nomination Portal</span></span>
- <span data-ttu-id="d9255-126">Office 365、Office 365 U.S. Government、Office 365 U.S. Government - High、Office 365 U.S. Government Defense</span><span class="sxs-lookup"><span data-stu-id="d9255-126">Office 365, Office 365 U.S. Government, Office 365 U.S. Government - High, Office 365 U.S. Government Defense</span></span>
- <span data-ttu-id="d9255-127">Power Apps</span><span class="sxs-lookup"><span data-stu-id="d9255-127">Power Apps</span></span>
- <span data-ttu-id="d9255-128">Power Automate</span><span class="sxs-lookup"><span data-stu-id="d9255-128">Power Automate</span></span>
- <span data-ttu-id="d9255-129">Power BI</span><span class="sxs-lookup"><span data-stu-id="d9255-129">Power BI</span></span>
- <span data-ttu-id="d9255-130">Power Virtual Agents (Azure Government の対象外)</span><span class="sxs-lookup"><span data-stu-id="d9255-130">Power Virtual Agents (not in scope for Azure Government)</span></span>
- <span data-ttu-id="d9255-131">Update Compliance (Azure Government の対象外)</span><span class="sxs-lookup"><span data-stu-id="d9255-131">Update Compliance (not in scope for Azure Government)</span></span>

## <a name="azure-dynamics-365-and-soc-3"></a><span data-ttu-id="d9255-132">Azure、Dynamics 365、および SOC 3</span><span class="sxs-lookup"><span data-stu-id="d9255-132">Azure, Dynamics 365, and SOC 3</span></span>

<span data-ttu-id="d9255-133">Azure、Dynamics 365、およびその他のオンライン サービス コンプライアンスの詳細情報については、[Azure SOC 3 オファリング](/azure/compliance/offerings/offering-soc-3)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9255-133">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure SOC 3 offering](/azure/compliance/offerings/offering-soc-3).</span></span>

## <a name="office-365-and-soc-3"></a><span data-ttu-id="d9255-134">Office 365 および SOC 3</span><span class="sxs-lookup"><span data-stu-id="d9255-134">Office 365 and SOC 3</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="d9255-135">Office 365 クラウド環境</span><span class="sxs-lookup"><span data-stu-id="d9255-135">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="d9255-136">Office 365 の適用性と範囲内のサービス</span><span class="sxs-lookup"><span data-stu-id="d9255-136">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="d9255-137">以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。</span><span class="sxs-lookup"><span data-stu-id="d9255-137">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="d9255-138">**適用性**</span><span class="sxs-lookup"><span data-stu-id="d9255-138">**Applicability**</span></span> | <span data-ttu-id="d9255-139">**範囲内のサービス**</span><span class="sxs-lookup"><span data-stu-id="d9255-139">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="d9255-140">**Office 365**</span><span class="sxs-lookup"><span data-stu-id="d9255-140">**Office 365**</span></span> | <span data-ttu-id="d9255-141">コンプライアンス マネージャー、カスタマー ロックボックス、Delve、Exchange Online Protection、Exchange Online、Forms、Griffin、Identity Manager、Lockbox (Torus)、Microsoft Teams、MyAnalytics、Office 365 Customer Portal、Office 365 Microservices (Kaizala、ObjectStore、Sway、PowerPoint Online Document Service、Query Annotation Service、School Data Sync、Siphon、Speech、StaffHub、eXtensible Application Program を含むが、これらに限定されない)、Office Online、Office Services Infrastructure、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、Project Online、カスタマー キーによるサービスの暗号化、SharePoint Online、Skype for Business</span><span class="sxs-lookup"><span data-stu-id="d9255-141">Compliance Manager, Customer Lockbox, Delve, Exchange Online Protection, Exchange Online, Forms, Griffin, Identity Manager, Lockbox (Torus), Microsoft Teams, MyAnalytics, Office 365 Customer Portal, Office 365 Microservices (including but not limited to Kaizala, ObjectStore, Sway, PowerPoint Online Document Service, Query Annotation Service, School Data Sync, Siphon, Speech, StaffHub, eXtensible Application Program), Office Online, Office Services Infrastructure, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, Project Online, Service Encryption with Customer Key, SharePoint Online, Skype for Business</span></span> |
| <span data-ttu-id="d9255-142">**GCC**</span><span class="sxs-lookup"><span data-stu-id="d9255-142">**GCC**</span></span> | <span data-ttu-id="d9255-143">Azure Active Directory、コンプライアンス マネージャー、Delve、Exchange Online、</span><span class="sxs-lookup"><span data-stu-id="d9255-143">Azure Active Directory, Compliance Manager, Delve, Exchange Online,</span></span> 
<span data-ttu-id="d9255-144">、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream</span><span class="sxs-lookup"><span data-stu-id="d9255-144">, Microsoft Defender for Office 365, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business, Stream</span></span> |
| <span data-ttu-id="d9255-145">**GCC High**</span><span class="sxs-lookup"><span data-stu-id="d9255-145">**GCC High**</span></span> | <span data-ttu-id="d9255-146">Azure Active Directory、Exchange Online、Flow、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business</span><span class="sxs-lookup"><span data-stu-id="d9255-146">Azure Active Directory, Exchange Online, Flow, Microsoft Defender for Office 365, Microsoft Teams, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business</span></span> |
| <span data-ttu-id="d9255-147">**DoD**</span><span class="sxs-lookup"><span data-stu-id="d9255-147">**DoD**</span></span> | <span data-ttu-id="d9255-148">Azure Active Directory、Exchange Online、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power Automate、Power BI、SharePoint Online、Skype for Business</span><span class="sxs-lookup"><span data-stu-id="d9255-148">Azure Active Directory, Exchange Online, Microsoft Defender for Office 365, Microsoft Teams, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, Power Automate, Power BI, SharePoint Online, Skype for Business</span></span> |

### <a name="office-365-audit-reports"></a><span data-ttu-id="d9255-149">Office 365 監査レポート</span><span class="sxs-lookup"><span data-stu-id="d9255-149">Office 365 audit reports</span></span>

- [<span data-ttu-id="d9255-150">Office 365 Core - SSAE 18 SOC 3 レポート</span><span class="sxs-lookup"><span data-stu-id="d9255-150">Office 365 Core - SSAE 18 SOC 3 Report</span></span>](https://aka.ms/o365SOC-3)
- [<span data-ttu-id="d9255-151">ブリッジ レターおよびその他の監査レポートを参照する</span><span class="sxs-lookup"><span data-stu-id="d9255-151">See bridge letters and additional audit reports</span></span>](https://aka.ms/auditreports)

<span data-ttu-id="d9255-152">必要に応じて SOC 1 および SOC 2 の認証レポートと任意のブリッジ レターをダウンロードするには、Office 365 または Office 365 U.S. Government に既存のサブスクリプションまたは無料試用版アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="d9255-152">You must have an existing subscription or free trial account in Office 365 or Office 365 U.S. Government to download SOC 1 and SOC 2 attestation reports and any bridge letters as needed.</span></span>

### <a name="frequently-asked-questions"></a><span data-ttu-id="d9255-153">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="d9255-153">Frequently asked questions</span></span>

<span data-ttu-id="d9255-154">**Office 365 SOC レポートが発行される頻度はどれくらいですか?**</span><span class="sxs-lookup"><span data-stu-id="d9255-154">**How often are Office 365 SOC reports issued?**</span></span>

<span data-ttu-id="d9255-155">Office 365 およびその他のオンライン サービスの SOC レポートは、12 か月毎の実行間隔 (監査期間) に基づいており、半年ごとに新たな報告書が発行されます (期限は 3 月 31 日と 9 月 30 日)。</span><span class="sxs-lookup"><span data-stu-id="d9255-155">SOC reports for Office 365 and other online services are based on a rolling 12-month run window (audit period) with new reports issued semi-annually (period ends are March 31 and September 30).</span></span> <span data-ttu-id="d9255-156">*ブリッジ レター* は四半期ごとに発行され、過去 3 か月間をカバーします。</span><span class="sxs-lookup"><span data-stu-id="d9255-156">*Bridge letters* are issued each quarter to cover the prior three-month period.</span></span> <span data-ttu-id="d9255-157">たとえば、1 月のレターは 10 月 1 日から 12 月 31 日まで、4 月のレターは 1 月 1 日から 3 月 31 日まで、7 月のレターは 4 月 1 日から 6 月 30 日まで、10 月のレターは 7 月 1 日から 9 月 30 日までをカバーします。</span><span class="sxs-lookup"><span data-stu-id="d9255-157">For example, the January letter covers 1-Oct through 31-Dec, the April letter covers 1-Jan through 31-Mar, the July letter covers 1-Apr through 30-Jun, and the October letter covers 1-Jul through 30-Sep.</span></span>

<span data-ttu-id="d9255-158">**ブリッジ レターを含む Office 365 SOC 監査ドキュメントはどこで入手できますか?**</span><span class="sxs-lookup"><span data-stu-id="d9255-158">**Where can I get the Office 365 SOC audit documentation including bridge letters?**</span></span> <span data-ttu-id="d9255-159">監査ドキュメントへのリンクについては、監査レポートのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9255-159">For links to audit documentation, see the audit report section.</span></span> <span data-ttu-id="d9255-160">ログインするには、Office 365 または [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 U.S. Government に既存のサブスクリプションまたは無料試用版アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="d9255-160">You must have an existing subscription or free trial account in Office 365or [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 U.S. Government to login.</span></span> <span data-ttu-id="d9255-161">監査証明書、評価レポート、およびその他の該当するドキュメントをダウンロードして、独自の規制要件に役立てることができます。</span><span class="sxs-lookup"><span data-stu-id="d9255-161">You can then download audit certificates, assessment reports, and other applicable documents to help you with your own regulatory requirements.</span></span>

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="d9255-162">Microsoft コンプライアンス マネージャーを使用してリスクを評価する</span><span class="sxs-lookup"><span data-stu-id="d9255-162">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="d9255-163">[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d9255-163">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="d9255-164">コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="d9255-164">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="d9255-165">コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。</span><span class="sxs-lookup"><span data-stu-id="d9255-165">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="d9255-166">[コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。</span><span class="sxs-lookup"><span data-stu-id="d9255-166">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

### <a name="resources"></a><span data-ttu-id="d9255-167">リソース</span><span class="sxs-lookup"><span data-stu-id="d9255-167">Resources</span></span>

- [<span data-ttu-id="d9255-168">Service Trust Portal 監査レポート</span><span class="sxs-lookup"><span data-stu-id="d9255-168">Service Trust Portal audit reports</span></span>](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [<span data-ttu-id="d9255-169">サービス組織のための AICPA SOC</span><span class="sxs-lookup"><span data-stu-id="d9255-169">AICPA SOC for Service Organizations</span></span>](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/socforserviceorganizations.html)
- [<span data-ttu-id="d9255-170">SSAE No. 18、認証基準: 明確化と再策定 (AICPA プロフェッショナル標準)</span><span class="sxs-lookup"><span data-stu-id="d9255-170">SSAE No. 18, Attestation Standards: Clarification and Recodification (AICPA Professional Standards)</span></span>](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)
- <span data-ttu-id="d9255-171">[セキュリティ、可用性、処理の完全性、機密性またはプライバシーに関わる、サービス組織の全般統制の検査に関する SOC 2 レポート (AICPA ガイド)](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL) (購入可能)</span><span class="sxs-lookup"><span data-stu-id="d9255-171">[SOC 2 Reporting on an Examination of Controls at a Service Organization Relevant to Security, Availability, Processing Integrity, Confidentiality, or Privacy (AICPA Guide)](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL) (available for purchase)</span></span>
- [<span data-ttu-id="d9255-172">TSP セクション 100 (AICPA、2017 Trust Services Criteria)</span><span class="sxs-lookup"><span data-stu-id="d9255-172">TSP section 100 (AICPA, 2017 Trust Services Criteria)</span></span>](https://www.aicpa.org/content/dam/aicpa/interestareas/frc/assuranceadvisoryservices/downloadabledocuments/trust-services-criteria.pdf)
