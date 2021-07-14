---
title: Payment Card Industry (PCI) Data Security Standard (DSS)
description: Azure、SharePoint Online、OneDrive for Business は、Payment Card Industry Data Security Standards レベル 1 バージョン 3.2 に準拠します。
keywords: Microsoft 365、コンプライアンス、サービス
localization_priority: Priority
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
ms.openlocfilehash: ab92c2d12477e0e7fa1890ae25e06d264305e95c
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384387"
---
# <a name="payment-card-industry-pci-data-security-standard-dss"></a><span data-ttu-id="880d4-104">Payment Card Industry (PCI) Data Security Standard (DSS)</span><span class="sxs-lookup"><span data-stu-id="880d4-104">Payment Card Industry (PCI) Data Security Standard (DSS)</span></span>

## <a name="pci-dss-overview"></a><span data-ttu-id="880d4-105">PCI DSS の概要</span><span class="sxs-lookup"><span data-stu-id="880d4-105">PCI DSS overview</span></span>

<span data-ttu-id="880d4-106">Payment Card Industry (PCI) Data Security Standards (DSS) は、クレジット カードのデータを安全に管理して不正利用を防ぐ目的で策定されたグローバル情報セキュリティ基準です。</span><span class="sxs-lookup"><span data-stu-id="880d4-106">The Payment Card Industry (PCI) Data Security Standards (DSS) is a global information security standard designed to prevent fraud through increased control of credit card data.</span></span> <span data-ttu-id="880d4-107">クレジット カード主要 5 社 (Visa、MasterCard、American Express、Discover、ジェーシービー (JCB)) によるカード支払いを受け付ける、あらゆる規模の組織が PCI DSS 基準に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="880d4-107">Organizations of all sizes must follow PCI DSS standards if they accept payment cards from the five major credit card brands, Visa, MasterCard, American Express, Discover, and the Japan Credit Bureau (JCB).</span></span> <span data-ttu-id="880d4-108">この PCI DSS への準拠は、支払いとカード所有者に関するデータを保存、処理、または転送するすべての組織に求められます。</span><span class="sxs-lookup"><span data-stu-id="880d4-108">Compliance with PCI DSS is required for any organization that stores, processes, or transmits payment and cardholder data.</span></span>

## <a name="microsoft-and-pci-dss"></a><span data-ttu-id="880d4-109">Microsoft と PCI DSS</span><span class="sxs-lookup"><span data-stu-id="880d4-109">Microsoft and PCI DSS</span></span>

<span data-ttu-id="880d4-110">Microsoft では、年 1 回、認定 Qualified Security Assessor (QSA) による PCI DSS 評価を実施しています。</span><span class="sxs-lookup"><span data-stu-id="880d4-110">Microsoft completed an annual PCI DSS assessment using an approved Qualified Security Assessor (QSA).</span></span> <span data-ttu-id="880d4-111">監査人は、Microsoft Azure、Microsoft OneDrive for Business、および Microsoft SharePoint Online の環境を確認しました。これには、インフラストラクチャ、開発、運用、管理、サポート、および対象となるサービスの検証が含まれます。</span><span class="sxs-lookup"><span data-stu-id="880d4-111">The auditors reviewed Microsoft Azure, Microsoft OneDrive for Business, and Microsoft SharePoint Online  environments, which include validating the infrastructure, development, operations, management, support, and in-scope services.</span></span> <span data-ttu-id="880d4-112">PCI DSS では、取引量に応じて 4 つのレベルのコンプライアンスが指定されています。</span><span class="sxs-lookup"><span data-stu-id="880d4-112">The PCI DSS designates four levels of compliance based on transaction volume.</span></span> <span data-ttu-id="880d4-113">Azure、OneDrive for Business および SharePoint Online は、PCI DSS Version 3.2 サービス プロバイダー レベル 1 (年間取引量が最も多く、600 万件を超える) 準拠として認定されています。</span><span class="sxs-lookup"><span data-stu-id="880d4-113">Azure, OneDrive for Business, and SharePoint Online are certified as compliant under PCI DSS version 3.2 at Service Provider Level 1 (the highest volume of transactions, more than 6 million a year).</span></span>

<span data-ttu-id="880d4-114">評価の結果、お客様が利用できる Attestation of Compliance (AoC) と Report on Compliance (RoC) が QSA によって発行されています。</span><span class="sxs-lookup"><span data-stu-id="880d4-114">The assessment results in an Attestation of Compliance (AoC), which is available to customers and Report on Compliance (RoC) issued by the QSA.</span></span> <span data-ttu-id="880d4-115">コンプライアンスの有効期間は、監査に合格して、査定人から AoC を受け取ったときから始まり、その AoC に署名された日付の 1 年後に終了します。</span><span class="sxs-lookup"><span data-stu-id="880d4-115">The effective period for compliance begins upon passing the audit and receiving the AoC from the assessor and ends one year from the date the AoC is signed.</span></span> 

