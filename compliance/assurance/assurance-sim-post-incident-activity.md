---
title: 'Microsoft 365 セキュリティ インシデント管理: インシデント後のアクティビティ'
description: この記事では、Microsoft 365 のセキュリティ インシデント管理インシデント後のアクティビティ プロセスの概要について説明します。
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
ms.openlocfilehash: 66c25503ac574de512f5201981112a0e54714968
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040350"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a><span data-ttu-id="c7da3-103">Microsoft 365 セキュリティ インシデント管理: インシデント後のアクティビティ</span><span class="sxs-lookup"><span data-stu-id="c7da3-103">Microsoft 365 security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="c7da3-104">Postmortem</span><span class="sxs-lookup"><span data-stu-id="c7da3-104">Postmortem</span></span>

<span data-ttu-id="c7da3-105">セキュリティ インシデントの中には、特にお客様が影響を与えるインシデントやデータ侵害を引き起しているインシデントの中には、インシデントの完全な事後分析の対象となるものがあります。</span><span class="sxs-lookup"><span data-stu-id="c7da3-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="c7da3-106">Microsoft 365 セキュリティ対応チームは、セキュリティ インシデント対応に関わるすべての関係者と詳細な事後分析を行い、次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="c7da3-106">The Microsoft 365 Security Response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="c7da3-107">インシデントを発生した一連のイベントを文書化する</span><span class="sxs-lookup"><span data-stu-id="c7da3-107">Document the sequence of events that caused the incident</span></span>
- <span data-ttu-id="c7da3-108">違反に関与するアクターを含む証拠によってサポートされているインシデントの技術的な概要を作成します (既知の場合)。</span><span class="sxs-lookup"><span data-stu-id="c7da3-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="c7da3-109">この概要には、応答の実行方法と他の重要な項目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c7da3-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="c7da3-110">技術的な経過、手順の失敗、手動エラー、プロセスの欠陥、通信障害、セキュリティ インシデント対応中に特定された未知の攻撃ベクトルを特定します。</span><span class="sxs-lookup"><span data-stu-id="c7da3-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="c7da3-111">事後分析は、Microsoft 365 エンジニアリング開発サイクルで新しい優先順位を設定することで、Microsoft 365 サービスの改善、運用プロセス、およびドキュメントに直接影響します。</span><span class="sxs-lookup"><span data-stu-id="c7da3-111">The postmortem will directly influence Microsoft 365 service improvement, operational processes, and documentation by setting new priorities in the Microsoft 365 engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="c7da3-112">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="c7da3-112">Documentation</span></span>

<span data-ttu-id="c7da3-113">事後分析プロセスにおける主要な技術的な調査結果はすべて、バグや開発変更要求の形でレポートとサービスへの投資または修正に取り込まれています。</span><span class="sxs-lookup"><span data-stu-id="c7da3-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="c7da3-114">これらの結果は、適切なエンジニアリング チームとフォローアップされます。</span><span class="sxs-lookup"><span data-stu-id="c7da3-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="c7da3-115">プロセスの失敗と組織間の問題については、Microsoft 365 セキュリティ対応チームのデータベースに問題を文書化し、対応する適切なグループをフォローアップします。</span><span class="sxs-lookup"><span data-stu-id="c7da3-115">For process failures and cross-organizational issues, issues are documented in the Microsoft 365 Security Response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="c7da3-116">プロセスの改善</span><span class="sxs-lookup"><span data-stu-id="c7da3-116">Process improvement</span></span>

<span data-ttu-id="c7da3-117">Microsoft 365 のセキュリティ インシデントへの対応には、Microsoft 内の異なる組織に分散している複数のグループとの連携や、法執行機関などの適切な外部組織との連携が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c7da3-117">Responding to a security incident in Microsoft 365 involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="c7da3-118">十分性と完全性の両方について、セキュリティ インシデントが発生した後の対応を評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7da3-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="c7da3-119">特定された改善や変更に関して、Microsoft 365 セキュリティ対応チームは提案を適切なチームや関係者と相談して評価し、適切な場合は標準業務手順に組み込めます。</span><span class="sxs-lookup"><span data-stu-id="c7da3-119">For any identified improvements or changes, the Microsoft 365 Security Response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="c7da3-120">セキュリティ インシデント対応または事後活動中に特定された必要な変更、バグ、またはサービスの改善はすべて、内部の Microsoft 365 エンジニアリング データベースに記録および追跡されます。</span><span class="sxs-lookup"><span data-stu-id="c7da3-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft 365 engineering database.</span></span> <span data-ttu-id="c7da3-121">潜在的なバグや機能はすべて、適切な所有者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c7da3-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="c7da3-122">Microsoft 365 セキュリティ対応チームは、問題が解決されるまですべてのエントリを確認します。</span><span class="sxs-lookup"><span data-stu-id="c7da3-122">The Microsoft 365 Security Response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="c7da3-123">関連記事</span><span class="sxs-lookup"><span data-stu-id="c7da3-123">Related articles</span></span>

- [<span data-ttu-id="c7da3-124">Microsoft 365 セキュリティ インシデント管理</span><span class="sxs-lookup"><span data-stu-id="c7da3-124">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="c7da3-125">Microsoft 365 セキュリティ インシデント管理の準備</span><span class="sxs-lookup"><span data-stu-id="c7da3-125">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="c7da3-126">Microsoft 365 セキュリティ インシデント管理の検出と分析</span><span class="sxs-lookup"><span data-stu-id="c7da3-126">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="c7da3-127">Microsoft 365 セキュリティ インシデント管理の格納、強化、および復旧</span><span class="sxs-lookup"><span data-stu-id="c7da3-127">Microsoft 365 security incident management containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
