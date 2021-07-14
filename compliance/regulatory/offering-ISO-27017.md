---
title: ISO/IEC 27017:2015 情報セキュリティ コントロールの実施基準
description: Microsoft クラウド サービスでは、情報セキュリティ コントロールに関するこの実施基準が採用されています。
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
ms.openlocfilehash: 6c431d856fc03f328148722c14dfc558082aacb5
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384727"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a><span data-ttu-id="b821a-104">ISO/IEC 27017:2015 情報セキュリティ コントロールの実施基準</span><span class="sxs-lookup"><span data-stu-id="b821a-104">ISO/IEC 27017:2015 Code of Practice for Information Security Controls</span></span>

## <a name="iso-iec-27017-overview"></a><span data-ttu-id="b821a-105">ISO-IEC 27017 の概要</span><span class="sxs-lookup"><span data-stu-id="b821a-105">ISO-IEC 27017 Overview</span></span>

<span data-ttu-id="b821a-106">ISO/IEC 27017:2015 実施基準は、組織が ISO/IEC 27002:2013 に基づいてクラウド コンピューティング情報セキュリティ管理システムを実装するときにクラウド サービス情報セキュリティ コントロールを選択するためのリファレンスとして使用することを意図しています。</span><span class="sxs-lookup"><span data-stu-id="b821a-106">The ISO/IEC 27017:2015 code of practice is designed for organizations to use as a reference for selecting cloud services information security controls when implementing a cloud computing information security management system based on ISO/IEC 27002:2013.</span></span> <span data-ttu-id="b821a-107">また、クラウド サービス プロバイダーが、一般に受け入れられている保護コントロールを実装するためのガイダンス資料としても使用できます。</span><span class="sxs-lookup"><span data-stu-id="b821a-107">It can also be used by cloud service providers as a guidance document for implementing commonly accepted protection controls.</span></span>

<span data-ttu-id="b821a-108">この国際的な基準には、ISO/IEC 27002 に基づくクラウド特有の実装ガイダンスも提供されています。さらに、ISO/IEC 27002: 2013 の 5 項から 18 項で示されるコントロール、実装ガイダンスおよび各種情報に対するクラウド特有の情報セキュリティの脅威とリスクに対応するための追加コントロールも示されています。</span><span class="sxs-lookup"><span data-stu-id="b821a-108">This international standard provides additional cloud-specific implementation guidance based on ISO/IEC 27002, and provides additional controls to address cloud-specific information security threats and risks referring to clauses 5-18 in ISO/IEC 27002: 2013 for controls, implementation guidance, and other information.</span></span> <span data-ttu-id="b821a-109">具体的にはこの基準では ISO/IEC 27002 の 37 のコントロールに関するガイダンスを提供すると同時に、ISO/IEC 27002 では取り上げられていない 7 つの新しいコントロールにも言及しています。</span><span class="sxs-lookup"><span data-stu-id="b821a-109">Specifically, this standard provides guidance on 37 controls in ISO/IEC 27002, and it also features seven new controls that are not duplicated in ISO/IEC 27002.</span></span> <span data-ttu-id="b821a-110">これらの新しいコントロールは、次の重要な分野に対応しています。</span><span class="sxs-lookup"><span data-stu-id="b821a-110">These new controls address the following important areas:</span></span>

