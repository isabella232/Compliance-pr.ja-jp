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
ms.openlocfilehash: da53b5e2cdac7095e2fc3ff9b243d2863b85fdbf
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088786"
---
# <a name="new-zealand-government-cloud-computing-security-and-privacy-considerations"></a><span data-ttu-id="c78d9-104">ニュージーランド政府機関向けクラウド コンピューティングのセキュリティとプライバシーに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="c78d9-104">New Zealand Government Cloud Computing Security and Privacy Considerations</span></span>

## <a name="new-zealand-government-cloud-computing-security-and-privacy-overview"></a><span data-ttu-id="c78d9-105">ニュージーランド政府機関向けクラウド コンピューティングのセキュリティとプライバシーの概要</span><span class="sxs-lookup"><span data-stu-id="c78d9-105">New Zealand Government Cloud Computing Security and Privacy overview</span></span>

<span data-ttu-id="c78d9-106">2015 年 10 月、ニュージーランド政府は、公共部門全体での情報技術の使用に関する「クラウド ファースト」ポリシーを再確認した、改訂された全政府 ICT 戦略を支持しました。</span><span class="sxs-lookup"><span data-stu-id="c78d9-106">In October 2015, the New Zealand Government endorsed a revised all-government ICT strategy that reaffirmed its 'cloud first' policy on using information technology across the public sector.</span></span> <span data-ttu-id="c78d9-107">改訂された戦略は、NZ 政府最高情報責任者 (GCIO) の権限の下で開発および実装された「クラウド コンピューティング リスクと保証フレームワーク」を保持します。</span><span class="sxs-lookup"><span data-stu-id="c78d9-107">The revised strategy retains the 'Cloud Computing Risk and Assurance Framework' that was developed and implemented under the authority of the NZ Government Chief Information Officer (GCIO).</span></span>

<span data-ttu-id="c78d9-108">政府は、クラウド サービスを評価および採用する際に、すべてのニュージーランド国家サービス機関がこのフレームワーク内で機能すると予想しています。</span><span class="sxs-lookup"><span data-stu-id="c78d9-108">The government expects all New Zealand State Service agencies to work within this framework when assessing and adopting cloud services.</span></span> <span data-ttu-id="c78d9-109">「クラウド コンピューティングの要件」は、政府機関がクラウド サービスを導入する際に行う必要がある操作と、政府のクラウド ポリシーの履歴の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="c78d9-109">'Requirements for Cloud Computing' outlines what agencies must do when adopting cloud services along with an overview of the history of the government's cloud policy.</span></span>

