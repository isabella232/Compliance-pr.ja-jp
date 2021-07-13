---
title: NIST SP 800-171
description: Microsoft クラウド サービスは NIST SP 800-171 ガイドラインに準拠し、非プラットフォーム情報システムで制御された未分類情報 (CUI) を保護します。
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
ms.openlocfilehash: 19b312d1b9f31683d775049010d390710554df01
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385667"
---
# <a name="nist-sp-800-171"></a><span data-ttu-id="dc9a2-104">NIST SP 800-171</span><span class="sxs-lookup"><span data-stu-id="dc9a2-104">NIST SP 800-171</span></span>

## <a name="about-nist-sp-800-171"></a><span data-ttu-id="dc9a2-105">NIST SP 800-171 について</span><span class="sxs-lookup"><span data-stu-id="dc9a2-105">About NIST SP 800-171</span></span>

<span data-ttu-id="dc9a2-106">米国国立標準技術研究所 (NIST) は、連邦政府機関の情報および情報システムの保護に役立つ測定基準とガイドラインを推進し、維持しています。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-106">The US National Institute of Standards and Technology (NIST) promotes and maintains measurement standards and guidelines to help protect the information and information systems of federal agencies.</span></span> <span data-ttu-id="dc9a2-107">管理された未分類情報 (CUI) の管理に関するエグゼクティブ オーダー 13556 に応答して [、NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final) *、非* 分類情報システムおよび組織で制御された未分類情報の保護を公開しました。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-107">In response to Executive Order 13556 on managing controlled unclassified information (CUI), it published [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final), *Protecting Controlled Unclassified Information In Nonfederal Information Systems and Organizations*.</span></span> <span data-ttu-id="dc9a2-108">CUI は、デジタルと物理の両方の情報として定義され、政府 (またはその代わりにエンティティ) によって作成され、分類されていないが依然として機密性が高く、保護が必要です。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-108">CUI is defined as information, both digital and physical, created by a government (or an entity on its behalf) that, while not classified, is still sensitive and requires protection.</span></span>

<span data-ttu-id="dc9a2-109">NIST SP 800-171 は、もともと 2015 年 6 月に公開され、その後、進化するサイバー脅威に対応して何度も更新されています。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-109">NIST SP 800-171 was originally published in June 2015 and has been updated several times since then in response to evolving cyberthreats.</span></span> <span data-ttu-id="dc9a2-110">CUI に安全にアクセスし、送信し、非公式の情報システムおよび組織に保存する方法に関するガイドラインを提供します。要件は、次の 4 つの主要なカテゴリに分類されます。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-110">It provides guidelines on how CUI should be securely accessed, transmitted, and stored in nonfederal information systems and organizations; its requirements fall into four main categories:</span></span>

- <span data-ttu-id="dc9a2-111">管理と保護のためのコントロールとプロセス</span><span class="sxs-lookup"><span data-stu-id="dc9a2-111">Controls and processes for managing and protecting</span></span>
- <span data-ttu-id="dc9a2-112">IT システムの監視と管理</span><span class="sxs-lookup"><span data-stu-id="dc9a2-112">Monitoring and management of IT systems</span></span>
- <span data-ttu-id="dc9a2-113">エンド ユーザーの明確なプラクティスと手順</span><span class="sxs-lookup"><span data-stu-id="dc9a2-113">Clear practices and procedures for end users</span></span>
- <span data-ttu-id="dc9a2-114">技術的および物理的なセキュリティ対策の実装</span><span class="sxs-lookup"><span data-stu-id="dc9a2-114">Implementation of technological and physical security measures</span></span>

## <a name="microsoft-and-nist-sp-800-171"></a><span data-ttu-id="dc9a2-115">Microsoft および NIST SP 800-171</span><span class="sxs-lookup"><span data-stu-id="dc9a2-115">Microsoft and NIST SP 800-171</span></span>

