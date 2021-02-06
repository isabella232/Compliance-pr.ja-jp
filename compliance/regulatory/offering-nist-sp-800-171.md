---
title: NIST SP 800-171
description: Microsoft クラウド サービスは NIST SP 800-171 のガイドラインに準拠して、非Federal information systems の未分類の制御された情報 (CUI) を保護します。
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
ms.openlocfilehash: da5e2621969ff9cd4ce2778fa7f075522454aef7
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121116"
---
# <a name="nist-sp-800-171"></a><span data-ttu-id="5603f-104">NIST SP 800-171</span><span class="sxs-lookup"><span data-stu-id="5603f-104">NIST SP 800-171</span></span>

## <a name="about-nist-sp-800-171"></a><span data-ttu-id="5603f-105">NIST SP 800-171 について</span><span class="sxs-lookup"><span data-stu-id="5603f-105">About NIST SP 800-171</span></span>

<span data-ttu-id="5603f-106">米国標準技術協会 (NIST) は、連邦機関の情報および情報システムを保護するための測定基準とガイドラインを推進および維持しています。</span><span class="sxs-lookup"><span data-stu-id="5603f-106">The US National Institute of Standards and Technology (NIST) promotes and maintains measurement standards and guidelines to help protect the information and information systems of federal agencies.</span></span> <span data-ttu-id="5603f-107">管理下にある未分類情報 (CUI) の管理に関する Executive Order 13556 に対して [、NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final)、非分類情報システムおよび組織の制御された未分類情報の保護を公開 *しました。*</span><span class="sxs-lookup"><span data-stu-id="5603f-107">In response to Executive Order 13556 on managing controlled unclassified information (CUI), it published [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final), *Protecting Controlled Unclassified Information In Nonfederal Information Systems and Organizations*.</span></span> <span data-ttu-id="5603f-108">CUI は、デジタルと物理の両方の情報として定義され、政府 (または代わりにエンティティ) によって作成され、分類されていない場合でも機密性が高く、保護が必要です。</span><span class="sxs-lookup"><span data-stu-id="5603f-108">CUI is defined as information, both digital and physical, created by a government (or an entity on its behalf) that, while not classified, is still sensitive and requires protection.</span></span>

<span data-ttu-id="5603f-109">NIST SP 800-171 はもともと 2015 年 6 月に公開され、その後、進化するサイバー脅威に対応して何度か更新されています。</span><span class="sxs-lookup"><span data-stu-id="5603f-109">NIST SP 800-171 was originally published in June 2015 and has been updated several times since then in response to evolving cyberthreats.</span></span> <span data-ttu-id="5603f-110">また、CUI を安全にアクセス、転送、および非Federal information systems and organizations に格納する方法に関するガイドラインを提供します。その要件は、主に次の 4 つのカテゴリに分類されます。</span><span class="sxs-lookup"><span data-stu-id="5603f-110">It provides guidelines on how CUI should be securely accessed, transmitted, and stored in nonfederal information systems and organizations; its requirements fall into four main categories:</span></span>

- <span data-ttu-id="5603f-111">管理と保護のためのコントロールとプロセス</span><span class="sxs-lookup"><span data-stu-id="5603f-111">Controls and processes for managing and protecting</span></span>
- <span data-ttu-id="5603f-112">IT システムの監視と管理</span><span class="sxs-lookup"><span data-stu-id="5603f-112">Monitoring and management of IT systems</span></span>
- <span data-ttu-id="5603f-113">エンド ユーザーの明確なプラクティスと手順</span><span class="sxs-lookup"><span data-stu-id="5603f-113">Clear practices and procedures for end users</span></span>
- <span data-ttu-id="5603f-114">技術的および物理的なセキュリティ対策の実装</span><span class="sxs-lookup"><span data-stu-id="5603f-114">Implementation of technological and physical security measures</span></span>

## <a name="microsoft-and-nist-sp-800-171"></a><span data-ttu-id="5603f-115">Microsoft および NIST SP 800-171</span><span class="sxs-lookup"><span data-stu-id="5603f-115">Microsoft and NIST SP 800-171</span></span>

