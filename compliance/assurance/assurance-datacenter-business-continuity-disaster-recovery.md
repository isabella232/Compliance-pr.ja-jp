---
title: データセンターのビジネス継続性と障害復旧
description: Microsoft データセンターのビジネス継続性と障害復旧の詳細について説明します。
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 948e1f9e1b15b83817c072e63ffaae0b444445f8
ms.sourcegitcommit: cf424cb1e7c12048120977f294f780b776119a96
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/11/2021
ms.locfileid: "60265106"
---
# <a name="datacenter-business-continuity-and-disaster-recovery"></a>データセンターのビジネス継続性と障害復旧

障害は予測できないものですが、Microsoft のデータセンターと運用担当者は、障害発生時の最悪の事態を想定して準備しています。 回復性の高いアーキテクチャとテスト済みの最新の継続性計画により、潜在的な損害を軽減し、データセンター運用の迅速な復元を促進します。 危機管理計画では、危機の発生前、発生中、発生後における役割、責任、および軽減活動を明確にします。 危機状況において、これらの計画で定義される役割と連絡先は、指揮系統における効果的なエスカレーションを促します。

## <a name="business-resilience"></a>事業の回復性

Microsoft Cloud Operations and Innovation (CO+I) Business Continuity Program では、継続的な運用と危機イベントへの対応をテストするためにデータセンターが必要です。 各 Microsoft 管理データセンターには、CO+I Resilience Center of Excellence およびデータセンター運用の主要な専門分野の専門知識を使用して、サイト固有のコンテキストが緊急対応に組み込まれます。 これらの計画では、役割、責任、人事安全手順、通知基準、エスカレーション手順、およびさまざまな災害シナリオのチェックリストについて説明します。

Microsoft の CO+I 組織の復元機能は、Enterprise Business の継続性管理プログラムによって管理され、Enterprise ポリシーと標準に従います。 このプログラムのパフォーマンスは、事業継続性委員会、部門の上層部、そして最終的に Microsoft の上級リーダーシップ チームによって定期的に再評価されています。

## <a name="crisis-management-and-pandemic-response"></a>危機管理とパンデミック対策

Microsoft のグローバルなプレゼンスを考慮した場合、大規模な事案への Microsoft の対応において、危機管理プログラムは不可欠な部分です。 Microsoft の データセンター危機管理計画は業界のベスト プラクティスに基づいて作られており、戦術的な手法を使用して大規模な事案に対応する際に必要となる重要なコンポーネントを提供しています。 さらに、CO+I Resilience Center of Excellence は、運用上の影響を及ぼす可能性がある感染症に対応するために使用されるパンデミックおよび感染症計画を開発し、維持し続けます。 当社のパンデミック対応の一環として、回復力サポート チームは、包括的な軽減戦略を促進するために、Redmond ベースの Microsoft リーダーシップに重要かつ時期に合った地域の病気インテリジェンスを提供します。

Microsoft は、会社全体でビジネスEnterpriseプログラムを開発するためのガイドラインとして機能する、組織全体のビジネス継続性管理 (EBCM) フレームワークを確立しました。 プログラムには、ビジネス継続性ポリシー、実装ガイドライン、ビジネス影響分析 (BIA)、リスク評価、依存関係分析、およびプログラムの監視と改善のための手順が含まれます。 Enterprise回復性Office、Microsoft 全体のガバナンスとパフォーマンスレポートを管理します。 CO+I Resilience プログラムは、CO+I Resilience Center of Excellence を通じて調整され、プログラムが一貫した長期的なビジョンとミッションに準拠し、エンタープライズ プログラムの標準、メソッド、ポリシー、およびメトリックと一致します。 CO+I Resilience Center of Excellence は、CO+I 組織に追加のガバナンスを提供するように設計された一連の標準を確立しました。

CO+I テクノロジの復元計画 (TRP) は、重大なインシデントや災害からの復旧のために、CO+I 内のさまざまなエンジニアリング グループを対象とします。

Business Resilience Plan (BRP) と TRP には、サービス、復元手順、インシデント管理チームとの通信に関する範囲と適用可能な依存関係が含まれます。 BRP と TRP は、少なくとも年に 1 回は専用プランの所有者によって確認および承認され、適用可能なすべてのユーザーが利用できます。 計画は、適用可能な標準の一部として、定義されたテスト スケジュールに従ってテストされます。

## <a name="resiliency-program"></a>復元プログラム

Microsoft は、重大な有害事象の間に操作に対応、回復、再開するガイドとして BRP を定義しました。 BRP は、重要なビジネス プロセスと運用を継続するために必要な主要な人員、リソース、サービス、およびアクションについて説明します。 BRP の開発は、Microsoft の復元機能の推奨ガイドラインEnterprise基Office。

この計画の対象は、24 時間以内に必要に応じて定義された Microsoft の重要なビジネス プロセスです。 これらのプロセスは、Microsoft がプロセスを実行できない場合の潜在的な運用および財務上の影響を見積もり、回復時間目標 (RTO) と回復ポイント目標 (RPO) を決定する BIA の間に決定されます。 BIA に続いて、非技術的な依存関係分析が実行され、プロセスの実行に必要な特定のユーザー、アプリケーション、重要なレコード、およびユーザー要件が決定されます。

Microsoft は定期的に BRP をテストして、その有効性、使いやすさを評価し、リスクを排除または軽減できる領域を特定します。 該当する場合、サード パーティは、依存関係が関連付けられている場合、テストに関与します。 テストの結果は文書化され、検証され、適切な担当者によって承認されます。 この情報は、作業項目の作成と優先順位付けに使用されます。

## <a name="datacenter-resilience-program"></a>データセンターの復元プログラム

データセンターの復元プログラムの一環として、CO+I Resilience Center of Excellence チームは、組織のビジネス継続性に必要な情報セキュリティ要件に対応するメソッド、ポリシー、およびメトリックを開発します。 チームは、中断が発生した場合に重要なプロセスと必要なリソースの継続的な運用のために TRP を開発します。
