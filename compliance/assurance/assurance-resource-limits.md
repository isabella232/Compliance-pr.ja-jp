---
title: Microsoft 365 リソース制限
description: この記事では、Microsoft 365 内のさまざまなアプリケーションのリソース制限に関する情報を確認できます。
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 54ea001e542cdd1ab078546cf96bd011e27ab1dc
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497501"
---
# <a name="service-resource-limits"></a><span data-ttu-id="7c073-103">サービス リソースの制限</span><span class="sxs-lookup"><span data-stu-id="7c073-103">Service resource limits</span></span>

<span data-ttu-id="7c073-104">リソース制限は、クォータ (制限) と調整を使用して適用されます。</span><span class="sxs-lookup"><span data-stu-id="7c073-104">Resource limits are enforced using quotas (limits) and throttling.</span></span> <span data-ttu-id="7c073-105">Azure Active Directory (Azure AD) と個々の Microsoft 365 サービスは両方を使用します。</span><span class="sxs-lookup"><span data-stu-id="7c073-105">Azure Active Directory (Azure AD) and the individual Microsoft 365 services use both.</span></span> <span data-ttu-id="7c073-106">制限はサービス固有であり、新しい機能が追加されるに応じ、時間の流中で変化します。</span><span class="sxs-lookup"><span data-stu-id="7c073-106">Limits are service-specific and change over time as new capabilities are added.</span></span> <span data-ttu-id="7c073-107">さまざまなサービスの現在の制限の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c073-107">For details on the current limits for the various services, see the following topics:</span></span>

- [<span data-ttu-id="7c073-108">Azure ADサービスの制限と制限</span><span class="sxs-lookup"><span data-stu-id="7c073-108">Azure AD service limits and restrictions</span></span>](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [<span data-ttu-id="7c073-109">Exchange Online の制限</span><span class="sxs-lookup"><span data-stu-id="7c073-109">Exchange Online Limits</span></span>](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [<span data-ttu-id="7c073-110">SharePoint Online ソフトウェアの境界と制限</span><span class="sxs-lookup"><span data-stu-id="7c073-110">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="7c073-111">Skype for Business Limits</span><span class="sxs-lookup"><span data-stu-id="7c073-111">Skype for Business Limits</span></span>](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="7c073-112">Yammer REST API とレート制限</span><span class="sxs-lookup"><span data-stu-id="7c073-112">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="7c073-113">Sway のファイル サイズの制限</span><span class="sxs-lookup"><span data-stu-id="7c073-113">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="7c073-114">これらの制限に加えて、Azure ADおよび Microsoft 365 全体でいくつかの調整メカニズムが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7c073-114">In addition to these limits, several throttling mechanisms are used throughout Azure AD and Microsoft 365.</span></span> <span data-ttu-id="7c073-115">Microsoft のデータセンターのネットワーク リソースがサービスを使用する幅広い顧客に最適化されている場合、サービス内での調整は特に重要です。</span><span class="sxs-lookup"><span data-stu-id="7c073-115">Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services.</span></span> <span data-ttu-id="7c073-116">調整メカニズムには、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7c073-116">Throttling mechanisms include:</span></span>

- <span data-ttu-id="7c073-117">Azure ADおよび Microsoft 365 機能のユーザー レベル調整は、1 人のユーザーが実行できるトランザクションまたは同時呼び出し (スクリプトまたはコードによる) の数を制限します。</span><span class="sxs-lookup"><span data-stu-id="7c073-117">Azure AD and Microsoft 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="7c073-118">既定の PowerShell 調整ポリシーは、テナントの作成時に各テナントに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="7c073-118">A default PowerShell throttling policy is assigned to each tenant at tenant creation.</span></span> <span data-ttu-id="7c073-119">これらの設定は、1 人の管理者が同時に開くことができる PowerShell セッションの最大数など、他の項目に影響します。</span><span class="sxs-lookup"><span data-stu-id="7c073-119">These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="7c073-120">各 Exchange Online のお客様には、EWS クライアント操作と、すべての Outlook クライアントに適用される調整用に調整される既定の Exchange Web サービス (EWS) ポリシーがあります。</span><span class="sxs-lookup"><span data-stu-id="7c073-120">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