<span data-ttu-id="5603f-116">認定された第三者評価機関である、マイクロソフトと協力して、範囲内のクラウド サービスが CUI を処理する際に、NIST SP 800-171 の非分類情報システムおよび組織の制御されていない情報 *(CUI)* の保護の条件を満たしているか証明しました。</span><span class="sxs-lookup"><span data-stu-id="5603f-116">Accredited third-party assessment organizations, Kratos Secureinfo and Coalfire, partnered with Microsoft to attest that its in-scope cloud services meet the criteria in NIST SP 800-171, *Protecting Controlled Unclassified Information (CUI) in Nonfederal Information Systems and Organizations*, when they process CUI.</span></span> <span data-ttu-id="5603f-117">[FedRAMP](offering-fedramp.md)要件の Microsoft 実装は、Microsoft の対象クラウド サービスが、既に実施されているシステムとプラクティスを使用して、NIST SP 800-171 の要件を満たすか、それを超過していることを確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5603f-117">The [Microsoft implementation of FedRAMP](offering-fedramp.md) requirements help ensure Microsoft in-scope cloud services meet or exceed the requirements of NIST SP 800-171 using the systems and practices already in place.</span></span>

<span data-ttu-id="5603f-118">NIST SP 800-171 の要件は、FedRAMP が使用する標準である NIST SP 800-53 のサブセットです。</span><span class="sxs-lookup"><span data-stu-id="5603f-118">NIST SP 800-171 requirements are a subset of NIST SP 800-53, the standard that FedRAMP uses.</span></span> <span data-ttu-id="5603f-119">NIST SP 800-171 の付録 D では、CUI のセキュリティ要件と、範囲内のクラウド サービスが FedRAMP プログラムで既に評価および承認されている NIST SP 800-53 の関連するセキュリティ コントロールに直接対応しています。</span><span class="sxs-lookup"><span data-stu-id="5603f-119">Appendix D of NIST SP 800-171 provides a direct mapping of its CUI security requirements to the relevant security controls in NIST SP 800-53, for which the in-scope cloud services have already been assessed and authorized under the FedRAMP program.</span></span>

<span data-ttu-id="5603f-120">米国政府機関の CUI を処理または保存するエンティティ (調査機関、コンサルティング会社、製造請負業者) は、NIST SP 800-171 の厳しい要件に準拠する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5603f-120">Any entity that processes or stores US government CUI — research institutions, consulting companies, manufacturing contractors, must comply with the stringent requirements of NIST SP 800-171.</span></span> <span data-ttu-id="5603f-121">この構成証明は、Microsoft が完全に準拠しているという保証を得て、CUI ワークロードの展開を探しているお客様に Microsoft の対象クラウド サービスが対応できるという意味です。</span><span class="sxs-lookup"><span data-stu-id="5603f-121">This attestation means Microsoft in-scope cloud services can accommodate customers looking to deploy CUI workloads with the assurance that Microsoft is in full compliance.</span></span> <span data-ttu-id="5603f-122">たとえば、情報システム内の対象となる Microsoft クラウド サービスを使用して「対象となる防御情報」を処理、保存、または送信する DoD 請負業者はすべて、NIST SP 800-171 のセキュリティ要件に準拠する必要がある米国国防総省 DFARS 条項を満たしています。</span><span class="sxs-lookup"><span data-stu-id="5603f-122">For example, all DoD contractors who process, store, or transmit 'covered defense information' using in-scope Microsoft cloud services in their information systems meet the US Department of Defense DFARS clauses that require compliance with the security requirements of NIST SP 800-171.</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="5603f-123">対象となる Microsoft のクラウド サービス</span><span class="sxs-lookup"><span data-stu-id="5603f-123">Microsoft in-scope cloud services</span></span>

