---
title: 刑事司法情報サービス (CJIS) セキュリティ ポリシー
description: Microsoft Government クラウド サービスは、米国刑事司法情報サービスセキュリティ ポリシーに準拠しています。
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
ms.openlocfilehash: fe96da8b7a8ef89f9dd8ce14573e3489c75f93e7
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087616"
---
# <a name="criminal-justice-information-services-cjis-security-policy"></a><span data-ttu-id="ed2a0-104">刑事司法情報サービス (CJIS) セキュリティ ポリシー</span><span class="sxs-lookup"><span data-stu-id="ed2a0-104">Criminal Justice Information Services (CJIS) Security Policy</span></span>

## <a name="cjis-overview"></a><span data-ttu-id="ed2a0-105">CJIS の概要</span><span class="sxs-lookup"><span data-stu-id="ed2a0-105">CJIS overview</span></span>

<span data-ttu-id="ed2a0-106">米国連邦捜査局 (FBI) の刑事司法情報サービス (CJIS) 部門は、州、地方、および連邦の法執行機関および刑事司法機関に対して、指紋記録や犯罪歴など、刑事司法情報 (CJI) にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-106">The Criminal Justice Information Services (CJIS) Division of the US Federal Bureau of Investigation (FBI) gives state, local, and federal law enforcement and criminal justice agencies access to criminal justice information (CJI) — for example, fingerprint records and criminal histories.</span></span> <span data-ttu-id="ed2a0-107">米国の法執行機関および他の政府機関は、CJI の送信、ストレージ、または処理にクラウド サービスを使用する場合、CJI のセキュリティに関する最低限の要件と管理を確立する [CJIS](https://aka.ms/cjis-security-policy)セキュリティ ポリシーに準拠していることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-107">Law enforcement and other government agencies in the United States must ensure that their use of cloud services for the transmission, storage, or processing of CJI complies with the [CJIS Security Policy](https://aka.ms/cjis-security-policy), which establishes minimum security requirements and controls to safeguard CJI.</span></span>

<span data-ttu-id="ed2a0-108">CJIS セキュリティ ポリシーは、国家標準技術研究所 (NIST) のガイダンスと共に、大統領および FBI 指令、連邦法、刑事司法コミュニティのアドバイザリー ポリシー ボードの決定を統合します。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-108">The CJIS Security Policy integrates presidential and FBI directives, federal laws, and the criminal justice community's Advisory Policy Board decisions, along with guidance from the National Institute of Standards and Technology (NIST).</span></span> <span data-ttu-id="ed2a0-109">ポリシーは、進化するセキュリティ要件を反映するように定期的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-109">The Policy is periodically updated to reflect evolving security requirements.</span></span>

<span data-ttu-id="ed2a0-110">CJIS セキュリティ ポリシーは、クラウド サービス プロバイダーなどの民間請負業者が、クラウド サービスの使用が CJIS 要件と一致できるかどうかを判断するために評価する必要がある 13 の領域を定義します。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-110">The CJIS Security Policy defines 13 areas that private contractors such as cloud service providers must evaluate to determine if their use of cloud services can be consistent with CJIS requirements.</span></span> <span data-ttu-id="ed2a0-111">これらの領域は NIST 800-53 と密接に対応しています。これは、Microsoft が政府機関向けクラウド製品の認定を受けた連邦リスクおよび承認管理プログラム [(FedRAMP)](offering-FedRAMP.md)の基礎にもなっています。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-111">These areas correspond closely to NIST 800-53, which is also the basis for the [Federal Risk and Authorization Management Program (FedRAMP)](offering-FedRAMP.md), a program under which Microsoft has been certified for its Government Cloud offerings.</span></span>

<span data-ttu-id="ed2a0-112">さらに、CJI を処理するすべての民間請負業者は、セキュリティ ポリシーで必要な CJI のセキュリティと機密性の確保に役立つ米国司法長官によって承認された統一契約である CJIS Security Addendum に署名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-112">In addition, all private contractors who process CJI must sign the CJIS Security Addendum, a uniform agreement approved by the US Attorney General that helps ensure the security and confidentiality of CJI required by the Security Policy.</span></span> <span data-ttu-id="ed2a0-113">また、請負業者は、連邦および州の法律、規制、および標準に準拠したセキュリティ プログラムを維持し、CJI の使用を政府機関が提供した目的に限定します。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-113">It also commits the contractor to maintaining a security program consistent with federal and state laws, regulations, and standards, and limits the use of CJI to the purposes for which a government agency provided it.</span></span>

## <a name="microsoft-and-cjis-security-policy"></a><span data-ttu-id="ed2a0-114">Microsoft および CJIS セキュリティ ポリシー</span><span class="sxs-lookup"><span data-stu-id="ed2a0-114">Microsoft and CJIS Security Policy</span></span>

<span data-ttu-id="ed2a0-115">Microsoft は、CJIS 情報契約を使用して州の CJIS セキュリティ アドオンに署名します。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-115">Microsoft signs the CJIS Security Addendum in states with CJIS Information Agreements.</span></span> <span data-ttu-id="ed2a0-116">これらは、CJIS セキュリティ ポリシーの遵守を担当する州の法執行機関に、Microsoft のクラウド セキュリティ制御がデータの完全なライフサイクルを保護し、CJI にアクセスできる運用担当者の適切なバックグラウンド スクリーニングを保証する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-116">These tell state law enforcement authorities responsible for compliance with CJIS Security Policy how Microsoft's cloud security controls help protect the full lifecycle of data and ensure appropriate background screening of operating personnel with access to CJI.</span></span> <span data-ttu-id="ed2a0-117">Microsoft は引き続き州政府と取り組み、CJIS 情報契約を締結しています。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-117">Microsoft continues to work with state governments to enter into CJIS Information Agreements.</span></span>

<span data-ttu-id="ed2a0-118">Microsoft は、Microsoft Azure Government、Microsoft Office 365 米国政府機関、および Microsoft Dynamics 365 米国政府機関の運用ポリシーと手順を評価し、スコープ内サービスの使用に関する FBI 要件を満たす適切なサービス契約における能力を証明します。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-118">Microsoft has assessed the operational policies and procedures of Microsoft Azure Government, Microsoft Office 365 U.S. Government, and Microsoft Dynamics 365 U.S. Government, and will attest to their ability in the applicable services agreements to meet FBI requirements for the use of in-scope services.</span></span>

<span data-ttu-id="ed2a0-119">Microsoft Cloud での CJIS セキュリティ ポリシーの利点について説明します。 Genetec が犯罪捜査をクリアした方法 [を読む](https://customers.microsoft.com/story/genetec)</span><span class="sxs-lookup"><span data-stu-id="ed2a0-119">Learn about the benefits of CJIS Security policy on the Microsoft Cloud: [Read how Genetec cleared criminal investigations](https://customers.microsoft.com/story/genetec)</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="ed2a0-120">対象となる Microsoft のクラウド サービス</span><span class="sxs-lookup"><span data-stu-id="ed2a0-120">Microsoft in-scope cloud services</span></span>

- [<span data-ttu-id="ed2a0-121">Azure Government</span><span class="sxs-lookup"><span data-stu-id="ed2a0-121">Azure Government</span></span>](/azure/azure-government/documentation-government-welcome)
- [<span data-ttu-id="ed2a0-122">Dynamics 365 米国政府機関</span><span class="sxs-lookup"><span data-stu-id="ed2a0-122">Dynamics 365 U.S. Government</span></span>](/power-platform/admin/microsoft-dynamics-365-government#certifications-and-accreditations)
- [<span data-ttu-id="ed2a0-123">Office 365米国政府</span><span class="sxs-lookup"><span data-stu-id="ed2a0-123">Office 365 U.S. Government</span></span>](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/gcc#us-government-community-compliance)
- <span data-ttu-id="ed2a0-124">Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに搭載されているサービス)</span><span class="sxs-lookup"><span data-stu-id="ed2a0-124">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>

## <a name="audits-reports-and-certificates"></a><span data-ttu-id="ed2a0-125">監査、レポート、証明書</span><span class="sxs-lookup"><span data-stu-id="ed2a0-125">Audits, reports, and certificates</span></span>

<span data-ttu-id="ed2a0-126">FBI は、CJIS 要件に準拠した Microsoft の認定を提供していない。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-126">The FBI does not offer certification of Microsoft compliance with CJIS requirements.</span></span> <span data-ttu-id="ed2a0-127">代わりに、Microsoft の構成証明は、Microsoft と州の CJIS 機関との間、および Microsoft とその顧客間の契約に含まれています。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-127">Instead, a Microsoft attestation is included in agreements between Microsoft and a state's CJIS authority, and between Microsoft and its customers.</span></span>

[<span data-ttu-id="ed2a0-128">Microsoft CJIS クラウド要件</span><span class="sxs-lookup"><span data-stu-id="ed2a0-128">Microsoft CJIS Cloud Requirements</span></span>](https://aka.ms/MicrosoftCJISCloudRequirements)

## <a name="cjis-status-in-the-united-states-current-as-of-1152020"></a><span data-ttu-id="ed2a0-129">米国の CJIS ステータス (2020 年 11 月 5 日現在)</span><span class="sxs-lookup"><span data-stu-id="ed2a0-129">CJIS status in the United States (current as of 11/5/2020)</span></span>

<span data-ttu-id="ed2a0-130">45 の州とコロンビア特別区と管理契約が締結され、緑色のマップで強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-130">45 states and the District of Columbia with management agreements, highlighted on the map in green include:</span></span>

<span data-ttu-id="ed2a0-131">アラバマ州、アラスカ州、アリゾナ州、アーカンソー州、カリフォルニア州、コロラド州、コネチカット州、フロリダ州、ジョージア州、ハワイ州、アイダホ州、イリノイ州、インディアナ州、アイオワ州、 カンザス州、ケンタッキー州、メイン州、マサチューセッツ州、ミシガン州、ミネソタ州、ミネソタ州、ミシシッピ州、ミズーリ州、モンタナ州、ネブラスカ州、ネバダ州、ニューハンプシャー州、ニューハンプシャー州、ニューメキシコ州、ニューヨーク州、ノースカロライナ州、ノースダコタ州、オクラホマ州、オレゴン州、ペンシルベニア州、ロードアイランド州、サウスカロライナ州、テネシー州、テキサス州、ユタ州、バージニア州、ワシントン州、ウェストバージニア州、ウィスコンシン州、コロンビア州</span><span class="sxs-lookup"><span data-stu-id="ed2a0-131">Alabama, Alaska, Arizona, Arkansas, California, Colorado, Connecticut, Florida, Georgia, Hawaii, Idaho, Illinois, Indiana, Iowa, Kansas, Kentucky, Maine, Massachusetts, Michigan, Minnesota, Mississippi, Missouri, Montana, Nebraska, Nevada, New Hampshire, New Jersey, New Mexico, New York, North Carolina, North Dakota, Oklahoma, Oregon, Pennsylvania, Rhode Island, South Carolina, Tennessee, Texas, Utah, Vermont, Virginia, Washington, West Virginia, Wisconsin, and the District of Columbia.</span></span>

<span data-ttu-id="ed2a0-132">適用される CJIS 規制規制を遵守する Microsoft の取り組みにより、刑事司法組織はクラウドベースのソリューションを実装し、CJIS セキュリティ ポリシー V5.9 に準拠することができます。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-132">Microsoft's commitment to meeting the applicable CJIS regulatory controls allows Criminal Justice organizations to implement cloud-based solutions and be compliant with CJIS Security Policy V5.9.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="ed2a0-133">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="ed2a0-133">Frequently asked questions</span></span>

<span data-ttu-id="ed2a0-134">**コンプライアンス情報はどこで要求できますか?**</span><span class="sxs-lookup"><span data-stu-id="ed2a0-134">**Where can I request compliance information?**</span></span>

<span data-ttu-id="ed2a0-135">関心のある管轄区域に関する情報については、Microsoft アカウント担当者にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-135">Contact your Microsoft account representative for information on the jurisdiction you are interested in.</span></span> <span data-ttu-id="ed2a0-136">現在 <cjis@microsoft.com> 利用可能なサービスの状態に関する情報については、お問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-136">Contact <cjis@microsoft.com> for information on which services are currently available in which states.</span></span>

<span data-ttu-id="ed2a0-137">**Microsoft は、クラウド サービスが自分の状態の要件に準拠していることをどのように実証しますか?**</span><span class="sxs-lookup"><span data-stu-id="ed2a0-137">**How does Microsoft demonstrate that its cloud services enable compliance with my state's requirements?**</span></span>

<span data-ttu-id="ed2a0-138">Microsoft は、州 CJIS Systems Agency (CSA) と情報契約を締結します。州の CSA からコピーを要求できます。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-138">Microsoft signs an Information Agreement with a state CJIS Systems Agency (CSA); you may request a copy from your state's CSA.</span></span> <span data-ttu-id="ed2a0-139">さらに、Microsoft は、お客様に詳細なセキュリティ、プライバシー、コンプライアンス情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-139">In addition, Microsoft provides customers with in-depth security, privacy, and compliance information.</span></span> <span data-ttu-id="ed2a0-140">また、独立監査人が作成したセキュリティおよびコンプライアンス レポートを確認して、Microsoft が関連する監査範囲に適したセキュリティ制御 (ISO 27001 など) を実装したと検証することもできます。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-140">Customers may also review security and compliance reports prepared by independent auditors so they can validate that Microsoft has implemented security controls (such as ISO 27001) appropriate to the relevant audit scope.</span></span>

<span data-ttu-id="ed2a0-141">**代理店のコンプライアンスの取り組みからどこから始めるのですか?**</span><span class="sxs-lookup"><span data-stu-id="ed2a0-141">**Where do I start with my agency's compliance effort?**</span></span>

<span data-ttu-id="ed2a0-142">[CJIS セキュリティ ポリシーでは、CJI](https://aka.ms/cjis-security-policy) を保護するために代理店が取る必要がある予防措置について説明します。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-142">[CJIS Security Policy](https://aka.ms/cjis-security-policy) covers the precautions that your agency must take to protect CJI.</span></span> <span data-ttu-id="ed2a0-143">さらに、Microsoft アカウント担当者は、お客様の管轄地域の要件に精通しているユーザーと連絡を取り合う場合があります。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-143">In addition, your Microsoft account representative can put you in touch with those familiar with the requirements of your jurisdiction</span></span>

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="ed2a0-144">Microsoft コンプライアンス マネージャーを使用してリスクを評価する</span><span class="sxs-lookup"><span data-stu-id="ed2a0-144">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="ed2a0-145">[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-145">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="ed2a0-146">コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-146">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="ed2a0-147">コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-147">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="ed2a0-148">[コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。</span><span class="sxs-lookup"><span data-stu-id="ed2a0-148">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

## <a name="resources"></a><span data-ttu-id="ed2a0-149">リソース</span><span class="sxs-lookup"><span data-stu-id="ed2a0-149">Resources</span></span>

- [<span data-ttu-id="ed2a0-150">刑事司法情報サービス</span><span class="sxs-lookup"><span data-stu-id="ed2a0-150">Criminal Justice Information Services</span></span>](https://aka.ms/cjis)
- [<span data-ttu-id="ed2a0-151">CJIS セキュリティ ポリシー</span><span class="sxs-lookup"><span data-stu-id="ed2a0-151">CJIS Security Policy</span></span>](https://aka.ms/cjis-security-policy)
- [<span data-ttu-id="ed2a0-152">Azure Government の CJIS 実装ガイドライン</span><span class="sxs-lookup"><span data-stu-id="ed2a0-152">CJIS implementation guidelines for Azure Government</span></span>](https://aka.ms/cjisimplementationguidelines)
- [<span data-ttu-id="ed2a0-153">Microsoft Common Controls Hub コンプライアンス フレームワーク</span><span class="sxs-lookup"><span data-stu-id="ed2a0-153">Microsoft Common Controls Hub Compliance Framework</span></span>](https://www.microsoft.com/trustcenter/common-controls-hub)
- [<span data-ttu-id="ed2a0-154">Microsoft Government クラウド</span><span class="sxs-lookup"><span data-stu-id="ed2a0-154">Microsoft Government Cloud</span></span>](https://go.microsoft.com/fwlink/?linkid=2087246)
- [<span data-ttu-id="ed2a0-155">Microsoft Trust Center のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="ed2a0-155">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
