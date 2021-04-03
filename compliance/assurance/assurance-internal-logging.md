---
title: Microsoft 365 エンジニアリングの Microsoft 365 内部ログ
description: この記事では、Microsoft 365 エンジニアリング チームの内部ログがどのように機能するのかについて説明します。
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
ms.openlocfilehash: 110a61c27a00380eede4d4f2303acfb025a27a1f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497069"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a><span data-ttu-id="c9ab1-103">Microsoft 365 のエンジニアリングのための内部ログ記録</span><span class="sxs-lookup"><span data-stu-id="c9ab1-103">Internal logging for Microsoft 365 engineering</span></span>

<span data-ttu-id="c9ab1-104">お客様が利用できるイベントとログ データに加えて、Microsoft 365 のエンジニアが Microsoft 365 エンジニアが利用できる内部ログ データ収集システムもあります。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-104">In addition to the events and log data available for customers, there is also an internal log data collection system that is available to Microsoft 365 engineers at Microsoft.</span></span> <span data-ttu-id="c9ab1-105">さまざまな種類のログ データが Microsoft 365 サーバーから Cosmos と呼ばれる内部のビッグ データ コンピューティング サービスにアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-105">Many different types of log data are uploaded from Microsoft 365 servers to an internal, big data computing service called Cosmos.</span></span> <span data-ttu-id="c9ab1-106">各サービス チームは、それぞれのサーバーから Cosmos データベースに監査ログをアップロードして、集約と分析を行います。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-106">Each service team uploads audit logs from their respective servers into the Cosmos database for aggregation and analysis.</span></span> <span data-ttu-id="c9ab1-107">このデータ転送は、Office データ ローダー (ODL) と呼ばれる独自のオートメーション ツールを使用して、特に承認されたポートおよびプロトコル上の FIPS 140-2 検証済みの TLS 接続を使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-107">This data transfer occurs over a FIPS 140-2-validated TLS connection on specifically approved ports and protocols using a proprietary automation tool called the Office Data Loader (ODL).</span></span> <span data-ttu-id="c9ab1-108">Microsoft 365 で監査レコードの収集と処理に使用されるツールでは、元の監査レコードのコンテンツや時間の順序に対する永続的または不可逆的な変更は許可されません。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-108">The tools used in Microsoft 365 to collect and process audit records do not allow permanent or irreversible changes to the original audit record content or time ordering.</span></span>

<span data-ttu-id="c9ab1-109">サービス チームは、Cosmos を集中リポジトリとして使用して、アプリケーションの使用状況の分析、システムと運用パフォーマンスの測定、問題やセキュリティの問題を示す可能性のある異常やパターンを探します。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-109">Service teams use Cosmos as a centralized repository to conduct an analysis of application usage, to measure system and operational performance, and to look for abnormalities and patterns that may indicate problems or security issues.</span></span> <span data-ttu-id="c9ab1-110">各サービス チームは、分析する内容に応じて、次のようなログのベースラインを Cosmos にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-110">Each service team uploads a baseline of logs into Cosmos, depending on what they are looking to analyze, that often include:</span></span>

- <span data-ttu-id="c9ab1-111">イベント ログ</span><span class="sxs-lookup"><span data-stu-id="c9ab1-111">Event logs</span></span>
- <span data-ttu-id="c9ab1-112">AppLocker ログ</span><span class="sxs-lookup"><span data-stu-id="c9ab1-112">AppLocker logs</span></span>
- <span data-ttu-id="c9ab1-113">パフォーマンス データ</span><span class="sxs-lookup"><span data-stu-id="c9ab1-113">Performance data</span></span>
- <span data-ttu-id="c9ab1-114">System Center データ</span><span class="sxs-lookup"><span data-stu-id="c9ab1-114">System Center data</span></span>
- <span data-ttu-id="c9ab1-115">通話詳細レコード</span><span class="sxs-lookup"><span data-stu-id="c9ab1-115">Call detail records</span></span>
- <span data-ttu-id="c9ab1-116">エクスペリエンス データの品質</span><span class="sxs-lookup"><span data-stu-id="c9ab1-116">Quality of experience data</span></span>
- <span data-ttu-id="c9ab1-117">IIS Web Server ログ</span><span class="sxs-lookup"><span data-stu-id="c9ab1-117">IIS Web Server logs</span></span>
- <span data-ttu-id="c9ab1-118">SQL Serverログ</span><span class="sxs-lookup"><span data-stu-id="c9ab1-118">SQL Server logs</span></span>
- <span data-ttu-id="c9ab1-119">Syslog データ</span><span class="sxs-lookup"><span data-stu-id="c9ab1-119">Syslog data</span></span>
- <span data-ttu-id="c9ab1-120">セキュリティ監査ログ</span><span class="sxs-lookup"><span data-stu-id="c9ab1-120">Security audit logs</span></span>

