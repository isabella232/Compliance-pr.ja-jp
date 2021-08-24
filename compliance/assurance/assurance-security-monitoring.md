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
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 8ba736fbd6e72963badc3245e11cbed2292cba94
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481729"
---
# <a name="security-monitoring-overview"></a>セキュリティ監視の概要

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>セキュリティを監視する Microsoft の戦略は何ですか?

Microsoft は、Microsoft オンライン サービスに対する脅威を検出して対応するために、システムの継続的なセキュリティ監視に取り組む。 セキュリティ監視とアラートの主な原則は次のとおりです。

- 堅牢性: さまざまな攻撃動作を検出するシグナルとロジック
- 精度: ノイズの邪魔を避けるための意味のあるアラート
- 速度: 攻撃者を迅速にキャッチして、攻撃者を停止する能力

自動化、スケール、およびクラウド ベースのソリューションは、モニタリングおよび対応戦略の主要な柱です。 Microsoft の一部のオンライン サービスの規模で攻撃を効果的に防止するには、監視システムがリアルタイムで非常に正確なアラートを自動的に発生する必要があります。 同様に、問題が検出された場合は、大規模なリスクを軽減する機能が必要です。マシン別の問題を手動で修正するためにチームに頼る必要はありません。 大規模なリスクを軽減するために、クラウドベースのツールを使用して自動的に対策を適用し、承認された軽減アクションを環境全体に迅速に適用するためのツールをエンジニアに提供します。

## <a name="how-do-microsoft-online-services-perform-security-monitoring"></a>Microsoft オンライン サービスでセキュリティ監視を実行する方法

Microsoft オンライン サービスは、セキュリティ インシデントを示す可能性があるアクティビティのログ イベントを収集および分析するために、集中ログを使用します。 集中ログツールは、イベント ログ、アプリケーション ログ、アクセス制御ログ、ネットワーク ベースの侵入検知システムなどといった、全てのシステム コンポーネントのログを集計します。 サーバー ログとアプリケーション レベルのデータに加えて、コア インフラストラクチャには、詳細なテレメトリを生成し、ホスト ベースの侵入検出を提供するカスタマイズされたセキュリティ エージェントが装備されています。 このテレメトリは、モニタリングおよびフォレンジクスに使用します。

収集するログデータとテレメトリ データにより、24 時間 365 日セキュリティアラートが有効です。 アラート システムは、アップロードされたログデータを分析し、ほぼリアルタイムでアラートを生成します。 これには、ルール ベースのアラート、および機械学習モデルに基づいたより高度なアラートが含まれます。 モニタリング ロジックは、一般的な攻撃のシナリオにとどまらず、サービス アーキテクチャと操作についての深い理解が組み込まれています。 セキュリティ監視データを分析して、モデルを継続的に改善し、新しい種類の攻撃を検出し、セキュリティ監視の精度を向上します。

## <a name="how-do-microsoft-online-services-respond-to-security-monitoring-alerts"></a>Microsoft オンライン サービスはセキュリティ監視アラートに応答する方法を説明します。

アラートをトリガーするセキュリティ イベントで、サービス全体で迅速なアクションや法医学証拠の調査が必要な場合、クラウドベースのツールを使用すると、環境全体で迅速に対応できます。 これらのツールには、完全に自動化されたインテリジェントなエージェントが含まれ、セキュリティ対策によって、検出された脅威に対応します。 多くの場合、これらのエージェントは、ユーザーの介入を必要とせず、大規模なセキュリティ検出を軽減する自動的な対策を展開します。 この応答ができない場合、セキュリティ監視システムは、検出された脅威を大規模に軽減するためにリアルタイムで行動できる一連のツールを備えた適切なオンコール エンジニアに自動的に通知します。 潜在的なインシデントは、適切な Microsoft セキュリティ対応チームにエスカレートされ、セキュリティ インシデント対応プロセスを使用して解決されます。

## <a name="how-do-microsoft-online-services-monitor-system-availability"></a>Microsoft オンライン サービスは、システムの可用性を監視する方法を説明します。

Microsoft は、リソースの過剰利用と異常な使用のインジケーターについて、システムを積極的に監視します。 リソースの監視は、予期しないダウンタイムを回避し、製品やサービスへの信頼性の高いアクセスを顧客に提供するために、サービスの冗長性によって補完されます。 Microsoft オンライン サービスの正常性の問題は、サービス正常性ダッシュボード (SHD) を通じて、お客様に速やかに伝達されます。

Azure および Dynamics 365 オンライン サービスは、複数のインフラストラクチャ サービスを使用して、セキュリティと正常性の可用性を監視します。 代理トランザクション (STX) テストの実装により、Azure サービスと Dynamics サービスはサービスの可用性を確認できます。 STX フレームワークは、実行中のサービスのコンポーネントの自動テストをサポートするように設計され、ライブ サイト障害アラートでテストされます。 さらに、Azure Security Monitoring (ASM) サービスは、新しいサービスと実行中のサービスの両方で期待通りセキュリティアラート機能を確認する一元的な代理テスト手順を実装しています。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 セキュリティ監視に関連するコントロールの検証については、次の表を参照してください。

### <a name="azure-and-dynamics-365"></a>Azure と Dynamics 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------|:--------|:------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: 可用性の監視と容量の計画 | 2020 年 12 月 2 日 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: 可用性の監視と容量の計画 <br> A.16.1: 情報セキュリティ インシデントと改善の管理 | 2020 年 12 月 2 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: インシデント管理フレームワーク <br> IM-2: インシデント検出の構成 <br> IM-3: インシデント管理手順 <br> IM-4: インシデントの事後分析 <br> VM-1: セキュリティ イベントログとコレクション <br> VM-12: Azure サービスの可用性監視 <br> VM-4: 悪意のあるイベントの調査 <br> VM-6: セキュリティの脆弱性の監視 | 2021 年 3 月 31 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: インシデント管理フレームワーク <br> IM-2: インシデント検出の構成 <br> IM-3: インシデント管理手順 <br> IM-4: インシデントの事後分析 <br> PI-2: Azure portal SLA のパフォーマンス レビュー <br> VM-1: セキュリティ イベントログとコレクション <br> VM-12: Azure サービスの可用性監視 <br> VM-4: 悪意のあるイベントの調査 <br> VM-6: セキュリティの脆弱性の監視 | 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------|:--------|:------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-2: アカウント管理 <br> AC-17: リモート アクセス <br> AU-7: 監査の削減とレポート生成 <br> SI-4: 情報システムの監視 <br> SI-7: ソフトウェア、ファームウェア、および情報の整合性 <br> | 2020 年 9 月 24 日 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: 可用性の監視と容量の計画 | 2021 年 4 月 20 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: 変更監視 <br> CA-26: セキュリティ インシデント レポート <br> CA-29: オンコール エンジニア <br> CA-48: データセンターログ | 2020 年 12 月 24 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: 変更監視 <br> CA-26: セキュリティ インシデント レポート <br> CA-29: オンコール エンジニア <br> CA-30: 可用性の監視 <br> CA-48: データセンターログ | 2020 年 12 月 24 日 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: インシデントの報告 <br> CUEC-10: サービス コントラクト | 2020 年 12 月 24 日 |

## <a name="resources"></a>リソース

- [Behind the Scenes: Securing the Infrastructure Powering the Microsoft 365 Service (舞台裏: Microsoft 365 サービスを支えるインフラストラクチャの保護)](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
