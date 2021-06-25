---
title: 情報システム セキュリティ管理および評価プログラム (ISMAP)
description: Microsoft は、情報システム セキュリティ管理および評価プログラム (ISMAP) の要件を満たす制御を行っています。
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
ms.openlocfilehash: c6f2a33c0acc3459b220773dccbd63c24ef199af
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089628"
---
# <a name="information-system-security-management-and-assessment-program-ismap"></a><span data-ttu-id="2d449-104">情報システム セキュリティ管理および評価プログラム (ISMAP)</span><span class="sxs-lookup"><span data-stu-id="2d449-104">Information System Security Management and Assessment Program (ISMAP)</span></span>

## <a name="ismap-overview"></a><span data-ttu-id="2d449-105">ISMAP の概要</span><span class="sxs-lookup"><span data-stu-id="2d449-105">ISMAP overview</span></span>

<span data-ttu-id="2d449-106">情報システム セキュリティ管理および評価プログラム (ISMAP) は、日本政府が管理するクラウド サービスのアセスメント プログラムです。</span><span class="sxs-lookup"><span data-stu-id="2d449-106">The Information System Security Management and Assessment Program (ISMAP) is a cloud services assessment program administered by the Japanese government.</span></span> <span data-ttu-id="2d449-107">本プログラムは、2020 年 5 月 26 日に正式に発表されたもので、日本政府のセキュリティ要件を満たすクラウド サービスを評価し登録することで、政府機関向けクラウド サービス調達における適切なセキュリティを確保するために設計されています。</span><span class="sxs-lookup"><span data-stu-id="2d449-107">The program was officially announced on 26 May 2020, and it was designed to ensure appropriate security in government cloud services procurement by evaluating and registering cloud services that meet the Japanese government security requirements.</span></span> <span data-ttu-id="2d449-108">公的機関の調達プログラムへの参加を予定しているクラウド サービス プロバイダーは、ISMAP が承認した独立した第三者監査会社によって管理される ISMAP 認証を申請することができます。</span><span class="sxs-lookup"><span data-stu-id="2d449-108">Cloud service providers who intend to participate in public sector procurement programs can apply for ISMAP certification that is administered by an independent third-party auditing firm approved by ISMAP.</span></span> <span data-ttu-id="2d449-109">日本の政府機関は、ISMAP に登録されたクラウド サービス事業者からクラウド サービスを調達することで、個別に独自の評価を行う必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="2d449-109">Japanese government agencies can then procure cloud services from cloud service providers registered with ISMAP instead of conducting their own individual assessments.</span></span>

