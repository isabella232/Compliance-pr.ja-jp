---
title: Microsoft 365 データの破損に対処する
description: この記事では、Microsoft 365 のデータ破損と、データの防止と回復に対する Microsoft の取り組みについて説明します。
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
ms.openlocfilehash: 9e9f0951f7e349cc70bc96bb6a2d62275848cf04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497589"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a><span data-ttu-id="095dd-103">Microsoft 365 でのデータ破損の処理</span><span class="sxs-lookup"><span data-stu-id="095dd-103">Dealing with data corruption in Microsoft 365</span></span>

<span data-ttu-id="095dd-104">大規模なクラウド サービスを実行する難しい側面の 1 つは、大量のデータと独立したシステムを考えると、データの破損を処理する方法です。</span><span class="sxs-lookup"><span data-stu-id="095dd-104">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems.</span></span> <span data-ttu-id="095dd-105">データの破損は、次の原因で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="095dd-105">Data corruption can be caused by:</span></span>

- <span data-ttu-id="095dd-106">アプリケーションまたはインフラストラクチャのバグ、アプリケーションの状態の一部またはすべてが壊れている</span><span class="sxs-lookup"><span data-stu-id="095dd-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span>
- <span data-ttu-id="095dd-107">データの紛失やデータの読み取りが行えなくなっているハードウェアの問題</span><span class="sxs-lookup"><span data-stu-id="095dd-107">Hardware issues that result in lost data or an inability to read data</span></span>
- <span data-ttu-id="095dd-108">人的操作上のエラー</span><span class="sxs-lookup"><span data-stu-id="095dd-108">Human operational errors</span></span>
- <span data-ttu-id="095dd-109">悪意のあるハッカーと不満を持つ従業員</span><span class="sxs-lookup"><span data-stu-id="095dd-109">Malicious hackers and disgruntled employees</span></span>
- <span data-ttu-id="095dd-110">データが失われる外部サービスのインシデント</span><span class="sxs-lookup"><span data-stu-id="095dd-110">Incidents in external services that result in some loss of data</span></span>

<span data-ttu-id="095dd-111">データの整合性に対する復元性が高いということは、データ破損インシデントが少なくなっていることを意味します。Microsoft は、破損の発生を防ぐための Microsoft 365 保護メカニズムと、破損が発生した場合にデータを回復できるシステムとプロセスを組み込み込み、</span><span class="sxs-lookup"><span data-stu-id="095dd-111">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Microsoft 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does.</span></span> <span data-ttu-id="095dd-112">データの破損に対する復元性を高めるエンジニアリング リリース プロセスのさまざまな段階にチェックとプロセスが存在します。</span><span class="sxs-lookup"><span data-stu-id="095dd-112">Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>

- <span data-ttu-id="095dd-113">システム設計</span><span class="sxs-lookup"><span data-stu-id="095dd-113">System Design</span></span>
- <span data-ttu-id="095dd-114">コードの編成と構造</span><span class="sxs-lookup"><span data-stu-id="095dd-114">Code organization and structure</span></span>
- <span data-ttu-id="095dd-115">コード レビュー</span><span class="sxs-lookup"><span data-stu-id="095dd-115">Code review</span></span>
- <span data-ttu-id="095dd-116">単体テスト、統合テスト、およびシステム テスト</span><span class="sxs-lookup"><span data-stu-id="095dd-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="095dd-117">トリップ ワイヤーのテスト/ゲート</span><span class="sxs-lookup"><span data-stu-id="095dd-117">Trip wires tests/gates</span></span>

<span data-ttu-id="095dd-118">Microsoft 365 の実稼働環境では、データセンター間のピア レプリケーションによって、データのライブ コピーが常に複数存在します。</span><span class="sxs-lookup"><span data-stu-id="095dd-118">Within Microsoft 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data.</span></span> <span data-ttu-id="095dd-119">標準のイメージとスクリプトを使用して、失われたサーバーを回復し、レプリケートされたデータを使用して顧客データを復元します。</span><span class="sxs-lookup"><span data-stu-id="095dd-119">Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data.</span></span> <span data-ttu-id="095dd-120">組み込みのデータ復元チェックとプロセスにより、Microsoft は、SharePoint Online の組み込みレプリケーションと内部コード リポジトリ ツール Source Depot を使用して、Microsoft 365 情報システムのドキュメント (セキュリティ関連のドキュメントを含む) のバックアップのみを保持します。</span><span class="sxs-lookup"><span data-stu-id="095dd-120">Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Microsoft 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot.</span></span> <span data-ttu-id="095dd-121">システムドキュメントは SharePoint Online に保存され、Source Depot にはシステムイメージとアプリケーション イメージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="095dd-121">System documentation is stored in SharePoint Online, and Source Depot contains system and application images.</span></span> <span data-ttu-id="095dd-122">SharePoint Online と Source Depot の両方がバージョン管理を使用し、ほぼリアルタイムでレプリケートされます。</span><span class="sxs-lookup"><span data-stu-id="095dd-122">Both SharePoint Online and Source Depot use versioning and are replicated in near real time.</span></span>