- <span data-ttu-id="b821a-111">クラウド コンピューティング環境で共有される役割と責任</span><span class="sxs-lookup"><span data-stu-id="b821a-111">Shared roles and responsibilities within a cloud computing environment</span></span>
- <span data-ttu-id="b821a-112">契約終了時におけるクラウド サービスのお客様の資産の削除と返却</span><span class="sxs-lookup"><span data-stu-id="b821a-112">Removal and return of cloud service customer assets upon contract termination</span></span>
- <span data-ttu-id="b821a-113">お客様の仮想環境を他のお客様の仮想環境から保護および分離すること</span><span class="sxs-lookup"><span data-stu-id="b821a-113">Protection and separation of a customer's virtual environment from environments of other customers</span></span>
- <span data-ttu-id="b821a-114">ビジネス ニーズに応じた仮想マシンの要塞化要件</span><span class="sxs-lookup"><span data-stu-id="b821a-114">Virtual machine hardening requirements to meet business needs</span></span>
- <span data-ttu-id="b821a-115">クラウド コンピューティング環境の管理運用の手順</span><span class="sxs-lookup"><span data-stu-id="b821a-115">Procedures for administrative operations of a cloud computing environment</span></span>
- <span data-ttu-id="b821a-116">クラウド コンピューティング環境内の関連アクティビティに対する監視手段の提供</span><span class="sxs-lookup"><span data-stu-id="b821a-116">Enabling customers to monitor relevant activities within a cloud computing environment</span></span>
- <span data-ttu-id="b821a-117">仮想ネットワークと物理ネットワークのセキュリティ管理の連携</span><span class="sxs-lookup"><span data-stu-id="b821a-117">Alignment of security management for virtual and physical networks</span></span>

## <a name="microsoft-and-isoiec-27017"></a><span data-ttu-id="b821a-118">Microsoft と ISO/IEC 27017</span><span class="sxs-lookup"><span data-stu-id="b821a-118">Microsoft and ISO/IEC 27017</span></span>

<span data-ttu-id="b821a-119">ISO/IEC 27017 は、クラウド サービス プロバイダーとクラウド サービスお客様の両方にガイダンスを提供している点で独特です。</span><span class="sxs-lookup"><span data-stu-id="b821a-119">ISO/IEC 27017 is unique in providing guidance for both cloud service providers and cloud service customers.</span></span> <span data-ttu-id="b821a-120">また、クラウド サービスお客様がクラウド サービス プロバイダーに期待できることに関する実際的な情報も示しています。</span><span class="sxs-lookup"><span data-stu-id="b821a-120">It also provides cloud service customers with practical information on what they should expect from cloud service providers.</span></span> <span data-ttu-id="b821a-121">お客様が ISO/IEC 27017 から直接得られるメリットとして、クラウドにおける共同責任を理解できます。</span><span class="sxs-lookup"><span data-stu-id="b821a-121">Customers can benefit directly from ISO/IEC 27017 by ensuring they understand the shared responsibilities in the cloud.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="b821a-122">対象となる Microsoft のクラウド プラットフォームとサービス</span><span class="sxs-lookup"><span data-stu-id="b821a-122">Microsoft in-scope cloud platforms & services</span></span>

