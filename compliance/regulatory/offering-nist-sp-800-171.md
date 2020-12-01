---
title: NIST SP 800-171
description: Microsoft クラウドサービスは、非連邦情報システムの管理されていない未分類情報 (CUI) を保護するために、NIST SP 800-171 ガイドラインに準拠しています。
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
ms.openlocfilehash: 071bbbb24110b9d74aa75580d9a23628041455a6
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508424"
---
# <a name="nist-sp-800-171"></a><span data-ttu-id="b2b4a-104">NIST SP 800-171</span><span class="sxs-lookup"><span data-stu-id="b2b4a-104">NIST SP 800-171</span></span>

## <a name="about-nist-sp-800-171"></a><span data-ttu-id="b2b4a-105">NIST SP 800-171 について</span><span class="sxs-lookup"><span data-stu-id="b2b4a-105">About NIST SP 800-171</span></span>

<span data-ttu-id="b2b4a-106">米国国立標準技術局 (NIST) は、連邦政府機関の情報と情報システムを保護するための測定基準とガイドラインを推進および維持します。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-106">The US National Institute of Standards and Technology (NIST) promotes and maintains measurement standards and guidelines to help protect the information and information systems of federal agencies.</span></span> <span data-ttu-id="b2b4a-107">統制されていない未分類情報 (CUI) を管理するエグゼクティブオーダー13556への対応として、 [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final)が公開されました。 *連邦情報システムおよび組織の非分類情報を保護* しています。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-107">In response to Executive Order 13556 on managing controlled unclassified information (CUI), it published [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final), *Protecting Controlled Unclassified Information In Nonfederal Information Systems and Organizations*.</span></span> <span data-ttu-id="b2b4a-108">CUI は、電子情報として定義されており、政府によって作成された (またはその代理のエンティティによって) 分類されていないものの、機密情報を保護する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-108">CUI is defined as information, both digital and physical, created by a government (or an entity on its behalf) that, while not classified, is still sensitive and requires protection.</span></span>

<span data-ttu-id="b2b4a-109">NIST SP 800-171 は当初は2015年6月に公開されており、脅威の進化に対応するために複数回更新されています。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-109">NIST SP 800-171 was originally published in June 2015 and has been updated several times since then in response to evolving cyberthreats.</span></span> <span data-ttu-id="b2b4a-110">このガイドでは、政府機関以外の情報システムおよび組織に対して、CUI への安全なアクセス、転送、保存を行う方法についてのガイドラインを提供します。この要件は、次の4つの主なカテゴリに分類されます。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-110">It provides guidelines on how CUI should be securely accessed, transmitted, and stored in nonfederal information systems and organizations; its requirements fall into four main categories:</span></span>

- <span data-ttu-id="b2b4a-111">管理と保護のためのコントロールとプロセス</span><span class="sxs-lookup"><span data-stu-id="b2b4a-111">Controls and processes for managing and protecting</span></span>
- <span data-ttu-id="b2b4a-112">IT システムの監視と管理</span><span class="sxs-lookup"><span data-stu-id="b2b4a-112">Monitoring and management of IT systems</span></span>
- <span data-ttu-id="b2b4a-113">エンドユーザーのためのプラクティスと手順を明確にする</span><span class="sxs-lookup"><span data-stu-id="b2b4a-113">Clear practices and procedures for end users</span></span>
- <span data-ttu-id="b2b4a-114">技術的および物理的なセキュリティ対策の実装</span><span class="sxs-lookup"><span data-stu-id="b2b4a-114">Implementation of technological and physical security measures</span></span>

## <a name="microsoft-and-nist-sp-800-171"></a><span data-ttu-id="b2b4a-115">Microsoft および NIST SP 800-171</span><span class="sxs-lookup"><span data-stu-id="b2b4a-115">Microsoft and NIST SP 800-171</span></span>

<span data-ttu-id="b2b4a-116">サードパーティの認定組織、Kratos Secureinfo、および Coalfire は、Microsoft と提携して、 *米国連邦情報システムおよび組織で、管理されていない未分類の情報 (cui) を保護* する800-171 ことを証明しています。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-116">Accredited third-party assessment organizations, Kratos Secureinfo and Coalfire, partnered with Microsoft to attest that its in-scope cloud services meet the criteria in NIST SP 800-171, *Protecting Controlled Unclassified Information (CUI) in Nonfederal Information Systems and Organizations*, when they process CUI.</span></span> <span data-ttu-id="b2b4a-117">[Microsoft の FedRAMP 要件の実装](offering-fedramp.md)により、microsoft のスコープ内のクラウドサービスが、既に導入されているシステムとプラクティスを使用して、NIST SP 800-171 の要件を満たしていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-117">The [Microsoft implementation of FedRAMP](offering-fedramp.md) requirements help ensure Microsoft in-scope cloud services meet or exceed the requirements of NIST SP 800-171 using the systems and practices already in place.</span></span>

