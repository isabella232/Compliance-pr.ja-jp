---
title: 犯罪犯罪情報サービス (CJIS) のセキュリティ ポリシー
description: Microsoft 政府機関向けクラウド サービスは、米国の犯罪犯罪情報サービスのセキュリティ ポリシーに準拠しています。
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
ms.openlocfilehash: 0a8cc37a24d3a51d79fb1ac34c92d96fc7e76fdd
ms.sourcegitcommit: 66a26facea6ec9a95e5e61f1b5b69402f03db481
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "50279844"
---
# <a name="criminal-justice-information-services-cjis-security-policy"></a><span data-ttu-id="ea2dd-104">犯罪犯罪情報サービス (CJIS) のセキュリティ ポリシー</span><span class="sxs-lookup"><span data-stu-id="ea2dd-104">Criminal Justice Information Services (CJIS) Security Policy</span></span>

## <a name="cjis-overview"></a><span data-ttu-id="ea2dd-105">CJIS の概要</span><span class="sxs-lookup"><span data-stu-id="ea2dd-105">CJIS overview</span></span>

<span data-ttu-id="ea2dd-106">米国連邦捜査局 (FBI) の犯罪犯罪情報サービス (CJIS) 部門は、州、地方、連邦法執行機関、および連邦法執行機関および犯罪訴訟機関に、指紋記録や犯罪履歴など、犯罪犯罪情報 (CJI) へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-106">The Criminal Justice Information Services (CJIS) Division of the US Federal Bureau of Investigation (FBI) gives state, local, and federal law enforcement and criminal justice agencies access to criminal justice information (CJI) — for example, fingerprint records and criminal histories.</span></span> <span data-ttu-id="ea2dd-107">米国の法執行機関および他の政府機関は、CJI の転送、保管、または処理にクラウド サービスを使用する方法が [CJIS](https://aka.ms/cjis-security-policy)セキュリティ ポリシーに準拠していることを確認する必要があります。CJI を保護するための最低限のセキュリティ要件と制御を確立します。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-107">Law enforcement and other government agencies in the United States must ensure that their use of cloud services for the transmission, storage, or processing of CJI complies with the [CJIS Security Policy](https://aka.ms/cjis-security-policy), which establishes minimum security requirements and controls to safeguard CJI.</span></span>

<span data-ttu-id="ea2dd-108">CJIS セキュリティ ポリシーは、米国標準技術協会 (NIST) のガイダンスと共に、連邦法、連邦法、および犯罪コミュニティの勧告ポリシー委員会の決定を統合します。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-108">The CJIS Security Policy integrates presidential and FBI directives, federal laws, and the criminal justice community's Advisory Policy Board decisions, along with guidance from the National Institute of Standards and Technology (NIST).</span></span> <span data-ttu-id="ea2dd-109">ポリシーは、進化するセキュリティ要件を反映して定期的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-109">The Policy is periodically updated to reflect evolving security requirements.</span></span>

<span data-ttu-id="ea2dd-110">CJIS セキュリティ ポリシーでは、クラウド サービス プロバイダーなどの私的請負業者が、クラウド サービスの使用が CJIS の要件と一致できるかどうかを判断するために評価する必要がある 13 の領域が定義されています。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-110">The CJIS Security Policy defines 13 areas that private contractors such as cloud service providers must evaluate to determine if their use of cloud services can be consistent with CJIS requirements.</span></span> <span data-ttu-id="ea2dd-111">これらの分野は NIST 800-53 と密接に対応しています。これは、米国連邦政府のリスク/承認管理プログラム [(FedRAMP)](offering-FedRAMP.md)の基礎で、Microsoft が政府機関向けクラウド製品の認定を受けたプログラムです。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-111">These areas correspond closely to NIST 800-53, which is also the basis for the [Federal Risk and Authorization Management Program (FedRAMP)](offering-FedRAMP.md), a program under which Microsoft has been certified for its Government Cloud offerings.</span></span>

<span data-ttu-id="ea2dd-112">さらに、CJI を処理するすべての私的請負業者は、米国弁護士総長によって承認された統一された合意である CJIS セキュリティに関する追加文書に署名する必要があります。これは、セキュリティ ポリシーで必要とされる CJI のセキュリティと機密性を確保するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-112">In addition, all private contractors who process CJI must sign the CJIS Security Addendum, a uniform agreement approved by the US Attorney General that helps ensure the security and confidentiality of CJI required by the Security Policy.</span></span> <span data-ttu-id="ea2dd-113">また、請負業者は、連邦法および州法、規制、基準と一致するセキュリティ プログラムを維持し、CJI の使用を政府機関が提供した目的に限定します。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-113">It also commits the contractor to maintaining a security program consistent with federal and state laws, regulations, and standards, and limits the use of CJI to the purposes for which a government agency provided it.</span></span>

## <a name="microsoft-and-cjis-security-policy"></a><span data-ttu-id="ea2dd-114">Microsoft と CJIS のセキュリティ ポリシー</span><span class="sxs-lookup"><span data-stu-id="ea2dd-114">Microsoft and CJIS Security Policy</span></span>

<span data-ttu-id="ea2dd-115">Microsoft は、CJIS 情報契約を使用して、州で CJIS セキュリティに関する追加的な署名を行います。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-115">Microsoft signs the CJIS Security Addendum in states with CJIS Information Agreements.</span></span> <span data-ttu-id="ea2dd-116">これらは、CJIS セキュリティ ポリシーの遵守を担当する州法執行機関に、Microsoft のクラウド セキュリティ コントロールがデータのライフサイクル全体を保護し、CJI にアクセスできる運用担当者の適切なバックグラウンド スクリーン処理を行う方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-116">These tell state law enforcement authorities responsible for compliance with CJIS Security Policy how Microsoft's cloud security controls help protect the full lifecycle of data and ensure appropriate background screening of operating personnel with access to CJI.</span></span> <span data-ttu-id="ea2dd-117">Microsoft は引き続き州政府と一緒に CJIS 情報契約を締結しています。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-117">Microsoft continues to work with state governments to enter into CJIS Information Agreements.</span></span>

<span data-ttu-id="ea2dd-118">Microsoft は、Microsoft Azure Government、Microsoft Office 365 U.S. Government、および Microsoft Dynamics 365 U.S. Government の運用ポリシーと手順を評価し、対象サービスの使用に関する FBI 要件を満たすために該当するサービス契約の能力を証明します。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-118">Microsoft has assessed the operational policies and procedures of Microsoft Azure Government, Microsoft Office 365 U.S. Government, and Microsoft Dynamics 365 U.S. Government, and will attest to their ability in the applicable services agreements to meet FBI requirements for the use of in-scope services.</span></span>

<span data-ttu-id="ea2dd-119">Microsoft Cloud での CJIS セキュリティ ポリシーの利点について [説明します。](https://customers.microsoft.com/story/genetec)</span><span class="sxs-lookup"><span data-stu-id="ea2dd-119">Learn about the benefits of CJIS Security policy on the Microsoft Cloud: [Read how Genetec cleared criminal investigations](https://customers.microsoft.com/story/genetec)</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="ea2dd-120">対象となる Microsoft のクラウド サービス</span><span class="sxs-lookup"><span data-stu-id="ea2dd-120">Microsoft in-scope cloud services</span></span>

- [<span data-ttu-id="ea2dd-121">Azure Government</span><span class="sxs-lookup"><span data-stu-id="ea2dd-121">Azure Government</span></span>](/azure/azure-government/documentation-government-welcome)
- [<span data-ttu-id="ea2dd-122">Dynamics 365 U.S. Government</span><span class="sxs-lookup"><span data-stu-id="ea2dd-122">Dynamics 365 U.S. Government</span></span>](/power-platform/admin/microsoft-dynamics-365-government#certifications-and-accreditations)
- [<span data-ttu-id="ea2dd-123">Office 365 U.S. Government</span><span class="sxs-lookup"><span data-stu-id="ea2dd-123">Office 365 U.S. Government</span></span>](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/gcc#us-government-community-compliance)
- <span data-ttu-id="ea2dd-124">Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに搭載されているサービス)</span><span class="sxs-lookup"><span data-stu-id="ea2dd-124">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>

## <a name="audits-reports-and-certificates"></a><span data-ttu-id="ea2dd-125">監査、レポート、証明書</span><span class="sxs-lookup"><span data-stu-id="ea2dd-125">Audits, reports, and certificates</span></span>

<span data-ttu-id="ea2dd-126">FBI は、CJIS 要件に準拠した Microsoft の認定を提供していない。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-126">The FBI does not offer certification of Microsoft compliance with CJIS requirements.</span></span> <span data-ttu-id="ea2dd-127">代わりに、マイクロソフトの構成証明は、Microsoft と州の CJIS 機関との間、および Microsoft とそのお客様との間の契約に含まれています。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-127">Instead, a Microsoft attestation is included in agreements between Microsoft and a state's CJIS authority, and between Microsoft and its customers.</span></span>

[<span data-ttu-id="ea2dd-128">Microsoft CJIS クラウド要件</span><span class="sxs-lookup"><span data-stu-id="ea2dd-128">Microsoft CJIS Cloud Requirements</span></span>](https://aka.ms/MicrosoftCJISCloudRequirements)

## <a name="cjis-status-in-the-united-states-current-as-of-1152020"></a><span data-ttu-id="ea2dd-129">米国での CJIS の状態 (2020 年 11 月 5 日現在)</span><span class="sxs-lookup"><span data-stu-id="ea2dd-129">CJIS status in the United States (current as of 11/5/2020)</span></span>

<span data-ttu-id="ea2dd-130">44 州と管理契約を持つコロンビア特別区は、緑色で強調表示されています。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-130">44 states and the District of Columbia with management agreements, highlighted on the map in green include:</span></span>

<span data-ttu-id="ea2dd-131">アラバマ、カンソー島、アーカンソー州、カリフォルニア州、カリフォルニア州、コネチカット州、ジョージア州、ジョージア州、イダホ州、カンザス州、インドナ州 アイオワ、カンザッシー、メイン、マシトン、ナズン、ミネソタ、ミシシピ、ビルト、モンナ、ネブラカ、立ち上げ、ニューペンシア州、ニュージャージ州、ニューヨーク州、北地方、北ダコタ島、オクラホマ州、Oregon、Ipde アイランド、南アフリカ、テネシー州、テキサス州、ワシントン州、ワシントン州、西区、Wisconsin、および、[分区]</span><span class="sxs-lookup"><span data-stu-id="ea2dd-131">Alabama, Alaska, Arizona, Arkansas, California, Colorado, Connecticut, Florida, Georgia, Hawaii, Idaho, Illinois, Indiana, Iowa, Kansas, Kentucky, Maine, Massachusetts, Michigan, Minnesota, Mississippi, Missouri, Montana, Nebraska, Nevada, New Hampshire, New Jersey, New York, North Carolina, North Dakota, Oklahoma, Oregon, Pennsylvania, Rhode Island, South Carolina, Tennessee, Texas, Utah, Vermont, Virginia, Washington, West Virginia, Wisconsin, and the District of Columbia.</span></span>

<span data-ttu-id="ea2dd-132">適用される CJIS 規制の遵守に対する Microsoft の取り組みにより、犯罪犯罪組織はクラウドベースのソリューションを実装し、CJIS セキュリティ ポリシー V5.8 に準拠することができます。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-132">Microsoft's commitment to meeting the applicable CJIS regulatory controls allows Criminal Justice organizations to implement cloud-based solutions and be compliant with CJIS Security Policy V5.8.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="ea2dd-133">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="ea2dd-133">Frequently asked questions</span></span>

<span data-ttu-id="ea2dd-134">**コンプライアンス情報を要求できる場所**</span><span class="sxs-lookup"><span data-stu-id="ea2dd-134">**Where can I request compliance information?**</span></span>

<span data-ttu-id="ea2dd-135">関心のある管轄区域に関する情報については、Microsoft アカウントの担当者にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-135">Contact your Microsoft account representative for information on the jurisdiction you are interested in.</span></span> <span data-ttu-id="ea2dd-136">現在 <cjis@microsoft.com> 利用できるサービスの状態に関する情報については、お問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-136">Contact <cjis@microsoft.com> for information on which services are currently available in which states.</span></span>

<span data-ttu-id="ea2dd-137">**Microsoft は、そのクラウド サービスが州の要件への準拠を可能にしていることをどのように実証しますか?**</span><span class="sxs-lookup"><span data-stu-id="ea2dd-137">**How does Microsoft demonstrate that its cloud services enable compliance with my state's requirements?**</span></span>

<span data-ttu-id="ea2dd-138">Microsoft は、CJIS Systems Agency (CSA) 州と情報契約を締結しています。お客様は、お客様の状態の CSA にコピーを要求できます。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-138">Microsoft signs an Information Agreement with a state CJIS Systems Agency (CSA); you may request a copy from your state's CSA.</span></span> <span data-ttu-id="ea2dd-139">さらに、Microsoft は、セキュリティ、プライバシー、コンプライアンスに関する詳細な情報をお客様に提供します。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-139">In addition, Microsoft provides customers with in-depth security, privacy, and compliance information.</span></span> <span data-ttu-id="ea2dd-140">お客様は、独立監査人が作成したセキュリティおよびコンプライアンスレポートを確認して、Microsoft が関連する監査範囲に適したセキュリティコントロール (ISO 27001 など) を実装したと検証することもできます。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-140">Customers may also review security and compliance reports prepared by independent auditors so they can validate that Microsoft has implemented security controls (such as ISO 27001) appropriate to the relevant audit scope.</span></span>

<span data-ttu-id="ea2dd-141">**私のエージェンシーのコンプライアンス活動はどこから始めできますか?**</span><span class="sxs-lookup"><span data-stu-id="ea2dd-141">**Where do I start with my agency's compliance effort?**</span></span>

<span data-ttu-id="ea2dd-142">[CJIS セキュリティ ポリシーでは](https://aka.ms/cjis-security-policy) 、CJI を保護するために機関が講じなければならない予防措置について説明します。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-142">[CJIS Security Policy](https://aka.ms/cjis-security-policy) covers the precautions that your agency must take to protect CJI.</span></span> <span data-ttu-id="ea2dd-143">さらに、Microsoft アカウント担当者は、お客様の管轄区域の要件に精通しているユーザーと連絡を取り合えます。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-143">In addition, your Microsoft account representative can put you in touch with those familiar with the requirements of your jurisdiction</span></span>

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="ea2dd-144">Microsoft コンプライアンス マネージャーを使用してリスクを評価する</span><span class="sxs-lookup"><span data-stu-id="ea2dd-144">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="ea2dd-145">[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-145">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="ea2dd-146">コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-146">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="ea2dd-147">コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-147">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="ea2dd-148">[コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。</span><span class="sxs-lookup"><span data-stu-id="ea2dd-148">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

## <a name="resources"></a><span data-ttu-id="ea2dd-149">リソース</span><span class="sxs-lookup"><span data-stu-id="ea2dd-149">Resources</span></span>

- [<span data-ttu-id="ea2dd-150">犯罪犯罪情報サービス</span><span class="sxs-lookup"><span data-stu-id="ea2dd-150">Criminal Justice Information Services</span></span>](https://aka.ms/cjis)
- [<span data-ttu-id="ea2dd-151">CJIS セキュリティ ポリシー</span><span class="sxs-lookup"><span data-stu-id="ea2dd-151">CJIS Security Policy</span></span>](https://aka.ms/cjis-security-policy)
- [<span data-ttu-id="ea2dd-152">Azure Government の CJIS 実装ガイドライン</span><span class="sxs-lookup"><span data-stu-id="ea2dd-152">CJIS implementation guidelines for Azure Government</span></span>](https://aka.ms/cjisimplementationguidelines)
- [<span data-ttu-id="ea2dd-153">Microsoft Common Controls Hub コンプライアンス フレームワーク</span><span class="sxs-lookup"><span data-stu-id="ea2dd-153">Microsoft Common Controls Hub Compliance Framework</span></span>](https://www.microsoft.com/trustcenter/common-controls-hub)
- [<span data-ttu-id="ea2dd-154">Microsoft Government クラウド</span><span class="sxs-lookup"><span data-stu-id="ea2dd-154">Microsoft Government Cloud</span></span>](https://go.microsoft.com/fwlink/?linkid=2087246)
- [<span data-ttu-id="ea2dd-155">Microsoft Trust Center のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="ea2dd-155">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
