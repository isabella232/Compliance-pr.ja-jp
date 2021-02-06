---
title: Federal Information Processing Standard (FIPS) 文書 140-2
description: Microsoft は、暗号化モジュールが米国連邦情報処理規格に準拠すると認定しています。
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
ms.openlocfilehash: d7d1f47d7f76f9fc6d3cefa6cac5be807af98cbc
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120836"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>Federal Information Processing Standard (FIPS) 文書 140-2

## <a name="fips-140-2-standard-overview"></a>FIPS 140-2 標準の概要

Federal Information Processing Standard (FIPS) Publication 140-2 は、1996 年の情報技術管理書法第 5131 条に定義されている情報技術製品の暗号化モジュールの最小セキュリティ要件を定義する米国政府規格です。

暗号化モジュール検証プログラム (CMVP) は、米国立標準技術協会 (NIST) とカナダサイバー セキュリティ センター (CCCS) の共同で、暗号化モジュールを暗号化モジュールのセキュリティ要件 (FIPS 140-2 など) および関連する FIPS 暗号化標準に対して検証します。 [](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) FIPS 140-2 のセキュリティ要件は、暗号化モジュールの設計と実装に関連する 11 の領域をカバーしています。 NIST Information Technology Cryptographicy は、モジュール内の FIPS 承認済み暗号化アルゴリズムを検証する関連プログラムを運用しています。

## <a name="microsofts-approach-to-fips-140-2-validation"></a>FIPS 140-2 検証に対する Microsoft のアプローチ

Microsoft は、2001 年の標準の適用以降、検証済み暗号化モジュールを備え、140-2 の要件を満たすという積極的な取り組みを維持しています。 Microsoft は、National Institute of Standards and Technology (NIST) [Cryptographic Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP) の下で暗号化モジュールを検証します。 多数のクラウド サービスを含む複数の Microsoft 製品では、これらの暗号化モジュールが使用されます。

