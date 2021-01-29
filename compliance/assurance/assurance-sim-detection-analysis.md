---
title: 'Microsoft 365 セキュリティ インシデント管理: 検出と分析'
description: この記事では、Microsoft 365 のセキュリティ インシデント管理の検出と分析プロセスの概要について説明します。
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
ms.openlocfilehash: 1fbdca0c0b08c793732ba31414bedd943d4dc115
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037604"
---
# <a name="microsoft-365-security-incident-management-detection-and-analysis"></a><span data-ttu-id="84790-103">Microsoft 365 セキュリティ インシデント管理: 検出と分析</span><span class="sxs-lookup"><span data-stu-id="84790-103">Microsoft 365 security incident management: Detection and analysis</span></span>

<span data-ttu-id="84790-104">悪意のあるアクティビティを検出するために、Microsoft 365 はセキュリティ イベントおよびその他のデータを一からログに記録し、さまざまな分析手法を実行して異常または疑わしいアクティビティを検出します。</span><span class="sxs-lookup"><span data-stu-id="84790-104">To detect malicious activity, Microsoft 365 centrally logs security events and other data and performs various analytical techniques to find anomalous or suspicious activity.</span></span> <span data-ttu-id="84790-105">ログ ファイルは、Microsoft 365 サーバーとインフラストラクチャ デバイスから収集され、中央および統合データベースに格納されます。</span><span class="sxs-lookup"><span data-stu-id="84790-105">Log files are collected from Microsoft 365 servers and infrastructure devices and stored in a central and consolidated database.</span></span>

<span data-ttu-id="84790-106">Microsoft では、悪意のあるアクティビティを検出するためにリスクベースのアプローチを採用しています。</span><span class="sxs-lookup"><span data-stu-id="84790-106">Microsoft takes a risk-based approach to detecting malicious activity.</span></span> <span data-ttu-id="84790-107">インシデント データと脅威インテリジェンスを使用して、検出の定義と優先順位付けを行います。</span><span class="sxs-lookup"><span data-stu-id="84790-107">We use incident data and threat intelligence to define and prioritize our detections.</span></span>

<span data-ttu-id="84790-108">経験豊富で、熟練したスキルを持つ人たちのチームを採用することが、検出と分析のフェーズで成功を収める最も重要な柱の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="84790-108">Employing a team of highly experienced, proficient, and skilled people is one of the most important pillars to success in the detection and analysis phase.</span></span> <span data-ttu-id="84790-109">Microsoft 365 は複数のサービス チームを採用しています。これらのチームには、ネットワーク、ルーター、ファイアウォール、ロード バランサー、オペレーティング システム、アプリケーションなど、スタック内のすべてのコンポーネントでコンピテンシーを持つ従業員が含まれます。</span><span class="sxs-lookup"><span data-stu-id="84790-109">Microsoft 365 employs multiple service teams, and those teams include employees with competencies on all components within the stack, including the network, routers, firewalls, load balancers, operating systems, and applications.</span></span>

<span data-ttu-id="84790-110">Microsoft 365 のセキュリティ検出メカニズムには、さまざまなソースによって開始される通知とアラートも含まれます。</span><span class="sxs-lookup"><span data-stu-id="84790-110">The security detection mechanisms in Microsoft 365 also include notification and alerts that are initiated by different sources.</span></span> <span data-ttu-id="84790-111">Microsoft 365 セキュリティ対応チームは、セキュリティ インシデントエスカレーション プロセスの主要なオーケストレーターです。</span><span class="sxs-lookup"><span data-stu-id="84790-111">The Microsoft 365 Security Response team is the key orchestrator of the security incident escalation process.</span></span> <span data-ttu-id="84790-112">このチームは、すべてのエスカレーションを受け取り、セキュリティ インシデントの有効性の分析と確認を担当します。</span><span class="sxs-lookup"><span data-stu-id="84790-112">This team receives all escalations and is responsible for analyzing and confirming the validity of the security incident.</span></span>

<span data-ttu-id="84790-113">検出の主な柱の 1 つは通知です。</span><span class="sxs-lookup"><span data-stu-id="84790-113">One of the primary pillars of detection is notification:</span></span>