<span data-ttu-id="b2b4a-118">NIST SP 800-171 の要件は、NIST SP 800-53 のサブセットで、FedRAMP が使用する標準です。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-118">NIST SP 800-171 requirements are a subset of NIST SP 800-53, the standard that FedRAMP uses.</span></span> <span data-ttu-id="b2b4a-119">付録 D (NIST SP 800-171) は、自分のセキュリティ要件を NIST SP 800-53 の関連するセキュリティコントロールに直接マッピングしています。この場合、スコープ内のクラウドサービスは、FedRAMP プログラムで既に評価および承認されています。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-119">Appendix D of NIST SP 800-171 provides a direct mapping of its CUI security requirements to the relevant security controls in NIST SP 800-53, for which the in-scope cloud services have already been assessed and authorized under the FedRAMP program.</span></span>

<span data-ttu-id="b2b4a-120">米国政府機関を処理または保存するエンティティ (研究機関、コンサルティング会社、製造業者) は、NIST SP 800-171 の厳格な要件に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-120">Any entity that processes or stores US government CUI — research institutions, consulting companies, manufacturing contractors, must comply with the stringent requirements of NIST SP 800-171.</span></span> <span data-ttu-id="b2b4a-121">この構成証明とは、microsoft が完全に準拠していることを保証するために CUI ワークロードの展開を検討しているお客様に対して、Microsoft のスコープを持つクラウドサービスが可能になります。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-121">This attestation means Microsoft in-scope cloud services can accommodate customers looking to deploy CUI workloads with the assurance that Microsoft is in full compliance.</span></span> <span data-ttu-id="b2b4a-122">たとえば、「対象となる防衛情報」を処理、保存、または送信するすべての DoD 請負業者は、情報システムの Microsoft クラウドサービスをスコープ内で使用することにより、米国国防総省の、米国国防総省の、NIST SP 800-171 のセキュリティ要件に準拠する必要があることを満たします。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-122">For example, all DoD contractors who process, store, or transmit 'covered defense information' using in-scope Microsoft cloud services in their information systems meet the US Department of Defense DFARS clauses that require compliance with the security requirements of NIST SP 800-171.</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="b2b4a-123">対象となる Microsoft のクラウド サービス</span><span class="sxs-lookup"><span data-stu-id="b2b4a-123">Microsoft in-scope cloud services</span></span>

