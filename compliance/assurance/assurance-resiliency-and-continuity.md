---
title: 回復性と継続性
description: Microsoft 365 の回復性と継続性について
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
ms.openlocfilehash: 2cc3f35a9d109a1a84159de8d0518f58270e3fe9
ms.sourcegitcommit: 1dc97ae3f0511cb1a41565da56e725bbe0cb013c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/14/2020
ms.locfileid: "49671182"
---
# <a name="resiliency-and-continuity-overview"></a>回復性と継続性の概要

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>障害またはサービスの可用性に対するその他の脅威が発生した場合、Microsoft はどのようにビジネス継続性を確保しますか?

Microsoft の Enterprise Business Continuity Management (EBCM) チームは、Microsoft サービスとクラウドサービス全体のビジネス継続性管理と障害復旧アクティビティを監督します。 Microsoft 365 などの Microsoft ビジネス ユニットの代表者は、EBCM チームと調整して、ビジネス継続性計画を策定し、ビジネス継続性要件への準拠を検証します。

ビジネス継続性管理 (BCM) の方法論の中核をなすのは、BCM ライフサイクルです。 この 3 段階のプロセスは、Microsoft 全体のさまざまなビジネス モデルで実装できるよう、適応可能に設計されています。 まず、ビジネス継続性 **プログラム** に含める必要がある重要なプロセスと目標を特定するための Assessment フェーズから始まります。 評価フェーズでは、ビジネス影響分析 (BIA) も必要です。 **計画** フェーズでは、回復力と回復戦略の策定と展開方法、そしてそれらを公式のビジネス継続性計画としてドキュメント化することに重点を置きます。 最後に、 **機能検証では** 、ビジネス継続性計画とその実装をテストして、有効性を検証し、潜在的な改善点を特定します。

Microsoft 365 のビジネス継続性戦略では、ハードウェア、ネットワーク、データセンターの冗長性を活用しています。 データ センター間のデータ レプリケーションは、災害が発生した場合の高可用性と信頼性を提供します。 また、分離されたハードウェア障害やデータの破損など、非常に大きく発生するインシデントに対する回復性も向上します。

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Microsoft はビジネス継続性と障害復旧計画をテストする方法を説明します。

Microsoft のエンタープライズ ビジネス継続性管理 (EBCM) ポリシーでは、すべての Microsoft ビジネス継続性および障害復旧計画を年単位でテスト、更新、およびレビューする必要があります。 Microsoft 365 サービスは、EBCM ポリシーごとに少なくとも年に 1 回、ビジネス継続性計画をテストします。 After Action reports are created and reviewed to validate, test results and inform plan updates in response to any problems discovered during testing.

EBCM プログラムでは、さまざまなインシデントが発生した場合に備えて、リカバリ力とリカバリ戦略を検証するために、ユーザー、場所、および技術的に影響を与えるテスト シナリオを複数のカテゴリで定義します。 各サービスに必要な検証のレベルは、サービスのクリティカル度に基づいており、より重要なサービスではより厳密な検証を受けることができます。 各 Microsoft 365 サービス チームは、EBCM ガイドラインに従ってビジネス継続性計画をテストし、計画の有効性とサービス チームが計画を実行する準備を測定します。

EBCM ガイドラインに従って、ビジネス継続性計画と機能検証の年次レビューは、最後のレビューから 12 か月以内に行う必要があります。 機能の検証には、正確な状態を維持するために、BIA などのサポート ドキュメントのレビューを含める必要があります。 Microsoft では、四半期レポートを通じて、お客様が利用できる Microsoft 365 サービスを選択した場合の機能検証結果を作成しています。

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>Microsoft 365 では、システム容量が需要を満たす方法について説明します。

キャパシティ プランニングは、サービス チームが Microsoft 365 サービスの可用性をサポートために必要なリソースを割り当てるのに役立ちます。 Microsoft の EBCM プログラムの一部として、定期的な容量計画が必要です。 サービス チームは四半期のレビュー時および追加のキャパシティ レビューが必要とされる緊急時に、キャパシティのデータをレビューします。

容量計画用の生データは各サービス チームによって管理され、システム処理、メモリ、ハードウェア容量のような指標が含まれます。 スケジュールされたレビューでは、システムの現在の容量のモデルを使用し、緊急の状況で投影されたニーズに対してテストします。 モデルにおいてキャパシティにギャップが示された場合、システム キャパシティへの変更の提案が、レビューのためにサービス チーム リーダーシップに送信されます。 承認された変更は、実装前にサービスチームのエンジニアによって新しいモデルに組み込まれます。

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>日常的なシステム障害時に Microsoft 365 がサービスの可用性を維持する方法

Microsoft 365 は、冗長アーキテクチャ、データ レプリケーション、自動整合性チェックを通じてサービスの回復性を実現します。 冗長アーキテクチャでは、地理的および物理的に独立したハードウェアにサービスの複数のインスタンスを展開し、Microsoft 365 サービスのフォールト トレランスを高める必要があります。 データ レプリケーションにより、異なる障害領域に顧客データのコピーが常に複数あるため、破損、紛失、または誤って顧客によって削除された場合でも、重要な顧客データを回復できます。 自動整合性チェックは、さまざまな種類の物理的または論理的破損の影響を受けたデータを自動的に復元することで、データの可用性を向上します。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 回復性と継続性に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2: 対応計画 <br> CP-3: コントナンシー トレーニング <br> CP-4: コントナンシー計画のテスト <br> CP-6: 代替ストレージ サイト <br> CP-7: 代替処理サイト <br> CP-9: 情報システムのバックアップ <br> CP-10: 情報システムの回復と調整 | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: 情報セキュリティの継続性 <br> A.17.2: 冗長性 | 2020 月 2 月 22 日 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | すべてのコントロール | 2019 年 3 月 18 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: バックアップ ポリシー <br> CA-50: ビジネス継続性 <br> CA-51: データ レプリケーション | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: バックアップ ポリシー <br> CA-50: ビジネス継続性 <br> CA-51: データ レプリケーション | 2019 年 9 月 30 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-09: EXO 電子メールの復元 | 2019 年 9 月 30 日 |

## <a name="resources"></a>リソース

- [Microsoft Enterprise ビジネス継続性管理プログラムホワイトペーパー](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Microsoft Cloud EBCM および障害復旧計画検証レポート: FY21 Q1 および Q2](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=b4181ab3-b03d-4a62-b396-4bfd1c98ddb0&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>法的免責事項

- [エンタープライズ ビジネス継続性法的免責事項](assurance-ebcm-legal-disclaimer.md)