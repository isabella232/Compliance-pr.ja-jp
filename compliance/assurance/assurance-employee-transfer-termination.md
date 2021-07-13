---
title: Microsoft 従業員の異動と退職
description: Microsoft の従業員の転送と終了のプロセスについて詳しくは、Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 862bd05a84e5144602a24ac2aca1780cffaff3fe
ms.sourcegitcommit: 48b8ec2dd00e957508e5af82458bf697e1a97ebb
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53395617"
---
# <a name="microsoft-employee-transfer-and-termination"></a><span data-ttu-id="ec0ef-103">Microsoft 従業員の異動と退職</span><span class="sxs-lookup"><span data-stu-id="ec0ef-103">Microsoft employee transfer and termination</span></span>

<span data-ttu-id="ec0ef-104">Microsoft は、他のすべての組織と同様に、通常の業務の一環として従業員の転送と終了を処理します。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-104">Microsoft, like every other organization, handles employee transfers and terminations as a part of their normal business operation.</span></span> <span data-ttu-id="ec0ef-105">従業員が役職を変更したり、会社を離れる場合は、不適切なアクセスを不適切な方法で取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-105">When an employee changes positions or leaves the company, it is essential to revoke inappropriate access in a timely manner.</span></span> <span data-ttu-id="ec0ef-106">効率的なアクセス変更とアクセス取り消しを容易にするために、Microsoft は標準化された手順と自動化されたプロセスを使用して、人事情報システム (HRIS) と IDM (IDM) システムを調整します。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-106">To facilitate efficient access changes and access revocations, Microsoft uses standardized procedures and automated processes to coordinate the Human Resources Information System (HRIS) with the Identity Management (IDM) system.</span></span> <span data-ttu-id="ec0ef-107">これら 2 つのシステム間の自動オーケストレーションは、運用の一貫性を維持し、Microsoft のオンライン サービスとデータを保護し、特権の不気味を防止し、インサイダーの脅威に関連するリスクを軽減するために不可欠です。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-107">Automated orchestration between these two systems is essential to maintaining operational consistency, safeguarding Microsoft's online services and data, preventing privilege creep, and reducing risks related to insider threats.</span></span>

<span data-ttu-id="ec0ef-108">Microsoft のオンライン サービスは、エンジニアの運用環境への管理アクセスを常に行わずに動作するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-108">Microsoft online services are designed to operate without standing administrative access to production environments for our engineers.</span></span> <span data-ttu-id="ec0ef-109">Microsoft では、Just-In-Time (JIT) Just-Enough-Access (JEA) モデルを使用して、必要に応じてサービスをサポートするために必要な一時的なアクセスをエンジニアに提供します。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-109">Microsoft uses a Just-In-Time (JIT), Just-Enough-Access (JEA) model to provide engineers with the temporary access needed to support their service when required.</span></span> <span data-ttu-id="ec0ef-110">JIT アクセスにサービス チーム アカウントを要求して使用するには、IDM ツールを使用して資格を要求し、維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-110">To request and use a service team account for JIT access, engineers must request and maintain eligibilities through the IDM tool.</span></span> <span data-ttu-id="ec0ef-111">従業員が転送または終了すると、サービス チーム アカウントと関連する資格が自動的に変更され、不適切なアクセスが防止されます。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-111">When employees are transferred or terminated, their service team account and related eligibilities are automatically modified to prevent inappropriate access.</span></span>

## <a name="transfer-and-reassignment"></a><span data-ttu-id="ec0ef-112">転送と再割り当て</span><span class="sxs-lookup"><span data-stu-id="ec0ef-112">Transfer and reassignment</span></span>

<span data-ttu-id="ec0ef-113">従業員の転送は、従業員のマネージャーによる転送トランザクション要求によって開始されます。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-113">Employee transfers are initiated through a transfer transaction request by the employee's manager.</span></span> <span data-ttu-id="ec0ef-114">マネージャーは要求を作成し、オファーレタープロセスのグローバル人材獲得に従事します。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-114">The manager creates a requisition and engages with Global Talent Acquisition for the offer letter process.</span></span> <span data-ttu-id="ec0ef-115">従業員が新しい役割のオファーを受け入れると、人事サービスは人事コア ツールの転送を完了し、IDM がトリガーして、すべての従業員の適格性の有効期限を設定します。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-115">Once the employee accepts the offer for the new role, HR services completes the transfer in the HR core tools, triggering IDM to set an expiration date for all the employee's eligibilities.</span></span> <span data-ttu-id="ec0ef-116">従業員は、資格を保持するために、要求を提出し、新しいマネージャーから承認を受ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-116">The employee must submit a request and receive approval from their new manager to retain their eligibilities.</span></span> <span data-ttu-id="ec0ef-117">要求の送信またはマネージャーの承認の受信に失敗すると、転送された従業員の資格が取り消されます。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-117">Failure to submit a request or receive manager approval results in the revocation of the transferred employee's eligibilities.</span></span> <span data-ttu-id="ec0ef-118">特定のセキュリティ上の影響を含む転送では、システム アクセスとセキュリティ グループ メンバーシップが直ちに再評価され、新しい役割が反映されます。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-118">For transfers that include specific security implications, system accesses and security group memberships are reevaluated immediately to reflect their new role.</span></span>

## <a name="termination"></a><span data-ttu-id="ec0ef-119">退職</span><span class="sxs-lookup"><span data-stu-id="ec0ef-119">Termination</span></span>

<span data-ttu-id="ec0ef-120">Microsoft は、明確に定義されたポリシーと手順を使用して、従業員の退職時に、Microsoft のシステムとリソースへの物理的および論理的アクセスを即座に取り消します。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-120">Microsoft uses clearly defined policies and procedures to promptly revoke physical and logical access to Microsoft systems and resources when an employee is terminated.</span></span> <span data-ttu-id="ec0ef-121">従業員が通知を行った場合、従業員のマネージャーは終了日を HRIS に入力します。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-121">When an employee gives their notice, the employee's manager enters the termination date into the HRIS.</span></span> <span data-ttu-id="ec0ef-122">従業員の最後の勤務日の後、HRIS は従業員を終了としてマークし、IDM に情報を共有し、すべてのサービス チーム アカウントと資格を自動的に削除します。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-122">Following the employee's last working day, the HRIS marks the employee as terminated and shares the information to IDM, which removes all service team accounts and eligibilities automatically.</span></span>

<span data-ttu-id="ec0ef-123">不本意な終了の場合、人事担当者は従業員のマネージャーと一緒に適切な手順に従って従業員を終了およびオフボードします。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-123">For involuntary terminations, HR works with the employee's manager to follow the appropriate steps to terminate and offboard the employee.</span></span> <span data-ttu-id="ec0ef-124">任意の終了と同様に、終了情報は、有効な日付調整、アクセスの削除などの必要な手順と共に HRIS に入力されます。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-124">Similar to a voluntary termination, the termination information is entered into the HRIS along with any necessary steps such as effective date coordination, access removal.</span></span> <span data-ttu-id="ec0ef-125">ロール外への移行に関連するその他の手順。</span><span class="sxs-lookup"><span data-stu-id="ec0ef-125">and any other steps relative to transitioning out of role.</span></span>
