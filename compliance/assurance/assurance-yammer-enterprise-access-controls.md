---
title: Microsoft 365 Yammerエンタープライズ アクセス制御
description: この記事では、実稼働環境でのエンタープライズ アクセス制御Yammerについて簡単に説明します。
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
ms.openlocfilehash: 916f26d5f2defdfb21cb9babe3a64cf618e8cd4a
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120366"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="daac7-103">Yammerアクセス制御</span><span class="sxs-lookup"><span data-stu-id="daac7-103">Yammer enterprise access controls</span></span> 

<span data-ttu-id="daac7-104">実稼働環境への物理的および論理的Yammerアクセスは、一部のユーザー (インフラストラクチャと運用) に制限されます。</span><span class="sxs-lookup"><span data-stu-id="daac7-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="daac7-105">他の Microsoft 365 エンジニアと同様に、Yammerエンジニアは顧客データに常にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="daac7-105">As with other Microsoft 365 engineers, Yammer engineers have zero standing access to customer data.</span></span> <span data-ttu-id="daac7-106">制限された数の承認者を持つロックボックスと同様に、承認ベースの Just-In-Time アクセス制御システムを使用してアクセスを要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="daac7-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="daac7-107">承認者は要求を確認し (たとえば、要求が必要性、業務事例、時間などに基づいて正当かどうかを確認する)、要求を承認または拒否します。</span><span class="sxs-lookup"><span data-stu-id="daac7-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="daac7-108">要求が承認されると、定義された限られた時間に対して JIT アクセスが許可されます。</span><span class="sxs-lookup"><span data-stu-id="daac7-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="daac7-109">アクセス時間を超えると、アクセスは自動的に期限切れになります。</span><span class="sxs-lookup"><span data-stu-id="daac7-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="daac7-110">他の Microsoft 365 サービスと同様に、Yammer環境へのすべてのアクセスは多要素認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="daac7-110">As with other Microsoft 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="daac7-111">すべてのアクセスとコマンドの履歴はユーザーに関連付けされ、セキュリティ チームによって定期的にログYammer確認されます。</span><span class="sxs-lookup"><span data-stu-id="daac7-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="daac7-112">管理と管理の詳細Yammer、管理者向けヘルプ [Yammer参照してください](/yammer/yammer-landing-page)。</span><span class="sxs-lookup"><span data-stu-id="daac7-112">For more information about Yammer administration and management, see [Yammer admin help](/yammer/yammer-landing-page).</span></span>