---
title: Microsoft のサービス拒否防御戦略
description: この記事では、サービス拒否 (DoS) 攻撃に関する Microsoft 防御戦略の概要について説明します。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
hideEdit: true
ms.openlocfilehash: e1613765d3ffb7b43b80d07823fe8aef45719b70
ms.sourcegitcommit: cb0b058800d3a8f04921066b4c59fb427eb9c268
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2021
ms.locfileid: "59486194"
---
# <a name="microsoft-denial-of-service-defense-strategy"></a>Microsoft のサービス拒否防御戦略

## <a name="denial-of-service-defense-strategy"></a>サービス拒否防御の戦略

ネットワーク ベースの分散型サービス拒否 (DDoS) 攻撃から防御する Microsoft の戦略は、グローバルなフットプリントが大きかったため、他のほとんどの組織では利用できない戦略と手法を利用できる点で一意です。 さらに、Microsoft は、Microsoft パートナーやより広範なインターネット セキュリティ コミュニティを含む広範な脅威インテリジェンス ネットワークによって集約された集合的な知識に貢献し、そこから引き出します。 このインテリジェンスは、オンライン サービスおよび Microsoft のグローバル顧客ベースから収集された情報と共に、Microsoft のオンライン サービスのすべての資産を保護する Microsoft の DDoS 防御システムを継続的に改善します。

Microsoft の DDoS 戦略の礎は、グローバルプレゼンスです。 Microsoft は、世界中のインターネット プロバイダー、ピアリング プロバイダー (パブリックおよびプライベート)、および民間企業と関わっています。 この取り組みにより、Microsoft は重要なインターネットプレゼンスを提供し、Microsoft は大規模な表面積全体で攻撃を吸収できます。

Microsoft のエッジ容量が時間の長い間に増加する中、個々のエッジに対する攻撃の重要性は大幅に減少しています。 この減少により、Microsoft は DDoS 防止システムの検出コンポーネントと軽減コンポーネントを分離しました。 Microsoft は、エッジ ノードでグローバルな軽減策を維持しながら、飽和点に近い攻撃を検出するために、地域データセンターに多層検出システムを展開しています。 この戦略により、複数のMicrosoft サービス同時攻撃を処理できます。

DDoS 攻撃に対して Microsoft が採用する最も効果的で低コストの防御の 1 つは、サービス攻撃の表面を減らすことです。 不要なトラフィックは、データをインラインで分析、処理、スクラブするのではなく、ネットワーク エッジでドロップされます。

パブリック ネットワークとのインターフェイスでは、ファイアウォール、ネットワーク アドレス変換、IP フィルター機能に特別な目的のセキュリティ デバイスを使用します。 Microsoft では、グローバルな等コストマルチ パス (ECMP) ルーティングも使用します。 グローバル ECMP ルーティングは、サービスに到達するための複数のグローバル パスを確保するためのネットワーク フレームワークです。 各サービスへの複数のパスを使用すると、DDoS 攻撃は攻撃の発生元となる地域に限定されます。 エンド ユーザーが他のパスを使用してそれらの地域のサービスに到達する場合、他の地域は攻撃の影響を受けずに行う必要があります。 Microsoft は、フロー データ、パフォーマンス 指標、その他の情報を使用して DDoS 攻撃を迅速に検出する内部 DDoS 相関検出システムも開発しました。

クラウド サービスをさらに保護するために、Microsoft では、Microsoft Azure の継続的な監視および侵入テスト プロセスに組み込Microsoft Azure DDoS 防御システムである Azure DDoS Protection を使用しています。 Azure DDoS Protection は、外部攻撃に耐えるだけでなく、他の Azure テナントからの攻撃にも耐えるように設計されています。 Azure では、SYN Cookie、レート制限、接続制限などの標準的な検出と軽減の手法を使用して、DDoS 攻撃から保護します。 自動化された保護をサポートするために、ワークロード間の DDoS インシデント対応チームは、チーム全体の役割と責任、エスカレーションの基準、および影響を受けるチーム全体のインシデント処理のプロトコルを識別します。

