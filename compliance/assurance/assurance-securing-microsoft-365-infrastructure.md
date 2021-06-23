---
title: インフラストラクチャのセキュリティMicrosoft 365する
description: Microsoft がインフラストラクチャをセキュリティで保護するMicrosoft 365説明します。
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
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 224900bd60f2fd5637e7264f1aed98d5ff878b20
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089641"
---
# <a name="securing-the-microsoft-365-infrastructure"></a><span data-ttu-id="c56fe-103">インフラストラクチャのセキュリティMicrosoft 365する</span><span class="sxs-lookup"><span data-stu-id="c56fe-103">Securing the Microsoft 365 infrastructure</span></span>

<span data-ttu-id="c56fe-104">Microsoft 365は、世界最大のエンタープライズ およびコンシューマー クラウド サービスの 1 つであり、顧客ベース、製品、および機能の両方で急速に成長し続けています。</span><span class="sxs-lookup"><span data-stu-id="c56fe-104">Microsoft 365 is one of the largest enterprise and consumer cloud services in the world and continues to grow rapidly, both in customer base, products, and features.</span></span> <span data-ttu-id="c56fe-105">お客様はMicrosoft 365の生産性ソリューションだけでなく、絶えず進化し続けるサイバー脅威の状況から最も機密性の高い情報を保護します。</span><span class="sxs-lookup"><span data-stu-id="c56fe-105">Customers turn to Microsoft 365 not only for its world-class productivity solutions, but to help protect their most sensitive information from the constantly evolving cyber threat landscape.</span></span> <span data-ttu-id="c56fe-106">顧客データを安全に保ち、顧客の信頼を維持するのが Microsoft の最優先事項です。</span><span class="sxs-lookup"><span data-stu-id="c56fe-106">It is Microsoft's top priority to keep customer data secure and maintain customer trust.</span></span>

<span data-ttu-id="c56fe-107">セキュリティが後から考えられる場合は、この規模と複雑さのシステムをセキュリティで保護できないので、最初の設計プロセス中にセキュリティが統合されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="c56fe-107">Securing a system of this scale and complexity is not possible if security is an afterthought, it is only effective if security is integrated during the initial design process.</span></span> <span data-ttu-id="c56fe-108">自動化されたシステムと高度に熟練したエンジニアの両方からの迅速な応答を備えた堅牢な脅威検出システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="c56fe-108">It requires a robust threat detection system with prompt responses from both automated systems and highly skilled engineers.</span></span> <span data-ttu-id="c56fe-109">これらのシステムの継続的な評価と検証は、安全な構成を維持し、以前は不明な脆弱性を特定するために不可欠です。</span><span class="sxs-lookup"><span data-stu-id="c56fe-109">Continuous assessment and validation of these systems is essential to ensure secure configurations remain intact and previously unknown vulnerabilities are identified.</span></span>

## <a name="core-security-principles"></a><span data-ttu-id="c56fe-110">コア セキュリティの原則</span><span class="sxs-lookup"><span data-stu-id="c56fe-110">Core security principles</span></span>

<span data-ttu-id="c56fe-111">7 つのセキュリティ原則は、Microsoft 365 サービスを脅威から保護し、脅威を検出して対応し、それらの評価の結果に基づいてセキュリティ体制を継続的に評価し、サービスを改善するフレームワークの基盤を築いた。 </span><span class="sxs-lookup"><span data-stu-id="c56fe-111">Seven security principles lay the foundation for our framework of *protecting* the Microsoft 365 services from threats, *detecting and responding* to any threats, and continuously *assessing* the security posture and improving services based on the results of those assessments.</span></span>

