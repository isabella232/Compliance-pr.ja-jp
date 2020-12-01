---
title: データセンターのセキュリティの概要
description: Microsoft 365 でのデータセンターのセキュリティについて
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
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
ms.openlocfilehash: 52b8841f8d89571ea73fa469b05a776e0e0d3557
ms.sourcegitcommit: 186caf3b458d014f127bdf6e2d927c413276d9e1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/01/2020
ms.locfileid: "49520124"
---
# <a name="datacenter-security-overview"></a>データセンターのセキュリティの概要

## <a name="how-does-microsoft-host-its-online-services"></a>Microsoft は、オンラインサービスをどのようにホストしていますか?

Microsoft は、microsoft Azure、Microsoft 365、Microsoft Dynamics 365 などのエンタープライズサービスを24時間365日お客様に提供する、200を超えるクラウドサービスを提供しています。 これらのサービスは、グローバルに分散されたデータセンター、エッジコンピューティングノード、およびサービス運用センターから構成される Microsoft のクラウドインフラストラクチャにホストされます。 これらは、世界最大規模のグローバルネットワークの1つによってサポートされ、広範囲にわたるファイバーフットプリントによって接続されています。

Microsoft のクラウド サービスを支えるデータセンターは、世界中の顧客とパートナーのために、高い信頼性、運用の卓越性、費用対効果、環境の持続可能性、信頼できるオンライン エクスペリエンスに重点を置いています。 Microsoft は、社内およびサードパーティの監査を通して、データセンターのセキュリティを定期的にテストしています。 その結果、Microsoft のクラウドは、最も厳しい規制を受けている世界各地の組織から信頼されています。Microsoft のクラウドは、他のどのクラウド サービス プロバイダーよりも多くの認定に準拠しています。

## <a name="how-does-microsoft-protect-its-datacenters-from-unauthorized-access"></a>Microsoft は、承認されていないアクセスからどのようにデータセンターを保護しますか?

物理的なデータセンター機能へのアクセスは、境界線フェンス、セキュリティ担当者、ロックされたサーバーラック、統合されたアラームシステム、操作センターによる24時間ビデオ監視、および多要素アクセス制御を含む、各レベルで厳重に制御されます。 必要な人員のみが Microsoft データセンターへのアクセスを承認されています。 お客様のデータを含む Microsoft 365 インフラストラクチャへの論理的なアクセスは、Microsoft データセンター内から完全に禁止されています。

Microsoft のセキュリティ オペレーション センターでは、統合された電子アクセス制御システムと共にビデオ監視システムを使用して、データセンターのサービス拠点や施設を監視しています。 カメラは、施設の外周、エントランス、出荷エリア、サーバー ケージ、内部の通路、その他の機密性の高いセキュリティ上の注目ポイントを効果的にカバーするために戦略的に配置されています。 Microsoft の多層的なセキュリティ態勢の一環として、統合セキュリティ システムによって検出された不正な侵入の試みは、セキュリティ担当者へのアラートを生成し、即座に対応と是正を行います。

## <a name="how-does-microsoft-protect-its-datacenters-from-environmental-hazards"></a>Microsoft は、環境の危険からどのようにデータセンターを保護していますか?

Microsoft では、データセンターの可用性に対する環境上の脅威から保護するために、さまざまな予防手段を採用しています。 データセンターサイトは、洪水、地震、ハリケーン、その他の自然災害など、さまざまな要因からのリスクを最小限にするために戦略的に選択されています。 データセンターは、気候管理を使用して、スタッフ、機器、およびハードウェア用に最適化されたスペースを監視および維持します。 火災検知/抑制システムとウォーターセンサーを使用して、機器への火災や水の損傷を検出し、阻止します。

障害は予測できないものですが、Microsoft のデータセンターと運用担当者は、障害発生時の最悪の事態を想定して準備しています。 回復性の高いアーキテクチャとテスト済みの最新の継続性計画により、潜在的な損害を軽減し、データセンター運用の迅速な復元を促進します。 危機管理計画では、危機の発生前、発生中、発生後における役割、責任、および軽減活動を明確にします。 危機状況において、これらの計画で定義される役割と連絡先は、指揮系統における効果的なエスカレーションを促します。

## <a name="how-does-microsoft-verify-the-effectiveness-of-datacenter-security"></a>Microsoft はデータセンターのセキュリティの有効性を確認する方法を教えてください。

Microsoft では、お客様にクラウドのメリットを最大限に活用していただくには、お客様がクラウド サービス プロバイダーを信頼できる必要があることを理解しています。 Microsoft のクラウド サービスのインフラストラクチャとスイートは、お客様の厳しいセキュリティとプライバシーに関する要件に対処できるよう一から構築されています。 お客様は、クラウドサービスプロバイダーのコンプライアンスに関する最も包括的な一連のサービスを提供することにより、個人データの収集と使用を管理する各国、地域、および業界固有の要件に準拠しています。

Microsoft のクラウド インフラストラクチャとサービスは、ISO、HIPAA、FedRAMP、SOC などの国際的および業界固有のコンプライアンス標準の他、オーストラリアの IRAP、英国の G-Cloud、シンガポールの MTCS のような各国固有の標準に適合しています。 厳しい第三者監査により、これらの標準で義務付けられている厳格なセキュリティ制御に Microsoft が準拠していることが確認されます。  マイクロソフトのデータセンターインフラストラクチャとクラウドサービスの監査レポートは、 [Microsoft Service Trust Portal](https://servicetrust.microsoft.com/)から入手できます。

## <a name="related-external-regulations--certifications"></a>関連する外部規制 & 証明書

Microsoft のオンラインサービスは、社外の規制と証明書に準拠するために定期的に監査されます。 データセンターセキュリティに関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | 「PE-2: 物理的なアクセス承認」 <br> PE-3: 物理的なアクセス制御 <br> PE-6: 物理的なアクセスを監視する <br> PE-11: 緊急時電源 <br> PE-13: ファイヤプロテクション <br> PE-14: 温度と湿度の制御 <br> PE-15: ウォーターダメージ保護 | 2020年9月24日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | (11: 物理的および環境のセキュリティ | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | (11: 物理的および環境のセキュリティ | 2020 月 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-39: データセンターアクセスコントロール <br> CA-40: データセンターネットワーク認証 <br> CA-41: データセンター2要素認証 <br> CA-48: データセンターログ | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-39: データセンターアクセスコントロール <br> CA-40: データセンターネットワーク認証 <br> CA-41: データセンター2要素認証 <br> CA-48: データセンターログ | 2019 年 9 月 30 日 |
