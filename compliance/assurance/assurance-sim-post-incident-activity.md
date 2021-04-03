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
hideEdit: true
ms.openlocfilehash: 4ebd31c16f8abb3eddd6ed924a045d88597aba40
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496712"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a><span data-ttu-id="02eba-103">Microsoft 365 セキュリティ インシデント管理: インシデント後のアクティビティ</span><span class="sxs-lookup"><span data-stu-id="02eba-103">Microsoft 365 security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="02eba-104">事後分析</span><span class="sxs-lookup"><span data-stu-id="02eba-104">Postmortem</span></span>

<span data-ttu-id="02eba-105">一部のセキュリティ インシデント、特に顧客に影響を与えるインシデント、またはデータ漏洩の可能性があるインシデントは、完全なインシデントの事後分析の対象となります。</span><span class="sxs-lookup"><span data-stu-id="02eba-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="02eba-106">Microsoft 365 セキュリティ対応チームは、セキュリティ インシデント対応に関わるすべての関係者と詳細な事後分析を行います。</span><span class="sxs-lookup"><span data-stu-id="02eba-106">The Microsoft 365 Security Response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="02eba-107">インシデントの原因となる一連のイベントを文書化する</span><span class="sxs-lookup"><span data-stu-id="02eba-107">Document the sequence of events that caused the incident</span></span>
- <span data-ttu-id="02eba-108">侵害に関与するアクター (既知の場合) を含む証拠によってサポートされているインシデントの技術的な概要を作成します。</span><span class="sxs-lookup"><span data-stu-id="02eba-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="02eba-109">この概要には、応答の実行方法と他の主要なテイクアウトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="02eba-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="02eba-110">技術的な経過、手続き上の失敗、手動エラー、プロセスの欠陥、通信の不具合、および/またはセキュリティ インシデント対応中に特定された未知の攻撃ベクトルを特定します。</span><span class="sxs-lookup"><span data-stu-id="02eba-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="02eba-111">事後分析は、Microsoft 365 エンジニアリング開発サイクルで新しい優先順位を設定することで、Microsoft 365 サービスの改善、運用プロセス、およびドキュメントに直接影響します。</span><span class="sxs-lookup"><span data-stu-id="02eba-111">The postmortem will directly influence Microsoft 365 service improvement, operational processes, and documentation by setting new priorities in the Microsoft 365 engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="02eba-112">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="02eba-112">Documentation</span></span>

<span data-ttu-id="02eba-113">死後のプロセスにおける主要な技術的な調査結果はすべて、バグや開発変更要求の形でレポートとサービスへの投資または修正に取り込まれています。</span><span class="sxs-lookup"><span data-stu-id="02eba-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="02eba-114">これらの結果は、適切なエンジニアリング チームとフォローアップされます。</span><span class="sxs-lookup"><span data-stu-id="02eba-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="02eba-115">プロセスの失敗や組織間の問題については、Microsoft 365 セキュリティ対応チームのデータベースに問題が文書化され、それに対処するために適切なグループがフォローアップされます。</span><span class="sxs-lookup"><span data-stu-id="02eba-115">For process failures and cross-organizational issues, issues are documented in the Microsoft 365 Security Response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="02eba-116">プロセスの改善</span><span class="sxs-lookup"><span data-stu-id="02eba-116">Process improvement</span></span>

<span data-ttu-id="02eba-117">Microsoft 365 のセキュリティ インシデントに対応するには、Microsoft 内の異なる組織、および法執行機関などの適切な外部組織にまたがって複数のグループとの連携が必要です。</span><span class="sxs-lookup"><span data-stu-id="02eba-117">Responding to a security incident in Microsoft 365 involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="02eba-118">十分性と完全性の両方について、セキュリティ インシデントが発生した後の対応を評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02eba-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="02eba-119">特定された改善や変更に関して、Microsoft 365 セキュリティ対応チームは、適切なチームや関係者と協議して提案を評価し、適切な場合は標準の運用手順に組み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="02eba-119">For any identified improvements or changes, the Microsoft 365 Security Response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="02eba-120">セキュリティ インシデント対応または死後のアクティビティ中に特定された必要な変更、バグ、またはサービスの改善はすべて、内部の Microsoft 365 エンジニアリング データベースに記録および追跡されます。</span><span class="sxs-lookup"><span data-stu-id="02eba-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft 365 engineering database.</span></span> <span data-ttu-id="02eba-121">潜在的なバグや機能はすべて、適切な所有者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="02eba-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="02eba-122">Microsoft 365 セキュリティ対応チームは、問題が解決されるまですべてのエントリを確認します。</span><span class="sxs-lookup"><span data-stu-id="02eba-122">The Microsoft 365 Security Response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="02eba-123">関連記事</span><span class="sxs-lookup"><span data-stu-id="02eba-123">Related articles</span></span>

- [<span data-ttu-id="02eba-124">Microsoft 365 のセキュリティ インシデント管理</span><span class="sxs-lookup"><span data-stu-id="02eba-124">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="02eba-125">Microsoft 365 セキュリティ インシデント管理の準備</span><span class="sxs-lookup"><span data-stu-id="02eba-125">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="02eba-126">Microsoft 365 セキュリティ インシデント管理の検出と分析</span><span class="sxs-lookup"><span data-stu-id="02eba-126">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="02eba-127">Microsoft 365 セキュリティ インシデント管理の格納、根絶、および回復</span><span class="sxs-lookup"><span data-stu-id="02eba-127">Microsoft 365 security incident management containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
