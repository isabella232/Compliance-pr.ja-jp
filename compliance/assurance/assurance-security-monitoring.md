---
title: セキュリティ監視の概要
description: Microsoft 365 でのセキュリティ監視について
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
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: f3eae0aa5ba79372a7ce0d9a34d4dd35fe83a36b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508848"
---
# <a name="security-monitoring-overview"></a>セキュリティ監視の概要

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>セキュリティを監視するための Microsoft の戦略について

Microsoft 365 は、継続的なシステムのセキュリティ モニタリングを行うことで、Microsoft 365 サービスへの脅威を検出するのに、対応しています。 セキュリティの監視と警告の主な原則は次のとおりです。

- 堅牢性: さまざまな攻撃の動作を検出するためのシグナルとロジック
- 精度: 妨げを回避するための重要なアラート
- スピード: 攻撃者をすぐにキャッチして、それを止めることができます。

自動化、スケール、およびクラウド ベースのソリューションは、モニタリングおよび対応戦略の主要な柱です。 一部の Microsoft 365 コア サービスの規模で攻撃を効果的に見つけて停止するには、モニタリング システムが正確なアラートをほぼリアルタイムで自動的に生成する必要があります。 同様に、問題が検出された場合、リスクを軽減する機能が必要になりますが、チームがコンピューターごとに問題を手動で修正することはできません。 大規模なリスクを軽減するために、クラウドベースのツールを使用して、対策を自動的に適用させます。また、承認された軽減案を環境全体にすばやく適用させるために、ツールでエンジニアに提供することができます。

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>Microsoft 365 はセキュリティ監視を実行する方法を教えてください。

Microsoft 365 は集中ログを使用して、セキュリティインシデントを示している可能性があるアクティビティのログイベントを収集して分析します。 集中ログツールは、イベント ログ、アプリケーション ログ、アクセス制御ログ、ネットワーク ベースの侵入検知システムなどといった、全てのシステム コンポーネントのログを集計します。 サーバーのログ記録とアプリケーション レベルのデータに加えて、サービスのコアインフラストラクチャには、詳細なテレメトリを生成してホストベースの侵入検出を行う、カスタマイズされたセキュリティ エージェントが用意されています。 このテレメトリは、モニタリングおよびフォレンジクスに使用します。

収集するログおよびテレメトリデータは、24/7 のセキュリティ警告を有効にします。 アラート システムは、アップロードされたログデータを分析し、ほぼリアルタイムでアラートを生成します。 これには、ルール ベースのアラート、および機械学習モデルに基づいたより高度なアラートが含まれます。 モニタリング ロジックは、一般的な攻撃のシナリオにとどまらず、サービス アーキテクチャと操作についての深い理解が組み込まれています。 Microsoft では、新しい種類の攻撃を検出し、セキュリティ監視の精度を向上させるため、モデルに継続的にセキュリティ監視データを使用します。

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>Microsoft 365 は、セキュリティ監視の警告にどのように対応しますか?

アラートに何らかの対応が必要になった場合、またはサービス全体のフォレンジック エビデンスをさらに調査することが必要になった場合は、クラウド ベースのツールを使用すると、環境全体で迅速に対応することができます。 これらのツールには、完全に自動化されたインテリジェントなエージェントが含まれ、セキュリティ対策によって、検出された脅威に対応します。 多くの場合、これらのエージェントは、ユーザーの介入を必要とせず、大規模なセキュリティ検出を軽減する自動的な対策を展開します。 これができない場合、セキュリティ モニタリング システムは、検出された脅威をリアルタイムで軽減するための一連のツールを備えた、待機中の適切なエンジニアに自動的にアラートを生成します。 Microsoft 365 セキュリティ対応チームにエスカレートされる可能性のあるインシデントは、セキュリティインシデント対応プロセスを使用して解決されます。

## <a name="how-does-microsoft-365-monitor-system-availability"></a>Microsoft 365 はシステムの可用性をどのように監視していますか?

Microsoft 365 は、リソースの使用率と異常な使用状況のインジケーターを使用して、システムを積極的に監視します。 リソース監視は、予期しないダウンタイムを回避し、製品やサービスへの信頼できるアクセス権をお客様に提供するために、サービスの重複によって補完されます。 サービス正常性の問題は、サービス正常性ダッシュボード (SHD) を使用して迅速にお客様に伝達されます。

## <a name="related-external-regulations--certifications"></a>関連する外部規制 & 証明書

Microsoft のオンラインサービスは、社外の規制と証明書に準拠するために定期的に監査されます。 セキュリティ監視に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: アカウント管理 <br> AC-17: リモートアクセス <br> AU-7: 監査の削減とレポート生成 <br> SI-4: 情報システムの監視 <br> SI-7: ソフトウェア、ファームウェア、情報の整合性 <br> | 2020年9月24日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.1.3: 可用性の監視および容量の計画 | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.1.3: 可用性の監視および容量の計画 <br> 16.1: 情報セキュリティインシデントと改善の管理 | 2020 月 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19: 変更監視 <br> CA-26: セキュリティインシデントの報告 <br> CA-29: オンプレ呼び出しエンジニア <br> CA-48: データセンターログ | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19: 変更監視 <br> CA-26: セキュリティインシデントの報告 <br> CA-29: オンプレ呼び出しエンジニア <br> CA-30: 可用性の監視 <br> CA-48: データセンターログ | 2019 年 9 月 30 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-08: Reporting インシデント <br> CUEC-10: サービス契約 | 2019 年 9 月 30 日 |

## <a name="resources"></a>リソース

- [Behind the Scenes: Securing the Infrastructure Powering the Microsoft 365 Service (舞台裏: Microsoft 365 サービスを支えるインフラストラクチャの保護)](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
