---
title: Microsoft 365エンジニアリングの内部ログMicrosoft 365する
description: この記事では、エンジニアリング チームの内部ログMicrosoft 365説明します。
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
ms.openlocfilehash: 71b08509ae920ad88ecfa1566b9a11d640b0534f
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088596"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a><span data-ttu-id="4b160-103">Microsoft 365 のエンジニアリングのための内部ログ記録</span><span class="sxs-lookup"><span data-stu-id="4b160-103">Internal logging for Microsoft 365 engineering</span></span>

<span data-ttu-id="4b160-104">Microsoft は、お客様が利用できるイベントとログ データに加えて、ユーザーが使用できる内部ログ データ収集システムMicrosoft 365しています。</span><span class="sxs-lookup"><span data-stu-id="4b160-104">In addition to the events and log data available for customers, Microsoft maintains an internal log data collection system that is available to Microsoft 365 engineers.</span></span> <span data-ttu-id="4b160-105">Microsoft 365 サーバーから、ほぼリアルタイム (NRT) 分析用の独自のセキュリティ監視ソリューション、および長期ストレージ用の内部のビッグ データ コンピューティング サービス (Cosmos) に、さまざまな種類のログ データがアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="4b160-105">Many different types of log data are uploaded from Microsoft 365 servers to a proprietary security monitoring solution for near real-time (NRT) analysis and an internal, big data computing service (Cosmos) for long-term storage.</span></span> <span data-ttu-id="4b160-106">このデータ転送は、Office データ ローダー (ODL) と呼ばれる独自のオートメーション ツールを使用して、承認済みポートおよびプロトコル上の FIPS 140-2 検証済み TLS 接続を使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="4b160-106">This data transfer occurs over a FIPS 140-2-validated TLS connection on approved ports and protocols using a proprietary automation tool called the Office Data Loader (ODL).</span></span> <span data-ttu-id="4b160-107">監査レコードを収集Microsoft 365処理するために使用されるツールでは、元の監査レコードのコンテンツや時間の順序に対する永続的または不可逆的な変更は許可されません。</span><span class="sxs-lookup"><span data-stu-id="4b160-107">The tools used in Microsoft 365 to collect and process audit records do not allow permanent or irreversible changes to the original audit record content or time ordering.</span></span>

<span data-ttu-id="4b160-108">サービス チームは、Cosmos を集中リポジトリとして使用して、アプリケーションの使用状況の分析、システムと運用パフォーマンスの測定、および問題やセキュリティの問題を示す可能性のある異常やパターンを探します。</span><span class="sxs-lookup"><span data-stu-id="4b160-108">Service teams use Cosmos as a centralized repository to conduct an analysis of application usage, to measure system and operational performance, and to look for abnormalities and patterns that may indicate problems or security issues.</span></span> <span data-ttu-id="4b160-109">各サービス チームは、以下を含むベースラインをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="4b160-109">Each service team uploads a baseline that includes:</span></span>

- <span data-ttu-id="4b160-110">イベント ログ</span><span class="sxs-lookup"><span data-stu-id="4b160-110">Event logs</span></span>
- <span data-ttu-id="4b160-111">AppLocker ログ</span><span class="sxs-lookup"><span data-stu-id="4b160-111">AppLocker logs</span></span>
- <span data-ttu-id="4b160-112">パフォーマンス データ</span><span class="sxs-lookup"><span data-stu-id="4b160-112">Performance data</span></span>
- <span data-ttu-id="4b160-113">System Centerデータ</span><span class="sxs-lookup"><span data-stu-id="4b160-113">System Center data</span></span>
- <span data-ttu-id="4b160-114">通話詳細レコード</span><span class="sxs-lookup"><span data-stu-id="4b160-114">Call detail records</span></span>
- <span data-ttu-id="4b160-115">エクスペリエンス データの品質</span><span class="sxs-lookup"><span data-stu-id="4b160-115">Quality of experience data</span></span>
- <span data-ttu-id="4b160-116">IIS Web Server ログ</span><span class="sxs-lookup"><span data-stu-id="4b160-116">IIS Web Server logs</span></span>
- <span data-ttu-id="4b160-117">SQL Serverログ</span><span class="sxs-lookup"><span data-stu-id="4b160-117">SQL Server logs</span></span>
- <span data-ttu-id="4b160-118">Syslog データ</span><span class="sxs-lookup"><span data-stu-id="4b160-118">Syslog data</span></span>
- <span data-ttu-id="4b160-119">セキュリティ監査ログ</span><span class="sxs-lookup"><span data-stu-id="4b160-119">Security audit logs</span></span>

<span data-ttu-id="4b160-120">アップロードする前に、ODL アプリケーションはスクラブ サービスを使用して、テナント情報やエンドユーザー識別可能な情報など、顧客データを含むフィールドを削除し、それらのフィールドをハッシュ値に置き換える。</span><span class="sxs-lookup"><span data-stu-id="4b160-120">Prior to uploading, the ODL application uses a scrubbing service to remove any fields that contain customer data, such as tenant information and end-user identifiable information, and replace those fields with a hash value.</span></span> <span data-ttu-id="4b160-121">スクラブされたログは、Cosmosおよび潜在的なセキュリティ イベントとパフォーマンス インジケーターのログを分析する NRT セキュリティ監視ソリューションにアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="4b160-121">The scrubbed logs are uploaded to Cosmos and to the NRT security monitoring solution that analyzes the logs for potential security events and performance indicators.</span></span> <span data-ttu-id="4b160-122">監査ログ のデータ保持期間は、Cosmosチームによって決まります。ほとんどの監査ログ データは、セキュリティ インシデント調査をサポートし、規制保持要件を満たすために 90 日以上保持されます。</span><span class="sxs-lookup"><span data-stu-id="4b160-122">The period of audit log data retention in Cosmos is determined by the service teams; most audit log data is retained for 90 days or longer to support security incident investigations and to meet regulatory retention requirements.</span></span>

<span data-ttu-id="4b160-123">ユーザーにMicrosoft 365データへのアクセスは、Cosmos担当者に制限されます。</span><span class="sxs-lookup"><span data-stu-id="4b160-123">Access to Microsoft 365 data stored in Cosmos is restricted to authorized personnel.</span></span> <span data-ttu-id="4b160-124">Microsoft は、監査ログの管理を、監査機能を担当するセキュリティ チーム メンバーの限定されたサブセットに制限します。</span><span class="sxs-lookup"><span data-stu-id="4b160-124">Microsoft restricts the management of audit logs to a limited subset of Security Team members responsible for audit functionality.</span></span> <span data-ttu-id="4b160-125">セキュリティ チームは、管理者に対する永続的なアクセス権を持Cosmos、すべての変更が記録および監査されます。</span><span class="sxs-lookup"><span data-stu-id="4b160-125">The Security Team does not have standing administrative access to Cosmos, and all changes are recorded and audited.</span></span>

<span data-ttu-id="4b160-126">NRT 分析の後、各サービス チームは、データの相関関係、対話型クエリ、およびデータ分析に分析ツールとダッシュボードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4b160-126">After NRT analysis, each service team can use analysis tools and dashboards for data correlation, interactive queries, and data analytics.</span></span> <span data-ttu-id="4b160-127">これらのレポートは、サービスの全体的なパフォーマンスを監視および改善するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4b160-127">These reports are used to monitor and improve the overall performance of the service.</span></span>