- <span data-ttu-id="c56fe-112">**データのプライバシー**: お客様はデータを所有し、Microsoft は保管担当者です。</span><span class="sxs-lookup"><span data-stu-id="c56fe-112">**Data privacy**: Customers own their data and Microsoft is the custodian.</span></span> <span data-ttu-id="c56fe-113">Microsoft 365サービスは、顧客が明示的に要求および承認しない限り、エンジニアが顧客データにアクセスせずに動作するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="c56fe-113">Microsoft 365 services are designed to operate without engineers accessing customer data, unless explicitly requested and approved by the customer.</span></span>
- <span data-ttu-id="c56fe-114">**違反を想定** する: 人事とサービスは、侵害が本当の可能性である場合と同様に扱います。</span><span class="sxs-lookup"><span data-stu-id="c56fe-114">**Assume breach**: Personnel and services are treated as though compromise is a real possibility.</span></span>
- <span data-ttu-id="c56fe-115">**最小特権**: リソースへのアクセスとアクセス許可は、必要なタスクを実行するために必要なアクセス許可にのみ制限されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-115">**Least privilege**: Access and permissions to resources are limited to only what is necessary to perform needed tasks.</span></span>
- <span data-ttu-id="c56fe-116">**侵害の境界**: 1 つの境界内の ID とインフラストラクチャは、他の境界のリソースから分離されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-116">**Breach boundaries**: Identities and infrastructure in one boundary are isolated from resources in other boundaries.</span></span> <span data-ttu-id="c56fe-117">1 つの境界の侵害は、別の境界の侵害につながる必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c56fe-117">Compromise of one boundary should not lead to compromise of another.</span></span>
- <span data-ttu-id="c56fe-118">**サービス ファブリック統合セキュリティ**: セキュリティの優先順位と要件は、新しい機能の設計に組み込まれるので、強力なセキュリティの態勢が各サービスで拡張されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-118">**Service fabric integrated security**: Security priorities and requirements are built into the design of new features and capabilities, ensuring that a strong security posture scales with each service.</span></span>
- <span data-ttu-id="c56fe-119">**自動** および自動: Microsoft は、サービス セキュリティをインテリジェントかつ自動的に適用できる永続的な製品とアーキテクチャの開発に重点を当て、Microsoft エンジニアはセキュリティの脅威に対する対応を大規模に安全に管理できます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-119">**Automated and automatic**: Microsoft focuses on developing durable products and architectures that can intelligently and automatically enforce service security, while giving Microsoft engineers the ability to safely manage responses to security threats at scale.</span></span>
- <span data-ttu-id="c56fe-120">**アダプティブ セキュリティ**: Microsoft のセキュリティ機能は、機械学習モデル、定期的な侵入テスト、自動評価に適応し、強化されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-120">**Adaptive security**: Microsoft security capabilities adapt to and are enhanced by machine learning models, routine penetration testing, and automated assessments.</span></span>

## <a name="protection"></a><span data-ttu-id="c56fe-121">保護</span><span class="sxs-lookup"><span data-stu-id="c56fe-121">Protection</span></span>

### <a name="access-control"></a><span data-ttu-id="c56fe-122">アクセス制御</span><span class="sxs-lookup"><span data-stu-id="c56fe-122">Access control</span></span>

<span data-ttu-id="c56fe-123">既定では、サービス の開発と保守を担当Microsoft 365サービス インフラストラクチャへのゼロ スタンディング アクセス (ZSA) があります。</span><span class="sxs-lookup"><span data-stu-id="c56fe-123">By default, personnel responsible for developing and maintaining Microsoft 365 services have Zero Standing Access (ZSA) to the service infrastructure.</span></span> <span data-ttu-id="c56fe-124">Microsoft は最高のエンジニアのみを採用し、厳格なバックグラウンド チェックが必要ですが、Microsoft はオペレーティング サービスで既定で信頼されているという前提はありません。</span><span class="sxs-lookup"><span data-stu-id="c56fe-124">While Microsoft strives to hire only the best engineers and rigorous background checks are required, Microsoft does not assume that they are trusted by default in operating services.</span></span> <span data-ttu-id="c56fe-125">さらに、エンジニアが特権アクセスを承認されると、サービス インフラストラクチャの特定の範囲に必要なアクションのみを実行する限られた期間だけアクセス権が付与されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-125">Additionally, when engineers are approved for privileged access, they are only granted access for a limited duration to perform only the actions needed for a specific scope of the service infrastructure.</span></span> <span data-ttu-id="c56fe-126">Microsoft では、これらのポリシーを Just-in-Time (JIT) および Just-Enough-Access (JEA) と呼び、Lockbox と呼ばれるシステムを介して実装されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-126">Microsoft refers to these policies as Just-in-Time (JIT) and Just-Enough-Access (JEA) which are implemented through a system called Lockbox.</span></span>