<span data-ttu-id="c78d9-110">NZ 政府機関が潜在的なクラウド ソリューションに関する一貫した堅牢なデューデリジェンスを実施する際に支援するために、GCIO はクラウド コンピューティング: Information Security and [Privacy Considerations (ISPC)](https://www.digital.govt.nz/dmsdocument/1~cloud-computing-information-security-and-privacy-considerations/html)を公開しました。</span><span class="sxs-lookup"><span data-stu-id="c78d9-110">To assist NZ government agencies in conducting consistent and robust due diligence on potential cloud solutions, the GCIO has published [Cloud Computing: Information Security and Privacy Considerations (ISPC)](https://www.digital.govt.nz/dmsdocument/1~cloud-computing-information-security-and-privacy-considerations/html).</span></span> <span data-ttu-id="c78d9-111">このドキュメントには、データの主権、プライバシー、セキュリティ、ガバナンス、機密性、データ整合性、可用性、インシデント対応と管理に焦点を当てた 100 以上の質問が含まれている。</span><span class="sxs-lookup"><span data-stu-id="c78d9-111">This document contains more than 100 questions focused on data sovereignty, privacy, security, governance, confidentiality, data integrity, availability, and incident response and management.</span></span> <span data-ttu-id="c78d9-112">ISPC は、クラウド サービス プロバイダーが正式なコンプライアンスを実証する必要がある NZ 政府機関の標準を定義していない。</span><span class="sxs-lookup"><span data-stu-id="c78d9-112">The ISPC does not define a NZ government standard against which cloud service providers must demonstrate formal compliance.</span></span> <span data-ttu-id="c78d9-113">ただし、ドキュメントに記載されている質問の多くは、クラウド サービス プロバイダーがさまざまな関連基準に準拠する方法を理解することの重要性を示しています。</span><span class="sxs-lookup"><span data-stu-id="c78d9-113">Many of the questions set out in the document do, however, point toward the importance of understanding how cloud service providers comply with a wide array of relevant standards.</span></span>

## <a name="microsoft-and-new-zealand-government-cloud-computing-security-and-privacy-considerations"></a><span data-ttu-id="c78d9-114">Microsoft およびニュージーランド政府機関向けクラウド コンピューティングのセキュリティとプライバシーに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="c78d9-114">Microsoft and New Zealand Government Cloud Computing Security and Privacy Considerations</span></span>

<span data-ttu-id="c78d9-115">政府機関が Microsoft エンタープライズ クラウド サービスの分析と評価を行うのを支援するために、Microsoft ニュージーランドは、エンタープライズ クラウド サービスが Microsoft クラウド サービスが認定される標準にリンクすることで、「クラウド コンピューティング ISPC」に記載されている質問に対処する方法を示すドキュメントを作成しました。</span><span class="sxs-lookup"><span data-stu-id="c78d9-115">To help agencies undertake their analysis and evaluation of Microsoft enterprise cloud services, Microsoft New Zealand has produced documents showing how its enterprise cloud services address the questions set out in the 'Cloud Computing ISPC' by linking them to the standards against which Microsoft cloud services are certified.</span></span> <span data-ttu-id="c78d9-116">これらの認定は、Microsoft が、プライバシーとセキュリティのリスクを効果的に軽減し、データ主権の懸念に対処するために、クラウド サービスが設計、構築、運用されるという公的および民間部門の両方の顧客に保証する方法の中心です。</span><span class="sxs-lookup"><span data-stu-id="c78d9-116">These certifications are central to how Microsoft assures both public and private sector customers that its cloud services are designed, built, and operated to effectively mitigate privacy and security risks and address data sovereignty concerns.</span></span> <span data-ttu-id="c78d9-117">[クラウド コンピューティング ISPC に対する Azure の応答は](https://azure.microsoft.com/resources/microsoft-azure-response-to-nz-gcio-cloud-computing-information-security-privacy-considerations/)、お客様がダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="c78d9-117">The [Azure response to Cloud Computing ISPC](https://azure.microsoft.com/resources/microsoft-azure-response-to-nz-gcio-cloud-computing-information-security-privacy-considerations/) is available to customers for download.</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="c78d9-118">対象となる Microsoft のクラウド サービス</span><span class="sxs-lookup"><span data-stu-id="c78d9-118">Microsoft in-scope cloud services</span></span>

- [<span data-ttu-id="c78d9-119">Azure および Azure Government</span><span class="sxs-lookup"><span data-stu-id="c78d9-119">Azure and Azure Government</span></span>](https://aka.ms/AzureCompliance)
- [<span data-ttu-id="c78d9-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c78d9-120">Dynamics 365</span></span>](https://aka.ms/d365-compliance-list)
- <span data-ttu-id="c78d9-121">Intune</span><span class="sxs-lookup"><span data-stu-id="c78d9-121">Intune</span></span>
- <span data-ttu-id="c78d9-122">Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに搭載されているサービス)</span><span class="sxs-lookup"><span data-stu-id="c78d9-122">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>
- [<span data-ttu-id="c78d9-123">Office 365</span><span class="sxs-lookup"><span data-stu-id="c78d9-123">Office 365</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=2077751)
- <span data-ttu-id="c78d9-124">Exchange Online、SharePointオンライン、およびMicrosoft Teams。</span><span class="sxs-lookup"><span data-stu-id="c78d9-124">Exchange Online, SharePoint Online, and Microsoft Teams.</span></span> <span data-ttu-id="c78d9-125">Microsoft NZ は、GCIO チームと一緒に、アプリケーションと SEEMail を統合する参照Exchange Online開発しました。</span><span class="sxs-lookup"><span data-stu-id="c78d9-125">Microsoft NZ has worked with the GCIO team to develop a reference architecture for integrating Exchange Online and SEEMail.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="c78d9-126">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="c78d9-126">Frequently asked questions</span></span>

<span data-ttu-id="c78d9-127">**フレームワークは誰に適用されますか?**</span><span class="sxs-lookup"><span data-stu-id="c78d9-127">**To whom does the framework apply?**</span></span>

<span data-ttu-id="c78d9-128">GCIO の義務に該当する組織、公的および非公的サービス部門、20 の地区の保健委員会、および 7 つのクラウン エンティティは、クラウド サービスの使用を決定する際にフレームワークに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="c78d9-128">Organizations that fall under the GCIO mandate, the public and non-public service departments, the 20 district health boards, and 7 Crown entities, must adhere to the framework when they are deciding on the use of a cloud service.</span></span>

<span data-ttu-id="c78d9-129">**代理店は、ICT システムの認定プロセスで、このフレームワークに対する Microsoft の応答を使用できますか?**</span><span class="sxs-lookup"><span data-stu-id="c78d9-129">**Can my agency use Microsoft's responses to this framework in the certification process of our ICT systems?**</span></span>

<span data-ttu-id="c78d9-130">ニュージーランド情報セキュリティマニュアルの下で、機関が ICT システムの認定と[](https://go.microsoft.com/fwlink/p/?linkid=2099496)認定を受ける必要がある場合は、分析の一環としてこれらの応答を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c78d9-130">If your agency is required to undertake certification and accreditation of its ICT system under the [New Zealand Information Security Manual](https://go.microsoft.com/fwlink/p/?linkid=2099496), then you can use these responses as part of your analysis.</span></span>

## <a name="resources"></a><span data-ttu-id="c78d9-131">リソース</span><span class="sxs-lookup"><span data-stu-id="c78d9-131">Resources</span></span>

- [<span data-ttu-id="c78d9-132">オフショアホスト型生産性サービスのセキュリティ要件:Officeの準拠ガイドOffice 365</span><span class="sxs-lookup"><span data-stu-id="c78d9-132">Security requirements for offshore hosted Office productivity services: conformance guide for Office 365</span></span>](https://aka.ms/o365-gcio-conformance-guidance)
- [<span data-ttu-id="c78d9-133">NZ Government ICT Strategy 2015</span><span class="sxs-lookup"><span data-stu-id="c78d9-133">NZ Government ICT Strategy 2015</span></span>](https://www.ict.govt.nz/strategy-and-action-plan/strategy/)
- [<span data-ttu-id="c78d9-134">クラウド コンピューティング: 情報セキュリティとプライバシーに関する考慮事項 (ISPC)</span><span class="sxs-lookup"><span data-stu-id="c78d9-134">Cloud Computing: Information Security and Privacy Considerations (ISPC)</span></span>](https://www.digital.govt.nz/standards-and-guidance/technology-and-architecture/cloud-services/)
- [<span data-ttu-id="c78d9-135">Microsoft オンライン サービス条件</span><span class="sxs-lookup"><span data-stu-id="c78d9-135">Microsoft Online Services Terms</span></span>](https://aka.ms/Online-Services-Terms)
- [<span data-ttu-id="c78d9-136">Microsoft セキュリティ センターのコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="c78d9-136">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)

## <a name="microsoft-responses-to-cloud-computing-ipsc"></a><span data-ttu-id="c78d9-137">「クラウド コンピューティング IPSC」に対する Microsoft の応答</span><span class="sxs-lookup"><span data-stu-id="c78d9-137">Microsoft responses to 'Cloud Computing IPSC'</span></span>

- [<span data-ttu-id="c78d9-138">Azure</span><span class="sxs-lookup"><span data-stu-id="c78d9-138">Azure</span></span>](https://aka.ms/Azure-NZ-response)
- [<span data-ttu-id="c78d9-139">Intune</span><span class="sxs-lookup"><span data-stu-id="c78d9-139">Intune</span></span>](https://aka.ms/Intune-NZ-response)
- [<span data-ttu-id="c78d9-140">Office 365</span><span class="sxs-lookup"><span data-stu-id="c78d9-140">Office 365</span></span>](https://aka.ms/O365-NZ-Response)
- [<span data-ttu-id="c78d9-141">Power BI</span><span class="sxs-lookup"><span data-stu-id="c78d9-141">Power BI</span></span>](https://download.microsoft.com/download/5/1/7/51726B9B-2E76-49C4-9D4F-A36BF025CB93/Response-to-GCIO-105-questions-Power-BI.pdf)