- [<span data-ttu-id="b2b4a-124">Azure Government</span><span class="sxs-lookup"><span data-stu-id="b2b4a-124">Azure Government</span></span>](https://aka.ms/AzureCompliance)
- [<span data-ttu-id="b2b4a-125">Dynamics 365 米国政府</span><span class="sxs-lookup"><span data-stu-id="b2b4a-125">Dynamics 365 U.S. Government</span></span>](https://aka.ms/d365-compliance-list)
- <span data-ttu-id="b2b4a-126">Intune</span><span class="sxs-lookup"><span data-stu-id="b2b4a-126">Intune</span></span>
- [<span data-ttu-id="b2b4a-127">Office 365 米国政府機関向けコミュニティクラウド (GCC)、Office 365 GCC 高、DoD</span><span class="sxs-lookup"><span data-stu-id="b2b4a-127">Office 365 U.S. Government Community Cloud (GCC), Office 365 GCC High, and DoD</span></span>](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a><span data-ttu-id="b2b4a-128">監査、レポート、証明書</span><span class="sxs-lookup"><span data-stu-id="b2b4a-128">Audits, reports, and certificates</span></span>

- [<span data-ttu-id="b2b4a-129">NIST SP 800-171 に準拠するための Azure 自治体の構成証明</span><span class="sxs-lookup"><span data-stu-id="b2b4a-129">Azure Government Attestation of Compliance with NIST SP 800-171</span></span>](https://aka.ms/Azure-NIST-800-171)

## <a name="how-to-implement"></a><span data-ttu-id="b2b4a-130">実装方法</span><span class="sxs-lookup"><span data-stu-id="b2b4a-130">How to implement</span></span>

- <span data-ttu-id="b2b4a-131">[Azure 青写真サンプル](https://docs.microsoft.com/azure/governance/blueprints/samples/): NIST ベースのコントロールに準拠したワークロードの実装のサポートを受けることができます。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-131">[Azure Blueprint samples](https://docs.microsoft.com/azure/governance/blueprints/samples/): Get support for implementing workloads that comply with NIST-based controls.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="b2b4a-132">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="b2b4a-132">Frequently asked questions</span></span>

<span data-ttu-id="b2b4a-133">**組織の NIST SP 800-171 で Microsoft コンプライアンスを使用できますか?**</span><span class="sxs-lookup"><span data-stu-id="b2b4a-133">**Can I use Microsoft compliance with NIST SP 800-171 for my organization?**</span></span>

<span data-ttu-id="b2b4a-134">はい。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-134">Yes.</span></span> <span data-ttu-id="b2b4a-135">Microsoft のお客様は、独自の FedRAMP の一部としての、独立したサードパーティの評価組織 (3PAO) からのレポートで説明されている監査された統制を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-135">Microsoft customers may use the audited controls described in the reports from independent third-party assessment organizations (3PAO) on FedRAMP standards as part of their own FedRAMP and NIST risk analysis and qualification efforts.</span></span> <span data-ttu-id="b2b4a-136">これらのレポートは、Microsoft がスコープ内のクラウドサービスで実装した統制の有効性を証明します。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-136">These reports attest to the effectiveness of the controls Microsoft has implemented in its in-scope cloud services.</span></span> <span data-ttu-id="b2b4a-137">お客様は、CUI ワークロードが NIST SP 800-171 ガイドラインに準拠していることを確認する責任があります。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-137">Customers are responsible for ensuring that their CUI workloads comply with NIST SP 800-171 guidelines.</span></span>

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="b2b4a-138">Microsoft コンプライアンス マネージャーを使用してリスクを評価する</span><span class="sxs-lookup"><span data-stu-id="b2b4a-138">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="b2b4a-p107">[Microsoft コンプライアンス マネージャー](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager)は、[Microsoft 365 コンプライアンス センター](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。コンプライアンス マネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。テンプレートは、コンプライアンス マネージャーの **評価テンプレート** ページに見つかります。[コンプライアンス マネージャーで評価する方法](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments)をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-p107">[Microsoft Compliance Manager](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks. Compliance Manager offers a premium template for building an assessment for this regulation. Find the template in the **assessment templates** page in Compliance Manager. Learn how to [build assessments in Compliance Manager](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments).</span></span>

## <a name="resources"></a><span data-ttu-id="b2b4a-143">リソース</span><span class="sxs-lookup"><span data-stu-id="b2b4a-143">Resources</span></span>

- [<span data-ttu-id="b2b4a-144">Microsoft DoD 認定資格は、NIST 800-171 の要件を満たしている</span><span class="sxs-lookup"><span data-stu-id="b2b4a-144">Microsoft DoD Certification Meets NIST 800-171 Requirements</span></span>](offering-DoD-DISA-L2-L4-L5.md)
- [<span data-ttu-id="b2b4a-145">NIST 800-171 コンプライアンスは Cybersecurity のドキュメントで始まります。</span><span class="sxs-lookup"><span data-stu-id="b2b4a-145">NIST 800-171 Compliance Starts with Cybersecurity Documentation</span></span>](https://www.nist800171.com/)
- [<span data-ttu-id="b2b4a-146">Microsoft Cloud Services FedRAMP 承認</span><span class="sxs-lookup"><span data-stu-id="b2b4a-146">Microsoft Cloud Services FedRAMP Authorizations</span></span>](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [<span data-ttu-id="b2b4a-147">NIST 800-171 3.3 監査およびアカウンタビリティ (Office 365 GCC 高)</span><span class="sxs-lookup"><span data-stu-id="b2b4a-147">NIST 800-171 3.3 Audit and Accountability with Office 365 GCC High</span></span>](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [<span data-ttu-id="b2b4a-148">Microsoft および NIST Cybersecurity Framework</span><span class="sxs-lookup"><span data-stu-id="b2b4a-148">Microsoft and the NIST Cybersecurity Framework</span></span>](offering-nist-csf.md)
- [<span data-ttu-id="b2b4a-149">Microsoft Government クラウド</span><span class="sxs-lookup"><span data-stu-id="b2b4a-149">Microsoft Government Cloud</span></span>](https://www.microsoft.com/enterprise/government)
- [<span data-ttu-id="b2b4a-150">Microsoft Trust Center のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="b2b4a-150">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
