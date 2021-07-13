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
ms.openlocfilehash: 2c51979122aaedda90bac74740e95c9d1265de74
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385007"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a><span data-ttu-id="beb80-104">連邦情報処理標準 (FIPS) 文書 140-2</span><span class="sxs-lookup"><span data-stu-id="beb80-104">Federal Information Processing Standard (FIPS) Publication 140-2</span></span>

## <a name="fips-140-2-standard-overview"></a><span data-ttu-id="beb80-105">FIPS 140-2 標準の概要</span><span class="sxs-lookup"><span data-stu-id="beb80-105">FIPS 140-2 standard overview</span></span>

<span data-ttu-id="beb80-106">連邦情報処理標準 (FIPS) 文書 140-2 は、1996 年の情報技術管理改革法のセクション 5131 で定義されている情報技術製品の暗号化モジュールの最小セキュリティ要件を定義する米国政府の標準です。</span><span class="sxs-lookup"><span data-stu-id="beb80-106">The Federal Information Processing Standard (FIPS) Publication 140-2 is a U.S. government standard that defines minimum security requirements for cryptographic modules in information technology products, as defined in Section 5131 of the Information Technology Management Reform Act of 1996.</span></span>

<span data-ttu-id="beb80-107">米国[](https://csrc.nist.gov/Projects/cryptographic-module-validation-program)国立標準技術研究所 (NIST) とカナダサイバーセキュリティセンター (CCCS) の共同取り組みである暗号化モジュール検証プログラム (CMVP) は、暗号化モジュールのセキュリティ要件標準(FIPS 140-2) および関連する FIPS 暗号化標準を検証します。</span><span class="sxs-lookup"><span data-stu-id="beb80-107">The [Cryptographic Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP), a joint effort of the U.S. National Institute of Standards and Technology (NIST) and the Canadian Centre for Cyber Security (CCCS), validates cryptographic modules to the *Security Requirements for Cryptographic Modules* standard (i.e., FIPS 140-2) and related FIPS cryptography standards.</span></span> <span data-ttu-id="beb80-108">FIPS 140-2 のセキュリティ要件は、暗号化モジュールの設計と実装に関連する 11 の領域をカバーします。</span><span class="sxs-lookup"><span data-stu-id="beb80-108">The FIPS 140-2 security requirements cover 11 areas related to the design and implementation of a cryptographic module.</span></span> <span data-ttu-id="beb80-109">NIST Information Technology Laboratory は、モジュール内の FIPS 承認済み暗号化アルゴリズムを検証する関連プログラムを運営しています。</span><span class="sxs-lookup"><span data-stu-id="beb80-109">The NIST Information Technology Laboratory operates a related program that validates the FIPS approved cryptographic algorithms in the module.</span></span>

## <a name="microsofts-approach-to-fips-140-2-validation"></a><span data-ttu-id="beb80-110">FIPS 140-2 検証に対する Microsoft のアプローチ</span><span class="sxs-lookup"><span data-stu-id="beb80-110">Microsoft's approach to FIPS 140-2 validation</span></span>

<span data-ttu-id="beb80-111">Microsoft は、2001 年の標準の初めから暗号化モジュールを検証し、140-2 の要件を満たすという積極的な取り組みを維持しています。</span><span class="sxs-lookup"><span data-stu-id="beb80-111">Microsoft maintains an active commitment to meeting the 140-2 requirements, having validated cryptographic modules since the standard's inception in 2001.</span></span> <span data-ttu-id="beb80-112">Microsoft は、国立標準技術研究所 (NIST) 暗号化モジュール検証プログラム[](https://csrc.nist.gov/Projects/cryptographic-module-validation-program)(CMVP) の下で暗号化モジュールを検証します。</span><span class="sxs-lookup"><span data-stu-id="beb80-112">Microsoft validates its cryptographic modules under the National Institute of Standards and Technology (NIST) [Cryptographic Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP).</span></span> <span data-ttu-id="beb80-113">多くのクラウド サービスを含む複数の Microsoft 製品では、これらの暗号化モジュールを使用します。</span><span class="sxs-lookup"><span data-stu-id="beb80-113">Multiple Microsoft products, including many cloud services, use these cryptographic modules.</span></span>

<span data-ttu-id="beb80-114">Microsoft Windows 暗号化モジュール、各モジュールのセキュリティ ポリシー、および CMVP 証明書の詳細のカタログに関する技術情報については、「Windows および[Windows Server FIPS 140-2](https://aka.ms/AA6ehud)コンテンツ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="beb80-114">For technical information on Microsoft Windows cryptographic modules, the security policy for each module, and the catalog of CMVP certificate details, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="beb80-115">Microsoft のスコープ内クラウド プラットフォームと&サービス</span><span class="sxs-lookup"><span data-stu-id="beb80-115">Microsoft in-scope cloud platforms & services</span></span>

<span data-ttu-id="beb80-116">現在の CMVP FIPS 140-2 実装ガイダンスでは、クラウド サービス自体に対する FIPS 140-2 の検証が行えなっています。クラウド サービス プロバイダーは、クラウド サービスを構成するコンピューティング要素の FIPS 140 検証済み暗号化モジュールを取得して運用できます。</span><span class="sxs-lookup"><span data-stu-id="beb80-116">While the current CMVP FIPS 140-2 implementation guidance precludes a FIPS 140-2 validation for a cloud service itself; cloud service providers can choose to obtain and operate FIPS 140 validated cryptographic modules for the computing elements that comprise their cloud service.</span></span> <span data-ttu-id="beb80-117">FIPS 140-2 が検証されているコンポーネントを含む Microsoft オンライン サービスには、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="beb80-117">Microsoft online services that include components, which have been FIPS 140-2 validated include, among others:</span></span>

- <span data-ttu-id="beb80-118">Azure および Azure Government</span><span class="sxs-lookup"><span data-stu-id="beb80-118">Azure and Azure Government</span></span>
- <span data-ttu-id="beb80-119">Dynamics 365 および Dynamics 365 Government</span><span class="sxs-lookup"><span data-stu-id="beb80-119">Dynamics 365 and Dynamics 365 Government</span></span>
- <span data-ttu-id="beb80-120">Office 365、Office 365 U.S. Government、Office 365 U.S. Government Defense</span><span class="sxs-lookup"><span data-stu-id="beb80-120">Office 365, Office 365 U.S. Government, and Office 365 U.S. Government Defense</span></span>

## <a name="azure-dynamics-365-and-fips-140-2"></a><span data-ttu-id="beb80-121">Azure、Dynamics 365、および FIPS 140-2</span><span class="sxs-lookup"><span data-stu-id="beb80-121">Azure, Dynamics 365, and FIPS 140-2</span></span>

<span data-ttu-id="beb80-122">Azure、Dynamics 365、その他のオンライン サービスのコンプライアンスの詳細については [、「Azure FIPS 140-2](/azure/compliance/offerings/offering-fips-140-2)製品」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="beb80-122">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure FIPS 140-2 offering](/azure/compliance/offerings/offering-fips-140-2).</span></span>

## <a name="office-365-and-fips-140-2"></a><span data-ttu-id="beb80-123">Office 365 FIPS 140-2</span><span class="sxs-lookup"><span data-stu-id="beb80-123">Office 365 and FIPS 140-2</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="beb80-124">Office 365クラウド環境</span><span class="sxs-lookup"><span data-stu-id="beb80-124">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="beb80-125">Office 365とスコープ内サービス</span><span class="sxs-lookup"><span data-stu-id="beb80-125">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="beb80-126">次の表を使用して、サービスとサブスクリプションOffice 365を決定します。</span><span class="sxs-lookup"><span data-stu-id="beb80-126">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="beb80-127">**適用対象**</span><span class="sxs-lookup"><span data-stu-id="beb80-127">**Applicability**</span></span> | <span data-ttu-id="beb80-128">**スコープ内サービス**</span><span class="sxs-lookup"><span data-stu-id="beb80-128">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="beb80-129">Office 365、GCC、GCC High、DoD</span><span class="sxs-lookup"><span data-stu-id="beb80-129">Office 365, GCC, GCC High, DoD</span></span> | <span data-ttu-id="beb80-130">[「FIPS 140-2 検証」を参照してください。](/windows/security/threat-protection/fips-140-validation)</span><span class="sxs-lookup"><span data-stu-id="beb80-130">See [FIPS 140-2 Validation](/windows/security/threat-protection/fips-140-validation)</span></span> |

### <a name="frequently-asked-questions"></a><span data-ttu-id="beb80-131">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="beb80-131">Frequently asked questions</span></span>

<span data-ttu-id="beb80-132">**'FIPS 140 Validated' と 'FIPS 140 準拠' の違いは何ですか?**</span><span class="sxs-lookup"><span data-stu-id="beb80-132">**What is the difference between 'FIPS 140 Validated' and 'FIPS 140 compliant'?**</span></span>

<span data-ttu-id="beb80-133">'FIPS 140 Validated' は、暗号化モジュールまたはモジュールを埋め込む製品が、FIPS 140-2 の要件を満たすとして CMVP によって検証 ('認定') されたと意味します。</span><span class="sxs-lookup"><span data-stu-id="beb80-133">'FIPS 140 Validated' means that the cryptographic module, or a product that embeds the module has been validated ('certified') by the CMVP as meeting the FIPS 140-2 requirements.</span></span> <span data-ttu-id="beb80-134">'FIPS 140 準拠' は、暗号化機能のために FIPS 140 検証済み製品に依存する IT 製品の業界用語です。</span><span class="sxs-lookup"><span data-stu-id="beb80-134">'FIPS 140 compliant' is an industry term for IT products that rely on FIPS 140 Validated products for cryptographic functionality.</span></span>

<span data-ttu-id="beb80-135">**Microsoft が FIPS 140 検証を行うのは、いつですか?**</span><span class="sxs-lookup"><span data-stu-id="beb80-135">**When does Microsoft undertake a FIPS 140 validation?**</span></span>

<span data-ttu-id="beb80-136">モジュール検証を開始する場合のケイデンスは、サーバーとサーバーのWindows 10にWindowsします。</span><span class="sxs-lookup"><span data-stu-id="beb80-136">The cadence for starting a module validation aligns with the feature updates of Windows 10 and Windows Server.</span></span> <span data-ttu-id="beb80-137">ソフトウェア業界の進化に合って、オペレーティング システムは月次のソフトウェア更新プログラムを使用して、より頻繁にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="beb80-137">As the software industry evolved, operating systems are released more frequently, with monthly software updates.</span></span> <span data-ttu-id="beb80-138">Microsoft は機能リリースの検証を行いますが、リリースの間に暗号化モジュールへの変更を最小限に抑えます。</span><span class="sxs-lookup"><span data-stu-id="beb80-138">Microsoft undertakes validation for feature releases, but in between releases, seeks to minimize the changes to the cryptographic modules.</span></span>

<span data-ttu-id="beb80-139">**FIPS 140 検証に含まれるコンピューター**</span><span class="sxs-lookup"><span data-stu-id="beb80-139">**Which computers are included in a FIPS 140 validation?**</span></span>

<span data-ttu-id="beb80-140">Microsoft は、サーバーとサーバーで実行されているハードウェア構成の代表的なWindows 10検証Windowsします。</span><span class="sxs-lookup"><span data-stu-id="beb80-140">Microsoft validates cryptographic modules on a representative sample of hardware configurations running Windows 10 and Windows Server.</span></span> <span data-ttu-id="beb80-141">環境がハードウェアを使用する場合、この FIPS 140-2 検証を受け入れるのは、検証プロセスに使用されるサンプルと似ています。</span><span class="sxs-lookup"><span data-stu-id="beb80-141">It is common industry practice to accept this FIPS 140-2 validation when an environment uses hardware, which is similar to the samples used for the validation process.</span></span>

<span data-ttu-id="beb80-142">**NIST Web サイトには多数のモジュールがリストされています。自分の代理店に適用される対象を知る方法**</span><span class="sxs-lookup"><span data-stu-id="beb80-142">**There are many modules listed on the NIST website. How do I know which one applies to my agency?**</span></span>

<span data-ttu-id="beb80-143">FIPS 140-2 で検証された暗号化モジュールを使用する必要がある場合は、使用するバージョンが検証リストに表示されるのを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="beb80-143">If you are required to use cryptographic modules validated through FIPS 140-2, you need to verify that the version you use appears on the validation list.</span></span> <span data-ttu-id="beb80-144">CMVP と Microsoft は、製品リリース別に整理された検証済み暗号化モジュールの一覧と、Windows システムにインストールされているモジュールを識別する手順を管理します。</span><span class="sxs-lookup"><span data-stu-id="beb80-144">The CMVP and Microsoft maintain a list of validated cryptographic modules, organized by product release, along with instructions for identifying which modules are installed on a Windows system.</span></span> <span data-ttu-id="beb80-145">準拠するシステムを構成する方法の詳細については、「Windowsサーバー [FIPS 140-2 Windows」を参照してください](https://aka.ms/AA6ehud)。</span><span class="sxs-lookup"><span data-stu-id="beb80-145">For more information on configuring systems to be compliant, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

<span data-ttu-id="beb80-146">**証明書で 'FIPS モードで動作する場合' とはどういう意味ですか?**</span><span class="sxs-lookup"><span data-stu-id="beb80-146">**What does 'When operated in FIPS mode' mean on a certificate?**</span></span>

<span data-ttu-id="beb80-147">この警告は、FIPS 140-2 セキュリティ ポリシーと一致する方法で暗号化モジュールを使用するために必要な構成およびセキュリティ ルールに従う必要があるという情報を読み取り者に通知します。</span><span class="sxs-lookup"><span data-stu-id="beb80-147">This caveat informs the reader that required configuration and security rules must be followed to use the cryptographic module in a way that is consistent with its FIPS 140-2 security policy.</span></span> <span data-ttu-id="beb80-148">各モジュールには、独自のセキュリティ ポリシー (動作するセキュリティ ルールの正確な仕様) が用意され、承認された暗号化アルゴリズム、暗号化キー管理、および認証手法が採用されています。</span><span class="sxs-lookup"><span data-stu-id="beb80-148">Each module has its own security policy — a precise specification of the security rules under which it will operate — and employs approved cryptographic algorithms, cryptographic key management, and authentication techniques.</span></span> <span data-ttu-id="beb80-149">セキュリティ ルールは、各モジュールのセキュリティ ポリシーで定義されます。</span><span class="sxs-lookup"><span data-stu-id="beb80-149">The security rules are defined in the security policy for each module.</span></span> <span data-ttu-id="beb80-150">CMVP を通じて検証された各モジュールのセキュリティ ポリシーへのリンクを含む詳細については、「Windows および[Windows Server FIPS 140-2](https://aka.ms/AA6ehud)コンテンツ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="beb80-150">For more information, including links to the security policy for each module validated through the CMVP, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

<span data-ttu-id="beb80-151">**FedRAMP は FIPS 140-2 検証を必要としますか?**</span><span class="sxs-lookup"><span data-stu-id="beb80-151">**Does FedRAMP require FIPS 140-2 validation?**</span></span>

<span data-ttu-id="beb80-152">はい、連邦リスクおよび承認管理プログラム (FedRAMP) は [、NIST SP 800-53](https://nvd.nist.gov/800-53/Rev4/)リビジョン 4 で定義された制御基準に依存しています。FIPS 検証された暗号化または NSA 承認済み暗号化の使用を要求する [SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) 暗号化保護を含みます。</span><span class="sxs-lookup"><span data-stu-id="beb80-152">Yes, the Federal Risk and Authorization Management Program (FedRAMP) relies on control baselines defined by the [NIST SP 800-53 Revision 4](https://nvd.nist.gov/800-53/Rev4/), including [SC-13 Cryptographic Protection](https://nvd.nist.gov/800-53/Rev4/control/SC-13) mandating the use of FIPS-validated cryptography or NSA-approved cryptography.</span></span>

<span data-ttu-id="beb80-153">**代理店の認定プロセスで Microsoft の FIPS 140-2 への準拠を使用できますか?**</span><span class="sxs-lookup"><span data-stu-id="beb80-153">**Can I use Microsoft's adherence to FIPS 140-2 in my agency's certification process?**</span></span>

<span data-ttu-id="beb80-154">FIPS 140-2 に準拠するには、暗号化モジュールが FIPS 承認済みアルゴリズムのみを使用するように、FIPS 承認済み操作モードで実行するようにシステムを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="beb80-154">To comply with FIPS 140-2, your system must be configured to run in a FIPS approved mode of operation, which includes ensuring that a cryptographic module uses only FIPS-approved algorithms.</span></span> <span data-ttu-id="beb80-155">準拠するシステムを構成する方法の詳細については、「Windowsサーバー [FIPS 140-2 Windows」を参照してください](https://aka.ms/AA6ehud)。</span><span class="sxs-lookup"><span data-stu-id="beb80-155">For more information on configuring systems to be compliant, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

<span data-ttu-id="beb80-156">**FIPS 140-2 と共通の条件の関係は何ですか?**</span><span class="sxs-lookup"><span data-stu-id="beb80-156">**What is the relationship between FIPS 140-2 and Common Criteria?**</span></span>

<span data-ttu-id="beb80-157">これらは、2 つの独立したセキュリティ標準で、相互に補完的な目的が異なります。</span><span class="sxs-lookup"><span data-stu-id="beb80-157">These are two separate security standards with different, but complementary, purposes.</span></span> <span data-ttu-id="beb80-158">FIPS 140-2 はソフトウェアとハードウェアの暗号化モジュールを検証するために特別に設計され、Common Criteria は IT ソフトウェアおよびハードウェア製品のセキュリティ機能を評価するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="beb80-158">FIPS 140-2 is designed specifically for validating software and hardware cryptographic modules, while the Common Criteria is designed to evaluate security functions in IT software and hardware products.</span></span> <span data-ttu-id="beb80-159">一般的な Criteria 評価は、基本的な暗号化機能が適切に実装されていることを保証するために、FIPS 140-2 検証に依存する場合が多い。</span><span class="sxs-lookup"><span data-stu-id="beb80-159">Common Criteria evaluations often rely on FIPS 140-2 validations to provide assurance that basic cryptographic functionality is implemented properly.</span></span>

### <a name="resources"></a><span data-ttu-id="beb80-160">リソース</span><span class="sxs-lookup"><span data-stu-id="beb80-160">Resources</span></span>

- [<span data-ttu-id="beb80-161">FIPS Pub 140-2 暗号化モジュールのセキュリティ要件</span><span class="sxs-lookup"><span data-stu-id="beb80-161">FIPS Pub 140-2 Security Requirements for Cryptographic Modules</span></span>](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [<span data-ttu-id="beb80-162">NIST 暗号化モジュール検証プログラム</span><span class="sxs-lookup"><span data-stu-id="beb80-162">NIST Cryptographic Module Validation Program</span></span>](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [<span data-ttu-id="beb80-163">Windows、Windows サーバー、および FIPS 140-2</span><span class="sxs-lookup"><span data-stu-id="beb80-163">Windows, Windows Server, and FIPS 140-2</span></span>](/windows/security/threat-protection/fips-140-validation)
- [<span data-ttu-id="beb80-164">Microsoft Trust Center のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="beb80-164">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
