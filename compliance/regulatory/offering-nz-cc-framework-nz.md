---
title: ニュージーランド政府機関向けクラウド コンピューティングのセキュリティとプライバシーに関する考慮事項
description: Microsoft NZ は、ニュージーランドのクラウド コンピューティング フレームワークで公開されている質問に対応します。
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
ms.openlocfilehash: 4c27c84d2abc2de4866471d652d8b11351bc3168
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385657"
---
# <a name="new-zealand-government-information-security-and-privacy-considerations-ispc"></a><span data-ttu-id="b31f2-104">ニュージーランド政府機関の情報セキュリティとプライバシーに関する考慮事項 (ISPC)</span><span class="sxs-lookup"><span data-stu-id="b31f2-104">New Zealand Government Information Security and Privacy Considerations (ISPC)</span></span>

## <a name="new-zealand-government-information-security-and-privacy-considerations-overview"></a><span data-ttu-id="b31f2-105">ニュージーランド政府機関の情報セキュリティとプライバシーに関する考慮事項の概要</span><span class="sxs-lookup"><span data-stu-id="b31f2-105">New Zealand Government Information Security and Privacy Considerations overview</span></span>

<span data-ttu-id="b31f2-106">2015 年 10 月、ニュージーランド政府は、公共部門全体での情報技術の使用に関する「クラウド ファースト」ポリシーを再確認した、改訂された全政府 ICT 戦略を支持しました。</span><span class="sxs-lookup"><span data-stu-id="b31f2-106">In October 2015, the New Zealand Government endorsed a revised all-government ICT strategy that reaffirmed its 'cloud first' policy on using information technology across the public sector.</span></span> <span data-ttu-id="b31f2-107">改訂された戦略は、NZ 政府最高情報責任者 (GCIO) の権限の下で開発および実装された「クラウド コンピューティング リスクと保証フレームワーク」を保持します。</span><span class="sxs-lookup"><span data-stu-id="b31f2-107">The revised strategy retains the 'Cloud Computing Risk and Assurance Framework' that was developed and implemented under the authority of the NZ Government Chief Information Officer (GCIO).</span></span>

<span data-ttu-id="b31f2-108">政府は、クラウド サービスを評価および採用する際に、すべてのニュージーランド国家サービス機関がこのフレームワーク内で機能すると予想しています。</span><span class="sxs-lookup"><span data-stu-id="b31f2-108">The government expects all New Zealand State Service agencies to work within this framework when assessing and adopting cloud services.</span></span> <span data-ttu-id="b31f2-109">「クラウド コンピューティングの要件」は、政府機関がクラウド サービスを導入する際に行う必要がある操作と、政府のクラウド ポリシーの履歴の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="b31f2-109">'Requirements for Cloud Computing' outlines what agencies must do when adopting cloud services along with an overview of the history of the government's cloud policy.</span></span>

