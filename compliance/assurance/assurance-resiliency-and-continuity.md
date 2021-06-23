---
title: 回復性および継続性
description: 回復性と継続性の詳細については、Microsoft 365
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
hideEdit: true
ms.openlocfilehash: 9ac4a87670d1889e9c74e5ec6afe8920b96946fc
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088776"
---
# <a name="resiliency-and-continuity-overview"></a>回復性および継続性の概要

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>障害やサービスの可用性に対するその他の脅威が発生した場合、Microsoft はどのようにビジネスの継続性を確保しますか?

Microsoft の Enterprise ビジネス継続性管理 (EBCM) チームは、ビジネス継続性管理と障害復旧活動を、Microsoft サービスおよびクラウド製品全体にわたって監督します。 microsoft ビジネス ユニット (Microsoft 365 など) の担当者は、EBCM チームと調整して、ビジネス継続性計画を策定し、ビジネス継続性要件への準拠を検証します。

ビジネス継続性管理 (BCM) の方法論の中核となるのは、BCM ライフサイクルです。 この 3 フェーズ プロセスは、Microsoft 全体のさまざまなビジネス モデルによって実装できるよう、適応可能な設計です。 まず、ビジネス継続性 **プログラム** に含める必要がある重要なプロセスと目標を特定するための評価フェーズから始まります。 また、評価フェーズでは、ビジネス影響分析 (BIA) も必要です。 **計画** フェーズでは、回復力と回復戦略の策定と展開方法、そしてそれらを公式のビジネス継続性計画としてドキュメント化することに重点を置きます。 最後に、 **機能検証は** 、ビジネス継続性計画とその実装をテストして、有効性を検証し、潜在的な改善点を特定します。

Microsoft 365のビジネス継続性戦略は、ハードウェア、ネットワーク、データセンターの冗長性を活用します。 データセンター間のデータ レプリケーションは、致命的なインシデントが発生した場合の高可用性と信頼性を提供します。 また、分離されたハードウェア障害やデータ破損などの平凡なインシデントに対する回復力も向上します。

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Microsoft は、ビジネス継続性と障害復旧計画をテストする方法を説明します。

Microsoft の Enterprise Business Continuity Management (EBCM) ポリシーでは、すべての Microsoft ビジネス継続性と障害復旧計画を毎年テスト、更新、およびレビューする必要があります。 Microsoft 365サービスは、EBCM ポリシーごとに少なくとも毎年、ビジネス継続性計画をテストします。 After Action reports are created and reviewed to validate, test results and inform plan updates to response to discovered any problems in test.

EBCM プログラムでは、さまざまなインシデントが発生した場合に備えて、リカバリ力とリカバリ戦略を検証するために、ユーザー、場所、および技術的に影響を与えるテスト シナリオを複数のカテゴリで定義します。 各サービスに必要な検証のレベルは、サービスの重大性に基づいており、より重要なサービスは、より厳密な検証を受け取ります。 各Microsoft 365サービス チームは、EBCM ガイドラインに従ってビジネス継続計画をテストし、計画の有効性とサービス チームが計画を実行する準備を測定します。

EBCM ガイドラインに従って、ビジネス継続性計画と機能検証の年次レビューは、前回のレビューから 12 か月以内に行う必要があります。 機能の検証には、正確な状態を維持するために、BIA などのサポート ドキュメントのレビューが含まれる必要があります。 Microsoft は、四半期ごとにレポートを通じてMicrosoft 365サービスの機能検証結果を利用できます。

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>システム容量がMicrosoft 365満たされる方法

キャパシティ プランニングは、サービス チームが Microsoft 365 サービスの可用性をサポートために必要なリソースを割り当てるのに役立ちます。 Microsoft の EBCM プログラムの一部として、定期的な容量計画が必要です。 サービス チームは四半期のレビュー時および追加のキャパシティ レビューが必要とされる緊急時に、キャパシティのデータをレビューします。

容量計画の生データは、各サービス チームによって管理され、システム処理、メモリ、ハードウェア容量など、メトリックが含まれます。 スケジュールされたレビューでは、システムの現在の容量のモデルを使用し、緊急の状況で計画されたニーズに対してテストします。 モデルにおいてキャパシティにギャップが示された場合、システム キャパシティへの変更の提案が、レビューのためにサービス チーム リーダーシップに送信されます。 承認された変更は、実装前にサービスチームのエンジニアによって新しいモデルに組み込まれます。

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>定期的なシステムMicrosoft 365サービスの可用性を維持する方法

Microsoft 365アーキテクチャ、データ レプリケーション、自動整合性チェックにより、サービスの復元を実現します。 冗長アーキテクチャでは、地理的および物理的に分離されたハードウェアにサービスの複数のインスタンスを展開し、サービスのフォールト トレランスをMicrosoft 365します。 データレプリケーションにより、異なる障害領域に顧客データのコピーが常に複数含まれており、顧客が破損、紛失、または誤って削除した場合に重要な顧客データを回復できます。 自動整合性チェックは、さまざまな種類の物理的または論理的な破損の影響を受けたデータを自動的に復元することで、データの可用性を向上します。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 回復性と継続性に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2: コントナンシー プラン <br> CP-3: コントナンシー トレーニング <br> CP-4: コントナンシー 計画のテスト <br> CP-6: 代替ストレージ サイト <br> CP-7: 代替処理サイト <br> CP-9: 情報システムのバックアップ <br> CP-10: 情報システムの回復と再調整 | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: 情報セキュリティの継続性 <br> A.17.2: 冗長性 | 2021 年 4 月 20 日 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | すべてのコントロール | 2019 年 3 月 18 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: バックアップ ポリシー <br> CA-50: ビジネスの継続性 <br> CA-51: データ レプリケーション | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: バックアップ ポリシー <br> CA-50: ビジネスの継続性 <br> CA-51: データ レプリケーション | 2020 年 12 月 24 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-09: EXO メールの復元 | 2020 年 12 月 24 日 |

## <a name="resources"></a>リソース

- [Microsoft Enterprise ビジネス継続性管理プログラム Whitepaper](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Microsoft Cloud EBCM と障害復旧計画検証レポート: FY21 Q3](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=c072d11c-9cc9-42e1-b1cf-7281572fb1dd&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>法的免責事項

- [エンタープライズ ビジネス継続性法的免責事項](assurance-ebcm-legal-disclaimer.md)