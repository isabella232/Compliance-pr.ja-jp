---
title: Microsoft セキュリティ インシデント管理
description: この記事では、Microsoft オンライン サービスのセキュリティ インシデント管理プロセスの概要について説明します。
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: cb9d27f02ec53c98e2f00d3106f8e4be8798d78f
ms.sourcegitcommit: 9766d656d0e270f478437bd39c0546ad2e4d846f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/27/2021
ms.locfileid: "58678586"
---
# <a name="microsoft-security-incident-management"></a>Microsoft セキュリティ インシデント管理

Microsoft は、Microsoft のお客様に高いセキュリティでエンタープライズ レベルのサービスを提供するために継続的に取り扱っていますが、セキュリティ インシデントは避けられない現実であり、徹底的かつ迅速に管理する必要があります。 このドキュメントでは、Microsoft が潜在的な影響を最小限に抑えるために、正しい方法とテクノロジを使用してセキュリティ インシデントを処理する方法の概要を説明します。 セキュリティ インシデントとは、Microsoft の機器または Microsoft の施設に保存されている顧客データへの違法なアクセス、または顧客データの損失、開示、または変更を引き起す可能性のある機器または施設への不正アクセスを指します。 セキュリティ インシデントに対応する際の Microsoft の目標は、顧客データと Microsoft のオンライン サービスを保護することです。

Microsoft Online Services セキュリティ チームとさまざまなサービス チームは、共同で作業し、セキュリティ インシデントに対して同じアプローチを取っています。

- 準備
- 検出と分析
- 格納、根絶、および回復
- インシデント後のアクティビティ

## <a name="microsoft-approach-to-security-incident-management"></a>セキュリティ インシデント管理に対する Microsoft のアプローチ