<span data-ttu-id="b31f2-110">NZ 政府機関が潜在的なクラウド ソリューションに関する一貫した堅牢なデューデリジェンスを実施する際に支援するために、GCIO はクラウド コンピューティング: Information Security and [Privacy Considerations (ISPC)](https://www.digital.govt.nz/dmsdocument/1~cloud-computing-information-security-and-privacy-considerations/html)を公開しました。</span><span class="sxs-lookup"><span data-stu-id="b31f2-110">To assist NZ government agencies in conducting consistent and robust due diligence on potential cloud solutions, the GCIO has published [Cloud Computing: Information Security and Privacy Considerations (ISPC)](https://www.digital.govt.nz/dmsdocument/1~cloud-computing-information-security-and-privacy-considerations/html).</span></span> <span data-ttu-id="b31f2-111">このドキュメントには、データの主権、プライバシー、セキュリティ、ガバナンス、機密性、データ整合性、可用性、インシデント対応と管理に焦点を当てた 100 以上の質問が含まれている。</span><span class="sxs-lookup"><span data-stu-id="b31f2-111">This document contains more than 100 questions focused on data sovereignty, privacy, security, governance, confidentiality, data integrity, availability, and incident response and management.</span></span> <span data-ttu-id="b31f2-112">ISPC は、クラウド サービス プロバイダーが正式なコンプライアンスを実証する必要がある NZ 政府機関の標準を定義していない。</span><span class="sxs-lookup"><span data-stu-id="b31f2-112">The ISPC does not define a NZ government standard against which cloud service providers must demonstrate formal compliance.</span></span> <span data-ttu-id="b31f2-113">ただし、ドキュメントに記載されている質問の多くは、クラウド サービス プロバイダーがさまざまな関連基準に準拠する方法を理解することの重要性を示しています。</span><span class="sxs-lookup"><span data-stu-id="b31f2-113">Many of the questions set out in the document do, however, point toward the importance of understanding how cloud service providers comply with a wide array of relevant standards.</span></span>

## <a name="microsoft-and-new-zealand-government-cloud-computing-security-and-privacy-considerations"></a><span data-ttu-id="b31f2-114">Microsoft およびニュージーランド政府機関向けクラウド コンピューティングのセキュリティとプライバシーに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="b31f2-114">Microsoft and New Zealand Government Cloud Computing Security and Privacy Considerations</span></span>

<span data-ttu-id="b31f2-115">政府機関が Microsoft エンタープライズ クラウド サービスの分析と評価を行うのを支援するために、Microsoft ニュージーランドは、エンタープライズ クラウド サービスが Microsoft クラウド サービスが認定される標準にリンクすることで、「クラウド コンピューティング ISPC」に記載されている質問に対処する方法を示すドキュメントを作成しました。</span><span class="sxs-lookup"><span data-stu-id="b31f2-115">To help agencies undertake their analysis and evaluation of Microsoft enterprise cloud services, Microsoft New Zealand has produced documents showing how its enterprise cloud services address the questions set out in the 'Cloud Computing ISPC' by linking them to the standards against which Microsoft cloud services are certified.</span></span> <span data-ttu-id="b31f2-116">これらの認定は、Microsoft が、プライバシーとセキュリティのリスクを効果的に軽減し、データ主権の懸念に対処するために、クラウド サービスが設計、構築、運用されるという公的および民間部門の両方の顧客に保証する方法の中心です。</span><span class="sxs-lookup"><span data-stu-id="b31f2-116">These certifications are central to how Microsoft assures both public and private sector customers that its cloud services are designed, built, and operated to effectively mitigate privacy and security risks and address data sovereignty concerns.</span></span> <span data-ttu-id="b31f2-117">[クラウド コンピューティング ISPC に対する Azure の応答は](https://azure.microsoft.com/resources/microsoft-azure-response-to-nz-gcio-cloud-computing-information-security-privacy-considerations/)、お客様がダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="b31f2-117">The [Azure response to Cloud Computing ISPC](https://azure.microsoft.com/resources/microsoft-azure-response-to-nz-gcio-cloud-computing-information-security-privacy-considerations/) is available to customers for download.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="b31f2-118">Microsoft のスコープ内クラウド プラットフォームと&サービス</span><span class="sxs-lookup"><span data-stu-id="b31f2-118">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="b31f2-119">Azure および Azure Government</span><span class="sxs-lookup"><span data-stu-id="b31f2-119">Azure and Azure Government</span></span>
- [<span data-ttu-id="b31f2-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b31f2-120">Dynamics 365</span></span>](https://aka.ms/d365-compliance-list)
- <span data-ttu-id="b31f2-121">Intune</span><span class="sxs-lookup"><span data-stu-id="b31f2-121">Intune</span></span>
- <span data-ttu-id="b31f2-122">Office 365</span><span class="sxs-lookup"><span data-stu-id="b31f2-122">Office 365</span></span>
- <span data-ttu-id="b31f2-123">Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに搭載されているサービス)</span><span class="sxs-lookup"><span data-stu-id="b31f2-123">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>

## <a name="office-365-and-ispc"></a><span data-ttu-id="b31f2-124">Office 365 ISPC</span><span class="sxs-lookup"><span data-stu-id="b31f2-124">Office 365 and ISPC</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="b31f2-125">Office 365クラウド環境</span><span class="sxs-lookup"><span data-stu-id="b31f2-125">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="b31f2-126">Office 365とスコープ内サービス</span><span class="sxs-lookup"><span data-stu-id="b31f2-126">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="b31f2-127">次の表を使用して、サービスとサブスクリプションOffice 365を決定します。</span><span class="sxs-lookup"><span data-stu-id="b31f2-127">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="b31f2-128">**適用対象**</span><span class="sxs-lookup"><span data-stu-id="b31f2-128">**Applicability**</span></span> | <span data-ttu-id="b31f2-129">**スコープ内サービス**</span><span class="sxs-lookup"><span data-stu-id="b31f2-129">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="b31f2-130">**Office 365**</span><span class="sxs-lookup"><span data-stu-id="b31f2-130">**Office 365**</span></span> | <span data-ttu-id="b31f2-131">Exchange Online, SharePoint, Skype for Business</span><span class="sxs-lookup"><span data-stu-id="b31f2-131">Exchange Online, SharePoint Online, Skype for Business</span></span> |

>[!Note]
><span data-ttu-id="b31f2-132">Microsoft NZ は GCIO チームと連携して、「Office 365: SEEMail Integration and Reference Architecture」で説明されている Exchange Online と SEEMail を統合するリファレンス アーキテクチャを開発しました。</span><span class="sxs-lookup"><span data-stu-id="b31f2-132">Microsoft NZ has worked with the GCIO team to develop a reference architecture for integrating Exchange Online and SEEMail described in Office 365: SEEMail Integration and Reference Architecture.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="b31f2-133">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="b31f2-133">Frequently asked questions</span></span>

<span data-ttu-id="b31f2-134">**フレームワークは誰に適用されますか?**</span><span class="sxs-lookup"><span data-stu-id="b31f2-134">**To whom does the framework apply?**</span></span>

<span data-ttu-id="b31f2-135">GCIO の義務に該当する組織、公的および非公的サービス部門、20 の地区の保健委員会、および 7 つのクラウン エンティティは、クラウド サービスの使用を決定する際にフレームワークに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b31f2-135">Organizations that fall under the GCIO mandate, the public and non-public service departments, the 20 district health boards, and 7 Crown entities, must adhere to the framework when they are deciding on the use of a cloud service.</span></span>

<span data-ttu-id="b31f2-136">**代理店は、ICT システムの認定プロセスで、このフレームワークに対する Microsoft の応答を使用できますか?**</span><span class="sxs-lookup"><span data-stu-id="b31f2-136">**Can my agency use Microsoft's responses to this framework in the certification process of our ICT systems?**</span></span>

<span data-ttu-id="b31f2-137">ニュージーランド情報セキュリティマニュアルの下で、機関が ICT システムの認定と[](https://go.microsoft.com/fwlink/p/?linkid=2099496)認定を受ける必要がある場合は、分析の一環としてこれらの応答を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b31f2-137">If your agency is required to undertake certification and accreditation of its ICT system under the [New Zealand Information Security Manual](https://go.microsoft.com/fwlink/p/?linkid=2099496), then you can use these responses as part of your analysis.</span></span>

## <a name="resources"></a><span data-ttu-id="b31f2-138">リソース</span><span class="sxs-lookup"><span data-stu-id="b31f2-138">Resources</span></span>

- [<span data-ttu-id="b31f2-139">オフショアホスト型生産性サービスのセキュリティ要件:Officeの準拠ガイドOffice 365</span><span class="sxs-lookup"><span data-stu-id="b31f2-139">Security requirements for offshore hosted Office productivity services: conformance guide for Office 365</span></span>](https://aka.ms/o365-gcio-conformance-guidance)
- [<span data-ttu-id="b31f2-140">NZ Government ICT Strategy 2015</span><span class="sxs-lookup"><span data-stu-id="b31f2-140">NZ Government ICT Strategy 2015</span></span>](https://www.ict.govt.nz/strategy-and-action-plan/strategy/)
- [<span data-ttu-id="b31f2-141">クラウド コンピューティング: 情報セキュリティとプライバシーに関する考慮事項 (ISPC)</span><span class="sxs-lookup"><span data-stu-id="b31f2-141">Cloud Computing: Information Security and Privacy Considerations (ISPC)</span></span>](https://www.digital.govt.nz/standards-and-guidance/technology-and-architecture/cloud-services/)
- [<span data-ttu-id="b31f2-142">Microsoft  オンライン サービス条件</span><span class="sxs-lookup"><span data-stu-id="b31f2-142">Microsoft Online Services Terms</span></span>](https://aka.ms/Online-Services-Terms)
- [<span data-ttu-id="b31f2-143">Microsoft セキュリティ センターのコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="b31f2-143">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)

## <a name="microsoft-responses-to-cloud-computing-ipsc"></a><span data-ttu-id="b31f2-144">クラウド コンピューティング IPSC に対する Microsoft の応答</span><span class="sxs-lookup"><span data-stu-id="b31f2-144">Microsoft responses to Cloud Computing IPSC</span></span>

- [<span data-ttu-id="b31f2-145">Azure</span><span class="sxs-lookup"><span data-stu-id="b31f2-145">Azure</span></span>](https://aka.ms/Azure-NZ-response)
- [<span data-ttu-id="b31f2-146">Intune</span><span class="sxs-lookup"><span data-stu-id="b31f2-146">Intune</span></span>](https://aka.ms/Intune-NZ-response)
- [<span data-ttu-id="b31f2-147">Office 365</span><span class="sxs-lookup"><span data-stu-id="b31f2-147">Office 365</span></span>](https://aka.ms/O365-NZ-Response)
- [<span data-ttu-id="b31f2-148">Power BI</span><span class="sxs-lookup"><span data-stu-id="b31f2-148">Power BI</span></span>](https://download.microsoft.com/download/5/1/7/51726B9B-2E76-49C4-9D4F-A36BF025CB93/Response-to-GCIO-105-questions-Power-BI.pdf)
