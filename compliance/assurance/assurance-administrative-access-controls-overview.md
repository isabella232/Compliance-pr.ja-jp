---
title: Microsoft 365 の管理アクセス制御
description: この記事では、Microsoft 365 の管理アクセス制御とデータ分類の概要について説明します。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: d3d6cd30fbe682de979d5c04943c57cedc86552f
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120716"
---
# <a name="administrative-access-controls-in-microsoft-365"></a><span data-ttu-id="b9ee3-103">Microsoft 365 の管理アクセス制御</span><span class="sxs-lookup"><span data-stu-id="b9ee3-103">Administrative access controls in Microsoft 365</span></span> 

<span data-ttu-id="b9ee3-104">Microsoft は、Microsoft による顧客コンテンツへのアクセスを意図的に制限しながら、ほとんどの Microsoft 365 操作を自動化するシステムとコントロールに多額の投資を行っています。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-104">Microsoft has invested heavily in systems and controls that automate most Microsoft 365 operations while intentionally limiting access to customer content by Microsoft.</span></span> <span data-ttu-id="b9ee3-105">人間がサービスを管理し、ソフトウェアがサービスを運用します。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-105">Humans govern the service, and software operates the service.</span></span> <span data-ttu-id="b9ee3-106">この構造により、Microsoft は Microsoft 365 を大規模に管理し、顧客コンテンツに対する内部の脅威のリスクを管理できます。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-106">This structure enables Microsoft to manage Microsoft 365 at scale and manage the risks of internal threats to customer content.</span></span>

<span data-ttu-id="b9ee3-107">既定では、Microsoft のエンジニアは、Microsoft 365 の顧客コンテンツに対する永続的な管理特権と永続的なアクセス権を持ち合っています。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-107">By default, Microsoft engineers have zero standing administrative privileges and zero standing access to customer content in Microsoft 365.</span></span> <span data-ttu-id="b9ee3-108">Microsoft のエンジニアは、限られた期間、制限付き、監査、およびセキュリティで保護されたアクセスをお客様のコンテンツに持ち込む可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-108">A Microsoft engineer can have limited, audited, and secured access to a customer's content for a limited amount of time.</span></span> <span data-ttu-id="b9ee3-109">アクセスは、サービス運用に必要な場合と、Microsoft 上級管理職のメンバーによって承認された場合にのみ行います。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-109">Access is only when necessary for service operations and only when approved by a member of Microsoft senior management.</span></span> <span data-ttu-id="b9ee3-110">カスタマー ロックボックスライセンスのお客様の場合、お客様は Microsoft 365 でホストされているコンテンツへのアクセス承認を提供します。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-110">For Customer Lockbox licensed customers, the customer provides access approval to their content hosted on Microsoft 365.</span></span>

<span data-ttu-id="b9ee3-111">Microsoft は、複数の形式のクラウド配信を使用してオンライン サービスを提供しています。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-111">Microsoft provides online services using multiple forms of cloud delivery:</span></span>

- <span data-ttu-id="b9ee3-112">**パブリック クラウド:** Microsoft 365、Azure、および北米、南アメリカ、ヨーロッパ、アジア、オーストラリアなどにホストされているその他のサービスのマルチテナント バージョンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-112">**Public clouds:** Includes multi-tenant versions of Microsoft 365, Azure, and other services hosted in North America, South America, Europe, Asia, Australia, etc.</span></span>
- <span data-ttu-id="b9ee3-113">**国内クラウド:** 中国の Microsoft 365 (21Vianet が運用) やドイツの Microsoft 365 (Microsoft が運用していますが、ドイツ のデータ トラスティである Deutsche Telekom が顧客データを含むシステムに対する Microsoft のアクセスを制御および監視するモデルの下で) など、米国外のすべての独立したクラウドと第三者が運用するクラウド (前に説明したクラウドを除く) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-113">**National clouds:** Includes all sovereign and third party-operated clouds outside of the United States (except ones noted previously), such as Microsoft 365 in China (operated by 21Vianet), and Microsoft 365 in Germany (operated by Microsoft, but under a model in which a German data trustee, Deutsche Telekom, controls and monitors Microsoft's access to customer data and systems that contain customer data).</span></span>
- <span data-ttu-id="b9ee3-114">**政府機関用クラウド:** 米国政府機関のお客様が利用できる Microsoft 365 および Azure サービスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-114">**Government clouds:** Includes Microsoft 365 and Azure services that are available to United States government customers.</span></span>

