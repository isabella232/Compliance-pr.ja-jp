---
title: Microsoft 365 でのデータの回復性
description: この記事では、Microsoft 365 でのデータの復元と回復の設計と原則について説明します。
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
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 6e990facde47b07d50f594afb55353a5ef81dd78
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497623"
---
# <a name="data-resiliency-in-microsoft-365"></a><span data-ttu-id="4b4ae-103">Microsoft 365 でのデータの復元</span><span class="sxs-lookup"><span data-stu-id="4b4ae-103">Data resiliency in Microsoft 365</span></span>

<span data-ttu-id="4b4ae-104">クラウド コンピューティングの複雑な性質を考えると、Microsoft は問題が起きる場合ではなく、その場合に気を付けることができます。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-104">Given the complex nature of cloud computing, Microsoft is mindful that it's not a case of if things will go wrong, but rather when.</span></span> <span data-ttu-id="4b4ae-105">クラウド サービスを設計して、信頼性を最大限に高め、問題が発生した場合のお客様への悪影響を最小限に抑えています。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-105">We design our cloud services to maximize reliability and minimize the negative effects on customers when things do go wrong.</span></span> <span data-ttu-id="4b4ae-106">複雑な物理インフラストラクチャに依存する従来の戦略を超えて、クラウド サービスに冗長性を直接組み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-106">We have moved beyond the traditional strategy of relying on complex physical infrastructure, and we have built redundancy directly into our cloud services.</span></span> <span data-ttu-id="4b4ae-107">複雑度の低い物理インフラストラクチャとインテリジェントなソフトウェアを組み合わせて使用し、データの復元性をサービスに組み込み、お客様に高可用性を提供します。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-107">We use a combination of less complex physical infrastructure and more intelligent software that builds data resiliency into our services and delivers high availability to our customers.</span></span>

## <a name="resiliency-and-recoverability-are-built-in"></a><span data-ttu-id="4b4ae-108">復元性と回復性が組み込み</span><span class="sxs-lookup"><span data-stu-id="4b4ae-108">Resiliency and recoverability are built-in</span></span>

<span data-ttu-id="4b4ae-109">復元と回復の構築は、基盤となるインフラストラクチャとプロセスが何らかの時点で失敗するという前提から始まります。ハードウェア (インフラストラクチャ) が失敗し、人間が間違いを犯し、ソフトウェアにバグが発生します。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-109">Building in resiliency and recovery starts with the assumption that the underlying infrastructure and processes will fail at some point: hardware (infrastructure) will fail, humans will make mistakes, and software will have bugs.</span></span> <span data-ttu-id="4b4ae-110">ソフトウェア開発者がクラウドの前にこれらのことを考えていないと言うのは間違っていますが、これらの問題が一般的な IT 実装でどのように処理されるかは、クラウドの前で異なっていました。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-110">While it would be incorrect to say that software developers were not thinking about these things before the cloud, how these issues were handled in a typical IT implementation was different before the cloud:</span></span>

- <span data-ttu-id="4b4ae-111">まず、ハードウェアとインフラストラクチャの保護が重要でした。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-111">First, hardware and infrastructure protections were significant.</span></span> <span data-ttu-id="4b4ae-112">この構造は、99.99% の信頼性を持つデータセンターに大きな電力とネットワークの冗長性が必要であり、サーバーはハードウェア ベースのクラスタリング、デュアル電源、デュアル ネットワーク インターフェイスなどによって実装されました。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-112">This structure meant having datacenters with 99.99% reliability required significant power and network redundancy, and servers were implemented with hardware-based clustering, dual power supplies, dual network interfaces, and the like.</span></span>
- <span data-ttu-id="4b4ae-113">第 2 に、プロセスが最も重要でした。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-113">Second, process was paramount.</span></span> <span data-ttu-id="4b4ae-114">運用チームは厳格な手順を維持し、変更ウィンドウが採用され、多くの場合、プロジェクト管理のオーバーヘッドが大きかった。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-114">Operations teams maintained rigorous procedures, change windows were employed, and there was often significant project management overhead.</span></span>
- <span data-ttu-id="4b4ae-115">第 3 に、展開は氷河のペースで行いました。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-115">Third, deployment took place at a glacial pace.</span></span> <span data-ttu-id="4b4ae-116">ソースを所有せずにコードを展開すると、パッチリリースを待つことを意味し、メジャー バージョンのリリースにはハードウェアの交換と大幅な資本のアウトレイが含まれる。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-116">Deploying code without owning the source meant waiting for patch releases, and major version releases involved hardware replacement and significant capital outlay.</span></span> <span data-ttu-id="4b4ae-117">さらに、問題を修正する唯一の方法はロールバックでした。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-117">Moreover, the only way to correct a problem was to roll back.</span></span> <span data-ttu-id="4b4ae-118">したがって、ほとんどの IT 組織では、最新の状態を維持する作業を避けるため、メジャー リリースのみを展開します。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-118">Thus, most IT organizations would deploy only major releases to avoid the work to keep up to date.</span></span>
- <span data-ttu-id="4b4ae-119">最後に、展開されたシステムの規模とその相互接続のレベルは、従来よりずっと小さかった。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-119">Finally, the scale of deployed systems and the level of their interconnectedness was historically much smaller than it is now.</span></span>