<span data-ttu-id="c56fe-127">管理者特権を取得するために、Microsoft エンジニアは特定のタスクに対する要求を送信し、実行する時間枠を指定します。</span><span class="sxs-lookup"><span data-stu-id="c56fe-127">To acquire elevated privileges, Microsoft engineers submit a request for the specific task and specify the time frame to perform it.</span></span> <span data-ttu-id="c56fe-128">承認されると、Lockbox は、要求されたタスクのみを実行できる特殊な JIT アカウントを生成します。</span><span class="sxs-lookup"><span data-stu-id="c56fe-128">Once approved, Lockbox generates a specialized JIT account with the ability to perform only the requested task.</span></span> <span data-ttu-id="c56fe-129">アクションは通常、必要なトラブルシューティングまたは回復を安全に実行する自動化されたワークフローの形式をとっています。</span><span class="sxs-lookup"><span data-stu-id="c56fe-129">Actions usually take the form of automated workflows that securely perform any troubleshooting or recovery required.</span></span> <span data-ttu-id="c56fe-130">まれに、インフラストラクチャへの直接アクセスが必要な場合は、厳密に監視された特権アクセス ワークステーション (PAW) が必要です。</span><span class="sxs-lookup"><span data-stu-id="c56fe-130">In rare instances when direct access to the infrastructure is necessary, strictly monitored Privileged Access Workstations (PAWs) are required.</span></span>

<span data-ttu-id="c56fe-131">不正なユーザーや侵害されたアカウントは、どの組織でも本当に可能性が高く、アクセス制御システムは、これらの脅威から保護するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="c56fe-131">Rogue users and compromised accounts are a real possibility in any organization, and our access control system are designed to protect against these threats.</span></span>

<span data-ttu-id="c56fe-132">アクセス制御の詳細については、「Identity and [access management overview」を参照してください](assurance-identity-and-access-management.md)。</span><span class="sxs-lookup"><span data-stu-id="c56fe-132">For more information about access control, see [Identity and access management overview](assurance-identity-and-access-management.md).</span></span>

### <a name="encryption"></a><span data-ttu-id="c56fe-133">暗号化</span><span class="sxs-lookup"><span data-stu-id="c56fe-133">Encryption</span></span>

<span data-ttu-id="c56fe-134">アクセス制御は、Microsoft 365 サービスを保護する上で重要な役割を果たしますが、Microsoft のお客様の機密性とプライバシーをさらに保護するために、データ ライフサイクル全体で暗号化が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-134">While access controls provide a vital role in defending Microsoft 365 services, encryption is used throughout the data lifecycle to further protect confidentiality and privacy for Microsoft customers.</span></span>

<span data-ttu-id="c56fe-135">クライアント コンピューター、Microsoft 365 サーバー、およびサーバー以外のサーバー間Microsoft 365転送中のデータは、TLS 1.2 を使用して暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-135">Data in transit between client machines, Microsoft 365 servers, and non-Microsoft 365 servers is encrypted using TLS 1.2.</span></span> <span data-ttu-id="c56fe-136">使用している暗号とプロトコルを定期的に確認し、利用可能な場合はプロトコルを改善し、必要に応じて弱いプロトコルを削除します。</span><span class="sxs-lookup"><span data-stu-id="c56fe-136">We regularly review the ciphers and protocols in use, adding improved protocols when available and removing weaker ones as needed.</span></span>

<span data-ttu-id="c56fe-137">Microsoft サーバーで保存されている顧客コンテンツは、BitLocker を使用してボリューム レベルで暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-137">Customer content at rest on Microsoft servers is encrypted at the volume-level using BitLocker.</span></span> <span data-ttu-id="c56fe-138">アプリケーション レベルの暗号化は、Microsoft または顧客が管理するキーを使用して、さらに適用できます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-138">Application-level encryption can additionally be applied using keys managed by either Microsoft or the customer.</span></span> <span data-ttu-id="c56fe-139">Microsoft が管理するキーへのアクセスは、JIT および JEA プロセスを通じて承認および承認された場合にのみ可能です。</span><span class="sxs-lookup"><span data-stu-id="c56fe-139">Access to Microsoft-managed keys is only possible when authorized and approved through the JIT and JEA process.</span></span>

<span data-ttu-id="c56fe-140">暗号化の詳細については、「暗号化とキー Microsoft 365概要[」を参照してください](assurance-encryption.md)。</span><span class="sxs-lookup"><span data-stu-id="c56fe-140">For more information about encryption in Microsoft 365, see [Encryption and key management overview](assurance-encryption.md).</span></span>

### <a name="network-isolation"></a><span data-ttu-id="c56fe-141">ネットワークの分離</span><span class="sxs-lookup"><span data-stu-id="c56fe-141">Network isolation</span></span>

