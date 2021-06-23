---
title: 連邦情報処理標準 (FIPS) 文書 140-2
description: Microsoft は、暗号化モジュールが米国連邦情報処理標準に準拠しているという認定を行います。
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
ms.openlocfilehash: 0838ce11e732f5c6e8c79c40af0e85bff9d22caf
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089731"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a><span data-ttu-id="a5a1e-104">連邦情報処理標準 (FIPS) 文書 140-2</span><span class="sxs-lookup"><span data-stu-id="a5a1e-104">Federal Information Processing Standard (FIPS) Publication 140-2</span></span>

## <a name="fips-140-2-standard-overview"></a><span data-ttu-id="a5a1e-105">FIPS 140-2 標準の概要</span><span class="sxs-lookup"><span data-stu-id="a5a1e-105">FIPS 140-2 standard overview</span></span>

<span data-ttu-id="a5a1e-106">連邦情報処理標準 (FIPS) 文書 140-2 は、1996 年の情報技術管理改革法のセクション 5131 で定義されている情報技術製品の暗号化モジュールの最小セキュリティ要件を定義する米国政府の標準です。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-106">The Federal Information Processing Standard (FIPS) Publication 140-2 is a U.S. government standard that defines minimum security requirements for cryptographic modules in information technology products, as defined in Section 5131 of the Information Technology Management Reform Act of 1996.</span></span>

