---
title: ロシアの個人データローカライズ要件
description: 個人データ、ロシア市民の個人データ記録、systematization、蓄積、保存、明確化、および抽出が、ロシアにある Microsoft サービスおよびデータベースで実行される方法について説明します。
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
ms.openlocfilehash: 07dbfce49dc202ed23a4f2fed6336e00dcec95e1
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2020
ms.locfileid: "49509222"
---
# <a name="russian-personal-data-localization-requirements"></a><span data-ttu-id="77151-104">ロシアの個人データローカライズ要件</span><span class="sxs-lookup"><span data-stu-id="77151-104">Russian Personal Data Localization Requirements</span></span>

<span data-ttu-id="77151-105">2015年9月1日時点で、個人データオペレーターと見なされる組織では、個人データを収集する際に、ロシア市民の個人データ記録、systematization、蓄積、保存、説明 (更新、変更)、および抽出がロシアにあるデータベース (「個人データのローカリゼーション要件」) によって実行されることを保証する必要があります。<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="77151-105">As of September 1, 2015, organizations that are considered personal data operators must ensure that, when collecting personal data, Russian citizens' personal data recording, systematization, accumulation, storage, clarification (updating, changing), and extraction are performed through the databases located in Russia ('personal data localization requirement').<sup>1</sup></span></span>