<span data-ttu-id="dc9a2-116">認定されたサード パーティの評価組織である Kratos Secureinfo および Coalfire は、Microsoft と提携して、スコープ内クラウド サービスが CUI を処理する際に、非統合情報システムおよび組織の NIST SP 800-171「Protecting Controlled *Unclassified Information (CUI)」* の条件を満たしているのを証明しました。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-116">Accredited third-party assessment organizations, Kratos Secureinfo and Coalfire, partnered with Microsoft to attest that its in-scope cloud services meet the criteria in NIST SP 800-171, *Protecting Controlled Unclassified Information (CUI) in Nonfederal Information Systems and Organizations*, when they process CUI.</span></span> <span data-ttu-id="dc9a2-117">[FedRAMP](offering-fedramp.md)要件の Microsoft の実装は、Microsoft のスコープ内クラウド サービスが、既に導入されているシステムとプラクティスを使用して NIST SP 800-171 の要件を満たすか、それを超える要件を満たしていることを確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-117">The [Microsoft implementation of FedRAMP](offering-fedramp.md) requirements help ensure Microsoft in-scope cloud services meet or exceed the requirements of NIST SP 800-171 using the systems and practices already in place.</span></span>

<span data-ttu-id="dc9a2-118">NIST SP 800-171 の要件は、FedRAMP が使用する標準である NIST SP 800-53 のサブセットです。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-118">NIST SP 800-171 requirements are a subset of NIST SP 800-53, the standard that FedRAMP uses.</span></span> <span data-ttu-id="dc9a2-119">NIST SP 800-171 の付録 D は、CUI セキュリティ要件を、FedRAMP プログラムの下で既に評価および承認されている NIST SP 800-53 の関連するセキュリティ制御に直接マッピングします。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-119">Appendix D of NIST SP 800-171 provides a direct mapping of its CUI security requirements to the relevant security controls in NIST SP 800-53, for which the in-scope cloud services have already been assessed and authorized under the FedRAMP program.</span></span>

<span data-ttu-id="dc9a2-120">米国政府の CUI (研究機関、コンサルティング会社、製造請負業者) を処理または保存するエンティティは、NIST SP 800-171 の厳しい要件に準拠する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-120">Any entity that processes or stores US government CUI — research institutions, consulting companies, manufacturing contractors, must comply with the stringent requirements of NIST SP 800-171.</span></span> <span data-ttu-id="dc9a2-121">この構成証明により、Microsoft のスコープ内クラウド サービスは、Microsoft が完全に準拠しているという保証を受け、CUI ワークロードの展開を探しているお客様に対応できます。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-121">This attestation means Microsoft in-scope cloud services can accommodate customers looking to deploy CUI workloads with the assurance that Microsoft is in full compliance.</span></span> <span data-ttu-id="dc9a2-122">たとえば、情報システムでスコープ内の Microsoft クラウド サービスを使用して「対象となる防御情報」を処理、保存、または送信するすべての DoD 請負業者は、NIST SP 800-171 のセキュリティ要件に準拠する必要がある米国国防総省 DFARS 条項を満たしています。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-122">For example, all DoD contractors who process, store, or transmit 'covered defense information' using in-scope Microsoft cloud services in their information systems meet the US Department of Defense DFARS clauses that require compliance with the security requirements of NIST SP 800-171.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="dc9a2-123">Microsoft のスコープ内クラウド プラットフォームと&サービス</span><span class="sxs-lookup"><span data-stu-id="dc9a2-123">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="dc9a2-124">Azure Commercial, Azure Government</span><span class="sxs-lookup"><span data-stu-id="dc9a2-124">Azure Commercial, Azure Government</span></span>
- <span data-ttu-id="dc9a2-125">Dynamics 365 米国政府機関</span><span class="sxs-lookup"><span data-stu-id="dc9a2-125">Dynamics 365 U.S. Government</span></span>
- <span data-ttu-id="dc9a2-126">Intune</span><span class="sxs-lookup"><span data-stu-id="dc9a2-126">Intune</span></span>
- <span data-ttu-id="dc9a2-127">Office 365米国のGovernment Community Cloud (GCC)、Office 365 GCC DoD</span><span class="sxs-lookup"><span data-stu-id="dc9a2-127">Office 365 U.S. Government Community Cloud (GCC), Office 365 GCC High, and DoD</span></span>