- [<span data-ttu-id="b821a-123">Azure、Azure Government、Azure Germany</span><span class="sxs-lookup"><span data-stu-id="b821a-123">Azure, Azure Government, and Azure Germany</span></span>](https://aka.ms/AzureCompliance)
- <span data-ttu-id="b821a-124">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b821a-124">Microsoft Cloud App Security</span></span>
- [<span data-ttu-id="b821a-125">Dynamics 365、Dynamics 365、Dynamics 365 ドイツ</span><span class="sxs-lookup"><span data-stu-id="b821a-125">Dynamics 365, Dynamics 365, and Dynamics 365 Germany</span></span>](https://aka.ms/d365-compliance-list)
- <span data-ttu-id="b821a-126">Intune</span><span class="sxs-lookup"><span data-stu-id="b821a-126">Intune</span></span>
- <span data-ttu-id="b821a-127">Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="b821a-127">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="b821a-128">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="b821a-128">Microsoft Graph</span></span>
- <span data-ttu-id="b821a-129">Microsoft Healthcare Bot</span><span class="sxs-lookup"><span data-stu-id="b821a-129">Microsoft Healthcare Bot</span></span>
- [<span data-ttu-id="b821a-130">Microsoft マネージド デスクトップ</span><span class="sxs-lookup"><span data-stu-id="b821a-130">Microsoft Managed Desktop</span></span>](/microsoft-365/managed-desktop/intro/compliance)
- <span data-ttu-id="b821a-131">Office 365、Office 365 米国政府、Office 365 米国防総省、Office 365 Germany</span><span class="sxs-lookup"><span data-stu-id="b821a-131">Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense, and Office 365 Germany</span></span>
- <span data-ttu-id="b821a-132">Power Automate (旧称 Microsoft Flow) スタンドアロン サービス、または Office 365 や Dynamics 365 ブランド プランあるいはスイートに搭載されているサービスとしてのクラウド サービス</span><span class="sxs-lookup"><span data-stu-id="b821a-132">Power Automate (formerly Microsoft Flow) cloud service either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite</span></span>
- <span data-ttu-id="b821a-133">Power Apps クラウド サービス (スタンドアロン サービス、または Office 365 および Dynamics 365 ブランド プランあるいはスイートに搭載されているサービス)</span><span class="sxs-lookup"><span data-stu-id="b821a-133">PowerApps cloud service either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite</span></span>
- <span data-ttu-id="b821a-134">Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに組み込まれているサービス)</span><span class="sxs-lookup"><span data-stu-id="b821a-134">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>
- <span data-ttu-id="b821a-135">Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="b821a-135">Power BI Embedded</span></span>

## <a name="azure-dynamics-365-and-iso-270172015"></a><span data-ttu-id="b821a-136">Azure、Dynamics 365、ISO 27017:2015</span><span class="sxs-lookup"><span data-stu-id="b821a-136">Azure, Dynamics 365, and ISO 27017:2015</span></span>

<span data-ttu-id="b821a-137">Azure、Dynamics 365、およびその他のオンライン サービス コンプライアンスの詳細については、[Azure ISO 27017 サービス](/azure/compliance/offerings/offering-iso-27017)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b821a-137">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure ISO 27017 offering](/azure/compliance/offerings/offering-iso-27017).</span></span>

## <a name="office-365-and-iso-270172015"></a><span data-ttu-id="b821a-138">Office 365 と ISO 27017:2015</span><span class="sxs-lookup"><span data-stu-id="b821a-138">Office 365 and ISO 27017:2015</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="b821a-139">Office 365 のクラウド環境</span><span class="sxs-lookup"><span data-stu-id="b821a-139">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="b821a-140">Office 365 の適用性と範囲内のサービス</span><span class="sxs-lookup"><span data-stu-id="b821a-140">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="b821a-141">次の表を使用して、Office 365 サービスとサブスクリプションの適用対象を判断します。</span><span class="sxs-lookup"><span data-stu-id="b821a-141">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="b821a-142">**適用対象**</span><span class="sxs-lookup"><span data-stu-id="b821a-142">**Applicability**</span></span> | <span data-ttu-id="b821a-143">**範囲内のサービス**</span><span class="sxs-lookup"><span data-stu-id="b821a-143">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="b821a-144">**Office 365**</span><span class="sxs-lookup"><span data-stu-id="b821a-144">**Office 365**</span></span> | <span data-ttu-id="b821a-145">Access Online、Azure Active Directory、Azure Communications Service、コンプライアンス マネージャー、カスタマー ロックボックス、Delve、Exchange Online、Exchange Online Protection、Forms、Griffin、Identity Manager、Lockbox (Torus)、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 Customer Portal、Office 365 Microservices (Kaizala、ObjectStore、Sway、PowerPoint Online Document Service、Query Annotation Service、School Data Sync、Siphon、Speech、StaffHub、eXtensible Application Program を含むがこれらに限定されない)、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、Office Services Infrastructure、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、Project Online、カスタマー キーによるサービスの暗号化、SharePoint Online、Skype for Business、Stream</span><span class="sxs-lookup"><span data-stu-id="b821a-145">Access Online, Azure Active Directory, Azure Communications Service, Compliance Manager, Customer Lockbox, Delve, Exchange Online, Exchange Online Protection, Forms, Griffin, Identity Manager, Lockbox (Torus), Microsoft Defender for Office 365, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance add-on, Office 365 Customer Portal, Office 365 Microservices (including but not limited to Kaizala, ObjectStore, Sway, PowerPoint Online Document Service, Query Annotation Service, School Data Sync, Siphon, Speech, StaffHub, eXtensible Application Program), Office 365 Security & Compliance Center, Office Online, Office Pro Plus, Office Services Infrastructure, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, Project Online, Service Encryption with Customer Key, SharePoint Online, Skype for Business, Stream</span></span> |
| <span data-ttu-id="b821a-146">**GCC**</span><span class="sxs-lookup"><span data-stu-id="b821a-146">**GCC**</span></span> | <span data-ttu-id="b821a-147">Azure Active Directory、Azure Communications Service、コンプライアンス マネージャー、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream</span><span class="sxs-lookup"><span data-stu-id="b821a-147">Azure Active Directory, Azure Communications Service, Compliance Manager, Delve, Exchange Online, Forms, Microsoft Defender for Office 365, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business, Stream</span></span> |
| <span data-ttu-id="b821a-148">**GCC High**</span><span class="sxs-lookup"><span data-stu-id="b821a-148">**GCC High**</span></span> | <span data-ttu-id="b821a-149">Azure Active Directory、Azure Communications Service、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business</span><span class="sxs-lookup"><span data-stu-id="b821a-149">Azure Active Directory, Azure Communications Service, Exchange Online, Forms, Microsoft Defender for Office 365, Microsoft Teams, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business</span></span> |
| <span data-ttu-id="b821a-150">**DoD**</span><span class="sxs-lookup"><span data-stu-id="b821a-150">**DoD**</span></span> | <span data-ttu-id="b821a-151">Azure Active Directory、Azure Communications Service、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power BI、SharePoint Online、Skype for Business</span><span class="sxs-lookup"><span data-stu-id="b821a-151">Azure Active Directory, Azure Communications Service, Exchange Online, Forms, Microsoft Defender for Office 365, Microsoft Teams, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, Power BI, SharePoint Online, Skype for Business</span></span> |

### <a name="office-365-audits-reports-and-certificates"></a><span data-ttu-id="b821a-152">Office 365 監査、レポート、証明書</span><span class="sxs-lookup"><span data-stu-id="b821a-152">Office 365 audits, reports, and certificates</span></span>

<span data-ttu-id="b821a-153">Microsoft クラウド サービスは、年 1 回、ISO/IEC 27001:2013 の認定プロセスの一環として、ISO/IEC 27017:2015 実施基準に関する監査を受けています。</span><span class="sxs-lookup"><span data-stu-id="b821a-153">Microsoft cloud services are audited once a year for the ISO/IEC 27017:2015 code of practice as part of the certification process for ISO/IEC 27001:2013.</span></span>

- [<span data-ttu-id="b821a-154">Office 365: ISO 27001、27018、27017 監査評価レポート</span><span class="sxs-lookup"><span data-stu-id="b821a-154">Office 365: ISO 27001, 27018, and 27017 Audit Assessment Report</span></span>](https://aka.ms/o365isoreport)

### <a name="frequently-asked-questions"></a><span data-ttu-id="b821a-155">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="b821a-155">Frequently asked questions</span></span>

<span data-ttu-id="b821a-156">**この標準はだれに適用されますか?**</span><span class="sxs-lookup"><span data-stu-id="b821a-156">**To whom does the standard apply?**</span></span>

<span data-ttu-id="b821a-157">この実施基準では、クラウド サービス プロバイダーとクラウド サービスお客様の両方にコントロールと実装のガイダンスが提供されています。</span><span class="sxs-lookup"><span data-stu-id="b821a-157">This code of practice provides controls and implementation guidance for both cloud service providers and cloud service customers.</span></span> <span data-ttu-id="b821a-158">ISO/IEC 27002:2013 と似た構成になっています。</span><span class="sxs-lookup"><span data-stu-id="b821a-158">It is structured in a format similar to ISO/IEC 27002:2013.</span></span>

<span data-ttu-id="b821a-159">**ISO/IEC 27017:2015 に関するMicrosoftコンプライアンス情報はどこで確認できますか?**</span><span class="sxs-lookup"><span data-stu-id="b821a-159">**Where can I view Microsoft's compliance information for ISO/IEC 27017:2015?**</span></span>

<span data-ttu-id="b821a-160">Azure、Intune、Power BI の [ISO/IEC 27017:2015 認定証](https://aka.ms/azureiso27017)をダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="b821a-160">You can download the [ISO/IEC 27017:2015 certificate](https://aka.ms/azureiso27017) for Azure, Intune, and Power BI.</span></span>

<span data-ttu-id="b821a-161">**Microsoft サービスの ISO/IEC 27017 コンプライアンスを私の組織の認定プロセスに利用できますか?**</span><span class="sxs-lookup"><span data-stu-id="b821a-161">**Can I use the ISO/IEC 27017 compliance of Microsoft services in my organization's certification process?**</span></span>

<span data-ttu-id="b821a-162">はい。</span><span class="sxs-lookup"><span data-stu-id="b821a-162">Yes.</span></span> <span data-ttu-id="b821a-163">ビジネスで求められているのが、Microsoft の適用エンタープライズ クラウド サービスのいずれかに展開されている実装の認定である場合は、Microsoft の関連認定をコンプライアンス評価で利用できます。</span><span class="sxs-lookup"><span data-stu-id="b821a-163">If your business is seeking certification for implementations deployed on any Microsoft in-scope enterprise cloud services, you can use Microsoft's relevant certifications in your compliance assessment.</span></span> <span data-ttu-id="b821a-164">ただし、コンプライアンスや、組織内の統制およびプロセスに関して、実装を評価する査定人の手配の責任は、審査を受ける組織が負うものとします。</span><span class="sxs-lookup"><span data-stu-id="b821a-164">However, you are responsible for engaging an assessor to evaluate your implementation for compliance, and for the controls and processes within your own organization.</span></span>

<span data-ttu-id="b821a-165">**該当する監査レポートのコピーはどのようにして入手できますか?**</span><span class="sxs-lookup"><span data-stu-id="b821a-165">**How can I get copies of the applicable audit reports?**</span></span>

<span data-ttu-id="b821a-166">[Service Trust Portal](https://aka.ms/stphelp) では、独立している第三者監査レポートと他の関連資料が提供されています。</span><span class="sxs-lookup"><span data-stu-id="b821a-166">The [Service Trust Portal](https://aka.ms/stphelp) provides independent, third-party audit reports and other related documentation.</span></span> <span data-ttu-id="b821a-167">このポータルを利用して、お客様の規制要件に役立つ資料をダウンロードおよび確認できます。</span><span class="sxs-lookup"><span data-stu-id="b821a-167">You can use the portal to download and review this documentation for assistance with your own regulatory requirements.</span></span>

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="b821a-168">Microsoft コンプライアンス マネージャーを使用してリスクを評価する</span><span class="sxs-lookup"><span data-stu-id="b821a-168">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="b821a-169">[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b821a-169">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="b821a-170">コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="b821a-170">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="b821a-171">コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。</span><span class="sxs-lookup"><span data-stu-id="b821a-171">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="b821a-172">[コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。</span><span class="sxs-lookup"><span data-stu-id="b821a-172">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

### <a name="resources"></a><span data-ttu-id="b821a-173">リソース</span><span class="sxs-lookup"><span data-stu-id="b821a-173">Resources</span></span>

- [<span data-ttu-id="b821a-174">ISO/IEC 27017:2015 実施基準</span><span class="sxs-lookup"><span data-stu-id="b821a-174">ISO/IEC 27017:2015 code of practice</span></span>](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [<span data-ttu-id="b821a-175">Microsoft オンライン サービス条件</span><span class="sxs-lookup"><span data-stu-id="b821a-175">Microsoft Online Services Terms</span></span>](https://aka.ms/Online-Services-Terms)
- [<span data-ttu-id="b821a-176">Microsoft セキュリティ センターのコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="b821a-176">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