<span data-ttu-id="c9ab1-121">データを Cosmos にアップロードする前に、ODL アプリケーションはスクラブ サービスを使用して、テナント情報やエンドユーザー識別可能な情報など、顧客データを含むフィールドを難読化し、それらのフィールドをハッシュ値に置き換える。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-121">Prior to uploading data into Cosmos, the ODL application uses a scrubbing service to obfuscate any fields that contain customer data, such as tenant information and end-user identifiable information, and replace those fields with a hash value.</span></span> <span data-ttu-id="c9ab1-122">匿名化ログとハッシュ ログが書き換え、次に Cosmos にアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-122">The anonymized and hashed logs are rewritten and then uploaded into Cosmos.</span></span> <span data-ttu-id="c9ab1-123">サービス チームは、Cosmos のデータに対してスコープ付きクエリを実行して、相関関係、アラート、レポート作成を行います。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-123">Service teams run scoped queries against their data in Cosmos for correlation, alerting, and reporting.</span></span> <span data-ttu-id="c9ab1-124">Cosmos の監査ログ データ保持期間は、サービス チームによって決まります。ほとんどの監査ログ データは、セキュリティ インシデント調査をサポートし、規制保持要件を満たすために 90 日以上保持されます。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-124">The period of audit log data retention in Cosmos is determined by the service teams; most audit log data is retained for 90 days or longer to support security incident investigations and to meet regulatory retention requirements.</span></span>

<span data-ttu-id="c9ab1-125">Cosmos に格納されている Microsoft 365 データへのアクセスは、承認された担当者に制限されます。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-125">Access to Microsoft 365 data stored in Cosmos is restricted to authorized personnel.</span></span> <span data-ttu-id="c9ab1-126">Microsoft は、監査機能の管理を、監査機能を担当するサービス チーム メンバーの限定されたサブセットに制限します。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-126">Microsoft restricts the management of audit functionality to the limited subset of service team members that are responsible for audit functionality.</span></span> <span data-ttu-id="c9ab1-127">これらのチーム メンバーは、Cosmos からデータを変更または削除する機能を持たなく、Cosmos のログメカニズムに対する変更はすべて記録および監査されます。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-127">These team members do not have the ability to modify or delete data from Cosmos, and all changes to logging mechanisms for Cosmos are recorded and audited.</span></span>

<span data-ttu-id="c9ab1-128">各サービス チームは、特定のアプリケーションに特定の分析を実行する権限を与え、分析のためにログ データにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-128">Each service team accesses its log data for analysis by authorizing certain applications to conduct specific analysis.</span></span> <span data-ttu-id="c9ab1-129">たとえば、Microsoft 365 セキュリティ チームは、独自のイベント ログ パーサーを介して Cosmos のデータを使用して、Microsoft 365 の実稼働環境で疑わしいアクティビティに関するアクション可能なレポートを関連付け、警告し、生成します。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-129">For example, the Microsoft 365 Security team uses data from Cosmos through a proprietary event log parser to correlate, alert, and generate actionable reports on possible suspicious activity in the Microsoft 365 production environment.</span></span> <span data-ttu-id="c9ab1-130">このデータからのレポートは、脆弱性を修正し、サービスの全体的なパフォーマンスを向上させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-130">The reports from this data are used to correct vulnerabilities, and to improve the overall performance of the service.</span></span> <span data-ttu-id="c9ab1-131">特定のアラートまたはレポートで詳細な調査が必要な場合、サービス担当者はデータを Microsoft 365 サービスにインポートしなおす必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-131">If a specific alert or report requires further investigation, service personnel can request that data be imported back into the Microsoft 365 service.</span></span> <span data-ttu-id="c9ab1-132">Cosmos からインポートされる特定のログは暗号化され、サービス担当者は復号化キーにアクセスできないので、ターゲット ログは、スコープ設定された結果を承認されたサービス担当者に返す暗号化解除サービスをプログラムで渡されます。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-132">Since the specific log being imported from Cosmos is in encrypted and service personnel do not have access to decryption keys, the target log is programmatically passed through a decryption service that returns scoped results to the authorized service personnel.</span></span> <span data-ttu-id="c9ab1-133">この演習で見つかった脆弱性は、Microsoft の標準的なセキュリティ インシデント管理チャネルを使用して報告およびエスカレートされます。</span><span class="sxs-lookup"><span data-stu-id="c9ab1-133">Any vulnerabilities found from this exercise are reported and escalated using Microsoft's standard security incident management channels.</span></span>