## <a name="azure-dynamics-365-and-nist-sp-800-171"></a><span data-ttu-id="dc9a2-128">Azure、Dynamics 365、NIST SP 800-171</span><span class="sxs-lookup"><span data-stu-id="dc9a2-128">Azure, Dynamics 365, and NIST SP 800-171</span></span>

<span data-ttu-id="dc9a2-129">Azure、Dynamics 365、その他のオンライン サービスのコンプライアンスの詳細については [、「Azure NIST SP 800-171](/azure/compliance/offerings/offering-nist-800-171)の提供」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-129">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure NIST SP 800-171 offering](/azure/compliance/offerings/offering-nist-800-171).</span></span>

## <a name="office-365-and-nist-sp-800-171"></a><span data-ttu-id="dc9a2-130">Office 365 NIST SP 800-171</span><span class="sxs-lookup"><span data-stu-id="dc9a2-130">Office 365 and NIST SP 800-171</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="dc9a2-131">Office 365クラウド環境</span><span class="sxs-lookup"><span data-stu-id="dc9a2-131">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="dc9a2-132">Office 365とスコープ内サービス</span><span class="sxs-lookup"><span data-stu-id="dc9a2-132">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="dc9a2-133">次の表を使用して、サービスとサブスクリプションOffice 365を決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-133">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="dc9a2-134">**適用対象**</span><span class="sxs-lookup"><span data-stu-id="dc9a2-134">**Applicability**</span></span> | <span data-ttu-id="dc9a2-135">**スコープ内サービス**</span><span class="sxs-lookup"><span data-stu-id="dc9a2-135">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="dc9a2-136">**GCC**</span><span class="sxs-lookup"><span data-stu-id="dc9a2-136">**GCC**</span></span> | <span data-ttu-id="dc9a2-137">アクティビティ フィード サービス、Bing サービス、Delve、Exchange Online、インテリジェント サービス、Microsoft Teams、Office 365 カスタマー ポータル、Office Online、Office サービス インフラストラクチャ、Office 利用状況レポート、OneDrive for Business、People Card、SharePoint Online、Skype for Business、Windows Ink</span><span class="sxs-lookup"><span data-stu-id="dc9a2-137">Activity Feed Service, Bing Services, Delve, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |
| <span data-ttu-id="dc9a2-138">**GCC High**</span><span class="sxs-lookup"><span data-stu-id="dc9a2-138">**GCC High**</span></span> | <span data-ttu-id="dc9a2-139">Activity Feed Service, Bing Services, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card,</span><span class="sxs-lookup"><span data-stu-id="dc9a2-139">Activity Feed Service, Bing Services, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card,</span></span> 
<span data-ttu-id="dc9a2-140">SharePointオンライン、Skype for Business、Windows Ink</span><span class="sxs-lookup"><span data-stu-id="dc9a2-140">SharePoint Online, Skype for Business, Windows Ink</span></span> |
| <span data-ttu-id="dc9a2-141">**DoD**</span><span class="sxs-lookup"><span data-stu-id="dc9a2-141">**DoD**</span></span> | <span data-ttu-id="dc9a2-142">Activity Feed Service, Bing Services, Exchange Online, Intelligent Services, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, Microsoft Teams, SharePoint Online, Skype for Business, Windows Ink</span><span class="sxs-lookup"><span data-stu-id="dc9a2-142">Activity Feed Service, Bing Services, Exchange Online, Intelligent Services, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, Microsoft Teams, SharePoint Online, Skype for Business, Windows Ink</span></span> |

