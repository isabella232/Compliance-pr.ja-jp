---
title: 'Microsoft セキュリティ インシデント管理: 格納、根絶、および回復'
description: この記事では、Microsoft オンライン サービスにおけるセキュリティ インシデント管理の格納、根絶、および回復プロセスの概要について説明します。
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 95e52107df2f3e745d393c62929f7c169bcf9a33
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377554"
---
# <a name="microsoft-security-incident-management-containment-eradication-and-recovery"></a><span data-ttu-id="78125-103">Microsoft セキュリティ インシデント管理: 格納、根絶、および回復</span><span class="sxs-lookup"><span data-stu-id="78125-103">Microsoft security incident management: Containment, eradication, and recovery</span></span>

<span data-ttu-id="78125-104">セキュリティ対応チーム、サービス チームなどが実行した分析に基づいて、セキュリティ インシデントの影響を最小限に抑えるための適切な格納および回復計画が作成されます。</span><span class="sxs-lookup"><span data-stu-id="78125-104">Based on the analysis performed by the security response team, the service team, and others, an appropriate containment and recovery plan is developed to minimize the effect of the security incident.</span></span> <span data-ttu-id="78125-105">適切なサービス チームは、セキュリティ対応チームのサポートを受けて、その計画を実稼働環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="78125-105">The appropriate service teams then apply that plan in production with support from the security response team.</span></span>

## <a name="containment"></a><span data-ttu-id="78125-106">コンテインメント</span><span class="sxs-lookup"><span data-stu-id="78125-106">Containment</span></span>

<span data-ttu-id="78125-107">セキュリティ インシデントを検出した後、敵対者がリソースにアクセスしたり、より多くの損害を与える前に侵入を含めすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="78125-107">After detecting a security incident, it is important to contain the intrusion before the adversary can access more resources or cause more damage.</span></span> <span data-ttu-id="78125-108">セキュリティ インシデント対応手順の主な目的は、顧客またはデータ、または Microsoft システム、サービス、およびアプリケーションへの影響を制限することです。</span><span class="sxs-lookup"><span data-stu-id="78125-108">The primary goal of our security incident response procedures is to limit impact to customers or their data, or to Microsoft systems, services, and applications.</span></span>

## <a name="eradication"></a><span data-ttu-id="78125-109">根絶</span><span class="sxs-lookup"><span data-stu-id="78125-109">Eradication</span></span>

<span data-ttu-id="78125-110">根絶は、高い信頼性を有するセキュリティ インシデントの根本原因を解消するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="78125-110">Eradication is the process of eliminating the root cause of the security incident with a high degree of confidence.</span></span> <span data-ttu-id="78125-111">目標は 2 倍です。</span><span class="sxs-lookup"><span data-stu-id="78125-111">The goal is two-fold:</span></span>

- <span data-ttu-id="78125-112">環境から敵対者を完全に追い出す</span><span class="sxs-lookup"><span data-stu-id="78125-112">to evict the adversary completely from the environment</span></span>
- <span data-ttu-id="78125-113">を有効にするか、または攻撃者が環境を再入力できる可能性がある脆弱性 (既知の場合) を軽減します。</span><span class="sxs-lookup"><span data-stu-id="78125-113">to mitigate the vulnerability (if known) that enabled or could enable the adversary to reenter the environment.</span></span>

<span data-ttu-id="78125-114">インシデントの性質、セキュリティ インシデントの範囲、侵入の深さ、および可能な反響に応じて、セキュリティ対応チームは、サービス チームが根絶技術を採用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="78125-114">Depending on the nature of the incident, the scope of the security incident, the depth of the penetration and possible repercussions, the security response team will recommend that service teams adopt eradication techniques.</span></span> <span data-ttu-id="78125-115">これらの根絶手順によって引き起こされる可能性のあるビジネスへの影響を考慮すると、これらの決定は、エグゼクティブ インシデント マネージャー (必要に応じて) による詳細な分析と承認の後、サービス チームとセキュリティ対応チームによって行います。</span><span class="sxs-lookup"><span data-stu-id="78125-115">Considering the potential business impact that may be caused by these eradication steps, these decisions will be made by service teams and the security response team after a detailed analysis and approval from the Executive Incident Manager (if necessary).</span></span>

## <a name="recovery"></a><span data-ttu-id="78125-116">回復</span><span class="sxs-lookup"><span data-stu-id="78125-116">Recovery</span></span>

<span data-ttu-id="78125-117">応答チームが、敵対者が環境から追い出され、既知のすべての脆弱なパスが排除されたという妥当なレベルの信頼を得たので、個々のサービス チームは、サービスを既知の良好な構成に戻す復元手順を開始します。</span><span class="sxs-lookup"><span data-stu-id="78125-117">As the response team gains a reasonable level of confidence that the adversary has been evicted from the environment and all known vulnerable paths have been eliminated, the individual service teams, will initiate restoration steps to bring the service to a known and good configuration.</span></span> <span data-ttu-id="78125-118">これらの復元手順は、セキュリティ対応チームと協議します。</span><span class="sxs-lookup"><span data-stu-id="78125-118">These restoration steps will be in consultation with the security response team.</span></span> <span data-ttu-id="78125-119">このアクティビティには、サービスの最後の既知の良好な状態の特定、バックアップからこの状態への復元、復元された状態での脆弱な攻撃パスの検査などが含まれます。セキュリティ対応チームは、サービス チームと協議して、環境に最適な回復計画を決定します。</span><span class="sxs-lookup"><span data-stu-id="78125-119">This activity includes identifying the last known good state of the service, restoring from backups to this state, inspecting vulnerable attack paths in the restored state, etc. The security response team, in consultation with the service teams, will determine the best possible recovery plan for the environment.</span></span>

