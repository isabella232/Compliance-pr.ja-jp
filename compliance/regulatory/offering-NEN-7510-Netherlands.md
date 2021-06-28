---
title: NEN 7510
description: オランダ国内の組織は NEN 7510 標準に従い、患者の医療データの統制を実施する必要があります。
keywords: Microsoft 365、コンプライアンス、サービス
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
ms.openlocfilehash: 9ae0ba0b3ad10e4b1f2d308090f05c698bce092f
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088486"
---
# <a name="nen-7510"></a><span data-ttu-id="b858a-104">NEN 7510</span><span class="sxs-lookup"><span data-stu-id="b858a-104">NEN 7510</span></span>

## <a name="nen-7510-overview"></a><span data-ttu-id="b858a-105">NEN 7510 の概要</span><span class="sxs-lookup"><span data-stu-id="b858a-105">NEN 7510 overview</span></span>

<span data-ttu-id="b858a-106">オランダ国内で患者の医療情報を取り扱う組織は、そのデータおよび組織への統制が NEN 7510 標準で定められた要件に適合していることを実証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b858a-106">Organizations in the Netherlands that process patient health information must demonstrate control over that data and their organization consistent with the requirements set out in the NEN 7510 standard.</span></span> <span data-ttu-id="b858a-107">Microsoft は NEN 7510 の規制の対象外ですが、医療分野のお客様は、Microsoft クラウドで構築されたソリューションに対して、NEN 7510 への準拠を確保する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b858a-107">Microsoft is not itself subject to NEN 7510, but its cloud customers in the healthcare sector need to establish that they comply with NEN 7510 regarding solutions built on the Microsoft Cloud.</span></span> <span data-ttu-id="b858a-108">Microsoft のクラウド サービスは、定期的にさまざまな認証や監査を受けており、その中には NEN 7510 で指定された要件に密接に関わる要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b858a-108">Microsoft cloud services undergo various periodic certifications and audits, some of which include elements closely related to requirements specified in NEN 7510.</span></span>

## <a name="microsoft-and-nen-75102011"></a><span data-ttu-id="b858a-109">Microsoft と NEN 7510:2011</span><span class="sxs-lookup"><span data-stu-id="b858a-109">Microsoft and NEN 7510:2011</span></span>

<span data-ttu-id="b858a-110">Microsoft では現在の認証と保証声明を分析し、[NEN 7510 カバレッジ レポート](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=3285c45c-921c-49ad-b881-be43e0b70490&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Compliance_Guides) (Service Trust Platform でご利用いただけます)。それらの認証や保証声明は、Microsoft がクラウド サービス プロバイダーとして責任を負う NEN 7510 規制に対して対応付けられています。</span><span class="sxs-lookup"><span data-stu-id="b858a-110">Microsoft has analyzed our current certifications and assurance statements and created a [NEN 7510 coverage report](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=3285c45c-921c-49ad-b881-be43e0b70490&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Compliance_Guides) (available on the Service Trust Platform), which maps those certifications and assurance statements against the NEN 7510 controls for which Microsoft is responsible as a cloud service provider.</span></span> <span data-ttu-id="b858a-111">この文書は、患者の医療情報の保管または処理に関連する Microsoft クラウド サービスの利用を NEN 7510 に準拠させるため、お客様がどの統制をさらに実施しなくてはならないか判断する上で役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b858a-111">This document can help customers determine which other controls they must implement to ensure that their use of Microsoft cloud services for the storage or processing of patient health information complies with NEN 7510.</span></span>