<span data-ttu-id="b9ee3-115">この記事の目的上、Microsoft 365 サービスには以下が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-115">For purposes of this article, Microsoft 365 services include:</span></span>

- [<span data-ttu-id="b9ee3-116">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b9ee3-116">Exchange Online</span></span>](/Exchange/exchange-online)
- [<span data-ttu-id="b9ee3-117">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="b9ee3-117">Exchange Online Protection</span></span>](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [<span data-ttu-id="b9ee3-118">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b9ee3-118">SharePoint Online</span></span>](/sharepoint/sharepoint-online)
- [<span data-ttu-id="b9ee3-119">OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="b9ee3-119">OneDrive for Business</span></span>](/OneDrive/onedrive)
- [<span data-ttu-id="b9ee3-120">Skype for Business</span><span class="sxs-lookup"><span data-stu-id="b9ee3-120">Skype for Business</span></span>](/SkypeForBusiness/skype-for-business-online)
- [<span data-ttu-id="b9ee3-121">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b9ee3-121">Microsoft Teams</span></span>](/MicrosoftTeams/Teams-overview)
- [<span data-ttu-id="b9ee3-122">Yammer</span><span class="sxs-lookup"><span data-stu-id="b9ee3-122">Yammer</span></span>](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a><span data-ttu-id="b9ee3-123">Microsoft 365 のアクセス制御</span><span class="sxs-lookup"><span data-stu-id="b9ee3-123">Microsoft 365 access controls</span></span>

<span data-ttu-id="b9ee3-124">アクセス制御の目的で、Microsoft は Microsoft 365 データを顧客データまたは他の種類のデータとして分類します。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-124">For access control purposes, Microsoft categorizes Microsoft 365 data as customer data or other types of data.</span></span>

### <a name="customer-data"></a><span data-ttu-id="b9ee3-125">顧客データ</span><span class="sxs-lookup"><span data-stu-id="b9ee3-125">Customer data</span></span>

<span data-ttu-id="b9ee3-126">顧客データとは、Microsoft 365 サービスを使用する際にお客様が提供または代理して提供するデータです。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-126">Customer data is all data provided by or on behalf of a customer when using Microsoft 365 services.</span></span> <span data-ttu-id="b9ee3-127">このデータは、Microsoft 365 ユーザーによって直接作成またはアップロードされた顧客コンテンツです。以下が含まれる。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-127">This data is customer content directly created or uploaded by Microsoft 365 users, including:</span></span>

- <span data-ttu-id="b9ee3-128">メール</span><span class="sxs-lookup"><span data-stu-id="b9ee3-128">Emails</span></span>
- <span data-ttu-id="b9ee3-129">SharePoint Online コンテンツ</span><span class="sxs-lookup"><span data-stu-id="b9ee3-129">SharePoint Online content</span></span>
- <span data-ttu-id="b9ee3-130">インスタント メッセージ</span><span class="sxs-lookup"><span data-stu-id="b9ee3-130">Instant messages</span></span>
- <span data-ttu-id="b9ee3-131">予定表アイテム</span><span class="sxs-lookup"><span data-stu-id="b9ee3-131">Calendar items</span></span>
- <span data-ttu-id="b9ee3-132">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="b9ee3-132">Documents</span></span>
- <span data-ttu-id="b9ee3-133">連絡先</span><span class="sxs-lookup"><span data-stu-id="b9ee3-133">Contacts</span></span>
- <span data-ttu-id="b9ee3-134">エンドユーザーを特定できる情報 (EUII) (ユーザーに固有のデータ、または個々のユーザーにリンク可能だが顧客コンテンツは含められないデータ)</span><span class="sxs-lookup"><span data-stu-id="b9ee3-134">End-user identifiable information (EUII) (data that is unique to a user or that is linkable to an individual user but does not include customer content)</span></span>

### <a name="other-types-of-data"></a><span data-ttu-id="b9ee3-135">その他の種類のデータ</span><span class="sxs-lookup"><span data-stu-id="b9ee3-135">Other types of data</span></span>

<span data-ttu-id="b9ee3-136">その他の種類のデータは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-136">Other types of data include:</span></span>

- <span data-ttu-id="b9ee3-137">**アカウント データ:** 管理データ (管理者がサービスをサインアップまたは購入するときに提供する情報)、支払いデータ (クレジット カードの詳細など、支払い方法に関する情報) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-137">**Account data:** Includes administrative data (information provided by administrators when they sign-up or purchase services), and payment data (information about payment instruments, such as credit card details).</span></span>
- <span data-ttu-id="b9ee3-138">**組織的に識別可能な情報:** テナントの識別に使用されるデータ、使用状況データが含まれます。個々のユーザーまたは顧客コンテンツにリンクできません。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-138">**Organizationally identifiable information:** Includes data used to identify a tenant, usage data, and not linkable to an individual user or included in customer content.</span></span>
- <span data-ttu-id="b9ee3-139">**システム メタデータ:** 構成設定、システム状態、Microsoft IP アドレス、およびサブスクリプションとテナントに関する技術情報を含むサービス ログが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-139">**System metadata:** Includes service logs that contain configuration settings, system status, Microsoft IP addresses, and technical information about subscriptions and tenants.</span></span>

<span data-ttu-id="b9ee3-140">Microsoft は、顧客データやアクセス制御データへの未承認のアクセスを許可しないユーザーがいなか、アクセス制御メカニズムを確立しています。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-140">Microsoft has established access control mechanisms to ensure that no one has unapproved access to Customer Data or access control data.</span></span> <span data-ttu-id="b9ee3-141">アクセス制御データは、お客様のコンテンツや EUII、Microsoft パスワード、セキュリティ証明書、その他の認証関連データへのアクセスなど、環境内の他の種類のデータまたは機能へのアクセスを管理します。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-141">Access control data manages access to other types of data or functions within the environment, including access to customer content or EUII, Microsoft passwords, security certificates, and other authentication-related data.</span></span> <span data-ttu-id="b9ee3-142">アクセス制御メカニズムは、Microsoft 365 の実稼働環境への未承認の物理的アクセス、論理アクセス、またはリモート アクセスに対する保護も行います。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-142">Access control mechanisms also guard against unapproved physical, logical, or remote access to the Microsoft 365 production environment.</span></span>

<span data-ttu-id="b9ee3-143">Microsoft 365 の運用に Microsoft が使用するアクセス制御には、次の 3 つのカテゴリがあります。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-143">There are three categories of access controls used by Microsoft for operating Microsoft 365:</span></span>

- <span data-ttu-id="b9ee3-144">分離の制御</span><span class="sxs-lookup"><span data-stu-id="b9ee3-144">Isolation controls</span></span>
- <span data-ttu-id="b9ee3-145">担当者の制御</span><span class="sxs-lookup"><span data-stu-id="b9ee3-145">Personnel controls</span></span>
- <span data-ttu-id="b9ee3-146">テクノロジの制御</span><span class="sxs-lookup"><span data-stu-id="b9ee3-146">Technology controls</span></span>

<span data-ttu-id="b9ee3-147">これらのコントロールを組み合わせると、Microsoft 365 の悪意のある操作を防止および検出できます。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-147">When combined, these controls help prevent and detect malicious actions in Microsoft 365.</span></span> <span data-ttu-id="b9ee3-148">Microsoft が使用する分離、人員、および技術のコントロールに加えて、コントロールの第 4 のカテゴリがあります。コントロールは、お客様によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-148">In addition to the isolation, personnel, and technology controls used by Microsoft, there is a fourth category of controls: those controls implemented by customers.</span></span>

<span data-ttu-id="b9ee3-149">Microsoft 365 では、オンプレミス環境でデータを管理するのと同じ方法でデータを管理できます。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-149">Microsoft 365 allows you to manage data the same way data is managed in on-premises environments.</span></span> <span data-ttu-id="b9ee3-150">Microsoft 365 の組織にサインインしたユーザーは、自動的にグローバル管理者になります。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-150">The person who signs up an organization for Microsoft 365 automatically becomes a global administrator.</span></span> <span data-ttu-id="b9ee3-151">グローバル管理者は、管理ポータルのすべての機能にアクセスできます。次の機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-151">The global admin has access to all features in Management Portals and can:</span></span>

- <span data-ttu-id="b9ee3-152">ユーザーを作成または編集する</span><span class="sxs-lookup"><span data-stu-id="b9ee3-152">Create or edit users</span></span>
- <span data-ttu-id="b9ee3-153">管理者ロールを他のユーザーに割り当てる</span><span class="sxs-lookup"><span data-stu-id="b9ee3-153">Assign admin roles to others</span></span>
- <span data-ttu-id="b9ee3-154">ユーザー パスワードをリセットする</span><span class="sxs-lookup"><span data-stu-id="b9ee3-154">Reset user passwords</span></span>
- <span data-ttu-id="b9ee3-155">ユーザー ライセンスを管理する</span><span class="sxs-lookup"><span data-stu-id="b9ee3-155">Manage user licenses</span></span>
- <span data-ttu-id="b9ee3-156">ドメインの管理</span><span class="sxs-lookup"><span data-stu-id="b9ee3-156">Manage domains</span></span>
- <span data-ttu-id="b9ee3-157">カスタマー ロックボックス要求を承認する</span><span class="sxs-lookup"><span data-stu-id="b9ee3-157">Approve Customer Lockbox requests</span></span>

<span data-ttu-id="b9ee3-158">各組織で少なくとも 2 つの管理者アカウントを構成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-158">We recommend that each organization configure at least two admin accounts.</span></span> <span data-ttu-id="b9ee3-159">大規模なエンタープライズ組織では、さまざまな機能を提供する専用の管理者アカウントをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-159">For large enterprise organizations, we recommend specialized admin accounts that serve different functions.</span></span>

<span data-ttu-id="b9ee3-160">管理者の役割とアクセス許可の割り当てについては、「管理者の役割の割り当て [」および](/microsoft-365/admin/add-users/assign-admin-roles) 「管理者の役割 [について」を参照してください](/microsoft-365/admin/add-users/about-admin-roles)。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-160">For information about assigning admin roles and permissions, see [Assign admin roles](/microsoft-365/admin/add-users/assign-admin-roles) and [About admin roles](/microsoft-365/admin/add-users/about-admin-roles).</span></span>

## <a name="related-links"></a><span data-ttu-id="b9ee3-161">関連リンク</span><span class="sxs-lookup"><span data-stu-id="b9ee3-161">Related Links</span></span>

- [<span data-ttu-id="b9ee3-162">Microsoft 365 での分離</span><span class="sxs-lookup"><span data-stu-id="b9ee3-162">Isolation in Microsoft 365</span></span>](assurance-isolation-in-microsoft-365.md)
- [<span data-ttu-id="b9ee3-163">Microsoft 就職前スクリーニング</span><span class="sxs-lookup"><span data-stu-id="b9ee3-163">Microsoft pre-employment screening</span></span>](assurance-pre-employment-screening.md)
- [<span data-ttu-id="b9ee3-164">Microsoft Cloud の背景チェック</span><span class="sxs-lookup"><span data-stu-id="b9ee3-164">Microsoft cloud background check</span></span>](assurance-cloud-background-check.md)
- [<span data-ttu-id="b9ee3-165">アクセス制御の監視と監査</span><span class="sxs-lookup"><span data-stu-id="b9ee3-165">Monitoring and Auditing Access Controls</span></span>](assurance-monitoring-and-auditing-access-controls.md)
- [<span data-ttu-id="b9ee3-166">Yammer Enterprise でのアクセス制御</span><span class="sxs-lookup"><span data-stu-id="b9ee3-166">Yammer Enterprise Access Controls</span></span>](assurance-yammer-enterprise-access-controls.md)