<span data-ttu-id="c56fe-142">最小特権の原則に従って、Microsoft 365インフラストラクチャの異なる部分間の通信を、運用に必要な情報にのみ制限します。</span><span class="sxs-lookup"><span data-stu-id="c56fe-142">In line with the principle of least privilege, Microsoft 365 restricts communication between different parts of the service infrastructure to only what is necessary to operate.</span></span> <span data-ttu-id="c56fe-143">既定では、すべてのネットワーク トラフィックが拒否され、明示的に定義された通信だけが許可されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-143">All network traffic is denied by default, with only explicitly defined communication being allowed.</span></span> <span data-ttu-id="c56fe-144">この制限により、インフラストラクチャ全体で侵害の境界が確立されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-144">This restriction establishes breach boundaries throughout the infrastructure.</span></span> <span data-ttu-id="c56fe-145">Teams機能をサービスに対応するために新しいネットワーク パスを追加する場合は、そのサービスを開く前に要求が評価され、承認されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c56fe-145">Teams that would like to add new network paths to accommodate a new feature to their service must have the request evaluated and approved before it can be opened.</span></span>

<span data-ttu-id="c56fe-146">ネットワーク分離の詳細については、「Microsoft 365分離[コントロールMicrosoft 365参照してください](/microsoft-365/enterprise/microsoft-365-isolation-controls)。</span><span class="sxs-lookup"><span data-stu-id="c56fe-146">For more information about network isolation in Microsoft 365, see [Microsoft 365 isolation controls](/microsoft-365/enterprise/microsoft-365-isolation-controls).</span></span>

## <a name="detection--response"></a><span data-ttu-id="c56fe-147">検出&応答</span><span class="sxs-lookup"><span data-stu-id="c56fe-147">Detection & Response</span></span>

### <a name="security-monitoring"></a><span data-ttu-id="c56fe-148">セキュリティ監視</span><span class="sxs-lookup"><span data-stu-id="c56fe-148">Security monitoring</span></span>

<span data-ttu-id="c56fe-149">Microsoft の大規模な規模でのセキュリティ監視は、自動化されたクラウドベースのソリューションを使用して非常に正確なアラートを生成することでのみ可能です。</span><span class="sxs-lookup"><span data-stu-id="c56fe-149">Security monitoring at Microsoft's massive scale is only possible by generating highly accurate alerts using automated cloud-based solutions.</span></span> <span data-ttu-id="c56fe-150">コア インフラストラクチャ全体から収集された各サービスとテレメトリ データの監査ログは、独自の集中リアルタイム処理およびアラート ソリューションに送信されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-150">Audit logs from each service and telemetry data gathered from throughout the core infrastructure is sent to a proprietary centralized near-real-time processing and alerting solution.</span></span>

<span data-ttu-id="c56fe-151">検出された脅威は、可能な場合は自動的にトリガーされるアクションを使用して修復されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-151">Detected threats are remediated using automatically triggered actions when possible.</span></span> <span data-ttu-id="c56fe-152">自動ソリューションが失敗したり、問題を解決できなかったりすると、オンコールの Microsoft エンジニアは直ちに脅威を軽減するためのアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c56fe-152">When automated solutions are unsuccessful or incapable of resolving the issue, on-call Microsoft engineers immediately take action to mitigate the threat.</span></span>

<span data-ttu-id="c56fe-153">セキュリティ監視の詳細については、「Microsoft 365の概要[」を参照してください](assurance-security-monitoring.md)。</span><span class="sxs-lookup"><span data-stu-id="c56fe-153">For more information about security monitoring in Microsoft 365, see [Security monitoring overview](assurance-security-monitoring.md).</span></span>

## <a name="assessment"></a><span data-ttu-id="c56fe-154">評価</span><span class="sxs-lookup"><span data-stu-id="c56fe-154">Assessment</span></span>

### <a name="automated-assessments"></a><span data-ttu-id="c56fe-155">自動評価</span><span class="sxs-lookup"><span data-stu-id="c56fe-155">Automated assessments</span></span>

