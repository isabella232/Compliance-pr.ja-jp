---
title: オンプレミス ファイル共有の GDPR
description: オンプレミスの Windows Server ファイルで共有一般データ保護規則 (GDPR) の要件に対応する方法について説明します。
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
ms.openlocfilehash: 5a3b192e4c374dac4248300627e5659a1b5f66fd
ms.sourcegitcommit: 18c7e403d6ffbc9afa323fadc04c673dbb7bd391
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2020
ms.locfileid: "49620762"
---
# <a name="gdpr-for-on-premises-windows-server-file-shares"></a><span data-ttu-id="2200b-103">オンプレミスの Windows Server ファイル共有の GDPR</span><span class="sxs-lookup"><span data-stu-id="2200b-103">GDPR for on-premises Windows Server file shares</span></span>

<span data-ttu-id="2200b-104">ファイル共有のための推奨される基本的なアプローチは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2200b-104">The basic recommended approach for file shares is:</span></span>

-   <span data-ttu-id="2200b-105">Azure Information Protection を使用して、機密データにラベルを付けます。</span><span class="sxs-lookup"><span data-stu-id="2200b-105">Use Azure Information Protection to label sensitive data.</span></span>

-   <span data-ttu-id="2200b-106">Azure Information Protection スキャナーを使用して、データを検索します。</span><span class="sxs-lookup"><span data-stu-id="2200b-106">Use Azure Information Protection scanner to find data.</span></span>

<span data-ttu-id="2200b-107">ファイル共有のための推奨されるアプローチには、次の手順が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2200b-107">The recommended approach for files shares includes these steps:</span></span>

1.  <span data-ttu-id="2200b-108">**Azure Information Protection スキャナーをインストールし、構成します。**</span><span class="sxs-lookup"><span data-stu-id="2200b-108">**Install and configure Azure Information Protection scanner.**</span></span>

    -   <span data-ttu-id="2200b-109">使用する機密データの種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="2200b-109">Decide which sensitive data types to use.</span></span>

    -   <span data-ttu-id="2200b-110">使用するローカル フォルダーとネットワーク共有を指定します。</span><span class="sxs-lookup"><span data-stu-id="2200b-110">Specify local folders and network shares to use.</span></span>

2.  <span data-ttu-id="2200b-111">**検出サイクルを完了します。**</span><span class="sxs-lookup"><span data-stu-id="2200b-111">**Complete a discovery cycle.**</span></span>

    -   <span data-ttu-id="2200b-112">検出モードでスキャナーを実行し、検出結果を検証します。</span><span class="sxs-lookup"><span data-stu-id="2200b-112">Run the scanner in discovery mode and validate the findings.</span></span>

    -   <span data-ttu-id="2200b-113">必要に応じて、条件と機密情報の種類を最適化します。</span><span class="sxs-lookup"><span data-stu-id="2200b-113">If needed, optimize the conditions and sensitive information types.</span></span>

    -   <span data-ttu-id="2200b-114">自動的に適用されるラベルの予期される影響を評価します。</span><span class="sxs-lookup"><span data-stu-id="2200b-114">Assess the expected impact of automatically applying labels.</span></span>

3.  <span data-ttu-id="2200b-115">**Azure Information Protection スキャナーを実行して、対象となるドキュメントにラベルを適用します**。</span><span class="sxs-lookup"><span data-stu-id="2200b-115">**Run the Azure Information Protection scanner to apply labels to qualifying documents**.</span></span>

4.  <span data-ttu-id="2200b-116">**保護のために、**</span><span class="sxs-lookup"><span data-stu-id="2200b-116">**For protection:**</span></span>

    -   <span data-ttu-id="2200b-117">目的としたラベルのドキュメントを保護するための Exchange データ損失防止ルールを構成します。</span><span class="sxs-lookup"><span data-stu-id="2200b-117">Configure Exchange data loss prevention rules to protect documents with the desired label.</span></span>

    -   <span data-ttu-id="2200b-118">アクセス許可を使用して、ファイルにアクセスできるユーザーを制限するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="2200b-118">Be sure to use permissions to limit who can access files.</span></span>

5.  <span data-ttu-id="2200b-119">**監視のため、Windows Server のログを SIEM ツールに統合します。**</span><span class="sxs-lookup"><span data-stu-id="2200b-119">**For monitoring, integrate Windows Server logs with a SIEM tool.**</span></span>

    -   <span data-ttu-id="2200b-p101">データ主体要求の個人データを検索するため、Azure Information Protection スキャナーを使用します。また、ファイル共有をクロールするよう、SharePoint Server 検索を構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="2200b-p101">To find personal data for data subject requests, use Azure Information Protection scanner. You can also configure SharePoint Server search to crawl file shares.</span></span>

<span data-ttu-id="2200b-122">Azure Information Protection スキャナーを使用して個人データを検索したりラベル付けしたりすることに関する詳細については、「Deploy AIP Scanner (AIP スキャナーの展開)」(<https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2200b-122">For more information on using Azure Information Protection scanner to find and label personal data, see [Deploy AIP Scanner](<https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner).</span></span>

<span data-ttu-id="2200b-p102">さまざまな条件でスキャナーを構成すること、また Office 365 データ損失防止 (DLP) のさまざまな機密情報タイプを使用することに関する情報については、「[Azure Information Protection 用の自動および推奨分類の条件を構成する方法](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-classification)」を参照してください。新しいタイプの Office 365 機密情報はスキャナーですぐに利用できるようになるわけではなく、カスタム機密情報タイプはスキャナーで使用できないことに注意ください。</span><span class="sxs-lookup"><span data-stu-id="2200b-p102">For information on configuring the scanner for conditions and using the Office 365 data loss prevention (DLP) sensitive information types, see [How to configure conditions for automatic and recommended classification for Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-classification). Note that new Office 365 sensitive information types will not be immediately available to use with the scanner and custom sensitive information types cannot be used with the scanner.</span></span>
