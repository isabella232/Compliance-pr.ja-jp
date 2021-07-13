---
title: 'Microsoft セキュリティ インシデント管理: インシデント後のアクティビティ'
description: この記事では、Microsoft オンライン サービスのセキュリティ インシデント管理インシデント後のアクティビティ プロセスの概要について説明します。
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
ms.openlocfilehash: 965c7d6d0d469b9eea981252805bda598c92a4c8
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377534"
---
# <a name="microsoft-security-incident-management-post-incident-activity"></a><span data-ttu-id="c2e29-103">Microsoft セキュリティ インシデント管理: インシデント後のアクティビティ</span><span class="sxs-lookup"><span data-stu-id="c2e29-103">Microsoft security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="c2e29-104">事後分析</span><span class="sxs-lookup"><span data-stu-id="c2e29-104">Postmortem</span></span>

<span data-ttu-id="c2e29-105">一部のセキュリティ インシデント、特に顧客に影響を与えるインシデント、またはデータ漏洩の可能性があるインシデントは、完全なインシデントの事後分析の対象となります。</span><span class="sxs-lookup"><span data-stu-id="c2e29-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="c2e29-106">セキュリティ対応チームは、セキュリティ インシデント対応に関わるすべての関係者と詳細な事後分析を行います。</span><span class="sxs-lookup"><span data-stu-id="c2e29-106">The security response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="c2e29-107">インシデントの原因となる一連のイベントを文書化します。</span><span class="sxs-lookup"><span data-stu-id="c2e29-107">Document the sequence of events that caused the incident.</span></span>
- <span data-ttu-id="c2e29-108">侵害に関与するアクター (既知の場合) を含む証拠によってサポートされているインシデントの技術的な概要を作成します。</span><span class="sxs-lookup"><span data-stu-id="c2e29-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="c2e29-109">この概要には、応答の実行方法と他の主要なテイクアウトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c2e29-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="c2e29-110">技術的な経過、手続き上の失敗、手動エラー、プロセスの欠陥、通信の不具合、および/またはセキュリティ インシデント対応中に特定された未知の攻撃ベクトルを特定します。</span><span class="sxs-lookup"><span data-stu-id="c2e29-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="c2e29-111">事後分析は、Microsoft オンライン サービスのエンジニアリング開発サイクルで新しい優先順位を設定することで、Microsoft オンライン サービスの改善、運用プロセス、およびドキュメントに直接影響します。</span><span class="sxs-lookup"><span data-stu-id="c2e29-111">The postmortem will directly influence Microsoft online service improvement, operational processes, and documentation by setting new priorities in the Microsoft online services engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="c2e29-112">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="c2e29-112">Documentation</span></span>

<span data-ttu-id="c2e29-113">死後のプロセスにおける主要な技術的な調査結果はすべて、バグや開発変更要求の形でレポートとサービスへの投資または修正に取り込まれています。</span><span class="sxs-lookup"><span data-stu-id="c2e29-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="c2e29-114">これらの結果は、適切なエンジニアリング チームとフォローアップされます。</span><span class="sxs-lookup"><span data-stu-id="c2e29-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="c2e29-115">プロセスの失敗や組織間の問題については、セキュリティ対応チームのデータベースに問題が文書化され、それに対処する適切なグループがフォローアップされます。</span><span class="sxs-lookup"><span data-stu-id="c2e29-115">For process failures and cross-organizational issues, issues are documented in the security response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="c2e29-116">プロセスの改善</span><span class="sxs-lookup"><span data-stu-id="c2e29-116">Process improvement</span></span>

<span data-ttu-id="c2e29-117">Microsoft オンライン サービスのセキュリティ インシデントに対応するには、Microsoft 内の異なる組織に分散する複数のグループとの連携や、法執行機関などの適切な外部組織との連携が必要です。</span><span class="sxs-lookup"><span data-stu-id="c2e29-117">Responding to a security incident in Microsoft online services involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="c2e29-118">十分性と完全性の両方について、セキュリティ インシデントが発生した後の対応を評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2e29-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="c2e29-119">特定された改善や変更については、セキュリティ対応チームが適切なチームや関係者と協議して提案を評価し、適切な場合は標準の運用手順に組み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2e29-119">For any identified improvements or changes, the security response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="c2e29-120">セキュリティ インシデント対応または死後のアクティビティ中に特定された必要な変更、バグ、またはサービスの改善はすべて、内部の Microsoft エンジニアリング データベースに記録および追跡されます。</span><span class="sxs-lookup"><span data-stu-id="c2e29-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft engineering database.</span></span> <span data-ttu-id="c2e29-121">潜在的なバグや機能はすべて、適切な所有者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c2e29-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="c2e29-122">Microsoft セキュリティ対応チームは、問題が解決されるまで、すべてのエントリを確認します。</span><span class="sxs-lookup"><span data-stu-id="c2e29-122">The Microsoft security response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="c2e29-123">関連記事</span><span class="sxs-lookup"><span data-stu-id="c2e29-123">Related articles</span></span>

- [<span data-ttu-id="c2e29-124">Microsoft セキュリティ インシデント管理</span><span class="sxs-lookup"><span data-stu-id="c2e29-124">Microsoft security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="c2e29-125">Microsoft セキュリティ インシデント管理: 準備</span><span class="sxs-lookup"><span data-stu-id="c2e29-125">Microsoft security incident management: Preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="c2e29-126">Microsoft セキュリティ インシデント管理: 検出と分析</span><span class="sxs-lookup"><span data-stu-id="c2e29-126">Microsoft security incident management: Detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="c2e29-127">Microsoft セキュリティ インシデント管理: 格納、根絶、および回復</span><span class="sxs-lookup"><span data-stu-id="c2e29-127">Microsoft security incident management: Containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
- [<span data-ttu-id="c2e29-128">セキュリティ イベントのサポート チケットをログに記録する方法</span><span class="sxs-lookup"><span data-stu-id="c2e29-128">How to Log a Security Event Support Ticket</span></span>](/azure/security/fundamentals/event-support-ticket)
- [<span data-ttu-id="c2e29-129">GDRP の下での Azure および Dynamics 365 の侵害通知</span><span class="sxs-lookup"><span data-stu-id="c2e29-129">Azure and Dynamics 365 breach notification under the GDPR</span></span>](/compliance/regulatory/gdpr-breach-azure-dynamics)