- [<span data-ttu-id="5603f-124">Azure Government</span><span class="sxs-lookup"><span data-stu-id="5603f-124">Azure Government</span></span>](https://aka.ms/AzureCompliance)
- [<span data-ttu-id="5603f-125">Azure Commercial</span><span class="sxs-lookup"><span data-stu-id="5603f-125">Azure Commercial</span></span>](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/)
- [<span data-ttu-id="5603f-126">Dynamics 365 U.S. Government</span><span class="sxs-lookup"><span data-stu-id="5603f-126">Dynamics 365 U.S. Government</span></span>](https://aka.ms/d365-compliance-list)
- <span data-ttu-id="5603f-127">Intune</span><span class="sxs-lookup"><span data-stu-id="5603f-127">Intune</span></span>
- [<span data-ttu-id="5603f-128">Office 365 米国政府機関コミュニティ クラウド (GCC)、Office 365 GCC High、DoD</span><span class="sxs-lookup"><span data-stu-id="5603f-128">Office 365 U.S. Government Community Cloud (GCC), Office 365 GCC High, and DoD</span></span>](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a><span data-ttu-id="5603f-129">監査、レポート、証明書</span><span class="sxs-lookup"><span data-stu-id="5603f-129">Audits, reports, and certificates</span></span>

- [<span data-ttu-id="5603f-130">Azure Government Attestation of Compliance with NIST SP 800-171</span><span class="sxs-lookup"><span data-stu-id="5603f-130">Azure Government Attestation of Compliance with NIST SP 800-171</span></span>](https://aka.ms/Azure-NIST-800-171)

## <a name="how-to-implement"></a><span data-ttu-id="5603f-131">実装方法</span><span class="sxs-lookup"><span data-stu-id="5603f-131">How to implement</span></span>

- <span data-ttu-id="5603f-132">[Azure Blueprint のサンプル](/azure/governance/blueprints/samples/): NIST ベースのコントロールに準拠するワークロードの実装のサポートを受け取る。</span><span class="sxs-lookup"><span data-stu-id="5603f-132">[Azure Blueprint samples](/azure/governance/blueprints/samples/): Get support for implementing workloads that comply with NIST-based controls.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="5603f-133">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="5603f-133">Frequently asked questions</span></span>

<span data-ttu-id="5603f-134">**組織で NIST SP 800-171 に準拠している Microsoft を使用できますか?**</span><span class="sxs-lookup"><span data-stu-id="5603f-134">**Can I use Microsoft compliance with NIST SP 800-171 for my organization?**</span></span>

<span data-ttu-id="5603f-135">はい。</span><span class="sxs-lookup"><span data-stu-id="5603f-135">Yes.</span></span> <span data-ttu-id="5603f-136">Microsoft のお客様は、FedRAMP 基準に関する独立した第三者評価組織 (3PAO) からのレポートに記載されている監査されるコントロールを、FedRAMP および NIST リスク分析および資格認定作業の一環として使用できます。</span><span class="sxs-lookup"><span data-stu-id="5603f-136">Microsoft customers may use the audited controls described in the reports from independent third-party assessment organizations (3PAO) on FedRAMP standards as part of their own FedRAMP and NIST risk analysis and qualification efforts.</span></span> <span data-ttu-id="5603f-137">これらのレポートは、Microsoft が範囲内のクラウド サービスに実装したコントロールの有効性を証明します。</span><span class="sxs-lookup"><span data-stu-id="5603f-137">These reports attest to the effectiveness of the controls Microsoft has implemented in its in-scope cloud services.</span></span> <span data-ttu-id="5603f-138">お客様は、CUI ワークロードが NIST SP 800-171 ガイドラインに準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5603f-138">Customers are responsible for ensuring that their CUI workloads comply with NIST SP 800-171 guidelines.</span></span>

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="5603f-139">Microsoft コンプライアンス マネージャーを使用してリスクを評価する</span><span class="sxs-lookup"><span data-stu-id="5603f-139">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="5603f-140">[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="5603f-140">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="5603f-141">コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="5603f-141">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="5603f-142">コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。</span><span class="sxs-lookup"><span data-stu-id="5603f-142">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="5603f-143">[コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。</span><span class="sxs-lookup"><span data-stu-id="5603f-143">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

## <a name="resources"></a><span data-ttu-id="5603f-144">リソース</span><span class="sxs-lookup"><span data-stu-id="5603f-144">Resources</span></span>

- [<span data-ttu-id="5603f-145">Microsoft DoD 認定は NIST 800-171 の要件を満たしています</span><span class="sxs-lookup"><span data-stu-id="5603f-145">Microsoft DoD Certification Meets NIST 800-171 Requirements</span></span>](offering-DoD-DISA-L2-L4-L5.md)
- [<span data-ttu-id="5603f-146">NIST 800-171 コンプライアンスの開始とサイバーセキュリティ に関するドキュメント</span><span class="sxs-lookup"><span data-stu-id="5603f-146">NIST 800-171 Compliance Starts with Cybersecurity Documentation</span></span>](https://www.nist800171.com/)
- [<span data-ttu-id="5603f-147">Microsoft Cloud Services FedRAMP の承認</span><span class="sxs-lookup"><span data-stu-id="5603f-147">Microsoft Cloud Services FedRAMP Authorizations</span></span>](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [<span data-ttu-id="5603f-148">NIST 800-171 3.3 監査とアOffice 365 GCC High</span><span class="sxs-lookup"><span data-stu-id="5603f-148">NIST 800-171 3.3 Audit and Accountability with Office 365 GCC High</span></span>](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [<span data-ttu-id="5603f-149">Microsoft と NIST サイバーセキュリティ フレームワーク</span><span class="sxs-lookup"><span data-stu-id="5603f-149">Microsoft and the NIST Cybersecurity Framework</span></span>](offering-nist-csf.md)
- [<span data-ttu-id="5603f-150">Microsoft Government クラウド</span><span class="sxs-lookup"><span data-stu-id="5603f-150">Microsoft Government Cloud</span></span>](https://www.microsoft.com/enterprise/government)
- [<span data-ttu-id="5603f-151">Microsoft Trust Center のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="5603f-151">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
