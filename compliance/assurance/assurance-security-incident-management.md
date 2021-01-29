---
title: Microsoft 365 セキュリティ インシデント管理
description: この記事では、Microsoft 365 のセキュリティ インシデント管理プロセスの概要について説明します。
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance0
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 9a76a258edf77708786cf19b160c4c5ee7af7ee6
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040360"
---
# <a name="microsoft-365-security-incident-management"></a>Microsoft 365 セキュリティ インシデント管理

Microsoft は、Microsoft 365 のお客様に高度なセキュリティで保護されたエンタープライズ レベルのサービスを提供するために継続的に取り扱っています。 このドキュメントでは、Microsoft が Microsoft 365 のセキュリティ インシデントを処理する方法について説明します。 セキュリティ インシデントとは、Microsoft の機器や施設に保管されている顧客データへの不正なアクセス、または顧客データの損失、開示、または改変の可能性がある機器や施設への不正アクセスを指します。 セキュリティ インシデントに対応する Microsoft の目標は、顧客データと Microsoft 365 サービスを保護することです。

Microsoft 365 セキュリティ チームとさまざまなサービス チームは、共同で作業し、セキュリティ インシデントに対して同じアプローチを取っています。

- 準備
- 検出と分析
- コンテインメント
- 根絶
- 回復
- インシデント後のアクティビティ

## <a name="microsoft-approach-to-security-incident-management"></a>セキュリティ インシデント管理に対する Microsoft のアプローチ

Microsoft によるセキュリティ インシデント管理のアプローチは、National [Institute of Standards and Technology (NIST)](https://www.nist.gov/) Special Publication (SP) 800-61 に準拠しています。 Microsoft には、セキュリティ インシデントの防止、監視、検出、対応に一緒に取り組む複数の専用チームがあります。

|**チーム/エリア**|**説明**|
|:------------|:--------------|
| Microsoft Security Response Center | セキュリティ インシデントと Microsoft ソフトウェアのセキュリティの脆弱性を特定、監視、解決、対応します。 |
| サイバー防御運用センター | サイバー防御オペレーション センターは、セキュリティ対応チームと専門家を集めて、リアルタイムで脅威の保護、検出、対応を支援する物理的な場所です。 |
| 企業、外部、法務 | 疑わしいセキュリティ インシデントに関する法的および規制上のアドバイスを提供します。 |
| Microsoft 365 セキュリティ対応チーム | Microsoft 365 サービス チームと協力して、適切なセキュリティ インシデント管理プロセスを構築し、セキュリティ インシデントへの対応を推進します。 |
| Office 365 信頼 | 規制要件、コンプライアンス、プライバシーに関するガイダンスを提供します。 |
| Microsoft 365 Datacenter Security Team | Microsoft 365 サービス アーキテクチャのリスクと脅威を保護、検出、および対応するために、さまざまなサービス全体で一般的なセキュリティ エンジニアリング投資に焦点を当てたチーム。 |
| サービス チーム | Exchange、SharePoint、Microsoft Teams などの Microsoft 365 サービスのエンジニアリング チーム。各サービスのセキュリティ関連のポリシーと決定を担当します。 |
| Microsoft Threat Intelligence Center (MSTIC) | Microsoft インフラストラクチャと資産に対するデジタル セキュリティの脅威に関する最新の機能を提供し、Microsoft 内のパートナー チームが軽減と防止の取り組み計画に優先順位を付け、ほぼリアルタイムのインシデント監視/検出を採用して保護を強化します。 |
| パートナー セキュリティ チーム | 主要なサービスを提供する Microsoft 内の他のパートナー セキュリティ チーム、または Azure Security Response チーム、Identity Security Response チーム、Microsoft Corporate Security Response チームなど、Microsoft 365 の主要な依存関係を担当するその他のパートナー セキュリティ チーム。 |
| Microsoft 365 カスタマー エクスペリエンス コミュニケーション | セキュリティおよびサービス インシデントに関する顧客との通信を担当するエンジニアリング チーム。 |

## <a name="response-management-process"></a>応答管理プロセス

Microsoft 365 セキュリティ チームとサービス チームは、NIST 800-61 対応管理フェーズに基づいて、同じアプローチでセキュリティ インシデントに取り組み、対応します。

- **準備**: ツール、プロセス、コンピテンシー、準備など、対応するために必要な組織の準備を指します。
- **検出&分析**: アクティビティを参照して、実稼働環境でセキュリティ インシデントを検出し、すべてのイベントを分析してセキュリティ インシデントの信頼性を確認します。
- **格納、強化、回復**: 前のフェーズで行われた分析に基づいて、セキュリティ インシデントを含むのに必要で適切なアクションを参照します。 セキュリティ インシデントから完全に復旧するために、このフェーズではさらに分析が必要になる場合があります。
- **インシデント後のアクティビティ**: セキュリティ インシデントの復旧後に実行された事後分析を参照します。 プロセス中に実行された操作が確認され、準備フェーズまたは検出フェーズと分析フェーズで変更が必要かどうかを判断します。

## <a name="federated-security-response-model"></a>フェデレーション セキュリティ応答モデル

Microsoft 365 サービスには、コア Microsoft オンライン サービス (Exchange、SharePoint、Microsoft Teams など) と、Azure Active Directory、Microsoft Commerce Platform、MSTIC などの他の Microsoft クラウド サービスが含まれます。 これらのサービスは、独自のセキュリティ運用プロセスを持つ個別のチームによって運用されます。 Microsoft の他のチームは、Microsoft 365 のさまざまなセキュリティの側面にも関与しています。 Microsoft 365 を構成するさまざまなサービス全体でセキュリティ運用管理に取り組む多数のチームのために、Microsoft はフェデレーション セキュリティ対応モデルを実装しています。

次の表に、さまざまな Microsoft 365 セキュリティ運用チームと Microsoft 365 サービス チームの間の運用上の境界を示します。

|**アクティビティ**|**Microsoft 365 セキュリティ チームの運用**|**Microsoft 365 サービス チームの運用**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| 検出と分析 | - 検出の要件 <br> - セキュリティの監視と分析 <br> - 侵害インジケーター (IOC) のスイープ <br> - 侵害ハント <br> - 24 時間 365 日のセキュリティ オンコールおよびインシデント対応リード | - 検出の要件 <br> - インフラストラクチャ展開の監視 <br> - サービス分析と分析情報 <br> - イベントとアラートのトリアージ <br> - 24 時間 365 日のサービス エンジニアリング オンコール  |
| 格納、分け入り、回復 | - インシデント対応リード <br> - Forensics 調査 <br> - セキュリティの専門知識とコンサルティング <br> - 回復ガイダンス | - セキュリティ インシデントの所有者 <br> - サービスの洞察と専門知識 <br> - 格納、権限の格納、回復の実行 |
| インシデント後のアクティビティ | - インシデント後分析のリード <br> - データの収集とアーカイブ <br> - 学習したレッスンとバグリクエスト <br> - インシデント レポート | - サービス側インシデント分析 <br> - フォローアップ アクティビティの優先順位付け <br> - セキュリティ投資の実装 <br> - サービス セキュリティの準備 |

## <a name="related-articles"></a>関連記事

- [Microsoft 365 セキュリティ インシデント管理の準備](assurance-sim-preparation.md)
- [Microsoft 365 セキュリティ インシデント管理の検出と分析](assurance-sim-detection-analysis.md)
- [Microsoft 365 セキュリティ インシデント管理の格納、復旧](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 セキュリティ インシデント管理インシデント後のアクティビティ](assurance-sim-post-incident-activity.md)
