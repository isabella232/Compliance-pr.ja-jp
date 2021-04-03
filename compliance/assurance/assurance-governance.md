---
title: ガバナンスの概要
description: Microsoft 365 のガバナンスの詳細
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
ms.openlocfilehash: 2ccbd650a2d97af8ea0774e6272fae819e8c732f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497191"
---
# <a name="governance-overview"></a>ガバナンスの概要

## <a name="how-does-microsoft-provide-effective-security-governance-across-the-enterprise"></a>Microsoft は、企業全体で効果的なセキュリティ ガバナンスを提供する方法を説明します。

Microsoft は、Microsoft の情報システムと顧客を保護するために、効果的なセキュリティ ポリシーを企業全体で一貫して実装する必要があります。 セキュリティポリシーは、ビジネス機能と情報システムのバリエーションを考慮して、普遍的に適用できるようにすることも必要です。 これらの要件を満たすために、Microsoft は Microsoft ポリシー フレームワークの一部として包括的なセキュリティ ガバナンス プログラムを実装しています。 セキュリティガバナンスは、Microsoft セキュリティポリシー (MSP) に含まれます。

MSP は、Microsoft のセキュリティ ポリシー、標準、および要件を整理し、すべての Microsoft エンジニアリング グループとビジネス ユニットに実装できます。 個々のビジネス単位は、Microsoft セキュリティポリシーの特定の実装を担当します。 たとえば、Microsoft 365 は、Microsoft 365 Information Security Policy および関連する Microsoft 365 コントロール フレームワークにセキュリティ実装を文書化しています。 これらのセキュリティ実装は、MSP の目標と目標に合わせて行います。

Microsoft のセキュリティ ガバナンス プログラムは、さまざまな規制およびコンプライアンス フレームワークによって通知され、対応します。 セキュリティ要件は、新しいテクノロジ、規制とコンプライアンスの要件、およびセキュリティの脅威を考慮して絶えず進化しています。 これらの変更により、Microsoft は Microsoft のシステムと顧客を保護し、コミットメントを満たし、顧客の信頼を維持するために、セキュリティ ポリシーとサポート ドキュメントを定期的に更新しています。

## <a name="how-does-microsoft-365-implement-the-microsoft-security-policy-msp"></a>Microsoft 365 は Microsoft セキュリティ ポリシー (MSP) を実装する方法を説明します。

Microsoft 365 は、Microsoft 365 情報セキュリティ ポリシーでセキュリティの実装を文書化しています。 このポリシーは、Microsoft セキュリティ ポリシーに準拠し、データの収集、処理、保守、使用、共有、配布、および廃棄に関連するすべての Microsoft 365 環境とすべてのリソースを含む Microsoft 365 情報システムを管理します。

Microsoft 365 情報システムには、Microsoft 365 情報セキュリティ ポリシーで管理される次のコンポーネントが含まれています。

- インフラストラクチャ: Microsoft 36 5システムの物理コンポーネントとハードウェアコンポーネント (設備、機器、ネットワーク)
- ソフトウェア: Microsoft 365 システムのプログラムとオペレーティング ソフトウェア (システム、アプリケーション、ユーティリティ)
- ユーザー: Microsoft 365 システムの操作と使用に関与する担当者 (開発者、オペレーター、ユーザー、マネージャー)
- 手順: Microsoft 365 システムの操作に関連するプログラムされた手順と手動の手順
- データ: Microsoft 365 システムによって生成、収集、処理された情報 (トランザクション ストリーム、ファイル、データベース、テーブル)

Microsoft 365 情報セキュリティ ポリシーは、Microsoft 365 コントロール フレームワークによって補足されます。 Microsoft 365 コントロール フレームワークでは、すべての Microsoft 365 サービスおよび情報システム コンポーネントの最小セキュリティ要件について詳しくは説明します。 また、各コントロールの背後にある法的要件と企業要件も参照します。 フレームワークには、サービス チームによる効果的な制御の実装を確実にするための制御アクティビティ名、説明、およびガイダンスが含まれています。 Microsoft 365 は、コントロール フレームワークを使用して、内部および外部レポートの制御実装を追跡します。

## <a name="how-does-microsoft-365-limit-and-track-exceptions-to-established-policies"></a>Microsoft 365 は、確立されたポリシーに対する例外を制限および追跡する方法を説明します。

Microsoft 365 情報セキュリティ ポリシーの例外はすべて、正当なビジネス上の正当性があり、Microsoft 365 内の適切なガバナンス エンティティによって承認される必要があります。 例外には、サービス チーム管理の承認も必要であり、Microsoft 365 リスク管理ツールに文書化されている必要があります。 例外の範囲とそれが表す潜在的なリスクによっては、例外の承認を企業の副社長以上から取得する必要がある場合があります。 例外は Microsoft 365 リスク管理ツールで追跡され、継続的な関連性が確認され、承認されます。

## <a name="how-does-microsoft-365-keep-security-and-compliance-requirements-updated"></a>Microsoft 365 では、セキュリティ要件とコンプライアンス要件を更新する方法を説明します。

Microsoft 365 信頼チームは、内部 Microsoft 365 コントロール フレームワークを継続的に維持するために取り組んでいます。 いくつかのシナリオでは、関連する規制や法律の変更、新たな脅威、侵入テスト結果、セキュリティ インシデント、監査フィードバック、新しいコンプライアンス要件など、管理フレームワークを更新する必要があります。 フレームワークの変更が必要な場合、信頼チームは、変更の承認と実装を担当する主要な関係者を特定し、それが実行可能であり、Microsoft 365 サービスに意図しない問題を引き起こさなくします。 信頼チームと関連する関係者が変更に必要な情報に同意すると、変更セットの目標完了日を実装するワークロードと、それぞれのサービス内で変更を実装するために作業を行います。 実装ターゲットが満たされた後、信頼チームは新しいコントロールまたは更新されたコントロールでコントロール フレームワークを更新します。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 ガバナンスに関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CA-2: セキュリティ評価 <br> PL-2: システム セキュリティ計画 | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.18.1: 法的および契約上の要件の遵守 | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.18.1: 法的および契約上の要件の遵守 | 2020 月 2 月 22 日 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.2.1: パブリック クラウド PII プロセッサの目的 | 2018 年 11 月 10 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-11: ポリシー フレームワークの更新 <br> CA-12: サービス レベル契約 (SLA) <br> CA-17: Microsoft セキュリティ ポリシー <br> CA-25: コントロール フレームワークの更新 | 2020 年 12 月 24 日 |

## <a name="resources"></a>リソース

- [Microsoft セキュリティ ポリシー](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=bc35aefb-ec41-4a0e-bfc7-10aa5169ca88&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Microsoft セキュリティ プログラム ポリシー](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=4b010ac5-2861-4d20-b8ff-db77875b43a9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)