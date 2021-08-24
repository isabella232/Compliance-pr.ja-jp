---
title: ガバナンスの概要
description: Microsoft オンライン サービスのコンプライアンス ガバナンスについて説明します。
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
ms.openlocfilehash: 86885737bb3e6acd0a9503c240b09cb3349da7a8
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481979"
---
# <a name="governance-overview"></a>ガバナンスの概要

## <a name="how-does-microsoft-provide-effective-security-governance-across-the-enterprise"></a>Microsoft は、企業全体で効果的なセキュリティ ガバナンスを提供する方法を説明します。

Microsoft は、Microsoft の情報システムと顧客を保護するために、効果的なセキュリティ ポリシーを企業全体で一貫して実装する必要があります。 セキュリティポリシーは、ビジネス機能と情報システムのバリエーションを考慮して、普遍的に適用できるようにすることも必要です。 これらの要件を満たすために、Microsoft は Microsoft ポリシー フレームワークの一部として包括的なセキュリティ ガバナンス プログラムを実装しています。 セキュリティガバナンスは、Microsoft セキュリティポリシー (MSP) に含まれます。

MSP は、Microsoft のセキュリティポリシー、標準、および要件が組み込まれており、すべての Microsoft エンジニアリング グループやビジネス ユニットに実装できるようにします。 個々のビジネス単位は、Microsoft セキュリティ ポリシーの特定の実装を担当します。 たとえば、Microsoft 365情報セキュリティ ポリシーと関連するコントロール フレームワークMicrosoft 365のセキュリティ実装をMicrosoft 365します。 Azure と Dynamics 365 は、セキュリティ実装を標準オペレーティング プロシージャ (SOP) と Azure Control Framework に文書化します。 これらのセキュリティ実装は、MSP の目標と目標に合わせて行います。

Microsoft のセキュリティ ガバナンス プログラムは、さまざまな規制およびコンプライアンス フレームワークによって通知され、対応します。 セキュリティ要件は、新しいテクノロジ、規制とコンプライアンスの要件、およびセキュリティの脅威を考慮して絶えず進化しています。 これらの変更により、Microsoft は Microsoft のシステムと顧客を保護し、コミットメントを満たし、顧客の信頼を維持するために、セキュリティ ポリシーとサポート ドキュメントを定期的に更新しています。

## <a name="how-do-microsoft-online-services-implement-the-microsoft-security-policy-msp"></a>Microsoft オンライン サービスは、Microsoft セキュリティ ポリシー (MSP) を実装する方法を説明します。

Microsoft 365 は、Microsoft 365 情報セキュリティ ポリシーでセキュリティの実装を文書化しています。 このポリシーは、Microsoft セキュリティ ポリシーに準拠し、データの収集、処理、保守、使用、共有、配布、および廃棄に関連するすべての Microsoft 365 環境とすべてのリソースを含む Microsoft 365 情報システムを管理します。 同様に、Azure と Dynamics 365 は Microsoft セキュリティ ポリシーを使用して情報システムを管理します。

情報システムには、Microsoft 365 情報セキュリティ ポリシー (Microsoft 365 用) と Microsoft セキュリティ ポリシー (Azure および Dynamics 365 用) が管理する次のコンポーネントが含まれます。

- インフラストラクチャ: Azure、Dynamics 365、および Microsoft 365 システム (施設、機器、およびネットワーク) の物理コンポーネントとハードウェア コンポーネント
- ソフトウェア: Azure、Dynamics 365、および Microsoft 365 システム (システム、アプリケーション、ユーティリティ) のプログラムとオペレーティング ソフトウェア
- ユーザー: Azure、Dynamics 365、および Microsoft 365 システム (開発者、オペレーター、ユーザー、管理者) の操作と使用に関わる担当者
- 手順: Azure、Dynamics 365、および Microsoft 365 システムの操作に関連する、プログラムと手動Microsoft 365手順
- データ: Azure、Dynamics 365、および Microsoft 365 システム (トランザクション ストリーム、ファイル、データベース、およびテーブル) によって生成、収集、および処理される情報

Microsoft 365 情報セキュリティ ポリシーは、Microsoft 365 コントロール フレームワークによって補足されます。 このMicrosoft 365コントロール フレームワークでは、すべてのサービスおよび情報システム コンポーネントのMicrosoft 365セキュリティ要件について詳しくは説明します。 また、各コントロールの背後にある法的要件と企業要件も参照します。 フレームワークには、サービス チームによる効果的な制御の実装を確実にするための制御アクティビティ名、説明、およびガイダンスが含まれています。 Microsoft 365フレームワークを使用して、内部および外部レポートの制御実装を追跡します。 同様に、Azure コントロール フレームワークでの Azure および Dynamics 365 レコード制御の実装も同様です。

