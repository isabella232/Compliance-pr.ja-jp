---
title: データセンターのセキュリティの概要
description: データ センターのセキュリティについてMicrosoft 365
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
ms.openlocfilehash: b2f88172d2a8158a2232acd1c4312217d7c3fef4
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482090"
---
# <a name="datacenter-security-overview"></a>データセンターのセキュリティの概要

## <a name="how-does-microsoft-host-its-online-services"></a>Microsoft はオンライン サービスをホストする方法を説明します。

Microsoft は、Microsoft Azure、Microsoft 365、Microsoft Dynamics 365 などのエンタープライズ サービスを含む 200 以上のクラウド サービスを 24x7x365 のお客様に提供しています。 これらのサービスは、グローバルに分散されたデータセンター、エッジ コンピューティング ノード、およびサービス運用センターで構成される Microsoft のクラウド インフラストラクチャでホストされます。 これらは、広範なファイバーフットプリントを持つ、世界最大のグローバル ネットワークの 1 つによってサポートされ、接続されています。

Microsoft のクラウド サービスを支えるデータセンターは、世界中の顧客とパートナーのために、高い信頼性、運用の卓越性、費用対効果、環境の持続可能性、信頼できるオンライン エクスペリエンスに重点を置いています。 Microsoft は、社内およびサードパーティの監査を通して、データセンターのセキュリティを定期的にテストしています。 その結果、Microsoft のクラウドは、最も厳しい規制を受けている世界各地の組織から信頼されています。Microsoft のクラウドは、他のどのクラウド サービス プロバイダーよりも多くの認定に準拠しています。

## <a name="how-does-microsoft-protect-its-datacenters-from-unauthorized-access"></a>Microsoft では、データ センターを不正アクセスから保護する方法を説明します。

物理的なデータセンター施設へのアクセスは、境界フェンシング、セキュリティ担当者、ロックされたサーバー ラック、統合アラーム システム、運用センターによる 24 時間体制のビデオ監視、多要素アクセス制御など、各レベルでセキュリティが強化されるとともに、外部および内部の境界によって厳しく制御されます。 Microsoft データセンターへのアクセスを許可されているのは、必須の担当者のみです。 顧客データを含Microsoft 365インフラストラクチャへの論理的なアクセスは、Microsoft データセンター内では禁止されています。

Microsoft のセキュリティ オペレーション センターでは、統合された電子アクセス制御システムと共にビデオ監視システムを使用して、データセンターのサービス拠点や施設を監視しています。 カメラは、施設の外周、エントランス、出荷エリア、サーバー ケージ、内部の通路、その他の機密性の高いセキュリティ上の注目ポイントを効果的にカバーするために戦略的に配置されています。 Microsoft の多層的なセキュリティ態勢の一環として、統合セキュリティ システムによって検出された不正な侵入の試みは、セキュリティ担当者へのアラートを生成し、即座に対応と是正を行います。

## <a name="how-does-microsoft-protect-its-datacenters-from-environmental-hazards"></a>Microsoft はデータセンターを環境上の危険からどのように保護しますか?

Microsoft では、データセンターの可用性に対する環境上の脅威から保護するために、さまざまなセーフガードを採用しています。 データセンター サイトは、洪水、地震、ハリケーン、その他の自然災害など、さまざまな要因によるリスクを最小限に抑えるために戦略的に選択されています。 データセンターでは、気候制御を使用して、スタッフ、機器、およびハードウェア用に最適化された調整スペースを監視および維持します。 火災検出および抑制システムと水センサーは、機器の火災や水の損傷を検出および防止するのに役立ちます。

障害は予測できないものですが、Microsoft のデータセンターと運用担当者は、障害発生時の最悪の事態を想定して準備しています。 回復性の高いアーキテクチャとテスト済みの最新の継続性計画により、潜在的な損害を軽減し、データセンター運用の迅速な復元を促進します。 危機管理計画では、危機の発生前、発生中、発生後における役割、責任、および軽減活動を明確にします。 危機状況において、これらの計画で定義される役割と連絡先は、指揮系統における効果的なエスカレーションを促します。

## <a name="how-does-microsoft-verify-the-effectiveness-of-datacenter-security"></a>Microsoft はデータセンター のセキュリティの有効性を確認する方法を説明します。

Microsoft では、お客様にクラウドのメリットを最大限に活用していただくには、お客様がクラウド サービス プロバイダーを信頼できる必要があることを理解しています。 Microsoft のクラウド サービスのインフラストラクチャとスイートは、お客様の厳しいセキュリティとプライバシーに関する要件に対処できるよう一から構築されています。 個人データの収集と使用を規定する国、地域、業界固有の要件にお客様が準拠できるよう、他のクラウド プロバイダーにはない、最も包括的なコンプライアンス サービスを提供します。

Microsoft のクラウド インフラストラクチャとサービスは、ISO、HIPAA、FedRAMP、SOC などの国際的および業界固有のコンプライアンス標準の他、オーストラリアの IRAP、英国の G-Cloud、シンガポールの MTCS のような各国固有の標準に適合しています。 厳しい第三者監査により、これらの標準で義務付けられている厳格なセキュリティ制御に Microsoft が準拠していることが確認されます。  データセンター インフラストラクチャとクラウド サービスの監査レポートは [、Microsoft Service Trust Portal で確認できます](https://servicetrust.microsoft.com/)。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 データセンター のセキュリティに関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|  
| [ISO 27001/27002 (Azure)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11: 物理的および環境的なセキュリティ | 2020 年 12 月 2 日 |
| [SOC 1 (Azure)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=66043614-5628-4e26-83be-057eb3bb026c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | PE-1: データセンターの物理アクセス プロビジョニング <br> PE-2: データセンターのセキュリティ検証 <br> PE-3: データセンターのユーザー アクセス レビュー <br> PE-4: データセンターの物理アクセスメカニズム <br> PE-5: データセンターの物理的監視監視 <br> PE-6: データセンターの重要な環境のメンテナンス <br> PE-7: データセンター環境制御 <br> PE-8: データセンターインシデント対応 | 2020 年 10 月 30 日 |
| [SOC 2 (Azure)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=ce5bfbea-3514-40ae-a8a6-3617106a0b56&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | PE-1: データセンターの物理アクセス プロビジョニング <br> PE-2: データセンターのセキュリティ検証 <br> PE-3: データセンターのユーザー アクセス レビュー <br> PE-4: データセンターの物理アクセスメカニズム <br> PE-5: データセンターの物理的監視監視 <br> PE-6: データセンターの重要な環境のメンテナンス <br> PE-7: データセンター環境制御 <br> PE-8: データセンターインシデント対応 | 2020 年 10 月 30 日 |

## <a name="resources"></a>リソース

- [Microsoft Story Labs: We Live in the Cloud](https://news.microsoft.com/stories/microsoft-datacenter-tour/)