<span data-ttu-id="4b4ae-120">今日、お客様は品質を損なうことなく Microsoft の継続的な技術革新を期待しています。これが、Microsoft のサービスとソフトウェアが回復性と回復性を念頭に置いて構築されている理由の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-120">Today, customers expect continuous innovation from Microsoft without compromising quality, and this is one of the reasons why Microsoft's services and software are built with resiliency and recoverability in mind.</span></span>

## <a name="microsoft-365-data-resiliency-principles"></a><span data-ttu-id="4b4ae-121">Microsoft 365 データ復元の原則</span><span class="sxs-lookup"><span data-stu-id="4b4ae-121">Microsoft 365 data resiliency principles</span></span>

<span data-ttu-id="4b4ae-122">復元とは、クラウド ベースのサービスが特定の種類の障害に耐え、お客様の観点から完全に機能し続け得る機能を指します。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-122">Resiliency refers to the ability of a cloud-based service to withstand certain types of failures and yet remain fully functional from the customers' perspective.</span></span> <span data-ttu-id="4b4ae-123">データの復元とは、Microsoft 365 内で発生したエラーに関係なく、重要な顧客データはそのままであり、影響を受けないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-123">Data resiliency means that no matter what failures occur within Microsoft 365, critical customer data remains intact and unaffected.</span></span> <span data-ttu-id="4b4ae-124">この目的のために、Microsoft 365 サービスは、次の 5 つの具体的な復元原則について設計されています。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-124">To that end, Microsoft 365 services have been designed around five specific resiliency principles:</span></span>

- <span data-ttu-id="4b4ae-125">重要なデータと重要でないデータがあります。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-125">There is critical and non-critical data.</span></span> <span data-ttu-id="4b4ae-126">重大でないデータ (メッセージが読み取ったかどうかなど) は、まれなエラー シナリオで削除できます。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-126">Non-critical data (for example, whether a message was read) can be dropped in rare failure scenarios.</span></span> <span data-ttu-id="4b4ae-127">重要なデータ (電子メール メッセージなどの顧客データなど) は、極端なコストで保護する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-127">Critical data (for example, customer data such as email messages) should be protected at extreme cost.</span></span> <span data-ttu-id="4b4ae-128">設計上の目標として、配信されたメール メッセージは常に重要であり、メッセージが読み取ったかどうかは重要ではない。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-128">As a design goal, delivered mail messages are always critical, and things like whether a message has been read is non-critical.</span></span>
- <span data-ttu-id="4b4ae-129">障害の分離を提供するには、顧客データのコピーを異なる障害領域または可能な限り多くの障害ドメイン (データセンターなど)に分け、単一の資格情報 (プロセス、サーバー、またはオペレーター) でアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-129">Copies of customer data must be separated into different fault zones or as many fault domains as possible (for example, datacenters, accessible by single credentials (process, server, or operator)) to provide failure isolation.</span></span> 
- <span data-ttu-id="4b4ae-130">重要な顧客データは、アトミック性、整合性、分離、耐久性 (ACID) の一部に障害が発生した場合に監視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-130">Critical customer data must be monitored for failing any part of Atomicity, Consistency, Isolation, Durability (ACID).</span></span>
- <span data-ttu-id="4b4ae-131">顧客データは破損から保護する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-131">Customer data must be protected from corruption.</span></span> <span data-ttu-id="4b4ae-132">アクティブにスキャンまたは監視され、修復可能で、回復可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-132">It must be actively scanned or monitored, repairable, and recoverable.</span></span>
- <span data-ttu-id="4b4ae-133">ほとんどのデータ損失は顧客のアクションから生じるので、誤って削除されたアイテムを復元できる GUI を使用して、ユーザーが自分で回復できます。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-133">Most data loss results from customer actions, so allow customers to recover on their own using a GUI that enables them to restore accidentally deleted items.</span></span>

<span data-ttu-id="4b4ae-134">Microsoft 365 は、これらの原則に対するクラウド サービスを構築し、堅牢なテストと検証と組み合わせて、継続的な技術革新と改善のためのプラットフォームを確保しながら、お客様の要件を満たし、超過することができます。</span><span class="sxs-lookup"><span data-stu-id="4b4ae-134">Through the building of our cloud services to these principles, coupled with robust testing and validation, Microsoft 365 is able to meet and exceed the requirements of customers while ensuring a platform for continuous innovation and improvement.</span></span>

## <a name="related-articles"></a><span data-ttu-id="4b4ae-135">関連記事</span><span class="sxs-lookup"><span data-stu-id="4b4ae-135">Related articles</span></span>

- [<span data-ttu-id="4b4ae-136">データの破損への対処</span><span class="sxs-lookup"><span data-stu-id="4b4ae-136">Dealing with Data Corruption</span></span>](assurance-dealing-with-data-corruption.md)
- [<span data-ttu-id="4b4ae-137">マルウェアと ランサムウェアからの保護</span><span class="sxs-lookup"><span data-stu-id="4b4ae-137">Malware and Ransomware Protection</span></span>](assurance-malware-and-ransomware-protection.md)
- [<span data-ttu-id="4b4ae-138">監視と自動修復</span><span class="sxs-lookup"><span data-stu-id="4b4ae-138">Monitoring and Self-Healing</span></span>](assurance-monitoring-and-self-healing.md)
- [<span data-ttu-id="4b4ae-139">Exchange データの復元</span><span class="sxs-lookup"><span data-stu-id="4b4ae-139">Exchange Data Resiliency</span></span>](assurance-exchange-data-resiliency.md)