- <span data-ttu-id="84790-114">各サービス チームは、Microsoft 365 セキュリティ チームの要件に基づいて、サービス内のアクションまたはイベントをログに記録する責任があります。</span><span class="sxs-lookup"><span data-stu-id="84790-114">Each service team is responsible to log any action or event inside the service based on the requirements from the Microsoft 365 Security team.</span></span> <span data-ttu-id="84790-115">異なるサービス チームによって作成されたログはすべて、定義済みのセキュリティおよび検出ルールを使用して、セキュリティ情報およびイベント管理 (SIEM) ソリューションによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="84790-115">All logs created by the different service teams are processed by a Security Information and Event Management (SIEM) solution with predefined security and detection rules.</span></span> <span data-ttu-id="84790-116">これらのルールは、Microsoft 365 セキュリティ チームの推奨事項に基づいて進化し、以前のセキュリティ インシデントから得た情報に基づいて、疑わしいアクティビティや悪意のあるアクティビティが存在するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="84790-116">These rules evolve based on the Microsoft 365 Security team’s recommendation, on information learned from previous security incidents, to determine if there is any suspicious or malicious activity.</span></span>
- <span data-ttu-id="84790-117">お客様がセキュリティ インシデントが進行中と判断した場合、Microsoft にサポート ケースを開く可能性があります。Microsoft は Microsoft 365 カスタマー エクスペリエンス (CxP) コミュニケーション チームに割り当て、すべての適切なチームへのエスカレーションに変わった可能性があります。</span><span class="sxs-lookup"><span data-stu-id="84790-117">If a customer determines that a security incident is underway, they may open a support case with Microsoft, which is assigned to the Microsoft 365 Customer Experience (CxP) Communications team and turned into an escalation to all appropriate teams.</span></span>

<span data-ttu-id="84790-118">また、Microsoft 365 サービス チームは、セキュリティ監視とログを使用して傾向分析で得られるインテリジェンスを使用して、攻撃やセキュリティ インシデントを示す可能性のある Microsoft 365 情報システムの異常を検出します。</span><span class="sxs-lookup"><span data-stu-id="84790-118">Microsoft 365 service teams also use the intelligence gained in trend analysis through security monitoring and logging to detect abnormalities in Microsoft 365 information systems that might indicate an attack or a security incident.</span></span> <span data-ttu-id="84790-119">Microsoft 365 サーバーは、これらのログからの出力を実稼働環境の集中ログ サーバーに集約します。</span><span class="sxs-lookup"><span data-stu-id="84790-119">Microsoft 365 servers aggregate output from these logs in the production environment into a centralized logging server.</span></span> <span data-ttu-id="84790-120">この集中ログ サーバーからログを調べて、実稼働環境全体の傾向を把握します。</span><span class="sxs-lookup"><span data-stu-id="84790-120">From this centralized logging server, logs are examined to spot trends throughout the production environment.</span></span> <span data-ttu-id="84790-121">集中管理されたサーバーで集計されたデータは、高度なクエリ、ダッシュボードの構築、異常および悪意のあるアクティビティの検出のためにログ サービスに安全に送信されます。</span><span class="sxs-lookup"><span data-stu-id="84790-121">Data aggregated in the centralized server is securely transmitted into a logging service for advanced querying, dashboard building and detecting anomalous and malicious activity.</span></span> <span data-ttu-id="84790-122">また、このサービスは機械学習を使用して、ログ出力で異常を検出します。</span><span class="sxs-lookup"><span data-stu-id="84790-122">The service also uses machine learning to detect anomalies with log output.</span></span>

<span data-ttu-id="84790-123">エスカレーション フェーズ中、およびセキュリティ インシデントの性質に応じて、Microsoft 365 セキュリティ対応チームは、Microsoft のさまざまなチームから 1 人または複数の分野の専門家と関わる場合があります。</span><span class="sxs-lookup"><span data-stu-id="84790-123">During the escalation phase and depending on the nature of the security incident, the Microsoft 365 Security Response team may engage one or more subject matter experts from various teams at Microsoft:</span></span>

- <span data-ttu-id="84790-124">Online Services セキュリティ/コンプライアンス チーム</span><span class="sxs-lookup"><span data-stu-id="84790-124">Online Services Security and Compliance team</span></span>
- <span data-ttu-id="84790-125">Microsoft Threat Intelligence Center (MSTIC)</span><span class="sxs-lookup"><span data-stu-id="84790-125">Microsoft Threat Intelligence Center (MSTIC)</span></span>
- <span data-ttu-id="84790-126">Microsoft セキュリティ レスポンス センター (MSRC)</span><span class="sxs-lookup"><span data-stu-id="84790-126">Microsoft Security Response Center (MSRC)</span></span>
- <span data-ttu-id="84790-127">企業、外部、および法務 (CELA)</span><span class="sxs-lookup"><span data-stu-id="84790-127">Corporate, External, and Legal Affairs (CELA)</span></span>
- <span data-ttu-id="84790-128">Azure Security</span><span class="sxs-lookup"><span data-stu-id="84790-128">Azure Security</span></span>
- <span data-ttu-id="84790-129">Microsoft 365 エンジニアリング、その他。</span><span class="sxs-lookup"><span data-stu-id="84790-129">Microsoft 365 engineering, and others.</span></span>

