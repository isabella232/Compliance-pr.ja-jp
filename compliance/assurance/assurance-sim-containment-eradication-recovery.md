---
title: 'Microsoft 365 セキュリティ インシデント管理: 格納、復旧、回復'
description: この記事では、Microsoft 365 のセキュリティ インシデント管理の格納、復旧、および回復プロセスの概要について説明します。
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
ms.openlocfilehash: 702735ed2ba35a4f3b0a02123f0c58b5fb4d397e
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037605"
---
# <a name="microsoft-365-security-incident-management-containment-eradication-and-recovery"></a><span data-ttu-id="b6c6f-103">Microsoft 365 セキュリティ インシデント管理: 格納、復旧、回復</span><span class="sxs-lookup"><span data-stu-id="b6c6f-103">Microsoft 365 security incident management: Containment, eradication, and recovery</span></span>

<span data-ttu-id="b6c6f-104">Microsoft 365 セキュリティ対応チーム、サービス チーム、その他によって実行された分析に基づいて、セキュリティ インシデントの影響を最小限に抑えるための適切な格納および復旧計画を作成します。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-104">Based on the analysis performed by the Microsoft 365 Security Response team, the service team, and others, an appropriate containment and recovery plan is developed to minimize the effect of the security incident.</span></span> <span data-ttu-id="b6c6f-105">適切なサービス チームは、Microsoft 365 セキュリティ対応チームのサポートを受けて、そのプランを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-105">The appropriate service teams then apply that plan in production with support from the Microsoft 365 Security Response team.</span></span>

## <a name="containment"></a><span data-ttu-id="b6c6f-106">コンテインメント</span><span class="sxs-lookup"><span data-stu-id="b6c6f-106">Containment</span></span>

<span data-ttu-id="b6c6f-107">セキュリティ インシデントを検出した後、攻撃者が多くのリソースにアクセスしたり、より多くの損害を与える前に侵入を含めすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-107">After detecting a security incident, it is important to contain the intrusion before the adversary can access more resources or cause more damage.</span></span> <span data-ttu-id="b6c6f-108">セキュリティ インシデント対応手順の主な目的は、お客様やデータ、または Microsoft のシステム、サービス、アプリケーションへの影響を制限することです。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-108">The primary goal of our security incident response procedures is to limit impact to customers or their data, or to Microsoft systems, services, and applications.</span></span>

## <a name="eradication"></a><span data-ttu-id="b6c6f-109">根絶</span><span class="sxs-lookup"><span data-stu-id="b6c6f-109">Eradication</span></span>

<span data-ttu-id="b6c6f-110">根絶は、高い信頼性を有するセキュリティ インシデントの根本原因を解消するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-110">Eradication is the process of eliminating the root cause of the security incident with a high degree of confidence.</span></span> <span data-ttu-id="b6c6f-111">目標は次の 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-111">The goal is two-fold:</span></span>

- <span data-ttu-id="b6c6f-112">環境から敵対者を完全に削除する</span><span class="sxs-lookup"><span data-stu-id="b6c6f-112">to evict the adversary completely from the environment</span></span>
- <span data-ttu-id="b6c6f-113">を使用して、攻撃者が環境に再入できる可能性がある脆弱性 (既知の場合) を軽減します。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-113">to mitigate the vulnerability (if known) that enabled or could enable the adversary to reenter the environment.</span></span>

<span data-ttu-id="b6c6f-114">インシデントの性質、セキュリティ インシデントの範囲、侵入の深さ、および可能な反言に応じて、Microsoft 365 セキュリティ対応チームは、サービス チームが採用する方法を推奨します。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-114">Depending on the nature of the incident, the scope of the security incident, the depth of the penetration and possible repercussions, the Microsoft 365 Security Response team will recommend that service teams adopt eradication techniques.</span></span> <span data-ttu-id="b6c6f-115">これらの取り組み手順によってビジネスに及ぼす可能性のある影響を考慮し、これらの決定は、エグゼクティブ インシデント マネージャーからの詳細な分析と承認の後 (必要に応じて) サービス チームと Microsoft 365 セキュリティ対応チームによって行います。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-115">Considering the potential business impact that may be caused by these eradication steps, these decisions will be made by service teams and the Microsoft 365 Security Response team after a detailed analysis and approval from the Executive Incident Manager (if necessary).</span></span>

## <a name="recovery"></a><span data-ttu-id="b6c6f-116">回復</span><span class="sxs-lookup"><span data-stu-id="b6c6f-116">Recovery</span></span>

