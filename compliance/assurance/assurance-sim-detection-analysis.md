---
title: 'Microsoft セキュリティ インシデント管理: 検出と分析'
description: この記事では、Microsoft オンライン サービスにおけるセキュリティ インシデント管理の検出および分析プロセスの概要について説明します。
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
ms.openlocfilehash: 445d812b33214a3d2287268b587607004ef96ab7
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377354"
---
# <a name="microsoft-security-incident-management-detection-and-analysis"></a><span data-ttu-id="8b98c-103">Microsoft セキュリティ インシデント管理: 検出と分析</span><span class="sxs-lookup"><span data-stu-id="8b98c-103">Microsoft security incident management: Detection and analysis</span></span>

<span data-ttu-id="8b98c-104">悪意のあるアクティビティを検出するために、Microsoft の各オンライン サービスは、セキュリティ イベントおよびその他のデータを一中心にログに記録し、さまざまな分析手法を実行して異常または疑わしいアクティビティを検出します。</span><span class="sxs-lookup"><span data-stu-id="8b98c-104">To detect malicious activity, each of Microsoft's online services centrally logs security events and other data and perform various analytical techniques to find anomalous or suspicious activity.</span></span> <span data-ttu-id="8b98c-105">ログ ファイルは、Microsoft のオンライン サービス サーバーとインフラストラクチャ デバイスから収集され、中央データベースと統合データベースに保存されます。</span><span class="sxs-lookup"><span data-stu-id="8b98c-105">Log files are collected from Microsoft online services servers and infrastructure devices and stored in central and consolidated databases.</span></span>

<span data-ttu-id="8b98c-106">Microsoft では、悪意のあるアクティビティを検出するためのリスクベースのアプローチを採用しています。</span><span class="sxs-lookup"><span data-stu-id="8b98c-106">Microsoft takes a risk-based approach to detecting malicious activity.</span></span> <span data-ttu-id="8b98c-107">インシデント データと脅威インテリジェンスを使用して、検出の定義と優先順位付けを行います。</span><span class="sxs-lookup"><span data-stu-id="8b98c-107">We use incident data and threat intelligence to define and prioritize our detections.</span></span>

<span data-ttu-id="8b98c-108">経験豊富で熟練した熟練した人材のチームを採用することが、検出と分析の段階で成功を収める最も重要な柱の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="8b98c-108">Employing a team of highly experienced, proficient, and skilled people is one of the most important pillars to success in the detection and analysis phase.</span></span> <span data-ttu-id="8b98c-109">Microsoft では、ネットワーク、ルーター、ファイアウォール、ロード バランサー、オペレーティング システム、アプリケーションなど、スタック内のすべてのコンポーネントにコンピテンシーを持つ従業員を含む複数のサービス チームを採用しています。</span><span class="sxs-lookup"><span data-stu-id="8b98c-109">Microsoft employs multiple service teams that include employees with competencies on all components within the stack, including the network, routers, firewalls, load balancers, operating systems, and applications.</span></span>

<span data-ttu-id="8b98c-110">Microsoft オンライン サービスのセキュリティ検出メカニズムには、さまざまなソースによって開始される通知とアラートも含まれます。</span><span class="sxs-lookup"><span data-stu-id="8b98c-110">The security detection mechanisms in Microsoft online services also include notifications and alerts that are initiated by different sources.</span></span> <span data-ttu-id="8b98c-111">Microsoft Online Services のセキュリティ対応チームは、セキュリティ インシデントエスカレーション プロセスの主要なオーケストレーターです。</span><span class="sxs-lookup"><span data-stu-id="8b98c-111">Microsoft online services security response teams are the key orchestrators of the security incident escalation process.</span></span> <span data-ttu-id="8b98c-112">これらのチームは、すべてのエスカレーションを受け取り、セキュリティ インシデントの有効性を分析および確認する責任があります。</span><span class="sxs-lookup"><span data-stu-id="8b98c-112">These teams receive all escalations and are responsible for analyzing and confirming the validity of the security incident.</span></span>

![セキュリティ インシデント管理ワークフロー](../media/assurance-sim-workflow.png)

<span data-ttu-id="8b98c-114">検出の主な柱の 1 つは通知です。</span><span class="sxs-lookup"><span data-stu-id="8b98c-114">One of the primary pillars of detection is notification:</span></span>