<span data-ttu-id="880d4-116">カード所有者環境またはカード処理サービスを開発しようとしているお客様は、基礎となる多くの部分でこれらの検証を使用できるため、独自の PCI DSS 証明を取得するために費やす労力とコストを削減できます。</span><span class="sxs-lookup"><span data-stu-id="880d4-116">Customers who want to develop a cardholder environment or card processing service can use these validations in many of the underlying portions, thereby reducing the associated effort and costs of getting their own PCI DSS certification.</span></span>

<span data-ttu-id="880d4-117">Azure、OneDrive for Business、および SharePoint Online の PCI DSS コンプライアンス ステータスが、顧客がプラットフォームで構築またはホストするサービスの PCI DSS 認定を直ちに意味するわけではありません。これを理解しておくことが重要です。</span><span class="sxs-lookup"><span data-stu-id="880d4-117">It is important to understand that PCI DSS compliance status for Azure, OneDrive for Business, and SharePoint Online not automatically translate to PCI DSS certification for the services that customers build or host on these platforms.</span></span> <span data-ttu-id="880d4-118">PCI DSS 要件への対応についてはお客様自身が責任を負います。</span><span class="sxs-lookup"><span data-stu-id="880d4-118">Customers are responsible for ensuring that they achieve compliance with PCI DSS requirements.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="880d4-119">対象となる Microsoft のクラウド プラットフォームとサービス</span><span class="sxs-lookup"><span data-stu-id="880d4-119">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="880d4-120">Azure および Azure Government</span><span class="sxs-lookup"><span data-stu-id="880d4-120">Azure and Azure Government</span></span>
- <span data-ttu-id="880d4-121">Intune</span><span class="sxs-lookup"><span data-stu-id="880d4-121">Intune</span></span>
- <span data-ttu-id="880d4-122">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="880d4-122">Microsoft Cloud App Security</span></span>
- [<span data-ttu-id="880d4-123">Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="880d4-123">Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- <span data-ttu-id="880d4-124">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="880d4-124">Microsoft Graph</span></span>
- <span data-ttu-id="880d4-125">Office 365</span><span class="sxs-lookup"><span data-stu-id="880d4-125">Office 365</span></span>
- <span data-ttu-id="880d4-126">OneDrive for Business および SharePoint Online (米国のみ)</span><span class="sxs-lookup"><span data-stu-id="880d4-126">OneDrive for Business and SharePoint Online (United States only)</span></span>
- <span data-ttu-id="880d4-127">PowerApps クラウド サービス (スタンドアロン サービス、または Office 365 および Dynamics 365 ブランド プランまたはスイートに搭載されているサービス)</span><span class="sxs-lookup"><span data-stu-id="880d4-127">PowerApps cloud service either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite</span></span>
- <span data-ttu-id="880d4-128">Power Automate (スタンドアロン サービス、または Office 365 および Dynamics 365 ブランド プランまたはスイートに搭載されているサービス)</span><span class="sxs-lookup"><span data-stu-id="880d4-128">Power Automate (either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite)</span></span>
- <span data-ttu-id="880d4-129">Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに搭載されているサービス)</span><span class="sxs-lookup"><span data-stu-id="880d4-129">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>

## <a name="azure-dynamics-365-and-pci-dss"></a><span data-ttu-id="880d4-130">Azure、Dynamics 365、PCI DSS</span><span class="sxs-lookup"><span data-stu-id="880d4-130">Azure, Dynamics 365, and PCI DSS</span></span>

<span data-ttu-id="880d4-131">Azure、Dynamics 365、およびその他のオンライン サービス コンプライアンスの詳細については、[Azure PCI DSS サービス](/azure/compliance/offerings/offering-pci-dss)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="880d4-131">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure PCI DSS offering](/azure/compliance/offerings/offering-pci-dss).</span></span>

## <a name="office-365-and-pci-dss"></a><span data-ttu-id="880d4-132">Office 365 と PCI DSS</span><span class="sxs-lookup"><span data-stu-id="880d4-132">Office 365 and PCI DSS</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="880d4-133">Office 365 のクラウド環境</span><span class="sxs-lookup"><span data-stu-id="880d4-133">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="880d4-134">Office 365 の適用性と範囲内のサービス</span><span class="sxs-lookup"><span data-stu-id="880d4-134">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="880d4-135">次の表を使用して、Office 365 サービスとサブスクリプションの適用対象を判断します。</span><span class="sxs-lookup"><span data-stu-id="880d4-135">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="880d4-136">**適用対象**</span><span class="sxs-lookup"><span data-stu-id="880d4-136">**Applicability**</span></span> | <span data-ttu-id="880d4-137">**範囲内のサービス**</span><span class="sxs-lookup"><span data-stu-id="880d4-137">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="880d4-138">**Office 365**</span><span class="sxs-lookup"><span data-stu-id="880d4-138">**Office 365**</span></span> | <span data-ttu-id="880d4-139">OneDrive for Business (米国)、SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="880d4-139">OneDrive for Business (United States), SharePoint Online</span></span> |