## <a name="how-do-online-services-limit-and-track-exceptions-to-established-policies-and-procedures"></a>オンライン サービスは、確立されたポリシーと手順に対して例外を制限および追跡する方法を説明します。

コントロール フレームワークのすべての例外は、正当なビジネス上の正当な理由を持ち、各オンライン サービス チーム内の適切なガバナンス エンティティによって承認される必要があります。 例外の範囲とそれが表す潜在的なリスクによっては、例外の承認を企業の副社長以上から取得する必要がある場合があります。 例外は追跡ツールで管理され、継続的な関連性が確認され、承認されます。

## <a name="how-do-online-services-keep-security-and-compliance-requirements-updated"></a>オンライン サービスでセキュリティとコンプライアンスの要件を更新する方法

各オンライン サービス (GRC) のガバナンス、リスク、コンプライアンス チームは、コントロール フレームワークを継続的に維持するために取り組んでいます。 関連する規制や法律の変更、新たな脅威、侵入テスト結果、セキュリティ インシデント、監査フィードバック、新しいコンプライアンス要件など、GRC チームが制御フレームワークを更新する必要がある場合があります。 フレームワークの変更が必要な場合、信頼チームは、変更の承認と実装を担当する主要な利害関係者を特定し、変更が実行可能であり、オンライン サービスに意図しない問題を引き起こさなくします。 GRC チームと関連する関係者が変更に必要な情報に同意すると、変更セットの目標完了日を実装するワークロードと、それぞれのサービス内での変更の実装に取り組みます。 実装ターゲットが満たされた後、信頼チームは新しいコントロールまたは更新されたコントロールでコントロール フレームワークを更新します。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 ガバナンスに関連するコントロールの検証については、次の表を参照してください。

### <a name="azure-and-dynamics-365"></a>Azure と Dynamics 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.18.1: 法的および契約上の要件の遵守 <br> A.18.2: 情報セキュリティ レビュー | 2020 年 12 月 2 日 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.18.1: 法的および契約上の要件の遵守 <br> A.18.2: 情報セキュリティ レビュー | 2020 年 12 月 2 日 |
| [SOC 1](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fservicetrust.microsoft.com%2FViewPage%2FMSComplianceGuideV3%3Fcommand%3DDownload%26downloadType%3DDocument%26downloadId%3D66043614-5628-4e26-83be-057eb3bb026c%26tab%3D7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb%26docTab%3D7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%252F_SSAE_16_Reports&data=04%7C01%7Csostah%40microsoft.com%7Cb9591cf4bd214d42c4f408d93cd83520%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637607721602686385%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=B2xjy%2Bx70e8vI%2FKC2BCa4AyJt0OSMzAGuhwllHF4NGM%3D&reserved=0) | IS-1: Microsoft セキュリティ ポリシー <br> IS-2: Microsoft セキュリティ ポリシーレビュー <br> IS-3: セキュリティの役割と責任 | 2021 年 3 月 31 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | C5-1: 標準的な操作手順 <br> IS-1: Microsoft セキュリティ ポリシー <br> IS-2: Microsoft セキュリティ ポリシーレビュー <br> IS-3: セキュリティの役割と責任 <br> SOC2-14: 秘密保持と秘密保持契約 <br> SOC2-18: 法定、規制、および契約上の要件 <br> SOC2-19: クロスファンクション コンプライアンス プログラム <br> SOC2-20: ISMS プログラム | 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | CA-2: セキュリティ評価 <br> PL-2: システム セキュリティ計画 | 2020 年 9 月 24 日 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.18.1: 法的および契約上の要件の遵守 <br> A.18.2: 情報セキュリティ レビュー | 2021 年 4 月 20 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-11: ポリシー フレームワークの更新 <br> CA-17: Microsoft セキュリティ ポリシー <br> CA-25: コントロール フレームワークの更新 | 2020 年 12 月 24 日 |

## <a name="resources"></a>リソース

- [Microsoft セキュリティ ポリシー](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=bc35aefb-ec41-4a0e-bfc7-10aa5169ca88&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Microsoft セキュリティ プログラム ポリシー](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=4b010ac5-2861-4d20-b8ff-db77875b43a9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)