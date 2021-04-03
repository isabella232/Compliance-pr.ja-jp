---
title: Office Server の GDPR
description: Office オンプレミスのサーバーで一般データ保護規則 (GDPR) の要件に対応する方法について説明します。
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.collection: MS-Compliance
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: 58f3d9108fe36175c2ce879054a35c2cc94d93c8
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496077"
---
# <a name="gdpr-for-office-on-premises-servers"></a><span data-ttu-id="de9e2-103">オンプレミス サーバー上の Office の GDPR</span><span class="sxs-lookup"><span data-stu-id="de9e2-103">GDPR for Office on-premises Servers</span></span>

<span data-ttu-id="de9e2-p101">一般データ保護規則 (GDPR) により、組織が個人データを保護し、データ主体要求に適切に応答するための要件が導入されます。このシリーズの記事では、オンプレミスのワークロードのために推奨されるアプローチを示します。</span><span class="sxs-lookup"><span data-stu-id="de9e2-p101">The General Data Protection Regulation (GDPR) introduces requirements for organizations to protect personal data and respond appropriately to data subject requests. This series of articles provides recommended approaches for on-premises workloads:</span></span>

- [<span data-ttu-id="de9e2-106">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="de9e2-106">SharePoint Server</span></span>](gdpr-for-sharepoint-server.md)

- [<span data-ttu-id="de9e2-107">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="de9e2-107">Exchange Server</span></span>](gdpr-for-exchange-server.md)

- [<span data-ttu-id="de9e2-108">Skype for Business Server</span><span class="sxs-lookup"><span data-stu-id="de9e2-108">Skype for Business Server</span></span>](gdpr-for-skype-for-business-server.md)

- [<span data-ttu-id="de9e2-109">Project Server</span><span class="sxs-lookup"><span data-stu-id="de9e2-109">Project Server</span></span>](gdpr-for-project-server.md)

- [<span data-ttu-id="de9e2-110">Office Web Apps Server および Office Online Server</span><span class="sxs-lookup"><span data-stu-id="de9e2-110">Office Web Apps Server and Office Online Server</span></span>](gdpr-for-office-online-server.md)

- [<span data-ttu-id="de9e2-111">オンプレミス ファイル共有</span><span class="sxs-lookup"><span data-stu-id="de9e2-111">On-premises file shares</span></span>](gdpr-for-on-premises-file-shares.md)

<span data-ttu-id="de9e2-112">GDPR について、また Microsoft による支援方法の詳細については、[Microsoft セキュリティ センター](https://www.microsoft.com/trust-center/privacy/gdpr-overview
)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de9e2-112">For more information about the GDPR and how Microsoft can help you, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center/privacy/gdpr-overview
).</span></span>

<span data-ttu-id="de9e2-p102">オンプレミス データで何らかの作業を実行する前に、法律およびコンプライアンスのチームに問い合わせて、ガイダンス情報を入手し、個人データを処理する際の既存の分類スキーマやアプローチについて確認してください。Microsoft では、[https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>) の Microsoft GDPR Data Discovery Toolkit で、分類スキーマの開発と拡張の推奨事項を提供しています。このツールキットでは、オンプレミス データをクラウドに移行するためのアプローチも記述されています。クラウドでは、必要に応じて、より洗練されたデータ ガバナンス機能を使用できます。このセクションの記事では、意図的にオンプレミスのままにするデータに関する推奨事項が示されています。</span><span class="sxs-lookup"><span data-stu-id="de9e2-p102">Before doing any work with on-premises data, consult with your legal and compliance teams to seek guidance and to learn about existing classification schemas and approaches to working with personal data. Microsoft provides recommendations for developing and extending classifications schemas in the Microsoft GDPR Data Discovery Toolkit at [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>). This toolkit also describes approaches for moving on-premises data to the cloud where you can use more sophisticated data governance capabilities, if this is desired. The articles in this section provide recommendations for data that is intended to remain on premises.</span></span>

<span data-ttu-id="de9e2-p103">次の図に、これらのワークロードそれぞれで、個人データを検出、分類、保護、監視するために使用する推奨機能のリストを示します。詳細については、このセクションの記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de9e2-p103">The following illustration lists recommended capabilities to use across each of these workloads to discover, classify, protect, and monitor personal data. See the articles in this section for more information.</span></span>

![ワークロード全体で個人データを検出、分類、保護、監視する機能を説明する図](../media/gdpr-for-office-servers-image1.png)

## <a name="illustration-description"></a><span data-ttu-id="de9e2-120">図の説明</span><span class="sxs-lookup"><span data-stu-id="de9e2-120">Illustration description</span></span>

<span data-ttu-id="de9e2-121">次の表では、図での例と同じものを見やすいように記載しています。</span><span class="sxs-lookup"><span data-stu-id="de9e2-121">For accessibility, the following table provides the same examples in the illustration.</span></span>

****