- <span data-ttu-id="8b98c-115">各サービス チームは、オンライン サービス セキュリティ チームの要件に基づいて、サービス内の任意のアクションまたはイベントをログに記録する責任があります。</span><span class="sxs-lookup"><span data-stu-id="8b98c-115">Each service team is responsible to log any action or event inside the service based on the requirements from the online service security team.</span></span> <span data-ttu-id="8b98c-116">異なるサービス チームによって作成されたログはすべて、定義済みのセキュリティおよび検出ルールを持つセキュリティ情報およびイベント管理 (SIEM) ソリューションによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="8b98c-116">All logs created by the different service teams are processed by a Security Information and Event Management (SIEM) solution with predefined security and detection rules.</span></span> <span data-ttu-id="8b98c-117">これらのルールは、以前のセキュリティ インシデントから学んだ情報に関するセキュリティ チームの推奨事項に基づいて進化し、疑わしいアクティビティや悪意のあるアクティビティが存在するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="8b98c-117">These rules evolve based on security team recommendations, on information learned from previous security incidents, to determine if there is any suspicious or malicious activity.</span></span>
- <span data-ttu-id="8b98c-118">お客様がセキュリティ インシデントが進行中と判断した場合、Microsoft でサポート ケースを開き、Microsoft コミュニケーション チームに割り当て、すべての適切なチームにエスカレーションを行う可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8b98c-118">If a customer determines that a security incident is underway, they may open a support case with Microsoft, which is assigned to the Microsoft communications team and turned into an escalation to all appropriate teams.</span></span>

<span data-ttu-id="8b98c-119">Azure、Dynamics 365、および Microsoft 365 サービス チームは、セキュリティ監視とログ記録を通じてトレンド分析で得たインテリジェンスを使用して、攻撃やセキュリティ インシデントを示す可能性のある Microsoft Online Services 情報システムの異常を検出します。</span><span class="sxs-lookup"><span data-stu-id="8b98c-119">Azure, Dynamics 365, and Microsoft 365 service teams also use the intelligence gained in trend analysis through security monitoring and logging to detect abnormalities in Microsoft online services information systems that might indicate an attack or a security incident.</span></span> <span data-ttu-id="8b98c-120">Microsoft Online Services システムは、実稼働環境のこれらのログからの出力を集中ログ サーバーに集約します。</span><span class="sxs-lookup"><span data-stu-id="8b98c-120">Microsoft online services systems aggregate output from these logs in the production environment into centralized logging servers.</span></span> <span data-ttu-id="8b98c-121">これらの集中ログ サーバーから、ログを調べて、実稼働環境全体の傾向を特定します。</span><span class="sxs-lookup"><span data-stu-id="8b98c-121">From these centralized logging servers, logs are examined to spot trends throughout the production environment.</span></span> <span data-ttu-id="8b98c-122">集中サーバーで集約されたデータは、高度なクエリ、ダッシュボードの構築、異常および悪意のあるアクティビティの検出を行うログ サービスに安全に送信されます。</span><span class="sxs-lookup"><span data-stu-id="8b98c-122">Data aggregated in the centralized servers are securely transmitted into a logging service for advanced querying, dashboard building and detecting anomalous and malicious activity.</span></span> <span data-ttu-id="8b98c-123">また、このサービスでは、機械学習を使用してログ出力を使用して異常を検出します。</span><span class="sxs-lookup"><span data-stu-id="8b98c-123">The service also uses machine learning to detect anomalies with log output.</span></span>

<span data-ttu-id="8b98c-124">エスカレーションフェーズ中、およびセキュリティ インシデントの性質によっては、セキュリティ対応チームが Microsoft のさまざまなチームから 1 つ以上の主題の専門家に従事する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8b98c-124">During the escalation phase and depending on the nature of the security incident, security response teams may engage one or more subject matter experts from various teams at Microsoft:</span></span>

- <span data-ttu-id="8b98c-125">Online Services セキュリティとコンプライアンス チーム</span><span class="sxs-lookup"><span data-stu-id="8b98c-125">Online Services Security and Compliance team</span></span>
- <span data-ttu-id="8b98c-126">Microsoft Threat Intelligence Center (MSTIC)</span><span class="sxs-lookup"><span data-stu-id="8b98c-126">Microsoft Threat Intelligence Center (MSTIC)</span></span>
- <span data-ttu-id="8b98c-127">Microsoft セキュリティ応答センター (MSRC)</span><span class="sxs-lookup"><span data-stu-id="8b98c-127">Microsoft Security Response Center (MSRC)</span></span>
- <span data-ttu-id="8b98c-128">企業、外部、法務 (CELA)</span><span class="sxs-lookup"><span data-stu-id="8b98c-128">Corporate, External, and Legal Affairs (CELA)</span></span>
- <span data-ttu-id="8b98c-129">Azure Security</span><span class="sxs-lookup"><span data-stu-id="8b98c-129">Azure Security</span></span>
- <span data-ttu-id="8b98c-130">Microsoft 365エンジニアリングなど。</span><span class="sxs-lookup"><span data-stu-id="8b98c-130">Microsoft 365 engineering, and others.</span></span>