セキュリティ インシデントを管理する Microsoft のアプローチは、国立標準技術研究所 [(NIST)](https://www.nist.gov/) Special Publication (SP) 800-61 に準拠しています。 Microsoft には、セキュリティ インシデントの防止、監視、検出、対応を行う専用のチームが複数あります。

|**チーム/エリア**|**説明**|
|:------------|:--------------|
| Microsoft Security Response Center | セキュリティ インシデントと Microsoft ソフトウェアのセキュリティの脆弱性を識別、監視、解決、および対応します。 |
| サイバー防御操作センター | サイバー防御運用センターは、セキュリティ対応チームと専門家をまとめて、脅威をリアルタイムで保護、検出、および対応するための物理的な場所です。 |
| 企業、外部、法務 | 疑わしいセキュリティ インシデントに関する法的および規制上のアドバイスを提供します。 |
| Microsoft データセンター セキュリティ チーム | サービス アーキテクチャのリスクと脅威を保護、検出、および対応するための一般的なセキュリティ エンジニアリング投資にさまざまなサービスに焦点を当てたチーム。 |
| Microsoft セキュリティ対応チーム | サービス チームと提携して適切なセキュリティ インシデント管理プロセスを構築し、セキュリティ インシデント対応を推進する独立した Azure、Dynamics 365、および Microsoft 365 セキュリティ チーム。 |
| Microsoft ガバナンス、リスク、コンプライアンス (GRC) チーム | 規制要件、コンプライアンス、およびプライバシーに関するガイダンスを提供します。 |
| サービス チーム | Azure、Dynamics 365 のエンジニアリング チームはMicrosoft 365サービスのセキュリティ関連のポリシーと決定を担当するチームです。 |
| Azure 運用マネージャー | Azure 関連のセキュリティおよびプライバシー インシデントの調査と解決を監督します。 |
| Microsoft Threat Intelligence Center (MSTIC) | Microsoft インフラストラクチャと資産に対するデジタル セキュリティ脅威の最新の状態を提供し、Microsoft 内のパートナー チームが軽減と予防の取り組みアクション プランを優先し、ほぼリアルタイムのインシデント監視/検出を採用して保護を強化します。 |
| カスタマー エクスペリエンスコミュニケーションチーム | セキュリティおよびサービス インシデントに関する顧客とのコミュニケーションを担当するエンジニアリング チーム。 個別のチームは、Azure、Dynamics 365、および Microsoft 365 専用です。 |

## <a name="response-management-process"></a>応答管理プロセス

Microsoft Online Services のセキュリティ チームとサービス チームは、NIST 800-61 の応答管理フェーズに基づいて、セキュリティ インシデントに対して同じアプローチで作業し、取り組む。

- **準備**: ツール、プロセス、コンピテンシー、準備など、対応するために必要な組織の準備を指します。
- **検出&** 分析 : 実稼働環境でセキュリティ インシデントを検出し、すべてのイベントを分析してセキュリティ インシデントの信頼性を確認するアクティビティを参照します。
- **格納、根絶、回復**: 前のフェーズで行われた分析に基づいてセキュリティ インシデントを含む必要な適切なアクションを参照します。 セキュリティ インシデントから完全に復旧するために、このフェーズでさらに分析が必要になる場合があります。
- **インシデント後のアクティビティ**: セキュリティ インシデントの復旧後に実行された事後分析を参照します。 プロセス中に実行される操作アクションがレビューされ、準備フェーズまたは検出および分析フェーズで変更が必要かどうかを判断します。

![セキュリティ インシデント管理フェーズ。](../media/assurance-sim-phases.png)

## <a name="federated-security-response-model"></a>フェデレーション セキュリティ応答モデル

Microsoft オンライン サービスは、Azure、Dynamics 365、および Microsoft の主要な製品Microsoft 365。 これらの各サービスは、独自のセキュリティ運用プロセスを持つ個別のチームによって運営されます。 MSTIC などの Microsoft の他のチームも、Microsoft オンライン サービスのさまざまなセキュリティ側面に従事しています。 Microsoft オンライン サービスを構成するさまざまなサービス全体でセキュリティ運用管理に取り組む多数のチームのために、Microsoft はフェデレーション セキュリティ対応モデルを実装しています。

次の表に、さまざまな Microsoft Online Service セキュリティ運用チームと Microsoft サービス チームの間の運用上の境界を示します。

|**アクティビティ**|**Microsoft セキュリティ チームの操作**|**Microsoft Service チームの操作**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| 検出と分析 | - 検出要件 <br> - セキュリティの監視と分析 <br> - 侵害のインジケーター (IOC) スイープ <br> - 違反ハント <br> - 24 時間 365 日のセキュリティ オンコールおよびインシデント対応リード | - 検出要件 <br> - インフラストラクチャの展開の監視 <br> - サービス分析と分析情報 <br> - イベントとアラートのトリアージ <br> - 24 時間 365 日のサービス エンジニアリングオンコール  |
| 格納、根絶、回復 | - インシデント対応リード <br> - Forensics の調査 <br> - セキュリティの専門知識とコンサルティング <br> - 回復のガイダンス | - セキュリティ インシデントの所有者 <br> - サービスの分析情報と専門知識 <br> - 格納、根絶、および回復を実行する |
| インシデント後のアクティビティ | - インシデント後の分析リード <br> - データ収集とアーカイブ <br> - 学習した教訓とバグ要求 <br> - インシデント レポート | - サービス側のインシデント分析 <br> - フォローアップ アクティビティの優先順位付け <br> - セキュリティ投資の実装 <br> - サービス セキュリティの準備 |

## <a name="related-articles"></a>関連記事

- [Microsoft セキュリティ インシデント管理: 準備](assurance-sim-preparation.md)
- [Microsoft セキュリティ インシデント管理: 検出と分析](assurance-sim-detection-analysis.md)
- [Microsoft セキュリティ インシデント管理: 格納、根絶、および回復](assurance-sim-containment-eradication-recovery.md)
- [Microsoft セキュリティ インシデント管理: インシデント後のアクティビティ](assurance-sim-post-incident-activity.md)