Microsoft Windows 暗号化モジュール、各モジュールのセキュリティ ポリシー、および CMVP 証明書の詳細のカタログの技術情報については [、Windows および Windows Server FIPS 140-2](https://aka.ms/AA6ehud)のコンテンツを参照してください。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

現在の CMVP FIPS 140-2 実装ガイダンスでは、クラウド サービス自体の FIPS 140-2 検証は行う必要はありません。クラウド サービス プロバイダーは、クラウド サービスを構成するコンピューティング要素の FIPS 140 検証済み暗号化モジュールを取得して操作できます。 FIPS 140-2 で検証されたコンポーネントを含む Microsoft オンライン サービスには、次のようなものがあります。

- [Azure および Azure Government](/azure/azure-government/documentation-government-plan-security)
- [Dynamics 365 および Dynamics 365 Government](/microsoft-365/compliance/office-365-encryption-in-microsoft-dynamics-365)
- [Office 365、Office 365 U.S. Government、Office 365 U.S. Government Defense](/microsoft-365/compliance/office-365-encryption-risks-and-protections)

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**"FIPS 140 Validated" と "FIPS 140 compliant" の違いは何ですか?**

"FIPS 140 Validated" は、FIPS 140-2 の要件を満たすとして、CMVP によって暗号化モジュールまたはモジュールを埋め込む製品が検証 ("認定") されたという意味です。 "FIPS 140 準拠" は、暗号化機能を FIPS 140 検証済み製品に依存する IT 製品の業界用語です。

**Microsoft が FIPS 140 検証を行うのは、いつですか?**

モジュール検証を開始する期間は、Windows 10 および Windows Server の機能更新プログラムに合わせて調整されます。 ソフトウェア業界の進化に合って、オペレーティング システムは毎月のソフトウェア更新プログラムを使用して、より頻繁にリリースされます。 Microsoft は機能リリースの検証を行いますが、リリースの間に暗号化モジュールの変更を最小限に抑えます。

**FIPS 140 検証に含まれるコンピューター**

Microsoft は、Windows 10 と Windows Server を実行しているハードウェア構成の代表的なサンプルで暗号化モジュールを検証します。 この FIPS 140-2 検証は、環境でハードウェアを使用する場合に受け入れるのが一般的です。これは、検証プロセスに使用されるサンプルに似ています。

**NIST Web サイトには多くのモジュールが一覧表示されています。自分のエージェンシーに適用されるポリシーを知る方法**

FIPS 140-2 で検証された暗号化モジュールを使用する必要がある場合は、使用するバージョンが検証リストに表示されるのを確認する必要があります。 CMVP と Microsoft は、検証済み暗号化モジュールの一覧を、製品リリース別に整理し、Windows システムにインストールされているモジュールを特定する手順を管理します。 準拠するシステムの構成の詳細については、Windows および [Windows Server FIPS 140-2 のコンテンツを参照してください](https://aka.ms/AA6ehud)。

**証明書に対して 「FIPS モードで操作された場合」とは何を意味しますか。**

この警告は、FIPS 140-2 セキュリティ ポリシーと一致する方法で暗号化モジュールを使用するために、必要な構成およびセキュリティ ルールに従う必要があるという情報を閲覧者に通知します。 各モジュールには独自のセキュリティ ポリシー (動作するセキュリティ ルールの正確な仕様) が用意され、承認された暗号化アルゴリズム、暗号化キー管理、および認証手法が採用されています。 セキュリティ ルールは、各モジュールのセキュリティ ポリシーで定義されます。 CMVP によって検証された各モジュールのセキュリティ ポリシーへのリンクを含む詳細については、Windows および [Windows Server FIPS 140-2](https://aka.ms/AA6ehud)のコンテンツを参照してください。

**FedRAMP は FIPS 140-2 検証を必要としますか?**

はい。連邦リスク/承認管理プログラム (FedRAMP) は [、NIST SP 800-53 リビジョン 4](https://nvd.nist.gov/800-53/Rev4/)で定義されている制御基準 (FIPS 検証暗号化または NSA 承認暗号化の使用を緩和する [SC-13 Cryptographic Protection](https://nvd.nist.gov/800-53/Rev4/control/SC-13) を含む) に依存しています。

**Microsoft Azure は FIPS 140-2 をサポートする方法を説明します。**

Azure は、ハードウェア、市販のオペレーティング システム (Linux と Windows)、Azure 固有のバージョンの Windows を組み合わせて構築されています。 Microsoft [Security Development Lifecycle](https://www.microsoft.com/securityengineering/sdl/) (SDL) を通じて、オペレーティング システムはハイパースケール クラウドでの運用中に FIPS 140-2 承認アルゴリズムを使用するので、すべての Azure サービスはデータ セキュリティに FIPS 140-2 承認アルゴリズムを使用します。

**Microsoft は、私の機関の認定プロセスで FIPS 140-2 に準拠していますか?**

FIPS 140-2 に準拠するには、FIPS 承認済みモードの操作で実行するようにシステムを構成する必要があります。これには、暗号化モジュールで FIPS 承認済みアルゴリズムのみを使用するように設定する必要があります。 準拠するシステムの構成の詳細については、Windows および [Windows Server FIPS 140-2 のコンテンツを参照してください](https://aka.ms/AA6ehud)。

**FIPS 140-2 と共通条件の関係**

これらは、補完的な目的が異なる 2 つの個別のセキュリティ標準です。 FIPS 140-2 はソフトウェアおよびハードウェアの暗号化モジュールを検証するために特別に設計されています。一方、Common Criteria は IT ソフトウェアおよびハードウェア製品のセキュリティ機能を評価するように設計されています。 一般的な条件の評価では、多くの場合、FIPS 140-2 検証を使用して、基本的な暗号化機能が適切に実装されていることを保証します。

## <a name="resources"></a>リソース

- [暗号化モジュールの FIPS Pub 140-2 セキュリティ要件](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [NIST Cryptographic Module Validation Program](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows、Windows Server、FIPS 140-2](/windows/security/threat-protection/fips-140-validation)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
