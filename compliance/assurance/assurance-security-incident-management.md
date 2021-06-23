---
title: Microsoft 365 のセキュリティ インシデント管理
description: この記事では、セキュリティ インシデント管理プロセスの概要について説明します。Microsoft 365。
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
hideEdit: true
ms.openlocfilehash: 5f3123d4b4ef853357c0b98f1b6973cc8ba4d1e8
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088889"
---
# <a name="microsoft-365-security-incident-management"></a>Microsoft 365 のセキュリティ インシデント管理

Microsoft は継続的に、セキュリティの高いエンタープライズ レベルのサービスを顧客に提供Microsoft 365しています。 このドキュメントでは、Microsoft がセキュリティ インシデントを処理する方法について説明Microsoft 365。 セキュリティ インシデントとは、Microsoft の機器または Microsoft の施設に保存されている顧客データへの違法なアクセス、または顧客データの損失、開示、または変更を引き起す可能性のある機器または施設への不正アクセスを指します。 セキュリティ インシデントに対応する際の Microsoft の目標は、顧客データとサービスを保護Microsoft 365です。

セキュリティ チームMicrosoft 365さまざまなサービス チームが共同で作業し、セキュリティ インシデントに対して同じアプローチを取っています。

- 準備
- 検出と分析
- コンテインメント
- 根絶
- 回復
- インシデント後のアクティビティ

## <a name="microsoft-approach-to-security-incident-management"></a>セキュリティ インシデント管理に対する Microsoft のアプローチ

セキュリティ インシデントを管理する Microsoft のアプローチは、国立標準技術研究所 [(NIST)](https://www.nist.gov/) Special Publication (SP) 800-61 に準拠しています。 Microsoft には、セキュリティ インシデントの防止、監視、検出、対応を行う専用のチームが複数あります。

|**チーム/エリア**|**説明**|
|:------------|:--------------|
| Microsoft Security Response Center | セキュリティ インシデントと Microsoft ソフトウェアのセキュリティの脆弱性を識別、監視、解決、および対応します。 |
| サイバー防御操作センター | サイバー防御運用センターは、セキュリティ対応チームと専門家をまとめて、脅威をリアルタイムで保護、検出、および対応するための物理的な場所です。 |
| 企業、外部、法務 | 疑わしいセキュリティ インシデントに関する法的および規制上のアドバイスを提供します。 |
| Microsoft 365セキュリティ対応チーム | パートナーはMicrosoft 365サービス チームと協力して、適切なセキュリティ インシデント管理プロセスを構築し、セキュリティ インシデント対応を推進します。 |
| Office 365信頼 | 規制要件、コンプライアンス、プライバシーに関するガイダンスを提供します。 |
| Microsoft 365データセンター セキュリティ チーム | さまざまなサービス全体に焦点を当て、サービス アーキテクチャのリスクと脅威を保護、検出、およびMicrosoft 365する一般的なセキュリティ エンジニアリング投資に焦点を当てたチーム。 |
| サービス チーム | Exchange、SharePoint、Microsoft Teams など、各サービスのセキュリティ関連のポリシーと決定を担当する Microsoft 365 サービスのエンジニアリング チーム。 |
| Microsoft Threat Intelligence Center (MSTIC) | Microsoft インフラストラクチャと資産に対するデジタル セキュリティ脅威の最新の状態を提供し、Microsoft 内のパートナー チームが軽減と予防の取り組みアクション プランを優先し、ほぼリアルタイムのインシデント監視/検出を採用して保護を強化します。 |
| パートナー セキュリティ チーム | 主要なサービスを提供する Microsoft 内の他のパートナー セキュリティ チーム、または azure Security Response チーム、Identity Security Response、Microsoft Corporate Security Response チームなど、Microsoft 365 の主要な依存関係を担当するパートナー セキュリティ チーム。 |
| Microsoft 365カスタマー エクスペリエンスコミュニケーション | セキュリティおよびサービス インシデントに関する顧客とのコミュニケーションを担当するエンジニアリング チーム。 |

## <a name="response-management-process"></a>応答管理プロセス

Microsoft 365チームとサービス チームは、NIST 800-61 の応答管理フェーズに基づいて、セキュリティ インシデントに対して同じアプローチで作業を行います。

- **準備**: ツール、プロセス、コンピテンシー、準備など、対応するために必要な組織の準備を指します。
- **検出&** 分析 : 実稼働環境でセキュリティ インシデントを検出し、すべてのイベントを分析してセキュリティ インシデントの信頼性を確認するアクティビティを参照します。
- **格納、根絶、回復**: 前のフェーズで行われた分析に基づいてセキュリティ インシデントを含む必要な適切なアクションを参照します。 セキュリティ インシデントから完全に復旧するために、このフェーズでさらに分析が必要になる場合があります。
- **インシデント後のアクティビティ**: セキュリティ インシデントの復旧後に実行された事後分析を参照します。 プロセス中に実行される操作アクションがレビューされ、準備フェーズまたは検出および分析フェーズで変更が必要かどうかを判断します。

![セキュリティ インシデント管理フェーズ](../media/assurance-sim-phases.png)

## <a name="federated-security-response-model"></a>フェデレーション セキュリティ応答モデル

Microsoft 365には、コア Microsoft オンライン サービス (Exchange、SharePoint、Microsoft Teams など) や、Azure Active Directory、Microsoft Commerce Platform、MSTIC などの他の Microsoft クラウド サービスが含まれます。 これらのサービスは、独自のセキュリティ運用プロセスを持つ個別のチームによって運用されます。 Microsoft の他のチームも、セキュリティに関するさまざまな側面にMicrosoft 365。 多数のチームがセキュリティ運用管理に取り組み、Microsoft 365を構成するさまざまなサービスにわたって、Microsoft はフェデレーション セキュリティ対応モデルを実装しています。

次の表に、さまざまなセキュリティ運用チームとサービス チームMicrosoft 365の運用上の境界Microsoft 365示します。

|**アクティビティ**|**Microsoft 365セキュリティ チームの操作**|**Microsoft 365サービス チームの操作**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| 検出と分析 | - 検出要件 <br> - セキュリティの監視と分析 <br> - 侵害のインジケーター (IOC) スイープ <br> - 違反ハント <br> - 24 時間 365 日のセキュリティ オンコールおよびインシデント対応リード | - 検出要件 <br> - インフラストラクチャの展開の監視 <br> - サービス分析と分析情報 <br> - イベントとアラートのトリアージ <br> - 24 時間 365 日のサービス エンジニアリングオンコール  |
| 格納、根絶、回復 | - インシデント対応リード <br> - Forensics の調査 <br> - セキュリティの専門知識とコンサルティング <br> - 回復のガイダンス | - セキュリティ インシデントの所有者 <br> - サービスの分析情報と専門知識 <br> - 格納、根絶、および回復を実行する |
| インシデント後のアクティビティ | - インシデント後の分析リード <br> - データ収集とアーカイブ <br> - 学習した教訓とバグ要求 <br> - インシデント レポート | - サービス側のインシデント分析 <br> - フォローアップ アクティビティの優先順位付け <br> - セキュリティ投資の実装 <br> - サービス セキュリティの準備 |

## <a name="related-articles"></a>関連記事

- [Microsoft 365インシデント管理の準備](assurance-sim-preparation.md)
- [Microsoft 365インシデント管理の検出と分析](assurance-sim-detection-analysis.md)
- [Microsoft 365インシデント管理の格納、根絶、および回復](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365インシデント管理のインシデント後のアクティビティの管理](assurance-sim-post-incident-activity.md)
