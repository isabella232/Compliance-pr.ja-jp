---
title: 連邦情報処理標準 (FIPS) 文書 140-2
description: Microsoft は、暗号化モジュールが米国連邦情報処理標準に準拠しているという認定を行います。
keywords: Microsoft 365、コンプライアンス、サービス
ms.localizationpriority: medium
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
ms.openlocfilehash: 0e087393901b76a798c4a4ea3bef25fad8dcda84
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59161020"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>連邦情報処理標準 (FIPS) 文書 140-2

## <a name="fips-140-2-standard-overview"></a>FIPS 140-2 標準の概要

連邦情報処理標準 (FIPS) 文書 140-2 は、1996 年の情報技術管理改革法のセクション 5131 で定義されている情報技術製品の暗号化モジュールの最小セキュリティ要件を定義する米国政府の標準です。

米国[](https://csrc.nist.gov/Projects/cryptographic-module-validation-program)国立標準技術研究所 (NIST) とカナダサイバーセキュリティセンター (CCCS) の共同取り組みである暗号化モジュール検証プログラム (CMVP) は、暗号化モジュールのセキュリティ要件標準(FIPS 140-2) および関連する FIPS 暗号化標準を検証します。 FIPS 140-2 のセキュリティ要件は、暗号化モジュールの設計と実装に関連する 11 の領域をカバーします。 NIST Information Technology Laboratory は、モジュール内の FIPS 承認済み暗号化アルゴリズムを検証する関連プログラムを運営しています。

## <a name="microsofts-approach-to-fips-140-2-validation"></a>FIPS 140-2 検証に対する Microsoft のアプローチ

Microsoft は、2001 年の標準の初めから暗号化モジュールを検証し、140-2 の要件を満たすという積極的な取り組みを維持しています。 Microsoft は、国立標準技術研究所 (NIST) 暗号化モジュール検証プログラム[](https://csrc.nist.gov/Projects/cryptographic-module-validation-program)(CMVP) の下で暗号化モジュールを検証します。 多くのクラウド サービスを含む複数の Microsoft 製品では、これらの暗号化モジュールを使用します。

Microsoft Windows 暗号化モジュール、各モジュールのセキュリティ ポリシー、および CMVP 証明書の詳細のカタログに関する技術情報については、「Windows および[Windows Server FIPS 140-2](https://aka.ms/AA6ehud)コンテンツ」を参照してください。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

現在の CMVP FIPS 140-2 実装ガイダンスでは、クラウド サービス自体に対する FIPS 140-2 の検証が行えなっています。クラウド サービス プロバイダーは、クラウド サービスを構成するコンピューティング要素の FIPS 140 検証済み暗号化モジュールを取得して運用できます。 FIPS 140-2 が検証されているコンポーネントを含む Microsoft オンライン サービスには、次のものが含まれます。

- Azure および Azure Government
- Dynamics 365 および Dynamics 365 Government
- Office 365、Office 365 米国政府、Office 365 米国防総省

## <a name="azure-dynamics-365-and-fips-140-2"></a>Azure、Dynamics 365、および FIPS 140-2

Azure、Dynamics 365、その他のオンライン サービスのコンプライアンスの詳細については [、「Azure FIPS 140-2](/azure/compliance/offerings/offering-fips-140-2)製品」を参照してください。

## <a name="office-365-and-fips-140-2"></a>Office 365 FIPS 140-2

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| Office 365、GCC、GCC High、DoD | [「FIPS 140-2 検証」を参照してください。](/windows/security/threat-protection/fips-140-validation) |

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**'FIPS 140 Validated' と 'FIPS 140 準拠' の違いは何ですか?**

'FIPS 140 Validated' は、暗号化モジュールまたはモジュールを埋め込む製品が、FIPS 140-2 の要件を満たすとして CMVP によって検証 ('認定') されたと意味します。 'FIPS 140 準拠' は、暗号化機能のために FIPS 140 検証済み製品に依存する IT 製品の業界用語です。

**Microsoft が FIPS 140 検証を行うのは、いつですか?**

モジュール検証を開始する場合のケイデンスは、サーバーとサーバーのWindows 10にWindowsします。 ソフトウェア業界の進化に合って、オペレーティング システムは月次のソフトウェア更新プログラムを使用して、より頻繁にリリースされます。 Microsoft は機能リリースの検証を行いますが、リリースの間に暗号化モジュールへの変更を最小限に抑えます。

**FIPS 140 検証に含まれるコンピューター**

Microsoft は、サーバーとサーバーで実行されているハードウェア構成の代表的なWindows 10検証Windowsします。 環境がハードウェアを使用する場合、この FIPS 140-2 検証を受け入れるのは、検証プロセスに使用されるサンプルと似ています。

**NIST Web サイトには多数のモジュールがリストされています。自分の代理店に適用される対象を知る方法**

FIPS 140-2 で検証された暗号化モジュールを使用する必要がある場合は、使用するバージョンが検証リストに表示されるのを確認する必要があります。 CMVP と Microsoft は、製品リリース別に整理された検証済み暗号化モジュールの一覧と、Windows システムにインストールされているモジュールを識別する手順を管理します。 準拠するシステムを構成する方法の詳細については、「Windowsサーバー [FIPS 140-2 Windows」を参照してください](https://aka.ms/AA6ehud)。

**証明書で 'FIPS モードで動作する場合' とはどういう意味ですか?**

この警告は、FIPS 140-2 セキュリティ ポリシーと一致する方法で暗号化モジュールを使用するために必要な構成およびセキュリティ ルールに従う必要があるという情報を読み取り者に通知します。 各モジュールには、独自のセキュリティ ポリシー (動作するセキュリティ ルールの正確な仕様) が用意され、承認された暗号化アルゴリズム、暗号化キー管理、および認証手法が採用されています。 セキュリティ ルールは、各モジュールのセキュリティ ポリシーで定義されます。 CMVP を通じて検証された各モジュールのセキュリティ ポリシーへのリンクを含む詳細については、「Windows および[Windows Server FIPS 140-2](https://aka.ms/AA6ehud)コンテンツ」を参照してください。

**FedRAMP は FIPS 140-2 検証を必要としますか?**

はい、連邦リスクおよび承認管理プログラム (FedRAMP) は [、NIST SP 800-53](https://nvd.nist.gov/800-53/Rev4/)リビジョン 4 で定義された制御基準に依存しています。FIPS 検証された暗号化または NSA 承認済み暗号化の使用を要求する [SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) 暗号化保護を含みます。

**代理店の認定プロセスで Microsoft の FIPS 140-2 への準拠を使用できますか?**

FIPS 140-2 に準拠するには、暗号化モジュールが FIPS 承認済みアルゴリズムのみを使用するように、FIPS 承認済み操作モードで実行するようにシステムを構成する必要があります。 準拠するシステムを構成する方法の詳細については、「Windowsサーバー [FIPS 140-2 Windows」を参照してください](https://aka.ms/AA6ehud)。

**FIPS 140-2 と共通の条件の関係は何ですか?**

これらは、2 つの独立したセキュリティ標準で、相互に補完的な目的が異なります。 FIPS 140-2 はソフトウェアとハードウェアの暗号化モジュールを検証するために特別に設計され、Common Criteria は IT ソフトウェアおよびハードウェア製品のセキュリティ機能を評価するように設計されています。 一般的な Criteria 評価は、基本的な暗号化機能が適切に実装されていることを保証するために、FIPS 140-2 検証に依存する場合が多い。

### <a name="resources"></a>リソース

- [FIPS Pub 140-2 暗号化モジュールのセキュリティ要件](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [NIST 暗号化モジュール検証プログラム](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows、Windows サーバー、および FIPS 140-2](/windows/security/threat-protection/fips-140-validation)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
