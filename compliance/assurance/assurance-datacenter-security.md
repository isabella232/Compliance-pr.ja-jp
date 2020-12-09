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
ms.openlocfilehash: 185f926db524f64851e715fecee31e699942fa22
ms.sourcegitcommit: 247ee66ab59d06d2e1b0a3f4dba301c334ebfe71
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "49601271"
---
# <a name="datacenter-security-overview"></a>データセンターのセキュリティの概要

## <a name="how-does-microsoft-host-its-online-services"></a>Microsoft は、オンラインサービスをどのようにホストしていますか?

Microsoft は、microsoft Azure、Microsoft 365、Microsoft Dynamics 365 などのエンタープライズサービスを24時間365日お客様に提供する、200を超えるクラウドサービスを提供しています。 これらのサービスは、グローバルに分散されたデータセンター、エッジコンピューティングノード、およびサービス運用センターから構成される Microsoft のクラウドインフラストラクチャにホストされます。 これらは、世界最大規模のグローバルネットワークの1つによってサポートされ、広範囲にわたるファイバーフットプリントによって接続されています。

Microsoft のクラウド サービスを支えるデータセンターは、世界中の顧客とパートナーのために、高い信頼性、運用の卓越性、費用対効果、環境の持続可能性、信頼できるオンライン エクスペリエンスに重点を置いています。 Microsoft は、社内およびサードパーティの監査を通して、データセンターのセキュリティを定期的にテストしています。 その結果、Microsoft のクラウドは、最も厳しい規制を受けている世界各地の組織から信頼されています。Microsoft のクラウドは、他のどのクラウド サービス プロバイダーよりも多くの認定に準拠しています。

## <a name="how-does-microsoft-protect-its-datacenters-from-unauthorized-access"></a>Microsoft は、承認されていないアクセスからどのようにデータセンターを保護しますか?

物理的なデータセンター機能へのアクセスは、境界線フェンス、セキュリティ担当者、ロックされたサーバーラック、統合されたアラームシステム、操作センターによる24時間ビデオ監視、および多要素アクセス制御を含む、各レベルで厳重に制御されます。 必要な人員のみが Microsoft データセンターへのアクセスを承認されています。 Microsoft のデータセンター内では、お客様のデータを含む、Microsoft 365 インフラストラクチャへの論理的なアクセスが禁止されています。

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
| [ISO 27001/27002 (Azure)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=3383676c-b365-4288-a3c0-086ed8d737e3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=4e5d7afb-2cee-4704-95cc-bb8c95a8e52a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | (11: 物理的および環境のセキュリティ | 2020年5月13日 |
| [SOC 1 (Azure)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=66043614-5628-4e26-83be-057eb3bb026c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | PE-1: データセンターの物理アクセスのプロビジョニング <br> PE-2: データセンターのセキュリティ検証 <br> -3: データセンターのユーザーアクセスのレビュー <br> PE-4: データセンターの物理アクセスメカニズム <br> PE-5: データセンターの物理的監視監視 <br> PE-6: データセンターの重要な環境のメンテナンス <br> PE-7: データセンター環境コントロール <br> PE-8: データセンターインシデントへの対応 | 2020年10月30日 |
| [SOC 2 (Azure)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=ce5bfbea-3514-40ae-a8a6-3617106a0b56&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | PE-1: データセンターの物理アクセスのプロビジョニング <br> PE-2: データセンターのセキュリティ検証 <br> -3: データセンターのユーザーアクセスのレビュー <br> PE-4: データセンターの物理アクセスメカニズム <br> PE-5: データセンターの物理的監視監視 <br> PE-6: データセンターの重要な環境のメンテナンス <br> PE-7: データセンター環境コントロール <br> PE-8: データセンターインシデントへの対応 | 2020年10月30日 |