<span data-ttu-id="a5a1e-107">米国[](https://csrc.nist.gov/Projects/cryptographic-module-validation-program)国立標準技術研究所 (NIST) とカナダサイバーセキュリティセンター (CCCS) の共同取り組みである暗号化モジュール検証プログラム (CMVP) は、暗号化モジュールのセキュリティ要件標準(FIPS 140-2) および関連する FIPS 暗号化標準を検証します。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-107">The [Cryptographic Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP), a joint effort of the U.S. National Institute of Standards and Technology (NIST) and the Canadian Centre for Cyber Security (CCCS), validates cryptographic modules to the *Security Requirements for Cryptographic Modules* standard (i.e., FIPS 140-2) and related FIPS cryptography standards.</span></span> <span data-ttu-id="a5a1e-108">FIPS 140-2 のセキュリティ要件は、暗号化モジュールの設計と実装に関連する 11 の領域をカバーします。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-108">The FIPS 140-2 security requirements cover 11 areas related to the design and implementation of a cryptographic module.</span></span> <span data-ttu-id="a5a1e-109">NIST Information Technology Laboratory は、モジュール内の FIPS 承認済み暗号化アルゴリズムを検証する関連プログラムを運営しています。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-109">The NIST Information Technology Laboratory operates a related program that validates the FIPS approved cryptographic algorithms in the module.</span></span>

## <a name="microsofts-approach-to-fips-140-2-validation"></a><span data-ttu-id="a5a1e-110">FIPS 140-2 検証に対する Microsoft のアプローチ</span><span class="sxs-lookup"><span data-stu-id="a5a1e-110">Microsoft's approach to FIPS 140-2 validation</span></span>

<span data-ttu-id="a5a1e-111">Microsoft は、2001 年の標準の初めから暗号化モジュールを検証し、140-2 の要件を満たすという積極的な取り組みを維持しています。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-111">Microsoft maintains an active commitment to meeting the 140-2 requirements, having validated cryptographic modules since the standard's inception in 2001.</span></span> <span data-ttu-id="a5a1e-112">Microsoft は、国立標準技術研究所 (NIST) 暗号化モジュール検証プログラム[](https://csrc.nist.gov/Projects/cryptographic-module-validation-program)(CMVP) の下で暗号化モジュールを検証します。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-112">Microsoft validates its cryptographic modules under the National Institute of Standards and Technology (NIST) [Cryptographic Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP).</span></span> <span data-ttu-id="a5a1e-113">多くのクラウド サービスを含む複数の Microsoft 製品では、これらの暗号化モジュールを使用します。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-113">Multiple Microsoft products, including many cloud services, use these cryptographic modules.</span></span>

<span data-ttu-id="a5a1e-114">Microsoft Windows 暗号化モジュール、各モジュールのセキュリティ ポリシー、および CMVP 証明書の詳細のカタログに関する技術情報については、「Windows および[Windows Server FIPS 140-2](https://aka.ms/AA6ehud)コンテンツ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-114">For technical information on Microsoft Windows cryptographic modules, the security policy for each module, and the catalog of CMVP certificate details, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="a5a1e-115">対象となる Microsoft のクラウド サービス</span><span class="sxs-lookup"><span data-stu-id="a5a1e-115">Microsoft in-scope cloud services</span></span>

<span data-ttu-id="a5a1e-116">現在の CMVP FIPS 140-2 実装ガイダンスでは、クラウド サービス自体に対する FIPS 140-2 の検証が行えなっています。クラウド サービス プロバイダーは、クラウド サービスを構成するコンピューティング要素の FIPS 140 検証済み暗号化モジュールを取得して運用できます。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-116">While the current CMVP FIPS 140-2 implementation guidance precludes a FIPS 140-2 validation for a cloud service itself; cloud service providers can choose to obtain and operate FIPS 140 validated cryptographic modules for the computing elements that comprise their cloud service.</span></span> <span data-ttu-id="a5a1e-117">FIPS 140-2 が検証されているコンポーネントを含む Microsoft オンライン サービスには、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-117">Microsoft online services that include components, which have been FIPS 140-2 validated include, among others:</span></span>

- [<span data-ttu-id="a5a1e-118">Azure および Azure Government</span><span class="sxs-lookup"><span data-stu-id="a5a1e-118">Azure and Azure Government</span></span>](/azure/azure-government/documentation-government-plan-security)
- [<span data-ttu-id="a5a1e-119">Dynamics 365 および Dynamics 365 Government</span><span class="sxs-lookup"><span data-stu-id="a5a1e-119">Dynamics 365 and Dynamics 365 Government</span></span>](/microsoft-365/compliance/office-365-encryption-in-microsoft-dynamics-365)
- [<span data-ttu-id="a5a1e-120">Office 365、Office 365 U.S. Government、Office 365 U.S. Government Defense</span><span class="sxs-lookup"><span data-stu-id="a5a1e-120">Office 365, Office 365 U.S. Government, and Office 365 U.S. Government Defense</span></span>](/microsoft-365/compliance/office-365-encryption-risks-and-protections)

## <a name="frequently-asked-questions"></a><span data-ttu-id="a5a1e-121">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="a5a1e-121">Frequently asked questions</span></span>

<span data-ttu-id="a5a1e-122">**'FIPS 140 Validated" と 'FIPS 140 準拠" の違いは何ですか?**</span><span class="sxs-lookup"><span data-stu-id="a5a1e-122">**What is the difference between 'FIPS 140 Validated” and 'FIPS 140 compliant”?**</span></span>

<span data-ttu-id="a5a1e-123">'FIPS 140 Validated" は、暗号化モジュールまたはモジュールを埋め込む製品が、FIPS 140-2 の要件を満たすとして CMVP によって検証 ('認定") されたという意味です。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-123">'FIPS 140 Validated” means that the cryptographic module, or a product that embeds the module has been validated ('certified”) by the CMVP as meeting the FIPS 140-2 requirements.</span></span> <span data-ttu-id="a5a1e-124">「FIPS 140 準拠」は、暗号化機能のために FIPS 140 検証済み製品に依存する IT 製品の業界用語です。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-124">'FIPS 140 compliant” is an industry term for IT products that rely on FIPS 140 Validated products for cryptographic functionality.</span></span>

<span data-ttu-id="a5a1e-125">**Microsoft が FIPS 140 検証を行うのは、いつですか?**</span><span class="sxs-lookup"><span data-stu-id="a5a1e-125">**When does Microsoft undertake a FIPS 140 validation?**</span></span>

<span data-ttu-id="a5a1e-126">モジュール検証を開始する場合のケイデンスは、サーバーとサーバーのWindows 10にWindowsします。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-126">The cadence for starting a module validation aligns with the feature updates of Windows 10 and Windows Server.</span></span> <span data-ttu-id="a5a1e-127">ソフトウェア業界の進化に合って、オペレーティング システムは月次のソフトウェア更新プログラムを使用して、より頻繁にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-127">As the software industry evolved, operating systems are released more frequently, with monthly software updates.</span></span> <span data-ttu-id="a5a1e-128">Microsoft は機能リリースの検証を行いますが、リリースの間に暗号化モジュールへの変更を最小限に抑えます。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-128">Microsoft undertakes validation for feature releases, but in between releases, seeks to minimize the changes to the cryptographic modules.</span></span>

<span data-ttu-id="a5a1e-129">**FIPS 140 検証に含まれるコンピューター**</span><span class="sxs-lookup"><span data-stu-id="a5a1e-129">**Which computers are included in a FIPS 140 validation?**</span></span>

<span data-ttu-id="a5a1e-130">Microsoft は、サーバーとサーバーで実行されているハードウェア構成の代表的なWindows 10検証Windowsします。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-130">Microsoft validates cryptographic modules on a representative sample of hardware configurations running Windows 10 and Windows Server.</span></span> <span data-ttu-id="a5a1e-131">環境がハードウェアを使用する場合、この FIPS 140-2 検証を受け入れるのは、検証プロセスに使用されるサンプルと似ています。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-131">It is common industry practice to accept this FIPS 140-2 validation when an environment uses hardware, which is similar to the samples used for the validation process.</span></span>

<span data-ttu-id="a5a1e-132">**NIST Web サイトには多数のモジュールがリストされています。自分の代理店に適用される対象を知る方法**</span><span class="sxs-lookup"><span data-stu-id="a5a1e-132">**There are many modules listed on the NIST website. How do I know which one applies to my agency?**</span></span>

<span data-ttu-id="a5a1e-133">FIPS 140-2 で検証された暗号化モジュールを使用する必要がある場合は、使用するバージョンが検証リストに表示されるのを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-133">If you are required to use cryptographic modules validated through FIPS 140-2, you need to verify that the version you use appears on the validation list.</span></span> <span data-ttu-id="a5a1e-134">CMVP と Microsoft は、製品リリース別に整理された検証済み暗号化モジュールの一覧と、Windows システムにインストールされているモジュールを識別する手順を管理します。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-134">The CMVP and Microsoft maintain a list of validated cryptographic modules, organized by product release, along with instructions for identifying which modules are installed on a Windows system.</span></span> <span data-ttu-id="a5a1e-135">準拠するシステムを構成する方法の詳細については、「Windowsサーバー [FIPS 140-2 Windows」を参照してください](https://aka.ms/AA6ehud)。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-135">For more information on configuring systems to be compliant, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

<span data-ttu-id="a5a1e-136">**証明書で 'FIPS モードで動作する場合' とはどういう意味ですか?**</span><span class="sxs-lookup"><span data-stu-id="a5a1e-136">**What does 'When operated in FIPS mode' mean on a certificate?**</span></span>

<span data-ttu-id="a5a1e-137">この警告は、FIPS 140-2 セキュリティ ポリシーと一致する方法で暗号化モジュールを使用するために必要な構成およびセキュリティ ルールに従う必要があるという情報を読み取り者に通知します。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-137">This caveat informs the reader that required configuration and security rules must be followed to use the cryptographic module in a way that is consistent with its FIPS 140-2 security policy.</span></span> <span data-ttu-id="a5a1e-138">各モジュールには、独自のセキュリティ ポリシー (動作するセキュリティ ルールの正確な仕様) が用意され、承認された暗号化アルゴリズム、暗号化キー管理、および認証手法が採用されています。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-138">Each module has its own security policy — a precise specification of the security rules under which it will operate — and employs approved cryptographic algorithms, cryptographic key management, and authentication techniques.</span></span> <span data-ttu-id="a5a1e-139">セキュリティ ルールは、各モジュールのセキュリティ ポリシーで定義されます。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-139">The security rules are defined in the security policy for each module.</span></span> <span data-ttu-id="a5a1e-140">CMVP を通じて検証された各モジュールのセキュリティ ポリシーへのリンクを含む詳細については、「Windows および[Windows Server FIPS 140-2](https://aka.ms/AA6ehud)コンテンツ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-140">For more information, including links to the security policy for each module validated through the CMVP, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

<span data-ttu-id="a5a1e-141">**FedRAMP は FIPS 140-2 検証を必要としますか?**</span><span class="sxs-lookup"><span data-stu-id="a5a1e-141">**Does FedRAMP require FIPS 140-2 validation?**</span></span>

<span data-ttu-id="a5a1e-142">はい、連邦リスクおよび承認管理プログラム (FedRAMP) は [、NIST SP 800-53](https://nvd.nist.gov/800-53/Rev4/)リビジョン 4 で定義された制御基準に依存しています。FIPS 検証された暗号化または NSA 承認済み暗号化の使用を要求する [SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) 暗号化保護を含みます。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-142">Yes, the Federal Risk and Authorization Management Program (FedRAMP) relies on control baselines defined by the [NIST SP 800-53 Revision 4](https://nvd.nist.gov/800-53/Rev4/), including [SC-13 Cryptographic Protection](https://nvd.nist.gov/800-53/Rev4/control/SC-13) mandating the use of FIPS-validated cryptography or NSA-approved cryptography.</span></span>

<span data-ttu-id="a5a1e-143">**FIPS 140-2 Microsoft Azureサポートする方法**</span><span class="sxs-lookup"><span data-stu-id="a5a1e-143">**How does Microsoft Azure support FIPS 140-2?**</span></span>

<span data-ttu-id="a5a1e-144">Azure は、ハードウェア、商用利用可能なオペレーティング システム (Linux および Windows)、および Azure 固有のバージョンのアプリケーションを組み合わせてWindows。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-144">Azure is built with a combination of hardware, commercially available operating systems (Linux and Windows), and Azure-specific version of Windows.</span></span> <span data-ttu-id="a5a1e-145">Microsoft [Security Development Lifecycle](https://www.microsoft.com/securityengineering/sdl/) (SDL) を通じて、すべての Azure サービスは、ハイパー スケール クラウドでの運用中に FIPS 140-2 承認済みアルゴリズムを使用するオペレーティング システムのため、データ セキュリティに FIPS 140-2 承認済みアルゴリズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-145">Through the Microsoft [Security Development Lifecycle](https://www.microsoft.com/securityengineering/sdl/) (SDL), all Azure services use FIPS 140-2 approved algorithms for data security because the operating system uses FIPS 140-2 approved algorithms while operating at a hyper scale cloud.</span></span>

<span data-ttu-id="a5a1e-146">**代理店の認定プロセスで Microsoft の FIPS 140-2 への準拠を使用できますか?**</span><span class="sxs-lookup"><span data-stu-id="a5a1e-146">**Can I use Microsoft's adherence to FIPS 140-2 in my agency's certification process?**</span></span>

<span data-ttu-id="a5a1e-147">FIPS 140-2 に準拠するには、暗号化モジュールが FIPS 承認済みアルゴリズムのみを使用するように、FIPS 承認済み操作モードで実行するようにシステムを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-147">To comply with FIPS 140-2, your system must be configured to run in a FIPS approved mode of operation, which includes ensuring that a cryptographic module uses only FIPS-approved algorithms.</span></span> <span data-ttu-id="a5a1e-148">準拠するシステムを構成する方法の詳細については、「Windowsサーバー [FIPS 140-2 Windows」を参照してください](https://aka.ms/AA6ehud)。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-148">For more information on configuring systems to be compliant, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

<span data-ttu-id="a5a1e-149">**FIPS 140-2 と共通の条件の関係は何ですか?**</span><span class="sxs-lookup"><span data-stu-id="a5a1e-149">**What is the relationship between FIPS 140-2 and Common Criteria?**</span></span>

<span data-ttu-id="a5a1e-150">これらは、2 つの独立したセキュリティ標準で、相互に補完的な目的が異なります。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-150">These are two separate security standards with different, but complementary, purposes.</span></span> <span data-ttu-id="a5a1e-151">FIPS 140-2 はソフトウェアとハードウェアの暗号化モジュールを検証するために特別に設計され、Common Criteria は IT ソフトウェアおよびハードウェア製品のセキュリティ機能を評価するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-151">FIPS 140-2 is designed specifically for validating software and hardware cryptographic modules, while the Common Criteria is designed to evaluate security functions in IT software and hardware products.</span></span> <span data-ttu-id="a5a1e-152">一般的な Criteria 評価は、基本的な暗号化機能が適切に実装されていることを保証するために、FIPS 140-2 検証に依存する場合が多い。</span><span class="sxs-lookup"><span data-stu-id="a5a1e-152">Common Criteria evaluations often rely on FIPS 140-2 validations to provide assurance that basic cryptographic functionality is implemented properly.</span></span>

## <a name="resources"></a><span data-ttu-id="a5a1e-153">リソース</span><span class="sxs-lookup"><span data-stu-id="a5a1e-153">Resources</span></span>

- [<span data-ttu-id="a5a1e-154">FIPS Pub 140-2 暗号化モジュールのセキュリティ要件</span><span class="sxs-lookup"><span data-stu-id="a5a1e-154">FIPS Pub 140-2 Security Requirements for Cryptographic Modules</span></span>](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [<span data-ttu-id="a5a1e-155">NIST 暗号化モジュール検証プログラム</span><span class="sxs-lookup"><span data-stu-id="a5a1e-155">NIST Cryptographic Module Validation Program</span></span>](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [<span data-ttu-id="a5a1e-156">Windows、Windows サーバー、および FIPS 140-2</span><span class="sxs-lookup"><span data-stu-id="a5a1e-156">Windows, Windows Server, and FIPS 140-2</span></span>](/windows/security/threat-protection/fips-140-validation)
- [<span data-ttu-id="a5a1e-157">Microsoft Trust Center のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="a5a1e-157">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