<span data-ttu-id="b6c6f-117">対応チームが、敵対者が環境から排除され、既知の脆弱なパスはすべて排除されたという妥当なレベルの信頼を得たので、個々のサービス チームは、サービスを既知の良好な構成に戻す復元手順を開始します。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-117">As the response team gains a reasonable level of confidence that the adversary has been evicted from the environment and all known vulnerable paths have been eliminated, the individual service teams, will initiate restoration steps to bring the service to a known and good configuration.</span></span> <span data-ttu-id="b6c6f-118">これらの復元手順は、Microsoft 365 セキュリティ対応チームと相談する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-118">These restoration steps will be in consultation with the Microsoft 365 Security Response team.</span></span> <span data-ttu-id="b6c6f-119">このアクティビティには、サービスの最新の既知の良好な状態の特定、バックアップからこの状態への復元、復元された状態での脆弱な攻撃パスの検査などが含まれます。Microsoft 365 セキュリティ対応チームは、サービス チームと相談して、環境に最適な回復計画を決定します。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-119">This activity includes identifying the last known good state of the service, restoring from backups to this state, inspecting vulnerable attack paths in the restored state, etc. The Microsoft 365 Security Response team, in consultation with the service teams, will determine the best possible recovery plan for the environment.</span></span>

<span data-ttu-id="b6c6f-120">回復の重要な側面は、回復計画が正常に実行され、環境に違反の兆候が存在しないか検証するために強化された監視と制御を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-120">A key aspect to the recovery is to have enhanced vigilance and controls in place to validate that the recovery plan has been successfully executed, and that no signs of breach exist in the environment.</span></span>

## <a name="customer-notification-of-security-incident"></a><span data-ttu-id="b6c6f-121">セキュリティ インシデントに関する顧客通知</span><span class="sxs-lookup"><span data-stu-id="b6c6f-121">Customer notification of security incident</span></span>

<span data-ttu-id="b6c6f-122">Microsoft がセキュリティ インシデントが発生したと判断した場合は、期限が近づいて、契約要件およびコンプライアンス要件内で Microsoft が合意した範囲内でお客様に通知します。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-122">If Microsoft determines that a security incident has occurred, we will notify you with undue delay, and within contractual and compliance requirements we have agreed to.</span></span> <span data-ttu-id="b6c6f-123">影響を受けるすべてのテナントを特定した後、Microsoft 365 カスタマー エクスペリエンス (CxP) コミュニケーション チームは影響を受けるテナントに適用される可能性のある関連規制を特定します。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-123">After identifying all affected tenants, the Microsoft 365 Customer Experience (CxP) Communications team works to identify any relevant regulations that might apply to affected tenants.</span></span> <span data-ttu-id="b6c6f-124">Microsoft 365 CxP コミュニケーション チームは、該当する規制で定義されている適切な通信チャネルを使用して、適切なテナントの連絡先に通知します。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-124">The Microsoft 365 CxP Communications team uses the appropriate communication channel defined in applicable regulations to notify the appropriate tenant contact.</span></span>

<span data-ttu-id="b6c6f-125">通知には、インシデントの説明、顧客データへの影響 (お持ちである場合)、Microsoft が実行したアクション、問題を解決して繰り返し発生を防止するためにお客様が実行する推奨アクションなど、インシデントに関する詳細情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-125">Notification will include detailed information about the incident, such as a description of the incident, the effect on customer data, if any, actions taken by Microsoft, and/or suggested actions for customers to take to resolve the issue and prevent recurrence.</span></span> <span data-ttu-id="b6c6f-126">通知は、Microsoft 365 テナントの指定された管理者に配信されます。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-126">Notification will be delivered to the designated administrator(s) of the Microsoft 365 tenant.</span></span> <span data-ttu-id="b6c6f-127">通知を確実に受信するには、管理者がテナント プロファイルに正確な連絡先情報を提供し、維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6c6f-127">To ensure notifications are received, you should ensure that your administrators provide and maintain accurate contact information in their tenant profiles.</span></span> <span data-ttu-id="b6c6f-128">また、インシデントの性質に応じて、Microsoft 365 サービス正常性ダッシュボードを使用して通知することもできます[。](http://status.yammer.com/)</span><span class="sxs-lookup"><span data-stu-id="b6c6f-128">In addition, depending on the nature of the incident, customers can also be notified via the Microsoft 365 Service Health Dashboard[.](http://status.yammer.com/)</span></span>

## <a name="related-articles"></a><span data-ttu-id="b6c6f-129">関連記事</span><span class="sxs-lookup"><span data-stu-id="b6c6f-129">Related articles</span></span>

- [<span data-ttu-id="b6c6f-130">Microsoft 365 セキュリティ インシデント管理</span><span class="sxs-lookup"><span data-stu-id="b6c6f-130">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="b6c6f-131">Microsoft 365 セキュリティ インシデント管理の準備</span><span class="sxs-lookup"><span data-stu-id="b6c6f-131">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="b6c6f-132">Microsoft 365 セキュリティ インシデント管理の検出と分析</span><span class="sxs-lookup"><span data-stu-id="b6c6f-132">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="b6c6f-133">Microsoft 365 セキュリティ インシデント管理インシデント後のアクティビティ</span><span class="sxs-lookup"><span data-stu-id="b6c6f-133">Microsoft 365 security incident management post-incident activity</span></span>](assurance-sim-post-incident-activity.md)
