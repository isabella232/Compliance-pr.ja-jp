---
title: 国防総省 (DoD) 影響レベル 2 (IL2)
description: Microsoft が国防総省 (DoD) の影響レベル 2 (IL2) 標準を満たす方法について説明します。
keywords: Microsoft 365、コンプライアンス、サービス
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 77e8cb50f815c167e50293d495b4a548a73d022e
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385725"
---
# <a name="department-of-defense-dod-impact-level-2-il2"></a><span data-ttu-id="c336a-104">国防総省 (DoD) 影響レベル 2 (IL2)</span><span class="sxs-lookup"><span data-stu-id="c336a-104">Department of Defense (DoD) Impact Level 2 (IL2)</span></span>

## <a name="dod-il2-overview"></a><span data-ttu-id="c336a-105">DoD IL2 の概要</span><span class="sxs-lookup"><span data-stu-id="c336a-105">DoD IL2 overview</span></span>

<span data-ttu-id="c336a-106">国防情報システム局 (DISA) は、DoD クラウド コンピューティング セキュリティ要件ガイド (SRG) の開発と保守を担当する米国国防総省 [(DoD)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)の機関です。</span><span class="sxs-lookup"><span data-stu-id="c336a-106">The Defense Information Systems Agency (DISA) is an agency of the US Department of Defense (DoD) that is responsible for developing and maintaining the DoD Cloud Computing [Security Requirements Guide (SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html).</span></span> <span data-ttu-id="c336a-107">SRG は、クラウド サービス プロバイダー (CSP) のセキュリティ態勢を評価するために DoD が使用するベースライン セキュリティ要件を定義し、CSP が DoD ミッションをホストできる DoD 暫定承認 (PA) を付与する決定をサポートします。</span><span class="sxs-lookup"><span data-stu-id="c336a-107">The SRG defines the baseline security requirements used by DoD to assess the security posture of a cloud service provider (CSP), supporting the decision to grant a DoD Provisional Authorization (PA) that allows a CSP to host DoD missions.</span></span> <span data-ttu-id="c336a-108">以前に公開された DoD クラウド セキュリティ モデル (CSM) を組み込み、取り消し、取り消し、DoD リスク管理フレームワーク (RMF) にマップします。</span><span class="sxs-lookup"><span data-stu-id="c336a-108">It incorporates, supersedes, and rescinds the previously published DoD Cloud Security Model (CSM) and maps to the DoD Risk Management Framework (RMF).</span></span>

<span data-ttu-id="c336a-109">DISA は、CSP の使用を計画および承認する DoD 機関および部門を案内します。</span><span class="sxs-lookup"><span data-stu-id="c336a-109">DISA guides DoD agencies and departments in planning and authorizing the use of a CSP.</span></span> <span data-ttu-id="c336a-110">また、CSP が SRG に準拠するための CSP 製品を評価します。認証プロセスでは、CSP は DoD 標準への準拠に関するドキュメントを提供できます。</span><span class="sxs-lookup"><span data-stu-id="c336a-110">It also evaluates CSP offerings for compliance with the SRG, an authorization process whereby CSPs can furnish documentation outlining their compliance with DoD standards.</span></span> <span data-ttu-id="c336a-111">必要に応じて DoD 暫定承認 (PA) が発行されます。そのため、DoD 機関やサポート組織は、完全な承認プロセスを独自に行わずにクラウド サービスを使用し、時間と労力を節約できます。</span><span class="sxs-lookup"><span data-stu-id="c336a-111">It issues DoD Provisional Authorizations (PAs) when appropriate, so DoD agencies and supporting organizations can use cloud services without having to go through a full approval process on their own, saving time and effort.</span></span>

<span data-ttu-id="c336a-112">商用クラウド コンピューティング サービスの取得と使用に関するガイダンスの更新に関する[2014 年 12 月 15](https://www.esi.mil/contentview.aspx?id=585)日の DoD CIO メモでは、「FedRAMP は、すべての DoD クラウド サービスの最小セキュリティ ベースラインとして機能する」と示されています。</span><span class="sxs-lookup"><span data-stu-id="c336a-112">The [15 December 2014 DoD CIO memo](https://www.esi.mil/contentview.aspx?id=585) regarding *Updated Guidance on the Acquisition and Use of Commercial Cloud Computing Services* states that 'FedRAMP will serve as the minimum security baseline for all DoD cloud services'.</span></span> <span data-ttu-id="c336a-113">SRG は、すべての情報影響レベル (IL) で FedRAMP モデレート ベースラインを使用し、一部ではハイ ベースラインと見なします。</span><span class="sxs-lookup"><span data-stu-id="c336a-113">The SRG uses the FedRAMP Moderate baseline at all information impact levels (IL) and considers the High Baseline at some.</span></span>

<span data-ttu-id="c336a-114">[SRG セクション 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *FedRAMP* セキュリティ コントロールの DoD の使用では、セクション 5.6.2 で説明されている人事セキュリティ要件に準拠した場合、FedRAMP モデレート PA と DoD レベル 2 PA を最小限に抑える CSP で IL2 情報がホストされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c336a-114">[SRG Section 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD use of FedRAMP Security Controls* states that IL2 information may be hosted in a CSP that minimally holds a FedRAMP Moderate PA and a DoD Level 2 PA, subject to compliance with the personnel security requirements outlined in Section 5.6.2.</span></span> <span data-ttu-id="c336a-115">ただし、この方法では、ミッション所有者の要求に応じて CSP が他のセキュリティ要件や統合要件を満たさないわけではありません。</span><span class="sxs-lookup"><span data-stu-id="c336a-115">However, this approach does not alleviate the CSP from meeting other security and integration requirements as required by the Mission Owner.</span></span> <span data-ttu-id="c336a-116">[SRG セクション 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2 の* 場所と分離の要件に従って、DoD IL2 PA は FedRAMP モデレート PA で適切にカバーされ、IL2 PA の要件は追加的に評価されません。</span><span class="sxs-lookup"><span data-stu-id="c336a-116">According to [SRG Section 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2 Location and Separation Requirements*, DoD IL2 PA is adequately covered by a FedRAMP Moderate PA such that the requirements will not be additionally assessed for an IL2 PA.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="c336a-117">Microsoft のスコープ内クラウド プラットフォームと&サービス</span><span class="sxs-lookup"><span data-stu-id="c336a-117">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="c336a-118">Azure</span><span class="sxs-lookup"><span data-stu-id="c336a-118">Azure</span></span>
- <span data-ttu-id="c336a-119">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c336a-119">Dynamics 365</span></span>
- <span data-ttu-id="c336a-120">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="c336a-120">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="c336a-121">Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="c336a-121">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="c336a-122">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="c336a-122">Microsoft Graph</span></span>
- <span data-ttu-id="c336a-123">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="c336a-123">Microsoft Intune</span></span>
- <span data-ttu-id="c336a-124">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="c336a-124">Microsoft Stream</span></span>
- <span data-ttu-id="c336a-125">Office 365米国政府、米国Office 365 - 高</span><span class="sxs-lookup"><span data-stu-id="c336a-125">Office 365 U.S. Government, Office 365 U.S. Government - High</span></span>
- <span data-ttu-id="c336a-126">Power アプリ</span><span class="sxs-lookup"><span data-stu-id="c336a-126">Power Apps</span></span>
- <span data-ttu-id="c336a-127">Power Automate</span><span class="sxs-lookup"><span data-stu-id="c336a-127">Power Automate</span></span>
- <span data-ttu-id="c336a-128">Power BI</span><span class="sxs-lookup"><span data-stu-id="c336a-128">Power BI</span></span>

## <a name="azure-dynamics-365-and-dod-il2"></a><span data-ttu-id="c336a-129">Azure、Dynamics 365、DoD IL2</span><span class="sxs-lookup"><span data-stu-id="c336a-129">Azure, Dynamics 365, and DoD IL2</span></span>

<span data-ttu-id="c336a-130">Azure、Dynamics 365、その他のオンライン サービスコンプライアンスの詳細については [、「Azure DoD IL2 製品」を参照してください](/azure/compliance/offerings/offering-dod-il2)。</span><span class="sxs-lookup"><span data-stu-id="c336a-130">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure DoD IL2 offering](/azure/compliance/offerings/offering-dod-il2).</span></span>

## <a name="office-365-and-dod-il2"></a><span data-ttu-id="c336a-131">Office 365 DoD IL2</span><span class="sxs-lookup"><span data-stu-id="c336a-131">Office 365 and DoD IL2</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="c336a-132">Office 365クラウド環境</span><span class="sxs-lookup"><span data-stu-id="c336a-132">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="c336a-133">Office 365とスコープ内サービス</span><span class="sxs-lookup"><span data-stu-id="c336a-133">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="c336a-134">次の表を使用して、サービスとサブスクリプションOffice 365を決定します。</span><span class="sxs-lookup"><span data-stu-id="c336a-134">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="c336a-135">**適用対象**</span><span class="sxs-lookup"><span data-stu-id="c336a-135">**Applicability**</span></span> | <span data-ttu-id="c336a-136">**スコープ内サービス**</span><span class="sxs-lookup"><span data-stu-id="c336a-136">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="c336a-137">**GCC**</span><span class="sxs-lookup"><span data-stu-id="c336a-137">**GCC**</span></span> | <span data-ttu-id="c336a-138">アクティビティ フィード サービス、Bing サービス、Delve、Exchange Online Protection、Exchange Online、インテリジェント サービス、Microsoft Teams、Office 365 カスタマー ポータル、Office Online、Office サービス インフラストラクチャ、Office 利用状況レポート、OneDrive for Business、People Card、SharePoint Online、Skype for Business、Windows Ink</span><span class="sxs-lookup"><span data-stu-id="c336a-138">Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |
| <span data-ttu-id="c336a-139">**GCC High**</span><span class="sxs-lookup"><span data-stu-id="c336a-139">**GCC High**</span></span> | <span data-ttu-id="c336a-140">アクティビティ フィード サービス、Bing サービス、Delve、Exchange Online Protection、Exchange Online、インテリジェント サービス、Microsoft Teams、Office 365 カスタマー ポータル、Office Online、Office サービス インフラストラクチャ、Office 利用状況レポート、OneDrive for Business、People Card、SharePoint Online、Skype for Business、Windows Ink</span><span class="sxs-lookup"><span data-stu-id="c336a-140">Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |

### <a name="resources"></a><span data-ttu-id="c336a-141">リソース</span><span class="sxs-lookup"><span data-stu-id="c336a-141">Resources</span></span>

- [<span data-ttu-id="c336a-142">Microsoft Government ソリューション</span><span class="sxs-lookup"><span data-stu-id="c336a-142">Microsoft government solutions</span></span>](https://www.microsoft.com/enterprise/government)
- [<span data-ttu-id="c336a-143">DoD Cloud Computing セキュリティ要件ガイド</span><span class="sxs-lookup"><span data-stu-id="c336a-143">DoD Cloud Computing Security Requirements Guide</span></span>](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [<span data-ttu-id="c336a-144">FedRAMP ドキュメント</span><span class="sxs-lookup"><span data-stu-id="c336a-144">FedRAMP documents</span></span>](https://www.fedramp.gov/documents/)
- <span data-ttu-id="c336a-145">[NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final)情報システムと組織のリスク管理フレームワーク *:* セキュリティLife-Cycleプライバシーに関するシステムLife-Cycleアプローチ</span><span class="sxs-lookup"><span data-stu-id="c336a-145">[NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*</span></span>
- <span data-ttu-id="c336a-146">[NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53)情報システムと組織のセキュリティと *プライバシー制御*</span><span class="sxs-lookup"><span data-stu-id="c336a-146">[NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *Security and Privacy Controls for Information Systems and Organizations*</span></span>
- <span data-ttu-id="c336a-147">[DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Information Technology (IT) の DoD リスク管理フレームワーク (RMF)*</span><span class="sxs-lookup"><span data-stu-id="c336a-147">[DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) for DoD Information Technology (IT)*</span></span>