<span data-ttu-id="84790-130">Microsoft 365 セキュリティ対応チームへのエスカレーションが発生する前に、サービス チームは、次のような定義済みの条件に基づいて、セキュリティ インシデントの重大度レベルを決定および設定する責任を負います。</span><span class="sxs-lookup"><span data-stu-id="84790-130">Before any escalation to the Microsoft 365 Security Response team occurs, the service team is responsible for determining and setting the severity level of the security incident based on defined criteria such as:</span></span>

- <span data-ttu-id="84790-131">プライバシー</span><span class="sxs-lookup"><span data-stu-id="84790-131">Privacy</span></span>
- <span data-ttu-id="84790-132">影響</span><span class="sxs-lookup"><span data-stu-id="84790-132">Impact</span></span>
- <span data-ttu-id="84790-133">範囲</span><span class="sxs-lookup"><span data-stu-id="84790-133">Scope</span></span>
- <span data-ttu-id="84790-134">影響を受けるテナントの数</span><span class="sxs-lookup"><span data-stu-id="84790-134">Number of affected tenants</span></span>
- <span data-ttu-id="84790-135">Region</span><span class="sxs-lookup"><span data-stu-id="84790-135">Region</span></span>
- <span data-ttu-id="84790-136">サービス</span><span class="sxs-lookup"><span data-stu-id="84790-136">Service</span></span>
- <span data-ttu-id="84790-137">インシデントの詳細</span><span class="sxs-lookup"><span data-stu-id="84790-137">Details of the incident</span></span>
- <span data-ttu-id="84790-138">特定の顧客業界または市場の規制。</span><span class="sxs-lookup"><span data-stu-id="84790-138">Specific customer industry or market regulations.</span></span>

<span data-ttu-id="84790-139">インシデントの位置付けは、インシデントの機能への影響、インシデントの情報への影響、インシデントからの回復可能性など、明確な要因を使用して決定されます。</span><span class="sxs-lookup"><span data-stu-id="84790-139">Incident prioritization is determined by using distinct factors, including but not limited to the functional impact of the incident, the informational impact of the incident, and the recoverability from the incident.</span></span>

<span data-ttu-id="84790-140">セキュリティ インシデントに関するエスカレーションを受けた後、Microsoft 365 セキュリティ チームは、Microsoft 365 セキュリティ対応チーム、サービス チーム、および Microsoft 365 インシデントコミュニケーション チームのメンバーで構成される仮想チーム (v チーム) を編成します。</span><span class="sxs-lookup"><span data-stu-id="84790-140">After receiving an escalation about a security incident, the Microsoft 365 Security team organizes a virtual team (v-team) comprised of members from Microsoft 365 Security Response team, service teams, and the Microsoft 365 Incident Communication team.</span></span> <span data-ttu-id="84790-141">この v チームのアクティビティの複雑な部分は、セキュリティ インシデントを確認し、誤検知を排除する作業です。</span><span class="sxs-lookup"><span data-stu-id="84790-141">The more complex part of activities of this v-team is to confirm the security incident and to eliminate any false positives.</span></span> <span data-ttu-id="84790-142">準備フェーズで決定されたインジケーターによって提供される情報の精度は重要です。</span><span class="sxs-lookup"><span data-stu-id="84790-142">The accuracy of information provided by the indicators determined in the preparation phase is critical.</span></span> <span data-ttu-id="84790-143">v チームは、ベクトル攻撃のカテゴリ別にこの情報を分析することで、セキュリティ インシデントが正当な懸念事項かどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="84790-143">By analyzing this information by category of vector attack, the v-team can determine if the security incident is a legitimate concern.</span></span>

<span data-ttu-id="84790-144">調査の開始時に、Office セキュリティ インシデント対応チームは、ケース管理ポリシーに従ってインシデントに関する情報を記録します。</span><span class="sxs-lookup"><span data-stu-id="84790-144">At the beginning of the investigation, the Office Security Incident Response team records all information about the incident according to our case management policies.</span></span> <span data-ttu-id="84790-145">ケースの進行に合わせ、進行中のアクションを追跡し、インシデント ライフサイクル全体でこのデータを収集、保持、およびセキュリティ保護するためのエビデンス処理基準に従います。</span><span class="sxs-lookup"><span data-stu-id="84790-145">As the case progresses, we track ongoing actions and follow evidence handling standards for gathering, retaining, and securing this data throughout the incident lifecycle.</span></span>