<span data-ttu-id="c56fe-156">システムの設計方法に関係なく、意図的で意図しない構成ドリフトが原因で、セキュリティ体制が低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c56fe-156">Regardless of how a system is designed, the security posture can degrade due to intentional and unintentional configuration drift over time.</span></span> <span data-ttu-id="c56fe-157">自動ツールは、未パッチMicrosoft 365構成されていないサービスを検索するシステムを常に評価します。</span><span class="sxs-lookup"><span data-stu-id="c56fe-157">Automated tools constantly assess Microsoft 365 systems that look for unpatched and misconfigured services.</span></span> <span data-ttu-id="c56fe-158">この評価は、多くの場合、パッチ適用、ウイルス対策、脆弱性、および構成スキャン (PAVC) と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-158">This assessment is often referred to as patching, anti-virus, vulnerability, and configuration scanning (PAVC).</span></span>

<span data-ttu-id="c56fe-159">また、このアーキテクチャは頻繁に検証され、未使用のオープン ポートや、永続的な管理アクセス権を持つアカウントなどのインスタンスを識別します。</span><span class="sxs-lookup"><span data-stu-id="c56fe-159">Our architecture is also frequently validated, identifying instances such as unused open ports and accounts with standing administrative access.</span></span> <span data-ttu-id="c56fe-160">定義済みの目的の状態から離れたサービスは、自動的に配置に戻されます。</span><span class="sxs-lookup"><span data-stu-id="c56fe-160">Any services that drift from a pre-defined desired state are automatically brought back into alignment.</span></span>

<span data-ttu-id="c56fe-161">セキュリティ監視の詳細については、「脆弱性管理Microsoft 365概要[」を参照してください](assurance-vulnerability-management.md)。</span><span class="sxs-lookup"><span data-stu-id="c56fe-161">For more information about security monitoring in Microsoft 365, see [Vulnerability management overview](assurance-vulnerability-management.md).</span></span>

### <a name="attack-simulation-and-penetration-testing"></a><span data-ttu-id="c56fe-162">攻撃シミュレーションと侵入テスト</span><span class="sxs-lookup"><span data-stu-id="c56fe-162">Attack simulation and penetration testing</span></span>

<span data-ttu-id="c56fe-163">Microsoft 365の最優先事項は、攻撃による防御の侵入を防ぐことです。</span><span class="sxs-lookup"><span data-stu-id="c56fe-163">Microsoft 365's top priority is to prevent attacks from infiltrating defenses.</span></span> <span data-ttu-id="c56fe-164">Microsoft 365には、これまで知られていない脆弱性を特定し、セキュリティ監視機能を向上させるために一定の豊富なデータストリームを提供するために、常にシミュレートされた攻撃を実行しているセキュリティ専門家の専用チームがあります。</span><span class="sxs-lookup"><span data-stu-id="c56fe-164">Microsoft 365 has a dedicated team of security experts who are constantly conducting simulated attacks to identify previously unknown vulnerabilities and to provide a constant stream of rich data to improve security monitoring capabilities.</span></span> <span data-ttu-id="c56fe-165">これらのシミュレートされた攻撃は、頻繁に自動化された小規模攻撃と専門家による深い潜水の形をとっています。</span><span class="sxs-lookup"><span data-stu-id="c56fe-165">These simulated attacks take the form of frequent automated small-scale attacks and expert-driven deep dives.</span></span> <span data-ttu-id="c56fe-166">これらのアクティビティから、Microsoft は攻撃者を検出、応答、および削除する機能を評価します。</span><span class="sxs-lookup"><span data-stu-id="c56fe-166">From these activities, Microsoft evaluates the ability to detect, respond, and evict attackers.</span></span>

<span data-ttu-id="c56fe-167">セキュリティ監視の詳細については、「Microsoft 365 の攻撃シミュレーション」[を参照Microsoft 365。](assurance-monitoring-and-testing.md)</span><span class="sxs-lookup"><span data-stu-id="c56fe-167">For more information about security monitoring in Microsoft 365, see [Attack simulation in Microsoft 365](assurance-monitoring-and-testing.md).</span></span>

## <a name="resources"></a><span data-ttu-id="c56fe-168">リソース</span><span class="sxs-lookup"><span data-stu-id="c56fe-168">Resources</span></span>

[<span data-ttu-id="c56fe-169">Behind the Scenes: Securing the Infrastructure Powering the Microsoft 365 Service (舞台裏: Microsoft 365 サービスを支えるインフラストラクチャの保護)</span><span class="sxs-lookup"><span data-stu-id="c56fe-169">Behind the Scenes: Securing the Infrastructure Powering the Microsoft 365 Service</span></span>](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
