---
title: Microsoft 365 Yammerアクセス制御
description: この記事では、実稼働環境でのエンタープライズ Yammerの概要について説明します。
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
ms.openlocfilehash: df345d922bbd0c9106cf0714377803a9c0870d82
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497351"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="3d6d4-103">Yammerアクセス制御</span><span class="sxs-lookup"><span data-stu-id="3d6d4-103">Yammer enterprise access controls</span></span> 

<span data-ttu-id="3d6d4-104">実稼働環境への物理的および論理的Yammerアクセスは、少人数のユーザー (インフラストラクチャと運用) に制限されます。</span><span class="sxs-lookup"><span data-stu-id="3d6d4-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="3d6d4-105">他の Microsoft 365 エンジニアと同様に、Yammerエンジニアは顧客データに常にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3d6d4-105">As with other Microsoft 365 engineers, Yammer engineers have zero standing access to customer data.</span></span> <span data-ttu-id="3d6d4-106">承認者の数が限られている Lockbox に似た承認ベースの Just-in-time アクセス制御システムを使用してアクセスを要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d6d4-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="3d6d4-107">承認者は要求を確認し (たとえば、要求が必要性、ビジネス ケース、時間などに基づいて正当かどうかを確認します)、要求を承認または拒否します。</span><span class="sxs-lookup"><span data-stu-id="3d6d4-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="3d6d4-108">要求が承認された場合、JIT アクセスは、定義された期間限定で付与されます。</span><span class="sxs-lookup"><span data-stu-id="3d6d4-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="3d6d4-109">アクセス時間を超えると、アクセスは自動的に期限切れになります。</span><span class="sxs-lookup"><span data-stu-id="3d6d4-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="3d6d4-110">他の Microsoft 365 サービスと同様に、すべてのアクセスは、Yammer多要素認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="3d6d4-110">As with other Microsoft 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="3d6d4-111">すべてのアクセス履歴とコマンド履歴はユーザーに属性付けされ、セキュリティ チームによって定期的にログYammerされます。</span><span class="sxs-lookup"><span data-stu-id="3d6d4-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="3d6d4-112">管理と管理の詳細Yammer、管理者のヘルプYammer [参照してください](/yammer/yammer-landing-page)。</span><span class="sxs-lookup"><span data-stu-id="3d6d4-112">For more information about Yammer administration and management, see [Yammer admin help](/yammer/yammer-landing-page).</span></span>