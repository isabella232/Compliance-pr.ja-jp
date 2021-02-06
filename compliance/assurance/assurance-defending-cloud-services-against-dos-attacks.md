---
title: サービス拒否攻撃から Microsoft 365 クラウド サービスを保護する
description: この記事では、Microsoft がサービス拒否 (DoS) 攻撃からクラウド サービスを保護する方法について説明します。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: e632c1524d5cc8c21aec9dab3d95d285a3b8801e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120576"
---
# <a name="defending-microsoft-365-cloud-services-against-denial-of-service-attacks"></a>サービス拒否攻撃から Microsoft 365 クラウド サービスを保護する

Microsoft データセンターは、境界フェンス、ビデオ カメラ、セキュリティ担当者、生体認証、スマートカード、多要素認証を使用する安全な入口を含む多層防御セキュリティによって保護されています。 詳細な防御セキュリティは、施設のすべての領域と各物理サーバー ユニットを通じて継続されます。 [Microsoft Cloud Infrastructure and Operations Group](https://www.microsoft.com/cloud-platform/global-datacenters)は、クラウド サービスのコア インフラストラクチャと基盤技術を提供します。 Microsoft のデータセンターは、物理的なセキュリティと信頼性に関する業界標準に準拠し、Microsoft の運用担当者によって管理、監視、管理されます。

Microsoft では、クラウド サービスをさらに保護するために、Microsoft Azure の継続的な監視および侵入テストプロセスの一部である DDoS 防御システムを提供しています。 Azure DDoS 防御システムは、外部からの攻撃だけでなく、他の Azure テナントからの攻撃にも対応するように設計されています。 Azure では、SYN Cookie、レート制限、接続制限などの標準的な検出と軽減の手法を使用して、DDoS 攻撃から保護します。

Microsoft のクラウド サービスは、複数のソースからの攻撃の脅威の対象です。 さまざまな DoS 脅威を軽減し、保護するために、高度にスケーラブルで動的な Azure ベースの脅威の検出と軽減システムが開発され、DoS 攻撃から基礎となるインフラストラクチャを保護し、クラウド サービスのお客様のサービス中断を防ぐことを主な目的として実装されています。 Azure DoS 軽減策システムは、受信、送信、地域間のトラフィックを保護します。

Open [Systems Interconnection](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) (OSI) モデルのネットワーク (L3) レイヤーとトランスポート (L4) レイヤーでターゲットに対して起動された DoS 攻撃のほとんど。 L3 レイヤーと L4 層に向けられた攻撃は、ネットワーク インターフェイスやサービスに攻撃トラフィックを使い込み、リソースを圧倒し、正当なトラフィックに対応する能力を拒否するように設計されています。 具体的には、L3 および L4 攻撃は、ネットワーク リンク、デバイス、またはサービスの容量を飽和状態にするか、アプリケーションをサポートするサーバーまたは仮想マシンの CPU を圧倒します。

L3 および L4 攻撃から保護するために、Microsoft は、これらのレイヤーを保護することで攻撃を受けたインフラストラクチャと顧客の標的を保護することを目的としたソリューションを設計、開発、および展開しました。 インフラストラクチャを保護することで、1 人の顧客を対象とした攻撃トラフィックが、他のお客様に対する副次的損害やネットワークのサービス品質の低下を引き起さなかったりすることを保証します。 このソリューションでは、データセンター ルーターからのトラフィック サンプリング データを使用します。 このデータは、ネットワーク監視サービスによって分析され、攻撃を検出します。 攻撃が検出されると、自動防御メカニズムが開始します。

## <a name="application-level-defenses"></a>Application-Level防御
Microsoft エンジニアリング チームは、お客様のデータを保護するために [、Microsoft 運用](https://www.microsoft.com/SDL/OperationalSecurityAssurance) セキュリティ アシュアランスによって定めらた厳格な基準に従います。 Microsoft のクラウド サービスは、非常に高い負荷をサポートし、アプリケーション レベルの DoS 攻撃を保護および軽減するために意図的に構築されています。 一部のワークロードでは、サービスが地域の分離と調整機能を使用して複数のグローバル データセンターに分散されるスケールアウト アーキテクチャを実装しました。

各お客様の国または地域は、お客様の管理者がサービスの初期セットアップ時に識別しますが、その顧客のデータの主要な保管場所を決定します。 顧客データは、プライマリ/バックアップ戦略に従って冗長データセンター間でレプリケートされます。 プライマリ データセンターは、アプリケーション ソフトウェアと共に、ソフトウェア上で実行されている主要な顧客データすべてと共にホストします。 バックアップ データセンターは自動フェールオーバーを提供します。 何らかの理由でプライマリ データセンターが機能しなくなると、要求はバックアップ データセンター内のソフトウェアデータと顧客データのコピーにリダイレクトされます。 顧客データは、いつでもプライマリ データセンターまたはバックアップ データセンターで処理できます。 複数のデータセンターにデータを分散すると、1 つのデータセンターが攻撃された場合に影響を受けるサーフェス領域が減少します。 さらに、影響を受けるデータセンター内のサービスを回復メカニズムの 1 つとしてセカンダリ データセンターに迅速にリダイレクトし、その逆に (サービスが復元された後にプライマリ データセンターにリダイレクトされる) 場合もあります。

個々のワークロードには、リソース使用率を管理する組み込み機能が含まれます。 たとえば、Exchange Online と SharePoint Online の調整メカニズムは、DoS 攻撃から防御するための多層的なアプローチの一部です。 Exchange Online ユーザーの調整は、エンド ユーザーが消費するリソースのレベル、リソースが Active Directory、Exchange Online の情報ストア、その他の場所にあるかどうかに基づいて行います。 ユーザーが消費するリソースを制限するために、各クライアントに予算が割り当てられる。 ユーザー アクティビティとシステム コンポーネントの Exchange Online 調整は、ワークロード管理に [基づいて行います](https://technet.microsoft.com/library/jj150503(v=exchg.150).aspx)。 Exchange Online ワークロードは、Exchange Online のシステム リソース管理のために明示的に定義されている Exchange Online の機能、プロトコル、またはサービスです。 各 Exchange Online ワークロードでは、ユーザー要求またはバックグラウンド作業を実行するために、CPU、メールボックス データベース操作、Active Directory 要求などのシステム リソースが必要です。 Exchange Online ワークロードの例としては、Outlook on the web、Exchange ActiveSync、メールボックスの移行、メールボックス アシスタントがあります。 テナント管理者は、Exchange 管理シェルを使用して、ユーザーの Exchange ワークロード管理調整設定を管理できます。 Exchange Online には、PowerShell、Exchange Web サービス、POP と IMAP、Exchange ActiveSync、モバイル デバイス接続、受信者など、さまざまな形式の調整が実装されています。 オンプレミスの Exchange 展開の管理者は調整ポリシーを構成することができますが、管理者は Exchange Online の調整ポリシーを構成できません。

SharePoint Online での調整の最も一般的なトリガーは、高すぎる頻度で多くのアクションを実行するクライアント側オブジェクト モデル (CSOM) コードです。 CSOM では、1 つの要求で多くのアクションを実行できます。この場合、使用量の制限を超え、ユーザーごとの調整が発生する可能性があります。

調整の影響を受けかねないアクティビティに関係なく、ユーザーが使用量の制限を超えると、SharePoint Online は、通常は短時間、そのユーザー アカウントからのそれ以上の要求を調整します。 ユーザーのスロットルが有効である間、そのユーザーによるすべてのアクションは、次の条件に従って調整が期限切れになるまで調整されます。
- ユーザーがブラウザーで直接実行した要求の場合、SharePoint Online は調整情報ページにリダイレクトし、要求は失敗します。
- CSOM 呼び出しを含む他のすべての要求では、SharePoint Online は HTTP ステータス コード 429 ("要求が多すぎます") を返し、要求は失敗します。

問題のプロセスが使用制限を超え続ける場合、SharePoint Online はプロセスを完全にブロックし、HTTP 状態コード 503 ("サービスを利用できません") を返す可能性があります。

## <a name="vulnerability-and-penetration-testing"></a>脆弱性と侵入テスト
Microsoft では[](https://www.microsoft.com/trustcenter/security/threatmanagement)、クラウド サービス、[](https://blogs.technet.microsoft.com/hybridcloud/2015/05/05/protecting-your-datacenter-and-cloud-from-emerging-threats/)仮想マシン (VM)、その他のシステムにマルウェア対策コンポーネントとサービスを使用するなど、最新の高度な脅威からクラウド インフラストラクチャとオンプレミス ネットワークを保護するために、多くのセキュリティ テクノロジとプラクティスを使用しています。 Advanced Threat Analytics は、ネットワーク、システム、およびユーザーの通常の使用パターンを監視し、機械学習を使用して、通常の定期的な侵入テストから外した動作にフラグを設定します。

独自の侵入テストを実行し [、Microsoft クラウド](https://technet.microsoft.com/mt784683)統合侵入テスト プログラムをお客様に提供するほか、クラウド サービスに対する定期的な脆弱性評価と侵入テストを実行するサード パーティのセキュリティ担当者と関わり合います。 これらのサードパーティの脆弱性評価のレポートは [、Service Trust](https://aka.ms/STP) ポータルと [Service Assurance](https://aka.ms/ServiceAssurance) ポータルからダウンロードできます。