<span data-ttu-id="77151-106">Microsoft Azure、Microsoft 365、Dynamics 365、電源プラットフォームなどの個人データ処理を有効にすることを含め、組織で利用可能な microsoft サービス (教育機関に限定されない) (hereinafter と呼ばれる)。 (詳細については、「 [Microsoft Trust Center」](https://www.microsoft.com/trust-center)を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="77151-106">Microsoft services available to organizations (including but not limited to educational institutions) (hereinafter referred to as 'customer'), including those enabling personal data processing such as Microsoft Azure, Microsoft 365, Dynamics 365, and Power Platform, are provided from data processing centers located outside of Russia (for more information visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center)).</span></span>

<span data-ttu-id="77151-107">ユーザー情報システムによって処理された情報の種類と内容に基づいて、Microsoft クラウド製品を使用しているものも含めて、個人データ情報システム (' PDIS ', ' ISPD ') と見なされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="77151-107">Based on the type and content of information processed by customer information systems, such systems, including those using Microsoft cloud products, may be deemed a personal data information system ('PDIS', 'ISPD').</span></span> <span data-ttu-id="77151-108">お客様が PDM として認定されているシステムで Microsoft サービスを使用することを希望している場合、Microsoft は、お客様に対して、次に示すその他のソリューションについて考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77151-108">In cases where the customer would like to use Microsoft services in a system that qualifies as PDIS through its architecture and types of information processed, Microsoft invites its customers to consider, amongst other things, available solutions specified below.</span></span> <span data-ttu-id="77151-109">提供されているすべてのシナリオは、標準のビジネス製品に対する追加オプションとして、お客様が利用できます。</span><span class="sxs-lookup"><span data-stu-id="77151-109">All the scenarios provided are available for customers as an additional option to standard business offerings.</span></span>

<span data-ttu-id="77151-110">このお客様には、PDIS 個人データ事業者がコンプライアンスを担当しており、個人データローカリゼーションの適用可能な法的要件を分析して評価する必要があることに注意してください。また、独自の判断で、PDIS の個人データの処理がロシアの個人データの法則に準拠していることを確認するために十分な<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="77151-110">It should be noted that it is the customer as personal data operator of PDIS who is in charge of compliance and shall analyze and assess applicable legal requirements for personal data localization, and at its own discretion, independently determine sufficient measures to ensure that personal data processing in PDIS complies with the Russian personal data law.<sup>2</sup></span></span>

## <a name="subscribing-to-microsoft-services"></a><span data-ttu-id="77151-111">Microsoft サービスのサブスクライブ</span><span class="sxs-lookup"><span data-stu-id="77151-111">Subscribing to Microsoft services</span></span>

### <a name="microsoft-id-management"></a><span data-ttu-id="77151-112">Microsoft ID の管理</span><span class="sxs-lookup"><span data-stu-id="77151-112">Microsoft ID Management</span></span>

<span data-ttu-id="77151-113">Microsoft は、Microsoft サービスへのサブスクライブを検討することをお客様に招待します。Microsoft Azure、Microsoft 365、Dynamics 365、および電源プラットフォーム-Microsoft クラウドソリューションプロバイダー (CSP) パートナー経由。</span><span class="sxs-lookup"><span data-stu-id="77151-113">Microsoft invites customers to consider subscribing to Microsoft services; Microsoft Azure, Microsoft 365, Dynamics 365, and Power Platform—via a Microsoft Cloud Solution Provider (CSP) partner.</span></span> <span data-ttu-id="77151-114">詳細については、 [CSP パートナーの一覧](https://pinpoint.microsoft.com/search?type=services&campaign=691)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77151-114">For more information, see this [list of CSP partners](https://pinpoint.microsoft.com/search?type=services&campaign=691).</span></span>

### <a name="managing-user-identity-and-access-for-microsoft-services"></a><span data-ttu-id="77151-115">Microsoft サービスのユーザー Id とアクセス権を管理する</span><span class="sxs-lookup"><span data-stu-id="77151-115">Managing User Identity and Access for Microsoft services</span></span>

<span data-ttu-id="77151-116">Microsoft Azure、Microsoft 365、Dynamics 365、および電源プラットフォームなどの Microsoft サービスの場合、ユーザーの確認とアクセスの管理は [Azure Active directory (Azure Active directory)](https://azure.microsoft.com/services/active-directory/)を通じて実行されます。</span><span class="sxs-lookup"><span data-stu-id="77151-116">For Microsoft services such as Microsoft Azure, Microsoft 365, Dynamics 365, and Power Platform, user verification and access management are performed through [Azure Active Directory (Azure Active Directory)](https://azure.microsoft.com/services/active-directory/).</span></span> <span data-ttu-id="77151-117">Microsoft のお客様が Microsoft クラウドサービス (Windows Server Active Directory (AD) やその他の ID 管理システムなど) に対してローカル id 管理システムを使用している場合、お客様は Azure AD Connect を介してこのようなシステムを Azure Active Directory (Azure Active Directory) に迅速に統合する機会を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="77151-117">In cases where a Microsoft customer uses a local identification management system for Microsoft cloud services (such as the Windows Server Active Directory (AD) or any other ID management system), the customer has an opportunity to swiftly integrate such system with the Azure Active Directory (Azure Active Directory) through Azure AD Connect.</span></span> <span data-ttu-id="77151-118">詳細については、「 [AZURE AD Connect](https://docs.microsoft.com/azure/active-directory/cloud-provisioning/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77151-118">For more information, see the [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/cloud-provisioning/).</span></span> <span data-ttu-id="77151-119">また、Microsoft のお客様は、サードパーティベンダーのアプリケーションやソリューションを使用してユーザーを管理し、そのローカル識別システムを Azure AD と統合することを検討することもできます。</span><span class="sxs-lookup"><span data-stu-id="77151-119">Microsoft customers may also consider using applications and solutions of third-party vendors for managing their users and integrating their local identification system with the Azure AD.</span></span>

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="77151-120">Microsoft コンプライアンス マネージャーを使用してリスクを評価する</span><span class="sxs-lookup"><span data-stu-id="77151-120">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="77151-p104">[Microsoft コンプライアンス マネージャー](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager)は、[Microsoft 365 コンプライアンス センター](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。コンプライアンス マネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。テンプレートは、コンプライアンス マネージャーの **評価テンプレート** ページに見つかります。[コンプライアンス マネージャーで評価する方法](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments)をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="77151-p104">[Microsoft Compliance Manager](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks. Compliance Manager offers a premium template for building an assessment for this regulation. Find the template in the **assessment templates** page in Compliance Manager. Learn how to [build assessments in Compliance Manager](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments).</span></span>

## <a name="questions-and-support"></a><span data-ttu-id="77151-125">質問とサポート</span><span class="sxs-lookup"><span data-stu-id="77151-125">Questions and support</span></span>

<span data-ttu-id="77151-126">技術的および請求に関する質問については、以下の Microsoft サポートリソースを参照してください。</span><span class="sxs-lookup"><span data-stu-id="77151-126">For technical and billing questions, refer to the Microsoft Support resources below.</span></span> <span data-ttu-id="77151-127">その他の質問や説明については、Microsoft の [プライバシーチーム](https://support.microsoft.com/gp/privacy-page)にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="77151-127">For additional questions or clarifications, contact the Microsoft [privacy team](https://support.microsoft.com/gp/privacy-page).</span></span>

### <a name="microsoft-azure"></a><span data-ttu-id="77151-128">Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="77151-128">Microsoft Azure</span></span>

- <span data-ttu-id="77151-129">**Web サイト**: [Microsoft Azure サポート](https://aka.ms/GetAzureSupport)</span><span class="sxs-lookup"><span data-stu-id="77151-129">**Website**: [Microsoft Azure support](https://aka.ms/GetAzureSupport)</span></span>
- <span data-ttu-id="77151-130">**無料電話** 番号: 8 800 200 8001</span><span class="sxs-lookup"><span data-stu-id="77151-130">**Toll Free**: 8 800 200 8001</span></span>
- <span data-ttu-id="77151-131">**ローカル通話**: 495 916 7171</span><span class="sxs-lookup"><span data-stu-id="77151-131">**Local Call**: 495 916 7171</span></span>
- <span data-ttu-id="77151-132">**オンラインサポート**: [Azure ポータル](https://portal.azure.com)経由でクエリを送信する</span><span class="sxs-lookup"><span data-stu-id="77151-132">**Online support**: Submit queries via the [Azure portal](https://portal.azure.com)</span></span>

### <a name="microsoft-365"></a><span data-ttu-id="77151-133">Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="77151-133">Microsoft 365</span></span>

- <span data-ttu-id="77151-134">**無料電話** 番号: 8 10 800 2548 1044</span><span class="sxs-lookup"><span data-stu-id="77151-134">**Toll Free**: 8 10 800 2548 1044</span></span>
- <span data-ttu-id="77151-135">**ローカル通話**: 499 922 8623</span><span class="sxs-lookup"><span data-stu-id="77151-135">**Local Call**: 499 922 8623</span></span>
- <span data-ttu-id="77151-136">**オンラインサポート**:[管理センター](https://portal.office.com/)からクエリを送信する</span><span class="sxs-lookup"><span data-stu-id="77151-136">**Online support**: Submit queries via the [Admin Center](https://portal.office.com/)</span></span>

### <a name="dynamics-365"></a><span data-ttu-id="77151-137">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="77151-137">Dynamics 365</span></span>

- <span data-ttu-id="77151-138">**無料電話** 番号: 8 10 800 2548 1044</span><span class="sxs-lookup"><span data-stu-id="77151-138">**Toll Free**: 8 10 800 2548 1044</span></span>
- <span data-ttu-id="77151-139">**ローカル通話**: 499 922 8623</span><span class="sxs-lookup"><span data-stu-id="77151-139">**Local Call**: 499 922 8623</span></span>
- <span data-ttu-id="77151-140">**オンラインサポート**: [Dynamics サポートポータル](https://dynamics.microsoft.com/support/)でクエリを送信する</span><span class="sxs-lookup"><span data-stu-id="77151-140">**Online support**: Submit queries via the [Dynamics Support portal](https://dynamics.microsoft.com/support/)</span></span>

### <a name="power-platform"></a><span data-ttu-id="77151-141">電源プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="77151-141">Power Platform</span></span>

- <span data-ttu-id="77151-142">**無料電話** 番号: 8 10 800 2548 1044</span><span class="sxs-lookup"><span data-stu-id="77151-142">**Toll Free**: 8 10 800 2548 1044</span></span>
- <span data-ttu-id="77151-143">**ローカル通話**: 499 922 8623</span><span class="sxs-lookup"><span data-stu-id="77151-143">**Local Call**: 499 922 8623</span></span>
- <span data-ttu-id="77151-144">**オンラインサポート**:[電源プラットフォームサポート](https://docs.microsoft.com/power-platform/admin/get-help-support)経由でクエリを送信する</span><span class="sxs-lookup"><span data-stu-id="77151-144">**Online support**: Submit queries via the [Power Platform Support](https://docs.microsoft.com/power-platform/admin/get-help-support)</span></span>

> [!NOTE]
> <span data-ttu-id="77151-145"><sup>1</sup> 連邦法はありません。</span><span class="sxs-lookup"><span data-stu-id="77151-145"><sup>1</sup> Federal Law No.</span></span> <span data-ttu-id="77151-146">242-FZ (edition 12.31.2014) ' は、ロシアのフェデレーションの特定の法律上の行動に対して、個人データの処理手順を明確にするための情報および電気通信ネットワークの07.21.2014</span><span class="sxs-lookup"><span data-stu-id="77151-146">242-FZ (edition dated 12.31.2014) 'On entering amendments into certain legislative acts of the Russian Federation about clarifying the procedure for personal data processing in information and telecommunication networks' dated 07.21.2014</span></span> <br>
> <span data-ttu-id="77151-147"><sup>2</sup> 連邦法はありません。</span><span class="sxs-lookup"><span data-stu-id="77151-147"><sup>2</sup> Federal Law No.</span></span> <span data-ttu-id="77151-148">07.27 の場合、個人データの 152-FZ。</span><span class="sxs-lookup"><span data-stu-id="77151-148">152-FZ on Personal data as of 07.27.</span></span> <span data-ttu-id="77151-149">2006</span><span class="sxs-lookup"><span data-stu-id="77151-149">2006</span></span><br>