### <a name="office-365-audit-reports-and-certificates"></a><span data-ttu-id="880d4-140">Office 365 監査、レポート、証明書</span><span class="sxs-lookup"><span data-stu-id="880d4-140">Office 365 audit, reports, and certificates</span></span>

- [<span data-ttu-id="880d4-141">OneDrive for Business および SharePoint Online の PCI DSS Attestation of Compliance (AoC)</span><span class="sxs-lookup"><span data-stu-id="880d4-141">OneDrive for Business and SharePoint Online PCI DSS Attestation of Compliance (AoC)</span></span>](https://aka.ms/spo-pci)

### <a name="frequently-asked-questions"></a><span data-ttu-id="880d4-142">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="880d4-142">Frequently asked questions</span></span>

<span data-ttu-id="880d4-143">**Attestation of Compliance (AoC) の表紙に「2018 年 6 月」と記載されているのはなぜですか?**</span><span class="sxs-lookup"><span data-stu-id="880d4-143">**Why does the Attestation of Compliance (AoC) cover page say 'June 2018'?**</span></span>

<span data-ttu-id="880d4-144">この表紙に表示されている「2018 年 6 月」の日付は、AoC のテンプレートが発行された日付です。</span><span class="sxs-lookup"><span data-stu-id="880d4-144">The June 2018 date on the cover page is when the AoC template was published.</span></span> <span data-ttu-id="880d4-145">評価の日付については、セクション 2 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="880d4-145">Refer to Section 2 for the date of the assessment.</span></span> 

<span data-ttu-id="880d4-146">**PA DSS と PCI DSS の間にはどのような関係があるのですか?**</span><span class="sxs-lookup"><span data-stu-id="880d4-146">**What is the relationship between the PA DSS and PCI DSS?**</span></span>

<span data-ttu-id="880d4-147">Payment Application Data Security Standard (PA DSS) は PCI DSS に準拠する一連の条件で、Visa の Payment Application Best Practices に代わるものであり、他の主要カード発行元のコンプライアンス要件が統合されています。</span><span class="sxs-lookup"><span data-stu-id="880d4-147">The Payment Application Data Security Standard (PA DSS) is a set of requirements that comply with the PCI DSS, and replaces Visa's Payment Application Best Practices, and consolidates the compliance requirements of the other primary card issuers.</span></span> <span data-ttu-id="880d4-148">PA DSS は、カード承認または決済処理の一環として、カード所有者の支払いデータを保存、処理、または転送するサード パーティ アプリケーションを、ソフトウェア ベンダーが開発する際に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="880d4-148">The PA DSS helps software vendors develop third-party applications that store, process, or transmit cardholder payment data as part of a card authorization or settlement process.</span></span> <span data-ttu-id="880d4-149">PCI DSS コンプライアンスを効率的に実現するには、小売り業者が PA DSS 認定アプリケーションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="880d4-149">Retailers must use PA DSS certified applications to efficiently achieve their PCI DSS compliance.</span></span> <span data-ttu-id="880d4-150">PA DSS は Azure には適用されません。</span><span class="sxs-lookup"><span data-stu-id="880d4-150">The PA DSS does not apply to Azure.</span></span>

<span data-ttu-id="880d4-151">**"取得者" とは何ですか? Azure では使用していますか?**</span><span class="sxs-lookup"><span data-stu-id="880d4-151">**What is an acquirer and does Azure use one?**</span></span>

<span data-ttu-id="880d4-152">取得者とは、銀行、またはカード支払い取引を処理するその他の当事者です。</span><span class="sxs-lookup"><span data-stu-id="880d4-152">An acquirer is a bank or other entity that processes payment card transactions.</span></span> <span data-ttu-id="880d4-153">Azure がカード支払い処理をサービスとして提供することはないため、取得者を利用することはありません。</span><span class="sxs-lookup"><span data-stu-id="880d4-153">Azure does not offer payment card processing as a service and thus does not use an acquirer.</span></span>

<span data-ttu-id="880d4-154">**PCI DSS はどのような組織や業者に適用されるのですか?**</span><span class="sxs-lookup"><span data-stu-id="880d4-154">**To what organizations and merchants does the PCI DSS apply?**</span></span>

<span data-ttu-id="880d4-155">PCI DSS は、規模や取引数に関係なく、カード会員データを受信、転送、または保存するすべての企業に適用されます。</span><span class="sxs-lookup"><span data-stu-id="880d4-155">PCI DSS applies to any company, no matter the size, or number of transactions, that accepts, transmits, or stores cardholder data.</span></span> <span data-ttu-id="880d4-156">つまり、お客様がクレジット カードまたはデビット カードを使用して企業に支払った場合は、必ず PCI DSS 要件が適用されます。</span><span class="sxs-lookup"><span data-stu-id="880d4-156">That is, if any customer ever pays a company using a credit or debit card, then the PCI DSS requirements apply.</span></span> <span data-ttu-id="880d4-157">企業は、12 か月間の取引量合計に基づいて 4 つのレベルのいずれかで検証されます。</span><span class="sxs-lookup"><span data-stu-id="880d4-157">Companies are validated at one of four levels based on the total transaction volume over a 12-month period.</span></span> <span data-ttu-id="880d4-158">レベル 1 は年間取引件数が 600 万件を超える企業、レベル 2 は 100 ～ 600 万件、レベル 3 は 2 ～ 100 万件、レベル 4 は 2 万件未満の企業を対象としています。</span><span class="sxs-lookup"><span data-stu-id="880d4-158">Level 1 is for companies that process over 6 million transactions a year; Level 2 for 1 million to 6 million transactions; Level 3 is for 20,000 to 1 million transactions; and Level 4 is for fewer than 20,000 transactions.</span></span>

<span data-ttu-id="880d4-159">**OneDrive for Business および SharePoint Online が米国以外で PCI DSS に準拠する計画はありますか?**</span><span class="sxs-lookup"><span data-stu-id="880d4-159">**Are there plans for OneDrive for Business and SharePoint Online to be PCI DSS-compliant outside of the United States?**</span></span>

<span data-ttu-id="880d4-160">現在 OneDrive for Business および SharePoint Online は、米国内でのみ PCI-DSS に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="880d4-160">Currently OneDrive for Business and SharePoint Online is PCI-DSS compliant only in the United States (US).</span></span> <span data-ttu-id="880d4-161">Microsoft は、米国以外の地域が追加された場合は、他の地域の要件や予定を評価し、更新情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="880d4-161">Microsoft will evaluate the requirements and timelines for regions outside of US and provide updates when and if other regions are added to the roadmap.</span></span>

<span data-ttu-id="880d4-162">**OneDrive for Business および SharePoint Online の対象ついて**</span><span class="sxs-lookup"><span data-stu-id="880d4-162">**What is in-scope for OneDrive for Business and SharePoint Online?**</span></span>

<span data-ttu-id="880d4-163">現在のところ、OneDrive for Business および SharePoint Online にアップロードされたファイルとドキュメントのみが PCI DSS に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="880d4-163">Currently, only files and documents uploaded to OneDrive for Business and SharePoint Online will be compliant with PCI DSS.</span></span>

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="880d4-164">Microsoft コンプライアンス マネージャーを使用してリスクを評価する</span><span class="sxs-lookup"><span data-stu-id="880d4-164">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="880d4-165">[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="880d4-165">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="880d4-166">コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="880d4-166">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="880d4-167">コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。</span><span class="sxs-lookup"><span data-stu-id="880d4-167">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="880d4-168">[コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。</span><span class="sxs-lookup"><span data-stu-id="880d4-168">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

### <a name="resources"></a><span data-ttu-id="880d4-169">リソース</span><span class="sxs-lookup"><span data-stu-id="880d4-169">Resources</span></span>

- [<span data-ttu-id="880d4-170">PCI Security Standards Council</span><span class="sxs-lookup"><span data-stu-id="880d4-170">PCI Security Standards Council</span></span>](https://www.pcisecuritystandards.org/)
- [<span data-ttu-id="880d4-171">PCI データ セキュリティ基準</span><span class="sxs-lookup"><span data-stu-id="880d4-171">PCI Data Security Standard</span></span>](https://www.pcisecuritystandards.org/documents/PCI_DSS_v3-1.pdf)
- [<span data-ttu-id="880d4-172">PCI DSS クイック レファレンス ガイド</span><span class="sxs-lookup"><span data-stu-id="880d4-172">PCI DSS Quick Reference Guide</span></span>](https://www.pcisecuritystandards.org/documents/PCISSC%20QRG%20August%202014%20-print.pdf)
- [<span data-ttu-id="880d4-173">Microsoft Trust Center のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="880d4-173">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
