---
title: Center for Internet Security (CIS) ベンチマーク
description: Center for Internet Security (CIS) は、Microsoft の製品とサービスに関する一連のベンチマークを公開しています
keywords: Microsoft 365、コンプライアンス、サービス
ms.localizationpriority: high
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
ms.openlocfilehash: 18da1f6b422327f42dc517fa0f9c8abe9c91e253
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59161028"
---
# <a name="center-for-internet-security-cis-benchmarks"></a>Center for Internet Security (CIS) ベンチマーク

## <a name="about-cis-benchmarks"></a>CIS ベンチマークについて

[Center for Internet Security](https://www.cisecurity.org/) は、"サイバー防衛のためのベスト プラクティス ソリューションを特定、開発、検証、促進、維持する" ことを使命とする非営利団体です。 世界中の政府、企業、学術界のサイバーセキュリティおよび IT の専門家が持つ専門知識を活用しています。 CIS ベンチマーク、コントロール、ハードニング済みイメージなどを含む標準およびベスト プラクティスを開発するために、コンセンサス意思決定モデルに従います。  
  
[CIS ベンチマーク](https://www.cisecurity.org/cis-benchmarks/)は、システムを安全に構成するための構成基準およびベスト プラクティスです。 各ガイダンスの推奨事項は、組織のサイバー防衛機能の向上を支援するために開発された 1 つ以上の [CIS コントロール](https://www.cisecurity.org/controls/)を参照しています。 CIS コントロールは、NIST Cybersecurity Framework (CSF) および NIST SP 800-53、ISO 27000 シリーズの規格、PCI DSS、HIPAA などを含む多くの確立された規格および規制の枠組みに対応しています。  
  
各ベンチマークは、コンセンサス レビューの 2 つのフェーズを経由します。 1 つ目は最初の開発中で、専門家が召集され作業用ドラフトについて議論し、作成し、テストをし、ベンチマークに関する合意に達するまで行われます。 ベンチマークが公開された後の第 2 フェーズでは、コンセンサス チームがインターネット コミュニティからのフィードバックをベンチマークに組み込むために確認します。  
  
CIS ベンチマークは、2 つのレベルのセキュリティ設定を提供します。

- **レベル 1** では、あらゆるシステムで構成でき、サービスの中断や機能の低下をほとんど、またはまったく引き起こさない、不可欠となる基本セキュリティ要件を推奨しています。
- **レベル 2** では、機能の低下を引き起こす可能性のある、より高度なセキュリティを必要とする環境向けのセキュリティ設定を推奨しています。

[CIS ハードニング済みイメージ](https://www.cisecurity.org/blog/cis-hardened-images-now-in-microsoft-azure-marketplace/) は、レベル 1 またはレベル 2 CIS ベンチマーク プロファイルへとハードニングされた CIS ベンチマークに基づき、安全に構成された仮想マシン イメージです。 ハードニングとは、システムをサイバー攻撃に対して脆弱にする潜在的な脆弱性を制限することにより、不正アクセス、サービス拒否 (DoS 攻撃)、およびその他のサイバー脅威からの保護を支援するプロセスです。

## <a name="microsoft-and-the-cis-benchmarks"></a>Microsoft と CIS ベンチマーク

Center for Internet Security (CIS) は、Microsoft Azure および Microsoft 365 基礎ベンチマーク、Windows 10 ベンチマーク、Windows Server 2016 ベンチマークなどを含む Microsoft 製品およびサービスのベンチマークを公開しています。 [CIS Microsoft Azure 基礎ベンチマーク](https://www.cisecurity.org/benchmark/azure/)は、Azure を組み込んだソリューションの開発、展開、評価、またはセキュリティ保護を計画しているお客様を対象としています。 このドキュメントでは、Azure の安全なベースライン構成を確立するための規範的なガイダンスを提供します。
  
CIS ベンチマークは、IT システムおよびデータをサイバー攻撃から守るためのセキュリティ規格として国際的に認められています。 何千もの企業で採用され、安全なベースライン構成を確立するための規範的なガイダンスを提供します。 システムおよびアプリケーションの管理者、セキュリティ スペシャリスト、および Microsoft 製品とサービスを使用してソリューションを開発するその他のユーザーは、これらのベスト プラクティスを使用してアプリケーションのセキュリティを評価および改善することができます。  
  
すべての CIS ベンチマークと同様に Microsoft ベンチマークは、ソフトウェア開発、監査とコンプライアンス、セキュリティ研究、運用、政府、法律に及ぶさまざまなバックグラウンドを持つ内容領域専門家からの情報提供に基づくコンセンサス レビュー プロセスを使用して作成されました。 Microsoft は、これらの CIS の取り組みにおいて不可欠なパートナーでした。 たとえば、リストされたサービスに対して Office 365 がテストされ、その結果となる Microsoft 365 基礎ベンチマークは、アカウントと認証、データ管理、アプリケーションのアクセス許可、ストレージ、およびその他のセキュリティ ポリシー領域を対象とした適切なセキュリティ ポリシーを設定するための幅広い推奨事項をカバーしています。  
  
CIS は、Microsoft 製品およびサービスのベンチマークに加えて、CIS ベンチマークを満たすように構成された [Azure での CIS ハードニング済みイメージ](https://www.cisecurity.org/cis-hardened-images/microsoft/)も公開しています。これは、Microsoft Azure Marketplace から入手できます。 これらのイメージには、Windows Server 2016、Windows Server 2019、Linux の多くのバージョンに対応する CIS ハードニング済みイメージが含まれます。 Azure Marketplace で利用可能なすべての CIS ハードニング済みイメージは、Microsoft Azure での実行が保証されています。 [CIS が述べているように](https://www.cisecurity.org/blog/cis-hardened-images-now-in-microsoft-azure-marketplace/)、Microsoft Azure パブリック クラウド、クラウド OS ネットワークを介してサービス プロバイダーがホストする Microsoft Cloud プラットフォーム、およびお客様が管理するオンプレミスのプライベート クラウド Windows Server Hyper-V 展開への用意および互換性は、事前テスト済みです。

[CIS ハードニング済みイメージ](https://www.cisecurity.org/cis-hardened-images/)は、レベル 1 またはレベル 2 の CIS ベンチマーク プロファイルへとハードニングされた CIS ベンチマークに基づき、安全に構成された仮想マシン イメージです。 ハードニングとは、システムをサイバー攻撃に対して脆弱にする潜在的な脆弱性を制限することにより、不正アクセス、サービス拒否 (DoS 攻撃)、およびその他のサイバー脅威からの保護を支援するプロセスです。 CIS ハードニング済みイメージは、Azure と Azure Government の両方で利用できます。

お客様をさらにサポートするため、Microsoft は [Azure Blueprints](https://azure.microsoft.com/services/blueprints/) を提供しています。これは、Azure Resource Manager テンプレートなどの構成可能な成果物を使用してリソース、役割ベースのアクセス制御、ポリシーをプロビジョニングすることで、クラウド環境を繰り返し展開および更新するのに役立つサービスです。 Azure Blueprints を通してプロビジョニングされたリソースは、組織の標準、パターン、コンプライアンス要件に準拠します。 Azure Blueprints の包括的な目標は、クラウド環境におけるコンプライアンスとサイバーセキュリティのリスク管理を自動化することです。 CIS Azure 基礎ベンチマークの推奨事項を実装する必要のある Azure ベースのアーキテクチャに主要なポリシーのセットを展開することをサポートするため、Microsoft は [CIS Microsoft Azure 基礎ベンチマークのための Azure Blueprint](/azure/governance/blueprints/samples/cis-azure-1-3-0) を公開しました。 アーキテクチャに割り当てられると、リソースが割り当てられたポリシー定義に準拠しているかどうかが Azure Policy によって評価されます。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- [Azure および Azure Government](https://aka.ms/AzureCompliance)
- [Office および Microsoft 365](https://aka.ms/o365-compliance-framework)
- SQL Server
- Windows 10
- Windows Server 2016

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

Microsoft 製品およびサービスの [CIS ベンチマークの全ての一覧](https://www.cisecurity.org/cis-benchmarks/)を入手してください。

- [CIS Azure 基礎ベンチマーク](https://www.cisecurity.org/benchmark/azure/)
- [CIS Microsoft 365 基礎ベンチマーク](https://www.cisecurity.org/benchmark/microsoft_office/)
- [Windows 10 ベンチマーク](https://www.cisecurity.org/benchmark/microsoft_windows_desktop/)
- [Windows Server 2016 ベンチマーク](https://www.cisecurity.org/benchmark/microsoft_windows_server/)

## <a name="how-to-implement"></a>実装方法

- [Azure 向け CIS ベンチマーク](https://azure.microsoft.com/mediahandler/files/resourcefiles/cis-microsoft-azure-foundations-security-benchmark/CIS_Microsoft_Azure_Foundations_Benchmark_v1.0.0.pdf): Azure の安全なベースライン構成を確立するための規範的なガイダンスを入手してください。  
- [Microsoft 365 セキュリティ ロードマップ](/microsoft-365/security/office-365-security/security-roadmap): このロードマップに従うことにより、データ漏洩またはアカウント侵害の可能性を最小限に抑えます。
- [Windows セキュリティ ベースライン](/windows/security/threat-protection/windows-security-baselines): 組織内でセキュリティ ベースラインを効果的に使用するには、これらのガイドラインに従ってください。
- [CIS Controls クラウド コンパニオン ガイド](https://www.cisecurity.org/white-papers/cis-controls-cloud-companion-guide/): CIS Controls バージョン 7 のセキュリティ ベスト プラクティスをクラウド環境に適用するためのガイダンスを入手してください。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**CIS ベンチマーク設定に準拠することにより、アプリケーションのセキュリティは確保されますか ?**

CIS ベンチマークは、対象となる Microsoft 製品およびサービスを採用しているすべてのユーザーに基礎レベルのセキュリティを確立します。 ただし、これらはすべての考えうるセキュリティ構成およびアーキテクチャを網羅したリストとしてではなく、出発点として見なされなければなりません。 各組織は、特定の状況、ワークロード、コンプライアンス要件を引き続き評価し、それに応じて環境を調整する必要があります。

**CIS ベンチマークはどの程度の頻度で更新されますか ?**

改訂された CIS ベンチマークのリリースは、それを開発した IT プロフェッショナルのコミュニティ、およびベンチマークがサポートするテクノロジーのリリース スケジュールに応じて変わってきます。 CIS は、新しいベンチマークおよび既存のベンチマークの更新を発表する月次レポートを配布します。 これらを受け取るには [CIS Workbench](https://workbench.cisecurity.org/) に登録し (無料)、プロフィール画面の [ニュースレターを受け取る] をオンにします。

**Microsoft CIS ベンチマークの開発に貢献したのは誰ですか ?**

CIS は、"ベンチマークは内容領域専門家、テクノロジ ベンダー、パブリックおよびプライベートの CIS ベンチマーク コミュニティ メンバー、および CIS ベンチマーク開発チームの惜しみないボランティア活動によって開発されています。" と述べています。 たとえば、「[CIS Microsoft Azure 基礎ベンチマーク v1.0.0 が公開されました (CIS Microsoft Azure Foundations Benchmark v1.0.0 Now Available)](https://www.cisecurity.org/blog/cis-microsoft-azure-foundations-benchmark-v1-0-0-now-available/)」に、Azure の貢献者の一覧が記載されています。

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

## <a name="resources"></a>リソース

- [Azure コンプライアンスのドキュメント](/azure/compliance/)
- [Azure はコンプライアンスの世界を実現する](https://azure.microsoft.com/resources/azure-enables-a-world-of-compliance/)
- [Microsoft 365 コンプライアンスのサービス](/compliance/regulatory/offering-home)
- [Microsoft トラスト センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
- [CIS Microsoft Azure 基礎ベンチマーク](https://www.cisecurity.org/benchmark/azure/)は、Azure のセキュリティ保護を順を追って説明するチェックリストを提供します。
- [Microsoft Azure の CIS ハードニング済みイメージ](https://www.cisecurity.org/cis-hardened-images/microsoft/)は、Azure によって認定され、CIS ベンチマークのセキュリティ上の推奨事項を満たすように事前に設定されています。  これらは Azure と Azure Government の両方で利用できます。
- [CIS Microsoft Azure 基礎ベンチマークのための Azure Blueprint](/azure/governance/blueprints/samples/cis-azure-1-3-0) は、お客様が CIS Azure 基礎ベンチマークの推奨事項を実装する必要のある Azure ベースのアーキテクチャに主要なポリシーのセットを展開するのに役立ちます。
- [Azure Policy の推奨事項マッピング](/azure/governance/policy/samples/cis-azure-1-3-0)は、上記の Blueprint に含まれるポリシー定義の詳細と、これらのポリシー定義が CIS Microsoft Azure 基礎ベンチマークのコンプライアンス ドメインおよびコントロールにマップされる方法について説明します。 アーキテクチャに割り当てられると、リソースが割り当てられたポリシー定義に準拠しているかどうかが Azure Policy によって評価されます。
- [CIS Controls クラウド コンパニオン ガイド](https://www.cisecurity.org/white-papers/cis-controls-cloud-companion-guide/)は、CIS Controls バージョン 7 のセキュリティ ベスト プラクティスをクラウド環境に適用するためのガイダンスを提供します。
- [CIS Microsoft 365 基礎ベンチマーク](https://www.cisecurity.org/benchmark/microsoft_office/)は、Microsoft 365 の安全なベースライン構成を確立するための規範的なガイダンスを提供します。
- [Windows 10 のセキュリティ ポリシー設定](/windows/security/threat-protection/security-policy-settings/security-policy-settings)
- [Windows 10 Enterprise のセキュリティ](/windows/security/index)
