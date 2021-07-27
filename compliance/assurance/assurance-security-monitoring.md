---
title: セキュリティ監視の概要
description: セキュリティ監視の詳細については、Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: d0285110c3fe4225ba2e2c6d1fb58820ff2a1dc8
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573615"
---
# <a name="security-monitoring-overview"></a>セキュリティ監視の概要

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>セキュリティを監視する Microsoft の戦略は何ですか?

Microsoft 365 は、継続的なシステムのセキュリティ モニタリングを行うことで、Microsoft 365 サービスへの脅威を検出し、対応しています。 セキュリティ監視とアラートの主な原則は次のとおりです。

- 堅牢性: さまざまな攻撃動作を検出するシグナルとロジック
- 精度: ノイズの邪魔を避けるための意味のあるアラート
- 速度: 攻撃者を迅速にキャッチして、攻撃者を停止する能力

自動化、スケール、およびクラウド ベースのソリューションは、モニタリングおよび対応戦略の主要な柱です。 一部の Microsoft 365 コア サービスの規模で攻撃を効果的に見つけて停止するには、モニタリング システムが正確なアラートをほぼリアルタイムで自動的に生成する必要があります。 同様に、問題が検出された場合は、大規模なリスクを軽減する機能が必要です。マシン別の問題を手動で修正するためにチームに頼る必要はありません。 大規模なリスクを軽減するために、クラウドベースのツールを使用して、対策を自動的に適用します。これにより、承認された軽減案を環境全体にすばやく適用するためのツールをエンジニアに提供することができます。

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>セキュリティ監視Microsoft 365実行する方法

Microsoft 365ログを使用して、セキュリティ インシデントを示す可能性があるアクティビティのログ イベントを収集および分析します。 集中ログツールは、イベント ログ、アプリケーション ログ、アクセス制御ログ、ネットワーク ベースの侵入検知システムなどといった、全てのシステム コンポーネントのログを集計します。 サーバーのログ記録とアプリケーション レベルのデータに加えて、サービスのコアインフラストラクチャには、詳細なテレメトリを生成してホストベースの侵入検出を行う、カスタマイズされたセキュリティ エージェントが用意されています。 このテレメトリは、モニタリングおよびフォレンジクスに使用します。

収集するログデータとテレメトリ データにより、24 時間 365 日セキュリティアラートが有効です。 アラート システムは、アップロードされたログデータを分析し、ほぼリアルタイムでアラートを生成します。 これには、ルール ベースのアラート、および機械学習モデルに基づいたより高度なアラートが含まれます。 モニタリング ロジックは、一般的な攻撃のシナリオにとどまらず、サービス アーキテクチャと操作についての深い理解が組み込まれています。 Microsoft では、新しい種類の攻撃を検出し、セキュリティ モニタリングの精度を向上させるため、モデルに継続的に改善を加えています。

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>セキュリティ監視Microsoft 365に応答する方法

アラートに何らかの対応が必要になった場合、またはサービス全体のフォレンジック エビデンスをさらに調査することが必要になった場合は、クラウド ベースのツールを使用すると、環境全体で迅速に対応することができます。 これらのツールには、完全に自動化されたインテリジェントなエージェントが含まれ、セキュリティ対策によって、検出された脅威に対応します。 多くの場合、これらのエージェントは、ユーザーの介入を必要とせず、大規模なセキュリティ検出を軽減する自動的な対策を展開します。 これができない場合、セキュリティ モニタリング システムは、検出された脅威をリアルタイムで軽減するための一連のツールを備えた、待機中の適切なエンジニアに自動的にアラートを生成します。 セキュリティ インシデント対応チームMicrosoft 365、セキュリティ インシデント対応プロセスを使用して解決される可能性のあるインシデント。

## <a name="how-does-microsoft-365-monitor-system-availability"></a>システムの可用性Microsoft 365監視する方法

Microsoft 365リソースの過剰使用と異常な使用のインジケーターをシステムで積極的に監視します。 リソースの監視は、予期しないダウンタイムを回避し、製品やサービスへの信頼性の高いアクセスを顧客に提供するために、サービスの冗長性によって補完されます。 サービス正常性の問題は、サービス正常性ダッシュボード (SHD) を通じて、お客様に速やかに伝達されます。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 セキュリティ監視に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: アカウント管理 <br> AC-17: リモート アクセス <br> AU-7: 監査の削減とレポート生成 <br> SI-4: 情報システムの監視 <br> SI-7: ソフトウェア、ファームウェア、および情報の整合性 <br> | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: 可用性の監視と容量の計画 | 2021 年 4 月 20 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: 可用性の監視と容量の計画 <br> A.16.1: 情報セキュリティ インシデントと改善の管理 | 2021 年 4 月 20 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: 変更監視 <br> CA-26: セキュリティ インシデント レポート <br> CA-29: オンコール エンジニア <br> CA-48: データセンターログ | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: 変更監視 <br> CA-26: セキュリティ インシデント レポート <br> CA-29: オンコール エンジニア <br> CA-30: 可用性の監視 <br> CA-48: データセンターログ | 2020 年 12 月 24 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: インシデントの報告 <br> CUEC-10: サービス コントラクト | 2020 年 12 月 24 日 |

## <a name="resources"></a>リソース

- [Behind the Scenes: Securing the Infrastructure Powering the Microsoft 365 Service (舞台裏: Microsoft 365 サービスを支えるインフラストラクチャの保護)](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
