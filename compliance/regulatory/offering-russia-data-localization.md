---
title: ロシアの個人データのローカライズ要件
description: 個人データの収集、ロシア市民の個人データの記録、システム化、蓄積、保存、説明、抽出が、ロシアにある Microsoft サービスおよびデータベースでどのように実行されるのかについて説明します。
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
ms.openlocfilehash: 6ee6dc8a6132e76bd39487fbb51e03509e7d2a95
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50119896"
---
# <a name="russian-personal-data-localization-requirements"></a><span data-ttu-id="c242f-104">ロシアの個人データのローカライズ要件</span><span class="sxs-lookup"><span data-stu-id="c242f-104">Russian Personal Data Localization Requirements</span></span>

<span data-ttu-id="c242f-105">2015 年 9 月 1 日の現在、個人データオペレーターと見なされる組織は、個人データの収集、ロシア市民の個人データの記録、システム化、収集、保存、説明 (更新、変更)、抽出を、ロシアにあるデータベース (「個人データのローカライズ要件」) を通じて実行する必要があります。<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="c242f-105">As of September 1, 2015, organizations that are considered personal data operators must ensure that, when collecting personal data, Russian citizens' personal data recording, systematization, accumulation, storage, clarification (updating, changing), and extraction are performed through the databases located in Russia ('personal data localization requirement').<sup>1</sup></span></span>