<span data-ttu-id="2d449-110">ISMAP の詳細については、公式 [ISMAPWeb サイト](https://www.ismap.go.jp/csm)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2d449-110">For more information about ISMAP, see the official [ISMAP web site](https://www.ismap.go.jp/csm).</span></span>

## <a name="microsoft-and-ismap"></a><span data-ttu-id="2d449-111">Microsoft と ISMAP</span><span class="sxs-lookup"><span data-stu-id="2d449-111">Microsoft and ISMAP</span></span>

<span data-ttu-id="2d449-112">Microsoft クラウド サービスは、公式 [ISMAP クラウド サービス リスト](https://www.ismap.go.jp/csm?id=cloud_service_list)に示されるように、ISMAP に基づいて評価され、認証されます。</span><span class="sxs-lookup"><span data-stu-id="2d449-112">Microsoft cloud services have been assessed and certified under ISMAP as shown on the official [ISMAP cloud services list](https://www.ismap.go.jp/csm?id=cloud_service_list).</span></span> <span data-ttu-id="2d449-113">この評価は、ISMAP の承認を受けた独立したサードパーティの監査法人によって行われました。</span><span class="sxs-lookup"><span data-stu-id="2d449-113">The assessment was conducted by an independent third-party auditing firm approved by ISMAP.</span></span> <span data-ttu-id="2d449-114">Microsoft の製品およびサービスには、組織が国、地域、および業界固有の要件に準拠するための包括的なコンプライアンス保証が用意されています。</span><span class="sxs-lookup"><span data-stu-id="2d449-114">Microsoft products and services provide comprehensive compliance assurances to help your organization comply with national, regional, and industry-specific requirements.</span></span>

## <a name="applicability"></a><span data-ttu-id="2d449-115">適用対象</span><span class="sxs-lookup"><span data-stu-id="2d449-115">Applicability</span></span>

<span data-ttu-id="2d449-116">ISMAP 認証の対象となる Azure リージョンは、以下の公式 [ISMAP クラウド サービス リスト](https://www.ismap.go.jp/csm?id=cloud_service_list)に示されているとおりです。</span><span class="sxs-lookup"><span data-stu-id="2d449-116">The following Azure regions are in scope for ISMAP certification as shown on the official [ISMAP cloud services list](https://www.ismap.go.jp/csm?id=cloud_service_list):</span></span>

- <span data-ttu-id="2d449-117">東日本</span><span class="sxs-lookup"><span data-stu-id="2d449-117">Japan East</span></span>
- <span data-ttu-id="2d449-118">西日本</span><span class="sxs-lookup"><span data-stu-id="2d449-118">Japan West</span></span>
- <span data-ttu-id="2d449-119">Azure Government と Azure China のリージョンを除き、日本の顧客が契約して利用できる世界のリージョンをさらに 40 件追加しました。</span><span class="sxs-lookup"><span data-stu-id="2d449-119">40 more regions worldwide that are available to Japanese customers under contract, excluding Azure Government and Azure China regions.</span></span>

## <a name="services-in-scope"></a><span data-ttu-id="2d449-120">対象となるサービス</span><span class="sxs-lookup"><span data-stu-id="2d449-120">Services in scope</span></span>

<span data-ttu-id="2d449-121">ISMAP 認証の対象となる Microsoft クラウド サービスは、以下の公式 [ISMAP クラウド サービス リスト](https://www.ismap.go.jp/csm?id=cloud_service_list)に示されているとおりです。</span><span class="sxs-lookup"><span data-stu-id="2d449-121">The following Microsoft cloud services are in scope for ISMAP certification as shown on the official [ISMAP cloud services list](https://www.ismap.go.jp/csm?id=cloud_service_list):</span></span>

- <span data-ttu-id="2d449-122">Azure、Azure DevOps、Dynamics 365、その他の Microsoft Online サービス</span><span class="sxs-lookup"><span data-stu-id="2d449-122">Azure, Azure DevOps, Dynamics 365, and other Microsoft online services</span></span>
- <span data-ttu-id="2d449-123">Office 365 サービス</span><span class="sxs-lookup"><span data-stu-id="2d449-123">Office 365 services</span></span>

## <a name="audit-reports-and-certificates"></a><span data-ttu-id="2d449-124">監査レポートと認証</span><span class="sxs-lookup"><span data-stu-id="2d449-124">Audit reports and certificates</span></span>

<span data-ttu-id="2d449-125">Microsoft ISMAP 認証のエビデンスは、公式 [ISMAP クラウド サービス リスト](https://www.ismap.go.jp/csm?id=cloud_service_list)で入手可能です。</span><span class="sxs-lookup"><span data-stu-id="2d449-125">Evidence of Microsoft ISMAP certification is available from the official [ISMAP cloud services list](https://www.ismap.go.jp/csm?id=cloud_service_list).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="2d449-126">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="2d449-126">Frequently asked questions</span></span>

<span data-ttu-id="2d449-127">**ISMAP 認証は誰に適用されますか?**</span><span class="sxs-lookup"><span data-stu-id="2d449-127">**To whom does ISMAP certification apply?**</span></span>

<span data-ttu-id="2d449-128">ISMAP 認証は、日本の政府機関が公的機関の調達プログラムを通じて利用可能なクラウド サービスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="2d449-128">ISMAP certification applies to cloud services that are available to Japanese government agencies through public sector procurement programs.</span></span> <span data-ttu-id="2d449-129">ISMAP は、日本政府のセキュリティ要件を満たすクラウド サービスを評価し登録することで、政府機関向けクラウド サービス調達における適切なセキュリティを確保するために設計されています。</span><span class="sxs-lookup"><span data-stu-id="2d449-129">ISMAP ensures appropriate security in government cloud services procurement by evaluating and registering cloud services that meet the Japanese government security requirements.</span></span>

<span data-ttu-id="2d449-130">**ISMAP 要件に関する詳細情報はどこで入手できますか?**</span><span class="sxs-lookup"><span data-stu-id="2d449-130">**Where can I get more information on ISMAP requirements?**</span></span>

<span data-ttu-id="2d449-131">ISMAP の詳細については、公式 [ISMAPWeb サイト](https://www.ismap.go.jp/csm)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2d449-131">For more information about ISMAP, see the official [ISMAP web site](https://www.ismap.go.jp/csm).</span></span>

<span data-ttu-id="2d449-132">**Microsoft の ISMAP へのアプローチについて、どこで情報を得ることができますか?**</span><span class="sxs-lookup"><span data-stu-id="2d449-132">**Where can I get more information about Microsoft approach to ISMAP?**</span></span>

<span data-ttu-id="2d449-133">ISMAP に対する Microsoft のアプローチについては、「[Microsoft のコンプライアンスへのアプローチ: ISMAP (日本語)](https://www.microsoft.com/ja-jp/mscorp/legal/compliance?activetab=service%3aprimaryr7)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d449-133">For more information about Microsoft approach to ISMAP, see [Microsoft approach to compliance: ISMAP (Japanese)](https://www.microsoft.com/ja-jp/mscorp/legal/compliance?activetab=service%3aprimaryr7).</span></span>

## <a name="resources"></a><span data-ttu-id="2d449-134">リソース</span><span class="sxs-lookup"><span data-stu-id="2d449-134">Resources</span></span>

- [<span data-ttu-id="2d449-135">ISMAP 公式サイト</span><span class="sxs-lookup"><span data-stu-id="2d449-135">ISMAP official site</span></span>](https://www.ismap.go.jp/csm)
- [<span data-ttu-id="2d449-136">Microsoft のコンプライアンスへのアプローチ: ISMAP (日本語)</span><span class="sxs-lookup"><span data-stu-id="2d449-136">Microsoft approach to compliance: ISMAP (Japanese)</span></span>](https://www.microsoft.com/ja-jp/mscorp/legal/compliance?activetab=service%3aprimaryr7)
- [<span data-ttu-id="2d449-137">日本クラウド セキュリティ ゴールド マーク</span><span class="sxs-lookup"><span data-stu-id="2d449-137">Japan Cloud Security Mark Gold</span></span>](offering-cs-mark-gold-japan.md)
- [<span data-ttu-id="2d449-138">FISC (日本)</span><span class="sxs-lookup"><span data-stu-id="2d449-138">FISC (Japan)</span></span>](offering-fisc-japan.md)
- [<span data-ttu-id="2d449-139">Microsoft オンライン サービス条件 (OST)</span><span class="sxs-lookup"><span data-stu-id="2d449-139">Microsoft Online Services Terms (OST)</span></span>](https://aka.ms/Online-Services-Terms)
- [<span data-ttu-id="2d449-140">Microsoft オンライン サービス規約 （OST） データ保護に関する補遺 （DPA）</span><span class="sxs-lookup"><span data-stu-id="2d449-140">Microsoft OST Data Protection Addendum (DPA)</span></span>](https://aka.ms/DPA)
- [<span data-ttu-id="2d449-141">Microsoft Trust Center のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="2d449-141">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