|<span data-ttu-id="de9e2-122">Action</span><span class="sxs-lookup"><span data-stu-id="de9e2-122">Action</span></span>|<span data-ttu-id="de9e2-123">Windows Server ファイル共有</span><span class="sxs-lookup"><span data-stu-id="de9e2-123">Windows Server file shares</span></span>|<span data-ttu-id="de9e2-124">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="de9e2-124">SharePoint Server</span></span>|<span data-ttu-id="de9e2-125">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="de9e2-125">Exchange Server</span></span>|<span data-ttu-id="de9e2-126">Skype for Business</span><span class="sxs-lookup"><span data-stu-id="de9e2-126">Skype for Business</span></span>|<span data-ttu-id="de9e2-127">Project Server</span><span class="sxs-lookup"><span data-stu-id="de9e2-127">Project Server</span></span>|
|---|---|---|---|---|---|
|<span data-ttu-id="de9e2-128">検索</span><span class="sxs-lookup"><span data-stu-id="de9e2-128">Discover</span></span>|<span data-ttu-id="de9e2-129">Azure Information Protection スキャナー<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="de9e2-129">Azure Information Protection scanner<sup>\*</sup></span></span>|<span data-ttu-id="de9e2-130">検索センターまたは eDiscovery (データが分類された後)</span><span class="sxs-lookup"><span data-stu-id="de9e2-130">Search Center or eDiscovery (after data is classified)</span></span> <br/><br/> <span data-ttu-id="de9e2-131">Azure Information Protection スキャナー<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="de9e2-131">Azure Information Protection scanner<sup>\*</sup></span></span>|<span data-ttu-id="de9e2-132">Exchange 電子情報開示ポータル</span><span class="sxs-lookup"><span data-stu-id="de9e2-132">Exchange eDiscovery Portal</span></span>|<span data-ttu-id="de9e2-133">Exchange 電子情報開示ポータル</span><span class="sxs-lookup"><span data-stu-id="de9e2-133">Exchange eDiscovery portal</span></span>|<span data-ttu-id="de9e2-134">検出およびエクスポートのための SQL スクリプト</span><span class="sxs-lookup"><span data-stu-id="de9e2-134">SQL scripts for discovery and exporting</span></span>|
|<span data-ttu-id="de9e2-135">分類</span><span class="sxs-lookup"><span data-stu-id="de9e2-135">Classify</span></span>|<span data-ttu-id="de9e2-136">Azure Information Protection スキャナー<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="de9e2-136">Azure Information Protection scanner<sup>\*</sup></span></span> <br/><br/> <span data-ttu-id="de9e2-137">Office 365 の機密情報の種類</span><span class="sxs-lookup"><span data-stu-id="de9e2-137">Office 365 sensitive information types</span></span>|<span data-ttu-id="de9e2-138">Azure Information Protection スキャナー<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="de9e2-138">Azure Information Protection scanner<sup>\*</sup></span></span> <br/><br/> <span data-ttu-id="de9e2-139">Office 365 の機密情報の種類</span><span class="sxs-lookup"><span data-stu-id="de9e2-139">Office 365 sensitive information types</span></span>|<span data-ttu-id="de9e2-140">Exchange 保持タグおよびアイテム保持ポリシー</span><span class="sxs-lookup"><span data-stu-id="de9e2-140">Exchange retention tags and retention policies</span></span>|<span data-ttu-id="de9e2-141">Exchange 保持タグおよびアイテム保持ポリシー</span><span class="sxs-lookup"><span data-stu-id="de9e2-141">Exchange retention tags and retention policies</span></span>||
|<span data-ttu-id="de9e2-142">保護</span><span class="sxs-lookup"><span data-stu-id="de9e2-142">Protect</span></span>||<span data-ttu-id="de9e2-143">Exchange Server データ損失防止ルール</span><span class="sxs-lookup"><span data-stu-id="de9e2-143">Exchange Server data loss prevention rules</span></span> <br/><br/> <span data-ttu-id="de9e2-144">アクセス許可、ライブラリの IRM による保護</span><span class="sxs-lookup"><span data-stu-id="de9e2-144">Permissions, IRM-protection for libraries</span></span>|<span data-ttu-id="de9e2-145">Exchange Server データ損失防止ルール</span><span class="sxs-lookup"><span data-stu-id="de9e2-145">Exchange Server data loss prevention rules</span></span> <br/><br/> <span data-ttu-id="de9e2-146">IRM と Exchange Server との統合</span><span class="sxs-lookup"><span data-stu-id="de9e2-146">IRM integration with Exchange Server</span></span>|||
|<span data-ttu-id="de9e2-147">監視する</span><span class="sxs-lookup"><span data-stu-id="de9e2-147">Monitor</span></span>|<span data-ttu-id="de9e2-148">SIEM ツールとのログ統合</span><span class="sxs-lookup"><span data-stu-id="de9e2-148">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="de9e2-149">SIEM ツールとのログ統合</span><span class="sxs-lookup"><span data-stu-id="de9e2-149">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="de9e2-150">SIEM ツールとのログ統合</span><span class="sxs-lookup"><span data-stu-id="de9e2-150">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="de9e2-151">SIEM ツールとのログ統合</span><span class="sxs-lookup"><span data-stu-id="de9e2-151">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="de9e2-152">SIEM ツールとのログ統合</span><span class="sxs-lookup"><span data-stu-id="de9e2-152">Integrate logs with SIEM tools</span></span>|
|

<span data-ttu-id="de9e2-153"><sup>\*</sup>保護機能によってファイルが暗号化されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="de9e2-153"><sup>\*</sup> Note that protection encrypts the file.</span></span> <span data-ttu-id="de9e2-154">その結果、SharePoint Server では、保護されたファイルの機密情報の種類を検索できなくなります。</span><span class="sxs-lookup"><span data-stu-id="de9e2-154">Consequently, SharePoint Server can't find the sensitive information types in protected files.</span></span>