<span data-ttu-id="84790-146">これらのアクションの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="84790-146">Some examples of these actions would include:</span></span>

- <span data-ttu-id="84790-147">概要。インシデントとその潜在的な影響の簡単な説明です。</span><span class="sxs-lookup"><span data-stu-id="84790-147">A summary, which is a brief description of the incident and its potential impact</span></span>
- <span data-ttu-id="84790-148">インシデントの重大度と優先度。潜在的な影響を評価することで導き出されます。</span><span class="sxs-lookup"><span data-stu-id="84790-148">The incident's severity and priority, which are derived by assessing the potential impact</span></span>
- <span data-ttu-id="84790-149">インシデントの検出につながったすべてのインジケーターの一覧</span><span class="sxs-lookup"><span data-stu-id="84790-149">A list of all indicators identified which led to detection of the incident</span></span>
- <span data-ttu-id="84790-150">関連するインシデントの一覧</span><span class="sxs-lookup"><span data-stu-id="84790-150">A list of any related incidents</span></span>
- <span data-ttu-id="84790-151">v-team が実行した操作の一覧</span><span class="sxs-lookup"><span data-stu-id="84790-151">A list of all actions taken by the v-team</span></span>
- <span data-ttu-id="84790-152">収集された証拠。事後分析と将来の法医学調査のためにも保持されます。</span><span class="sxs-lookup"><span data-stu-id="84790-152">Any gathered evidence, which will also be preserved for post-mortem analysis and future forensic investigations</span></span>
- <span data-ttu-id="84790-153">推奨される次のステップとアクション</span><span class="sxs-lookup"><span data-stu-id="84790-153">Recommended next steps and actions</span></span>

<span data-ttu-id="84790-154">セキュリティ インシデントの確認後、Microsoft 365 セキュリティ対応チームと適切なサービス チームの主な目標は、攻撃を含め、攻撃を受けたサービスを保護し、グローバルな影響を大きく回避します。</span><span class="sxs-lookup"><span data-stu-id="84790-154">After security incident confirmation, the primary goals of the Microsoft 365 Security Response team and the appropriate service team are to contain the attack, to protect the service(s) under attack, and to avoid a greater global impact.</span></span> <span data-ttu-id="84790-155">同時に、適切なエンジニアリング チームは根本原因を特定し、最初の復旧計画を準備します。</span><span class="sxs-lookup"><span data-stu-id="84790-155">At the same time, the appropriate engineering teams work to determine the root cause and to prepare the first recovery plan.</span></span>

<span data-ttu-id="84790-156">次のフェーズでは、Microsoft 365 セキュリティ対応チームは、セキュリティ インシデントの影響を受けるお客様を特定します (その場合)。</span><span class="sxs-lookup"><span data-stu-id="84790-156">In the next phase, the Microsoft 365 Security Response team identifies the customer(s) affected by the security incident, if any.</span></span> <span data-ttu-id="84790-157">有効範囲は、地域、データセンター、サービス、サーバー ファーム、サーバーなどによって決定に時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="84790-157">The scope of effect can take some time to determine, based on region, datacenter, service, server farm, server, and so forth.</span></span> <span data-ttu-id="84790-158">影響を受けるお客様の一覧は、サービス チームと Microsoft 365 CxP コミュニケーション チームによってコンパイルされ、契約上およびコンプライアンス上の義務の範囲内で顧客通知プロセスを処理します。</span><span class="sxs-lookup"><span data-stu-id="84790-158">The list of affected customers is compiled by the service team and the Microsoft 365 CxP Communications team, who then handle the customer notification process within contractual and compliance obligations.</span></span>

## <a name="related-articles"></a><span data-ttu-id="84790-159">関連記事</span><span class="sxs-lookup"><span data-stu-id="84790-159">Related articles</span></span>

- [<span data-ttu-id="84790-160">Microsoft 365 セキュリティ インシデント管理</span><span class="sxs-lookup"><span data-stu-id="84790-160">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="84790-161">Microsoft 365 セキュリティ インシデント管理の準備</span><span class="sxs-lookup"><span data-stu-id="84790-161">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="84790-162">Microsoft 365 セキュリティ インシデント管理の格納、復旧</span><span class="sxs-lookup"><span data-stu-id="84790-162">Microsoft 365 security incident management containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
- [<span data-ttu-id="84790-163">Microsoft 365 セキュリティ インシデント管理インシデント後のアクティビティ</span><span class="sxs-lookup"><span data-stu-id="84790-163">Microsoft 365 security incident management post-incident activity</span></span>](assurance-sim-post-incident-activity.md)