<span data-ttu-id="c242f-106">Microsoft Azure、Microsoft 365、Dynamics 365、Power Platform などの個人データ処理を有効にしている組織 (教育機関を含むが、これらに限定されない) (以下「お客様」と呼ばれる) が利用できる Microsoft サービスは、ロシアの外部にあるデータ処理センターから提供されます (詳細については [、Microsoft セキュリティ](https://www.microsoft.com/trust-center)センターを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="c242f-106">Microsoft services available to organizations (including but not limited to educational institutions) (hereinafter referred to as 'customer'), including those enabling personal data processing such as Microsoft Azure, Microsoft 365, Dynamics 365, and Power Platform, are provided from data processing centers located outside of Russia (for more information visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center)).</span></span>

<span data-ttu-id="c242f-107">顧客情報システムによって処理される情報の種類とコンテンツに基づいて、そのようなシステム (Microsoft クラウド製品を使用するシステムを含む) は、個人データ情報システム ('PDIS'、'ISPD') と見なされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c242f-107">Based on the type and content of information processed by customer information systems, such systems, including those using Microsoft cloud products, may be deemed a personal data information system ('PDIS', 'ISPD').</span></span> <span data-ttu-id="c242f-108">お客様が、そのアーキテクチャと処理される情報の種類を通じて PDIS と見なされるシステムで Microsoft サービスを使用する場合、Microsoft は、以下に示す利用可能なソリューションの中でお客様に検討を招待します。</span><span class="sxs-lookup"><span data-stu-id="c242f-108">In cases where the customer would like to use Microsoft services in a system that qualifies as PDIS through its architecture and types of information processed, Microsoft invites its customers to consider, amongst other things, available solutions specified below.</span></span> <span data-ttu-id="c242f-109">提供されるシナリオはすべて、標準的なビジネス サービスの追加オプションとして、お客様が利用できます。</span><span class="sxs-lookup"><span data-stu-id="c242f-109">All the scenarios provided are available for customers as an additional option to standard business offerings.</span></span>

<span data-ttu-id="c242f-110">コンプライアンスを担当し、個人データのローカライズに適用される法的要件を分析および評価する PDIS の個人データオペレーターであるお客様であり、独自の判断で、PDIS での個人データ処理がロシアの個人データ法に準拠していることを確認するための十分な手段を個別に決定する必要があります。<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="c242f-110">It should be noted that it is the customer as personal data operator of PDIS who is in charge of compliance and shall analyze and assess applicable legal requirements for personal data localization, and at its own discretion, independently determine sufficient measures to ensure that personal data processing in PDIS complies with the Russian personal data law.<sup>2</sup></span></span>

## <a name="subscribing-to-microsoft-services"></a><span data-ttu-id="c242f-111">Microsoft サービスのサブスクライブ</span><span class="sxs-lookup"><span data-stu-id="c242f-111">Subscribing to Microsoft services</span></span>

### <a name="microsoft-id-management"></a><span data-ttu-id="c242f-112">Microsoft ID の管理</span><span class="sxs-lookup"><span data-stu-id="c242f-112">Microsoft ID Management</span></span>

<span data-ttu-id="c242f-113">Microsoft は、Microsoft サービスへのサブスクライブを検討する顧客を招待します。Microsoft クラウド ソリューション プロバイダー (CSP) パートナー経由の Microsoft Azure、Microsoft 365、Dynamics 365、および Power Platform。</span><span class="sxs-lookup"><span data-stu-id="c242f-113">Microsoft invites customers to consider subscribing to Microsoft services; Microsoft Azure, Microsoft 365, Dynamics 365, and Power Platform—via a Microsoft Cloud Solution Provider (CSP) partner.</span></span> <span data-ttu-id="c242f-114">詳しくは、CSP パートナーの [一覧をご覧ください](https://pinpoint.microsoft.com/search?type=services&campaign=691)。</span><span class="sxs-lookup"><span data-stu-id="c242f-114">For more information, see this [list of CSP partners](https://pinpoint.microsoft.com/search?type=services&campaign=691).</span></span>

### <a name="managing-user-identity-and-access-for-microsoft-services"></a><span data-ttu-id="c242f-115">Microsoft サービスのユーザー ID とアクセスの管理</span><span class="sxs-lookup"><span data-stu-id="c242f-115">Managing User Identity and Access for Microsoft services</span></span>

<span data-ttu-id="c242f-116">Microsoft Azure、Microsoft 365、Dynamics 365、Power Platform などの Microsoft サービスの場合、ユーザーの検証とアクセス管理は [Azure Active Directory (Azure Active Directory)](https://azure.microsoft.com/services/active-directory/)を通じて実行されます。</span><span class="sxs-lookup"><span data-stu-id="c242f-116">For Microsoft services such as Microsoft Azure, Microsoft 365, Dynamics 365, and Power Platform, user verification and access management are performed through [Azure Active Directory (Azure Active Directory)](https://azure.microsoft.com/services/active-directory/).</span></span> <span data-ttu-id="c242f-117">Microsoft のお客様が Microsoft クラウド サービス (Windows Server Active Directory (AD) や他の ID 管理システムなど) にローカル ID 管理システムを使用している場合、お客様は Azure AD Connect を介してそのようなシステムを Azure Active Directory (Azure Active Directory) と迅速に統合する機会があります。</span><span class="sxs-lookup"><span data-stu-id="c242f-117">In cases where a Microsoft customer uses a local identification management system for Microsoft cloud services (such as the Windows Server Active Directory (AD) or any other ID management system), the customer has an opportunity to swiftly integrate such system with the Azure Active Directory (Azure Active Directory) through Azure AD Connect.</span></span> <span data-ttu-id="c242f-118">詳細については [、Azure AD Connect を参照してください](/azure/active-directory/cloud-provisioning/)。</span><span class="sxs-lookup"><span data-stu-id="c242f-118">For more information, see the [Azure AD Connect](/azure/active-directory/cloud-provisioning/).</span></span> <span data-ttu-id="c242f-119">Microsoft のお客様は、サードパーティ ベンダーのアプリケーションとソリューションを使用して、ユーザーを管理し、ローカル ID システムを Azure AD に統合する場合があります。</span><span class="sxs-lookup"><span data-stu-id="c242f-119">Microsoft customers may also consider using applications and solutions of third-party vendors for managing their users and integrating their local identification system with the Azure AD.</span></span>

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="c242f-120">Microsoft コンプライアンス マネージャーを使用してリスクを評価する</span><span class="sxs-lookup"><span data-stu-id="c242f-120">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="c242f-121">[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c242f-121">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="c242f-122">コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="c242f-122">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="c242f-123">コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。</span><span class="sxs-lookup"><span data-stu-id="c242f-123">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="c242f-124">[コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。</span><span class="sxs-lookup"><span data-stu-id="c242f-124">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

## <a name="questions-and-support"></a><span data-ttu-id="c242f-125">質問とサポート</span><span class="sxs-lookup"><span data-stu-id="c242f-125">Questions and support</span></span>

<span data-ttu-id="c242f-126">技術的および課金に関する質問については、以下の Microsoft サポート リソースを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c242f-126">For technical and billing questions, refer to the Microsoft Support resources below.</span></span> <span data-ttu-id="c242f-127">その他の質問や説明については、Microsoft プライバシー チームにお [問い合わせください](https://support.microsoft.com/gp/privacy-page)。</span><span class="sxs-lookup"><span data-stu-id="c242f-127">For additional questions or clarifications, contact the Microsoft [privacy team](https://support.microsoft.com/gp/privacy-page).</span></span>

### <a name="microsoft-azure"></a><span data-ttu-id="c242f-128">Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="c242f-128">Microsoft Azure</span></span>

- <span data-ttu-id="c242f-129">**Web サイト**: [Microsoft Azure サポート](https://aka.ms/GetAzureSupport)</span><span class="sxs-lookup"><span data-stu-id="c242f-129">**Website**: [Microsoft Azure support](https://aka.ms/GetAzureSupport)</span></span>
- <span data-ttu-id="c242f-130">**フリー ダイヤル**: 8 800 200 8001</span><span class="sxs-lookup"><span data-stu-id="c242f-130">**Toll Free**: 8 800 200 8001</span></span>
- <span data-ttu-id="c242f-131">**ローカル通話**: 495 916 7171</span><span class="sxs-lookup"><span data-stu-id="c242f-131">**Local Call**: 495 916 7171</span></span>
- <span data-ttu-id="c242f-132">**オンライン サポート**: Azure ポータル経由でクエリを [送信する](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="c242f-132">**Online support**: Submit queries via the [Azure portal](https://portal.azure.com)</span></span>

### <a name="microsoft-365"></a><span data-ttu-id="c242f-133">Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="c242f-133">Microsoft 365</span></span>

- <span data-ttu-id="c242f-134">**フリー ダイヤル**: 8 10 800 2548 1044</span><span class="sxs-lookup"><span data-stu-id="c242f-134">**Toll Free**: 8 10 800 2548 1044</span></span>
- <span data-ttu-id="c242f-135">**ローカル通話**: 499 922 8623</span><span class="sxs-lookup"><span data-stu-id="c242f-135">**Local Call**: 499 922 8623</span></span>
- <span data-ttu-id="c242f-136">**オンライン サポート**: 管理センターからクエリを [送信する](https://portal.office.com/)</span><span class="sxs-lookup"><span data-stu-id="c242f-136">**Online support**: Submit queries via the [Admin Center](https://portal.office.com/)</span></span>

### <a name="dynamics-365"></a><span data-ttu-id="c242f-137">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c242f-137">Dynamics 365</span></span>

- <span data-ttu-id="c242f-138">**フリー ダイヤル**: 8 10 800 2548 1044</span><span class="sxs-lookup"><span data-stu-id="c242f-138">**Toll Free**: 8 10 800 2548 1044</span></span>
- <span data-ttu-id="c242f-139">**ローカル通話**: 499 922 8623</span><span class="sxs-lookup"><span data-stu-id="c242f-139">**Local Call**: 499 922 8623</span></span>
- <span data-ttu-id="c242f-140">**オンライン サポート**: Dynamics サポート ポータルから [クエリを送信する](https://dynamics.microsoft.com/support/)</span><span class="sxs-lookup"><span data-stu-id="c242f-140">**Online support**: Submit queries via the [Dynamics Support portal](https://dynamics.microsoft.com/support/)</span></span>

### <a name="power-platform"></a><span data-ttu-id="c242f-141">Power Platform</span><span class="sxs-lookup"><span data-stu-id="c242f-141">Power Platform</span></span>

- <span data-ttu-id="c242f-142">**フリー ダイヤル**: 8 10 800 2548 1044</span><span class="sxs-lookup"><span data-stu-id="c242f-142">**Toll Free**: 8 10 800 2548 1044</span></span>
- <span data-ttu-id="c242f-143">**ローカル通話**: 499 922 8623</span><span class="sxs-lookup"><span data-stu-id="c242f-143">**Local Call**: 499 922 8623</span></span>
- <span data-ttu-id="c242f-144">**オンライン サポート**: Power Platform サポート経由で [クエリを送信する](/power-platform/admin/get-help-support)</span><span class="sxs-lookup"><span data-stu-id="c242f-144">**Online support**: Submit queries via the [Power Platform Support](/power-platform/admin/get-help-support)</span></span>

> [!NOTE]
> <span data-ttu-id="c242f-145"><sup>1</sup> 連邦法いいえ</span><span class="sxs-lookup"><span data-stu-id="c242f-145"><sup>1</sup> Federal Law No.</span></span> <span data-ttu-id="c242f-146">242-FZ (エディションの日付は 12.31.2014) '07.21.2014 日付の情報および通信ネットワークでの個人データ処理の手順を明確化するロシア連邦の特定の立法上の行為に修正を進める</span><span class="sxs-lookup"><span data-stu-id="c242f-146">242-FZ (edition dated 12.31.2014) 'On entering amendments into certain legislative acts of the Russian Federation about clarifying the procedure for personal data processing in information and telecommunication networks' dated 07.21.2014</span></span> <br>
> <span data-ttu-id="c242f-147"><sup>2</sup> 連邦法いいえ</span><span class="sxs-lookup"><span data-stu-id="c242f-147"><sup>2</sup> Federal Law No.</span></span> <span data-ttu-id="c242f-148">07.27 現在の個人データに対する 152- 的な保護。</span><span class="sxs-lookup"><span data-stu-id="c242f-148">152-FZ on Personal data as of 07.27.</span></span> <span data-ttu-id="c242f-149">2006</span><span class="sxs-lookup"><span data-stu-id="c242f-149">2006</span></span><br>