<span data-ttu-id="8b98c-131">セキュリティ対応チームへのエスカレーションが発生する前に、サービス チームは、次のような定義された条件に基づいてセキュリティ インシデントの重大度レベルを決定および設定する責任があります。</span><span class="sxs-lookup"><span data-stu-id="8b98c-131">Before an escalation to any security response team occurs, the service team is responsible for determining and setting the severity level of the security incident based on defined criteria such as:</span></span>

- <span data-ttu-id="8b98c-132">プライバシー</span><span class="sxs-lookup"><span data-stu-id="8b98c-132">Privacy</span></span>
- <span data-ttu-id="8b98c-133">影響</span><span class="sxs-lookup"><span data-stu-id="8b98c-133">Impact</span></span>
- <span data-ttu-id="8b98c-134">範囲</span><span class="sxs-lookup"><span data-stu-id="8b98c-134">Scope</span></span>
- <span data-ttu-id="8b98c-135">影響を受けるテナントの数</span><span class="sxs-lookup"><span data-stu-id="8b98c-135">Number of affected tenants</span></span>
- <span data-ttu-id="8b98c-136">地域</span><span class="sxs-lookup"><span data-stu-id="8b98c-136">Region</span></span>
- <span data-ttu-id="8b98c-137">サービス</span><span class="sxs-lookup"><span data-stu-id="8b98c-137">Service</span></span>
- <span data-ttu-id="8b98c-138">インシデントの詳細</span><span class="sxs-lookup"><span data-stu-id="8b98c-138">Details of the incident</span></span>
- <span data-ttu-id="8b98c-139">特定の顧客業界または市場規制。</span><span class="sxs-lookup"><span data-stu-id="8b98c-139">Specific customer industry or market regulations.</span></span>

<span data-ttu-id="8b98c-140">インシデントの事前設定は、インシデントの機能への影響、インシデントの情報的影響、インシデントからの回復可能性など、個別の要因を使用して決定されます。</span><span class="sxs-lookup"><span data-stu-id="8b98c-140">Incident prioritization is determined by using distinct factors, including but not limited to the functional impact of the incident, the informational impact of the incident, and the recoverability from the incident.</span></span>

<span data-ttu-id="8b98c-141">セキュリティ インシデントに関するエスカレーションを受けた後、セキュリティ チームは、Microsoft Online Service セキュリティ対応チーム、サービス チーム、インシデントコミュニケーション チームのメンバーで構成される仮想チーム (v チーム) を編成します。</span><span class="sxs-lookup"><span data-stu-id="8b98c-141">After receiving an escalation about a security incident, the security team organizes a virtual team (v-team) comprised of members from the Microsoft online service security response team, service teams, and the incident communication team.</span></span> <span data-ttu-id="8b98c-142">その後、v チームはセキュリティ インシデントの正当性を確認し、誤検知を排除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b98c-142">The v-team must then confirm the legitimacy of the security incident and eliminate any false positives.</span></span> <span data-ttu-id="8b98c-143">準備フェーズ中に決定されたインジケーターによって提供される情報の精度は重要です。</span><span class="sxs-lookup"><span data-stu-id="8b98c-143">The accuracy of information provided by the indicators determined during the preparation phase is critical.</span></span> <span data-ttu-id="8b98c-144">この情報をベクトル攻撃のカテゴリ別に分析することで、v チームはセキュリティ インシデントが正当な懸念事項かどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="8b98c-144">By analyzing this information by category of vector attack, the v-team can determine if the security incident is a legitimate concern.</span></span>

<span data-ttu-id="8b98c-145">調査の開始時に、セキュリティ インシデント対応チームは、ケース管理ポリシーに従ってインシデントに関する情報を記録します。</span><span class="sxs-lookup"><span data-stu-id="8b98c-145">At the beginning of the investigation, the security incident response team records all information about the incident according to our case management policies.</span></span> <span data-ttu-id="8b98c-146">ケースが進むにつれて、継続的なアクションを追跡し、インシデント ライフサイクル全体にわたってこのデータを収集、保持、およびセキュリティ保護するための基準を処理する証拠に従います。</span><span class="sxs-lookup"><span data-stu-id="8b98c-146">As the case progresses, we track ongoing actions and follow evidence handling standards for gathering, retaining, and securing this data throughout the incident lifecycle.</span></span>

<span data-ttu-id="8b98c-147">これらのアクションの例には、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="8b98c-147">Some examples of these actions would include:</span></span>

