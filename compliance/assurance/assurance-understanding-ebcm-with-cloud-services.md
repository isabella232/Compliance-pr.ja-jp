---
title: クラウドサービスによるエンタープライズ ビジネスの継続性の管理について
description: クラウドサービスが IT サービスに含まれている場合の、ビジネスの継続性の計画と実装の違いを説明します。
author: robmazz
ms.author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
f1.keywords:
- NOCSH
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- remotework
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 4d4b2f02eacb09f09aae4995f5ee2747fbfe59a6
ms.sourcegitcommit: 693bc6b1b51a5a9c9ff1758fa7f7ca3a204f147e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2020
ms.locfileid: "49574809"
---
# <a name="enterprise-business-continuity-management-ebcm-with-cloud-services"></a><span data-ttu-id="09e4d-103">クラウドサービスによるエンタープライズ ビジネスの継続性の管理 (EBCM) について</span><span class="sxs-lookup"><span data-stu-id="09e4d-103">Enterprise business continuity management (EBCM) with cloud services</span></span>

<span data-ttu-id="09e4d-104">組織のデジタル変換の一環として、Microsoft 365 クラウドサービスに依存しているビジネス プロセスに対応するために、障害復旧およびビジネスの継続性計画を見直す必要があります。</span><span class="sxs-lookup"><span data-stu-id="09e4d-104">As part of your organizations digital transformation, you need to revisit and update your disaster recovery and business continuity plans to account for the business process that depend on Microsoft 365 Cloud services.</span></span> <span data-ttu-id="09e4d-105">Microsoft 365 クラウドサービス (Exchange Online、SharePoint Online、OneDrive for Business など) は、優れた回復性を持つように設計されています。</span><span class="sxs-lookup"><span data-stu-id="09e4d-105">Microsoft 365 Cloud services, like Exchange Online, SharePoint Online and OneDrive for Business are designed and operated to be highly resilient.</span></span>

> [!NOTE]
> <span data-ttu-id="09e4d-106">Microsoft 独自の EBCM プランの詳細については、「[エンタープライズのビジネス継続性の管理プログラムのホワイトペーパー](https://go.microsoft.com/fwlink/?linkid=2121521)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="09e4d-106">You can learn more about Microsoft's own EBCM plan in the [Enterprise Business Continuity Management Program whitepaper](https://go.microsoft.com/fwlink/?linkid=2121521).</span></span> <span data-ttu-id="09e4d-107">ログインが必要です。</span><span class="sxs-lookup"><span data-stu-id="09e4d-107">Login is required.</span></span>

<span data-ttu-id="09e4d-108">たとえ回復性を備えていても、サービス インシデントは発生します。</span><span class="sxs-lookup"><span data-stu-id="09e4d-108">Even with this resilience, service incidents do occur.</span></span> <span data-ttu-id="09e4d-109">そのため、組織はよく準備し、ビジネスの継続性戦略を明確に定める必要があります。</span><span class="sxs-lookup"><span data-stu-id="09e4d-109">When they do, your organization should be prepared and have a well-defined business continuity strategy.</span></span>

<span data-ttu-id="09e4d-110">まだ計画を見直していない場合は、ここで紹介するトピックが戦略の計画に役立ちます。また、サービスが既知の状態になるのを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="09e4d-110">If you haven't updated your plans yet this series of topics helps you to plan your strategy so your services can fail to a known state.</span></span> <span data-ttu-id="09e4d-111">これらのトピックでは、連続性の準備を改善するための主な考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="09e4d-111">These topics highlight key considerations for improving your continuity readiness.</span></span>

## <a name="list-of-topics-with-links"></a><span data-ttu-id="09e4d-112">トピックの一覧とリンク</span><span class="sxs-lookup"><span data-stu-id="09e4d-112">List of topics with links</span></span>

- [<span data-ttu-id="09e4d-113">顧客およびクラウドパートナーの責任</span><span class="sxs-lookup"><span data-stu-id="09e4d-113">Customer and cloud partner responsibilities</span></span>](assurance-customer-and-cloud-partner-ebcm-responsibilities.md)
- [<span data-ttu-id="09e4d-114">Microsoft 365 サービスの回復性</span><span class="sxs-lookup"><span data-stu-id="09e4d-114">Microsoft 365 service resiliency</span></span>](assurance-m365-service-resiliency.md)
- [<span data-ttu-id="09e4d-115">連続性の計画を立てる</span><span class="sxs-lookup"><span data-stu-id="09e4d-115">Developing your continuity plan</span></span>](assurance-developing-your-ebcm-plan.md)
- [<span data-ttu-id="09e4d-116">Microsoft 365 のサービス インシデント対策のシナリオ</span><span class="sxs-lookup"><span data-stu-id="09e4d-116">Microsoft 365 service incident mitigation scenarios</span></span>](assurance-microsoft-365-mitigations.md)
- [<span data-ttu-id="09e4d-117">Microsoft 365 for business の継続性計画のトレーニングとリハーサル</span><span class="sxs-lookup"><span data-stu-id="09e4d-117">Microsoft 365 for business continuity plan training and rehearsal</span></span>](assurance-ebcm-plan-rehearsal-and-user-training.md)

## <a name="see-also"></a><span data-ttu-id="09e4d-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="09e4d-118">See also</span></span>

- [<span data-ttu-id="09e4d-119">エンタープライズ ビジネス継続性法的免責事項</span><span class="sxs-lookup"><span data-stu-id="09e4d-119">Enterprise business continuity legal disclaimer</span></span>](assurance-ebcm-legal-disclaimer.md)