<span data-ttu-id="78125-120">回復の重要な側面は、回復計画が正常に実行され、環境に侵害の兆候が存在しないか検証するために、警戒と制御を強化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="78125-120">A key aspect to the recovery is to have enhanced vigilance and controls in place to validate that the recovery plan has been successfully executed, and that no signs of breach exist in the environment.</span></span>

## <a name="customer-notification-of-security-incident"></a><span data-ttu-id="78125-121">セキュリティ インシデントの顧客通知</span><span class="sxs-lookup"><span data-stu-id="78125-121">Customer notification of security incident</span></span>

<span data-ttu-id="78125-122">Microsoft がセキュリティ インシデントが発生したと判断した場合、弊社は、契約要件およびコンプライアンス要件の範囲内で、遅延が発生した場合に通知します。</span><span class="sxs-lookup"><span data-stu-id="78125-122">If Microsoft determines that a security incident has occurred, we will notify you with undue delay, and within contractual and compliance requirements we have agreed to.</span></span> <span data-ttu-id="78125-123">影響を受けるすべてのテナントを特定した後、対応するコミュニケーション チームは、影響を受けるテナントに適用される可能性のある関連する規制を特定します。</span><span class="sxs-lookup"><span data-stu-id="78125-123">After identifying all affected tenants, the corresponding communications team works to identify any relevant regulations that might apply to affected tenants.</span></span> <span data-ttu-id="78125-124">コミュニケーション チームは、該当する規制で定義されている適切な通信チャネルを使用して、適切なテナント連絡先に通知します。</span><span class="sxs-lookup"><span data-stu-id="78125-124">The communications team uses the appropriate communication channel defined in applicable regulations to notify the appropriate tenant contact.</span></span>

<span data-ttu-id="78125-125">通知には、インシデントの説明、顧客データへの影響、Microsoft が実行したアクション、および/または問題の解決と再発防止のためにお客様が実行する推奨されるアクションなど、インシデントに関する詳細情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="78125-125">Notification will include detailed information about the incident, such as a description of the incident, the effect on customer data, if any, actions taken by Microsoft, and/or suggested actions for customers to take to resolve the issue and prevent recurrence.</span></span> <span data-ttu-id="78125-126">通知は、Microsoft Online Services テナントの指定された管理者に配信されます。</span><span class="sxs-lookup"><span data-stu-id="78125-126">Notification will be delivered to the designated administrator(s) of the Microsoft online services tenant.</span></span> <span data-ttu-id="78125-127">通知を確実に受信するには、管理者がテナント プロファイルに正確な連絡先情報を提供し、維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="78125-127">To ensure notifications are received, you should ensure that your administrators provide and maintain accurate contact information in their tenant profiles.</span></span> <span data-ttu-id="78125-128">さらに、インシデントの性質に応じて、Microsoft 365サービス正常性ダッシュボードを介してMicrosoft 365[通知することもできます](http://status.yammer.com/)。</span><span class="sxs-lookup"><span data-stu-id="78125-128">In addition, depending on the nature of the incident, Microsoft 365 customers can also be notified via the [Microsoft 365 Service Health Dashboard](http://status.yammer.com/).</span></span>

## <a name="related-articles"></a><span data-ttu-id="78125-129">関連記事</span><span class="sxs-lookup"><span data-stu-id="78125-129">Related articles</span></span>

- [<span data-ttu-id="78125-130">Microsoft セキュリティ インシデント管理</span><span class="sxs-lookup"><span data-stu-id="78125-130">Microsoft security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="78125-131">Microsoft セキュリティ インシデント管理: 準備</span><span class="sxs-lookup"><span data-stu-id="78125-131">Microsoft security incident management: Preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="78125-132">Microsoft セキュリティ インシデント管理: 検出と分析</span><span class="sxs-lookup"><span data-stu-id="78125-132">Microsoft security incident management: Detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="78125-133">Microsoft セキュリティ インシデント管理: インシデント後のアクティビティ</span><span class="sxs-lookup"><span data-stu-id="78125-133">Microsoft security incident management: Post-incident activity</span></span>](assurance-sim-post-incident-activity.md)
- [<span data-ttu-id="78125-134">セキュリティ イベントのサポート チケットをログに記録する方法</span><span class="sxs-lookup"><span data-stu-id="78125-134">How to Log a Security Event Support Ticket</span></span>](/azure/security/fundamentals/event-support-ticket)
- [<span data-ttu-id="78125-135">GDRP の下での Azure および Dynamics 365 の侵害通知</span><span class="sxs-lookup"><span data-stu-id="78125-135">Azure and Dynamics 365 breach notification under the GDPR</span></span>](/compliance/regulatory/gdpr-breach-azure-dynamics)