- <span data-ttu-id="8b98c-148">概要(インシデントとその潜在的な影響の簡単な説明)</span><span class="sxs-lookup"><span data-stu-id="8b98c-148">A summary, which is a brief description of the incident and its potential impact</span></span>
- <span data-ttu-id="8b98c-149">インシデントの重大度と優先度 (潜在的な影響を評価して導き出される)</span><span class="sxs-lookup"><span data-stu-id="8b98c-149">The incident's severity and priority, which are derived by assessing the potential impact</span></span>
- <span data-ttu-id="8b98c-150">インシデントの検出につながった、識別されたすべてのインジケーターの一覧</span><span class="sxs-lookup"><span data-stu-id="8b98c-150">A list of all indicators identified which led to detection of the incident</span></span>
- <span data-ttu-id="8b98c-151">関連するインシデントの一覧</span><span class="sxs-lookup"><span data-stu-id="8b98c-151">A list of any related incidents</span></span>
- <span data-ttu-id="8b98c-152">v-team が実行したすべてのアクションの一覧</span><span class="sxs-lookup"><span data-stu-id="8b98c-152">A list of all actions taken by the v-team</span></span>
- <span data-ttu-id="8b98c-153">収集された証拠は、事後分析と将来の法医学調査のためにも保持されます</span><span class="sxs-lookup"><span data-stu-id="8b98c-153">Any gathered evidence, which will also be preserved for post-mortem analysis and future forensic investigations</span></span>
- <span data-ttu-id="8b98c-154">推奨される次のステップとアクション</span><span class="sxs-lookup"><span data-stu-id="8b98c-154">Recommended next steps and actions</span></span>

<span data-ttu-id="8b98c-155">セキュリティ インシデントの確認後、セキュリティ対応チームと適切なサービス チームの主な目標は、攻撃を含め、攻撃を受けるサービスを保護し、グローバルに大きな影響を及ぼすのを防くことです。</span><span class="sxs-lookup"><span data-stu-id="8b98c-155">After security incident confirmation, the primary goals of the security response team and the appropriate service team are to contain the attack, to protect the service(s) under attack, and to avoid a greater global impact.</span></span> <span data-ttu-id="8b98c-156">同時に、適切なエンジニアリング チームが根本的な原因を特定し、最初の復旧計画を準備します。</span><span class="sxs-lookup"><span data-stu-id="8b98c-156">At the same time, the appropriate engineering teams work to determine the root cause and to prepare the first recovery plan.</span></span>

<span data-ttu-id="8b98c-157">次のフェーズでは、セキュリティインシデントの影響を受けるお客様をセキュリティ対応チームが特定します (その場合)。</span><span class="sxs-lookup"><span data-stu-id="8b98c-157">In the next phase, the security response team identifies the customer(s) affected by the security incident, if any.</span></span> <span data-ttu-id="8b98c-158">有効範囲は、地域、データセンター、サービス、サーバー ファーム、サーバーなどによって決定に時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="8b98c-158">The scope of effect can take some time to determine, based on region, datacenter, service, server farm, server, and so forth.</span></span> <span data-ttu-id="8b98c-159">影響を受ける顧客の一覧は、サービス チームと対応する Microsoft コミュニケーション チームによってコンパイルされ、契約上およびコンプライアンス上の義務の範囲内で顧客通知プロセスを処理します。</span><span class="sxs-lookup"><span data-stu-id="8b98c-159">The list of affected customers is compiled by the service team and the corresponding Microsoft communications team, who then handle the customer notification process within contractual and compliance obligations.</span></span>

## <a name="related-articles"></a><span data-ttu-id="8b98c-160">関連記事</span><span class="sxs-lookup"><span data-stu-id="8b98c-160">Related articles</span></span>

- [<span data-ttu-id="8b98c-161">Microsoft セキュリティ インシデント管理</span><span class="sxs-lookup"><span data-stu-id="8b98c-161">Microsoft security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="8b98c-162">Microsoft セキュリティ インシデント管理: 準備</span><span class="sxs-lookup"><span data-stu-id="8b98c-162">Microsoft security incident management: Preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="8b98c-163">Microsoft セキュリティ インシデント管理: 格納、根絶、および回復</span><span class="sxs-lookup"><span data-stu-id="8b98c-163">Microsoft security incident management: Containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
- [<span data-ttu-id="8b98c-164">Microsoft セキュリティ インシデント管理: インシデント後のアクティビティ</span><span class="sxs-lookup"><span data-stu-id="8b98c-164">Microsoft security incident management: Post-incident activity</span></span>](assurance-sim-post-incident-activity.md)
- [<span data-ttu-id="8b98c-165">セキュリティ イベントのサポート チケットをログに記録する方法</span><span class="sxs-lookup"><span data-stu-id="8b98c-165">How to Log a Security Event Support Ticket</span></span>](/azure/security/fundamentals/event-support-ticket)
- [<span data-ttu-id="8b98c-166">GDRP の下での Azure および Dynamics 365 の侵害通知</span><span class="sxs-lookup"><span data-stu-id="8b98c-166">Azure and Dynamics 365 breach notification under the GDPR</span></span>](/compliance/regulatory/gdpr-breach-azure-dynamics)