<span data-ttu-id="b858a-112">Azure セキュリティおよびコンプライアンス ブループリントを使用して NEN 7510 の展開を加速する方法を説明します。「[Microsoft クラウドをダウンロードする: Azure および Office 365 NEN7510-2011 標準範囲ユーザー ガイド](https://aka.ms/Azure-NEN7510-2011)」をダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="b858a-112">Learn how to accelerate your NEN 7510 deployment with our Azure Security and Compliance Blueprints: [Download the Microsoft Cloud: Azure and Office 365 NEN7510-2011 Standard Coverage User Guide](https://aka.ms/Azure-NEN7510-2011)</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="b858a-113">対象となる Microsoft のクラウド サービス</span><span class="sxs-lookup"><span data-stu-id="b858a-113">Microsoft in-scope cloud services</span></span>

- [<span data-ttu-id="b858a-114">Azure および Azure Government</span><span class="sxs-lookup"><span data-stu-id="b858a-114">Azure and Azure Government</span></span>](https://aka.ms/AzureCompliance)
- <span data-ttu-id="b858a-115">Intune</span><span class="sxs-lookup"><span data-stu-id="b858a-115">Intune</span></span>
- [<span data-ttu-id="b858a-116">Office 365</span><span class="sxs-lookup"><span data-stu-id="b858a-116">Office 365</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=2077751)

## <a name="audits-reports-and-certificates"></a><span data-ttu-id="b858a-117">監査、レポート、証明書</span><span class="sxs-lookup"><span data-stu-id="b858a-117">Audits, reports, and certificates</span></span>

- [<span data-ttu-id="b858a-118">Azure および Office 365 NEN 7510:2011 標準範囲</span><span class="sxs-lookup"><span data-stu-id="b858a-118">Azure and Office 365 NEN 7510:2011 Standard Coverage</span></span>](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=15d5a5fa-fbb6-4ea6-8126-2a2c684ae789&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_GRC_Assessment_Reports)

## <a name="frequently-asked-questions"></a><span data-ttu-id="b858a-119">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="b858a-119">Frequently asked questions</span></span>

<span data-ttu-id="b858a-120">**Microsoft クラウド サービスを利用する顧客は NEN 7510 に準拠しますか?**</span><span class="sxs-lookup"><span data-stu-id="b858a-120">**Is a customer that uses Microsoft cloud services compliant with NEN 7510?**</span></span>

<span data-ttu-id="b858a-121">NEN コンプライアンスへの準拠は、医療組織 (「顧客」) がその責任を負います。</span><span class="sxs-lookup"><span data-stu-id="b858a-121">Demonstrating NEN compliance is the responsibility of the healthcare organization (the 'customer').</span></span> <span data-ttu-id="b858a-122">クラウド サービス ベンダーを利用する場合、お客様は通常、ベンダーの保証を求め、独自の (他の) テクノロジ、組織の決定事項や選択事項、そしてプロセスを取り入れます。</span><span class="sxs-lookup"><span data-stu-id="b858a-122">When using a cloud services vendor, customers typically demand assurances from the vendor, and add their own (other) technology and organizational decisions, choices, and processes.</span></span> <span data-ttu-id="b858a-123">このことにより、結果的に NEN 7510 コンプライアンスに関して、総合的な評価は顧客が実施し、その内容は審査または認定のため、第三者の監査人に提出されることになります。</span><span class="sxs-lookup"><span data-stu-id="b858a-123">This effort results in an overall assessment by the customer on its NEN 7510 compliance, which can be submitted for review or certification to a third-party auditor.</span></span> <span data-ttu-id="b858a-124">NEN 7510 カバレッジ レポートでは、Microsoft クラウド サービスの対象となる NEN 7510 制御に関するインサイトが提供されていますが、そのため、エンド ツー エンドのコンプライアンスは取り上げられていません。</span><span class="sxs-lookup"><span data-stu-id="b858a-124">The NEN 7510 coverage report provides insight into which NEN 7510 controls are covered by Microsoft cloud services, but, as such, does not cover end-to-end compliance.</span></span>

<span data-ttu-id="b858a-125">**Microsoft は NEN 7510 に準拠していますか?**</span><span class="sxs-lookup"><span data-stu-id="b858a-125">**Is Microsoft compliant with NEN 7510?**</span></span>

<span data-ttu-id="b858a-126">NEN 7510 コンプライアンスの義務は、オランダの医療組織に適用されます。</span><span class="sxs-lookup"><span data-stu-id="b858a-126">The responsibility for NEN 7510 compliance is applicable to Dutch Healthcare organizations.</span></span> <span data-ttu-id="b858a-127">NEN 7510 コンプライアンスでは、組織が情報セキュリティ管理システムを実行し、適切な技術的および組織的な手段により対処することが求められています。</span><span class="sxs-lookup"><span data-stu-id="b858a-127">It requires the organization to implement an information security management system and to address risk with appropriate technical and organizational measures.</span></span> <span data-ttu-id="b858a-128">Microsoft はクラウド サービス プロバイダーとしての役割において、NEN 7510 コンプライアンスの準拠を目指してはおらず、また技術的に実現することはできません。</span><span class="sxs-lookup"><span data-stu-id="b858a-128">For Microsoft in its role as cloud service provider, NEN 7510 compliance is not the objective, nor is it technically feasible.</span></span> <span data-ttu-id="b858a-129">顧客が Microsoft クラウド サービスを導入または利用する場合、それらのサービスが NEN 7510 評価の対象範囲に含まれている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b858a-129">When a customer implements or uses Microsoft cloud services, those services may be in scope of a NEN 7510 evaluation.</span></span> <span data-ttu-id="b858a-130">ただし、組織は独自の (他の) 制御、選択事項、プロセスを取り入れる必要があり、これらは NEN7510 の総合評価に含まれます。</span><span class="sxs-lookup"><span data-stu-id="b858a-130">However, the organization must add its own (other) controls, choices, and processes that are part of the overall NEN 7510 evaluation.</span></span> <span data-ttu-id="b858a-131">レポートの目的は、医療事業者が NEN 7510 に準拠する形で Microsoft クラウド サービスを導入できることを示すことにあります。</span><span class="sxs-lookup"><span data-stu-id="b858a-131">The objective of the report is to demonstrate that a Healthcare entity can adopt the Microsoft cloud services in a manner that is compliant with NEN 7510.</span></span>

<span data-ttu-id="b858a-132">**NEN カバレージ レポートで NEN 7510 コンプライアンスが 100% カバーされていないということは、同コンプライアンスへの準拠は不可能だということですか?**</span><span class="sxs-lookup"><span data-stu-id="b858a-132">**The report does not show 100% coverage. Is NEN 7510 compliance not feasible?**</span></span>

<span data-ttu-id="b858a-133">Microsoft クラウド サービスでは、オランダ国内の医療分野の組織が持つ NEN 7510 コンプライアンスのニーズを支援する、多くの制御を提供しています。</span><span class="sxs-lookup"><span data-stu-id="b858a-133">Microsoft cloud services provide many controls that help organizations within Dutch Healthcare with their NEN 7510 compliance needs.</span></span> <span data-ttu-id="b858a-134">ただし、組織は自身で選択した実施事項、他の技術制御、そして管理プロセスに関しては、ベンダーによるそれらの保証を補完する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b858a-134">However, an organization needs to complement those vendor assurances with their own implementation choices, other technology controls, and administrative processes.</span></span> <span data-ttu-id="b858a-135">同レポートでは既に、適用可能なすべての統制の 94% 以上が直接カバーされてています。</span><span class="sxs-lookup"><span data-stu-id="b858a-135">The report shows already over 94% direct coverage of the full list of applicable controls.</span></span> <span data-ttu-id="b858a-136">カバーされていない規制に関しては、Microsoft がレポートにおいて、準拠する方法に関するガイダンスを提供しています。</span><span class="sxs-lookup"><span data-stu-id="b858a-136">For the remaining controls, Microsoft provides guidance in the report on how compliance with those controls can be demonstrated.</span></span>

> [!NOTE]
> <span data-ttu-id="b858a-137">NEN 7510 では、すべての規制を実施することを主要な目的としてはいませんがその大部分をカバーする Microsoft のオンライン サービスは、すべての規制に対応する上で役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b858a-137">Implementing the full list of controls is not the primary purpose of NEN 7510 (although the large coverage of Microsoft Online Services does help).</span></span> <span data-ttu-id="b858a-138">NEN 7510 では、組織がどの規制が適用されるか判断するため、組織が利用できるリスクベースの情報セキュリティ システムの実行を義務付けています。</span><span class="sxs-lookup"><span data-stu-id="b858a-138">NEN 7510 mandates the implementation of a risk-based information security system that can be used by an organization to determine which controls are applicable to them.</span></span>

<span data-ttu-id="b858a-139">**NEN 7510 カバレッジ レポートは法的拘束力を持つ文書ですか?**</span><span class="sxs-lookup"><span data-stu-id="b858a-139">**Is the NEN 7510 coverage report a legal binding document?**</span></span>

<span data-ttu-id="b858a-140">いいえ。</span><span class="sxs-lookup"><span data-stu-id="b858a-140">No.</span></span> <span data-ttu-id="b858a-141">これは、お客様の社内的な NEN 7510 保証プロセスをサポートするツールであり、NEN 7510 コンプライアンスの実行可能性への信頼と信任を確立するためのものです。</span><span class="sxs-lookup"><span data-stu-id="b858a-141">It is a supporting tool for the customer's internal NEN 7510 assurance process and helps to establish confidence and trust that NEN 7510 compliance is feasible.</span></span> <span data-ttu-id="b858a-142">独立監査人である KPMG によって作成されたこのレポートは、説明として提供され、法的な免責事項があります。</span><span class="sxs-lookup"><span data-stu-id="b858a-142">The report (created by independent auditor, KPMG) has a descriptive status and includes a legal disclaimer.</span></span>

<span data-ttu-id="b858a-143">**Microsoft はレポートの作成に出資しましたか?**</span><span class="sxs-lookup"><span data-stu-id="b858a-143">**Did Microsoft pay for the report?**</span></span>

<span data-ttu-id="b858a-144">Microsoft は自社の世界中の保証と NEN 7510 標準の統制との対応付けを実施しました。</span><span class="sxs-lookup"><span data-stu-id="b858a-144">Microsoft created a mapping between its global assurances to the controls in the NEN 7510 standard.</span></span> <span data-ttu-id="b858a-145">その後、Microsoft は NEN 7510 に対応付けられた統制に関する独立した審査を、独立監査人である KPMG に委託しました。</span><span class="sxs-lookup"><span data-stu-id="b858a-145">Microsoft then hired KPMG (an independent auditor) to perform an independent review on the control mapping to NEN 7510, which resulted in the report.</span></span>

<span data-ttu-id="b858a-146">**このレポートを共有することはできますか?**</span><span class="sxs-lookup"><span data-stu-id="b858a-146">**Can we share this report?**</span></span>

<span data-ttu-id="b858a-147">レポートは機密保持契約 (NDA) の元でお客様に提供され、お客様の参照のみを前提としており、また Microsoft の Service Trust Portal 以外のチャネルを介した複製および開示はできません。</span><span class="sxs-lookup"><span data-stu-id="b858a-147">The report is provided with you under a non-disclosure agreement (NDA), on the basis that it is for customer information only and that it will not be copied or disclosed via other channels than the Microsoft Service Trust Portal.</span></span>

<span data-ttu-id="b858a-148">お客様はレポートを、コンプライアンスまたは保証プロセスの一環として、社内外の監査人と共有することができます。</span><span class="sxs-lookup"><span data-stu-id="b858a-148">Customers can share the report with their own internal or external auditor as part of their compliance or assurance processes.</span></span>

## <a name="resources"></a><span data-ttu-id="b858a-149">リソース</span><span class="sxs-lookup"><span data-stu-id="b858a-149">Resources</span></span>

- [<span data-ttu-id="b858a-150">NEN について</span><span class="sxs-lookup"><span data-stu-id="b858a-150">About NEN</span></span>](https://www.nen.nl/About-NEN.htm)
- [<span data-ttu-id="b858a-151">NEN 7510:2011 標準</span><span class="sxs-lookup"><span data-stu-id="b858a-151">NEN 7510:2011 standard</span></span>](https://www.nen.nl/NEN-Shop-2/Standard/NEN-75102011-nl.htm)
- [<span data-ttu-id="b858a-152">Microsoft Trust Center のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="b858a-152">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