### <a name="frequently-asked-questions"></a><span data-ttu-id="dc9a2-143">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="dc9a2-143">Frequently asked questions</span></span>

<span data-ttu-id="dc9a2-144">**組織で Microsoft コンプライアンスと NIST SP 800-171 を使用できますか?**</span><span class="sxs-lookup"><span data-stu-id="dc9a2-144">**Can I use Microsoft compliance with NIST SP 800-171 for my organization?**</span></span>

<span data-ttu-id="dc9a2-145">はい。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-145">Yes.</span></span> <span data-ttu-id="dc9a2-146">Microsoft のお客様は、FedRAMP 標準に関する独立したサード パーティ評価組織 (3PAO) からのレポートに記載されている監査されたコントロールを、独自の FedRAMP および NIST リスク分析および資格の取り組みの一環として使用できます。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-146">Microsoft customers may use the audited controls described in the reports from independent third-party assessment organizations (3PAO) on FedRAMP standards as part of their own FedRAMP and NIST risk analysis and qualification efforts.</span></span> <span data-ttu-id="dc9a2-147">これらのレポートは、Microsoft がスコープ内クラウド サービスに実装したコントロールの有効性を証明します。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-147">These reports attest to the effectiveness of the controls Microsoft has implemented in its in-scope cloud services.</span></span> <span data-ttu-id="dc9a2-148">お客様は、CUI ワークロードが NIST SP 800-171 ガイドラインに準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-148">Customers are responsible for ensuring that their CUI workloads comply with NIST SP 800-171 guidelines.</span></span>

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="dc9a2-149">Microsoft コンプライアンス マネージャーを使用してリスクを評価する</span><span class="sxs-lookup"><span data-stu-id="dc9a2-149">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="dc9a2-150">[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-150">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="dc9a2-151">コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-151">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="dc9a2-152">コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-152">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="dc9a2-153">[コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。</span><span class="sxs-lookup"><span data-stu-id="dc9a2-153">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

### <a name="resources"></a><span data-ttu-id="dc9a2-154">リソース</span><span class="sxs-lookup"><span data-stu-id="dc9a2-154">Resources</span></span>

- [<span data-ttu-id="dc9a2-155">Microsoft DoD 認定は NIST 800-171 の要件を満たしています</span><span class="sxs-lookup"><span data-stu-id="dc9a2-155">Microsoft DoD Certification Meets NIST 800-171 Requirements</span></span>](offering-DoD-DISA-L2-L4-L5.md)
- [<span data-ttu-id="dc9a2-156">NIST 800-171 コンプライアンス:サイバーセキュリティ ドキュメントから始まる</span><span class="sxs-lookup"><span data-stu-id="dc9a2-156">NIST 800-171 Compliance Starts with Cybersecurity Documentation</span></span>](https://www.nist800171.com/)
- [<span data-ttu-id="dc9a2-157">Microsoft Cloud Services FedRAMP の承認</span><span class="sxs-lookup"><span data-stu-id="dc9a2-157">Microsoft Cloud Services FedRAMP Authorizations</span></span>](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [<span data-ttu-id="dc9a2-158">NIST 800-171 3.3 監査と説明責任とOffice 365 GCC高</span><span class="sxs-lookup"><span data-stu-id="dc9a2-158">NIST 800-171 3.3 Audit and Accountability with Office 365 GCC High</span></span>](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [<span data-ttu-id="dc9a2-159">Microsoft と NIST サイバーセキュリティ フレームワーク</span><span class="sxs-lookup"><span data-stu-id="dc9a2-159">Microsoft and the NIST Cybersecurity Framework</span></span>](offering-nist-csf.md)
- [<span data-ttu-id="dc9a2-160">Microsoft Government クラウド</span><span class="sxs-lookup"><span data-stu-id="dc9a2-160">Microsoft Government Cloud</span></span>](https://www.microsoft.com/enterprise/government)
- [<span data-ttu-id="dc9a2-161">Microsoft Trust Center のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="dc9a2-161">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
