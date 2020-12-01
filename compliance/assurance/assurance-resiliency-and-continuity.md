---
title: 復元性と継続性
description: Microsoft 365 の復元と連続性について
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
ms.openlocfilehash: 6763e363938c422ac419fe9e76f9170912627dd5
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507729"
---
# <a name="resiliency-and-continuity-overview"></a>復元と継続性の概要

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>Microsoft は、障害または他の脅威が発生した場合にビジネス継続性をどのように実現していますか。

Microsoft のエンタープライズビジネス継続性管理 (EBCM) チームは、Microsoft のサービスとクラウドサービスにわたってビジネス継続性管理および障害復旧のアクティビティを監視します。 Microsoft 365 などの Microsoft ビジネスユニットの代表者は、ビジネス継続性プランを開発し、ビジネス継続性要件に準拠していることを確認するために、EBCM チームと連携します。

Microsoft のビジネス継続性管理 (BCM) の方法論の中核となるのは、BCM のライフサイクルです。 この3フェーズプロセスは、Microsoft のさまざまなビジネスモデルで実装できるように、適応性を持たせるように設計されています。 ビジネス継続性プログラムに含める必要がある重要なプロセスと目標を特定するための **評価** フェーズから始めます。 評価フェーズでは、ビジネスへの影響分析 (BIA) も必要となります。 **計画** フェーズでは、回復力と回復戦略の策定と展開方法、そしてそれらを公式のビジネス継続性計画としてドキュメント化することに重点を置きます。 最後に、 **機能検証** は、ビジネス継続性プランとその実装をテストして、有効性を確認し、潜在的な改善を特定します。

Microsoft 365 のビジネス継続性戦略では、ハードウェア、ネットワーク、データセンターの冗長性が活用されます。 データセンター間のデータレプリケーションは、致命的なインシデントの場合に高可用性と信頼性を提供します。 また、孤立したハードウェア障害やデータ破損などの平凡なインシデントに対する復元性も向上します。

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Microsoft では、ビジネス継続性と障害復旧の計画をどのようにテストしますか?

Microsoft のエンタープライズビジネス継続性管理 (EBCM) ポリシーにより、Microsoft のすべてのビジネス継続性および障害復旧プランを、年間ベースでテスト、更新、およびレビューする必要があることが stipulates ます。 Microsoft 365 services では、EBCM ポリシーごとに、少なくとも1年間はビジネス継続性プランをテストします。 アクションレポートを作成して確認し、テスト中に検出された問題に対応して、テストの結果を確認して、計画の更新情報を通知します。

EBCM プログラムでは、さまざまなインシデントが発生した場合に備えて、リカバリ力とリカバリ戦略を検証するために、ユーザー、場所、および技術的に影響を与えるテスト シナリオを複数のカテゴリで定義します。 各サービスに必要な検証のレベルは、サービスの重要度に基づいており、より多くの重要なサービスがより厳格な検証を受信します。 各 Microsoft 365 サービスチームは、EBCM ガイドラインに従ってビジネス継続性プランをテストし、プランの有効性とプランを実行するためのサービスチームの準備状況を測定します。

EBCM のガイドラインに従って、ビジネス継続性プランおよび機能の検証の年間レビューは、最後のレビューから12か月以内に行う必要があります。 機能の検証には、BIA などのサポートドキュメントのレビューが含まれている必要があります。これが正確であることを確認する必要があります。 Microsoft は、四半期ごとのレポートを通じてお客様が利用できる Microsoft 365 サービスを選択して、機能の検証結果を提供します。

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>Microsoft 365 は、システム容量が需要を満たしているかどうかを確認します。

キャパシティ プランニングは、サービス チームが Microsoft 365 サービスの可用性をサポートために必要なリソースを割り当てるのに役立ちます。 通常の容量計画は、Microsoft の EBCM プログラムの一部として必要です。 サービス チームは四半期のレビュー時および追加のキャパシティ レビューが必要とされる緊急時に、キャパシティのデータをレビューします。

容量計画の生データは、各サービスチームによって維持され、システムの処理、メモリ、ハードウェアの容量などの測定基準が含まれます。 スケジュールされたレビューでは、システムの現在の容量のモデルを使用し、緊急時に予想されるニーズに照らしてテストします。 モデルにおいてキャパシティにギャップが示された場合、システム キャパシティへの変更の提案が、レビューのためにサービス チーム リーダーシップに送信されます。 承認された変更は、実装前にサービスチームのエンジニアによって新しいモデルに組み込まれます。

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>Microsoft 365 は、日常的なシステム障害時にサービスの可用性を維持する方法を教えてください。

Microsoft 365 は、冗長アーキテクチャ、データレプリケーション、および自動整合性チェックを通じてサービスの復元を実現します。 冗長アーキテクチャでは、サービスの複数のインスタンスを地理的に離れた物理的に独立したハードウェアに展開し、Microsoft 365 サービスのフォールトトレランスを向上させることが必要です。 データレプリケーションを使用すると、異なる障害ゾーンにある顧客データのコピーが常に複数存在することが保証されます。これにより、顧客が破損した場合や、破損した場合や、誤って削除された場合でも、重要な顧客データを回復できます。 整合性チェックの自動化により、多くの種類の物理的または論理的な破損によって影響を受けるデータを自動的に復元することで、データの可用性が向上します。

## <a name="related-external-regulations--certifications"></a>関連する外部規制 & 証明書

Microsoft のオンラインサービスは、社外の規制と証明書に準拠するために定期的に監査されます。 復元性と連続性に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2: コンティンジェンシー計画 <br> CP-3: 緊急時のトレーニング <br> CP-4: コンティンジェンシー計画テスト <br> CP-6: 代替ストレージサイト <br> CP-7: 代替処理サイト <br> CP-9: 情報システムのバックアップ <br> CP-10: 情報システムの回復と reconstitution | 2020年9月24日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 17.1: 情報セキュリティの継続性 <br> 17.2: 重複 | 2020 月 2 月 22 日 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | すべてのコントロール | 2019 年 3 月 18 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: バックアップポリシー <br> CA-50: ビジネス継続性 <br> CA-51: データレプリケーション | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: バックアップポリシー <br> CA-50: ビジネス継続性 <br> CA-51: データレプリケーション | 2019 年 9 月 30 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-09: EXO 電子メールの復元 | 2019 年 9 月 30 日 |

## <a name="resources"></a>リソース

- [Microsoft エンタープライズビジネス継続性管理プログラムに関するホワイトペーパー](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Microsoft Cloud EBCM および障害復旧計画の検証レポート: FY20 Q4](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=5437a1d9-5883-468b-aee0-8c8a8e4ef56a&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>法的免責事項

- [エンタープライズ ビジネス継続性法的免責事項](assurance-ebcm-legal-disclaimer.md)