ターゲットに対して起動されるほとんどの DDoS 攻撃は、Open [Systems Interconnection](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) (OSI) モデルのネットワーク (L3) およびトランスポート (L4) レイヤーです。 L3 層と L4 層に向けられた攻撃は、ネットワーク インターフェイスまたはサービスに攻撃トラフィックをフラッディングしてリソースを圧倒し、正当なトラフィックに応答する機能を拒否するように設計されています。 L3 および L4 攻撃から保護するために、Microsoft の DDoS ソリューションはデータセンター ルーターからのトラフィック サンプリング データを使用して、インフラストラクチャと顧客のターゲットを保護します。 トラフィック サンプリング データは、ネットワーク監視サービスによって分析され、攻撃を検出します。 攻撃が検出されると、自動防御メカニズムが開始され、攻撃を軽減し、1 人の顧客に向けられた攻撃トラフィックが、他の顧客に対する担保損害やネットワークのサービス品質の低下を引き起さなかったりします。

また、Microsoft は DDoS 防御に対して攻撃的なアプローチを取っています。 ボットネットは、攻撃を増幅し、匿名性を維持するために DDoS 攻撃を実行するためのコマンドと制御の一般的なソースです。 Microsoft Digital Crimes Unit (DCU) は、ボットネットの規模と影響を軽減するために、マルウェアの配布および通信インフラストラクチャの特定、調査、および中断に重点を当て行います。

## <a name="application-level-defenses"></a>アプリケーション レベルの防御

Microsoft エンジニアリング チームは、Microsoft オペレーショナル セキュリティ アシュアランスによって設定された厳格な基準に従 [って、お](https://www.microsoft.com/SDL/OperationalSecurityAssurance) 客様のデータを保護します。 Microsoft のクラウド サービスは、高負荷をサポートするために意図的に構築され、アプリケーション レベルの DDoS 攻撃から保護するのに役立ちます。 Microsoft のスケールアウトアーキテクチャは、地域の分離と、関連するワークロードに対するワークロード固有の調整機能を備え、複数のグローバル データセンターにサービスを分散します。

サービスの初期構成時に顧客の管理者が識別する各顧客の国または地域によって、その顧客のデータのプライマリストレージの場所が決定されます。 顧客データは、プライマリ/バックアップ戦略に従って冗長データセンター間でレプリケートされます。 プライマリ データセンターは、ソフトウェア上で実行されている主要な顧客データと共に、アプリケーション ソフトウェアをホストします。 バックアップ データセンターは、自動フェールオーバーを提供します。 プライマリ データセンターが何らかの理由で機能しなくなる場合、要求はバックアップ データセンター内のソフトウェアおよび顧客データのコピーにリダイレクトされます。 顧客データは、いつでもプライマリ データセンターまたはバックアップ データセンターで処理できます。 複数のデータセンターにデータを分散すると、1 つのデータセンターが攻撃された場合に影響を受ける表面積が減少します。 さらに、影響を受けるデータセンター内のサービスをセカンダリ データセンターにすばやくリダイレクトして、攻撃中の可用性を維持し、攻撃が軽減された後にプライマリ データセンターにリダイレクトすることができます。

DDoS 攻撃に対するもう 1 つの軽減策として、個々のワークロードには、リソース使用率を管理する組み込みの機能が含まれます。 たとえば、Exchange Online および SharePoint Online の調整メカニズムは、DDoS 攻撃から防御するための多層的なアプローチの一部です。

Azure SQL Database、IP アドレスに基づいて失敗したログイン試行を追跡する DoSGuard と呼ばれるゲートウェイ サービスの形式で、セキュリティの層が追加されています。 同じ IP からの失敗したログイン試行のしきい値に達すると、DoSGuard は事前に決定された時間のアドレスをブロックします。

## <a name="resources"></a>リソース

- [Azure DDoS Protection Standard の概要](/azure/ddos-protection/ddos-protection-overview)
- [Azure DDoS Protection Standard の基本的なベスト プラクティス](/azure/ddos-protection/fundamental-best-practices)
- [DDoS 応答戦略のコンポーネント](/azure/ddos-protection/ddos-response-strategy)
