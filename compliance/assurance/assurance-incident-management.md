---
title: ドキュメント管理の概要
description: Microsoft 365 でのインシデント管理の詳細
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
ms.openlocfilehash: 45636bbefc0bdd85ab2d8f21091060d49dbaa4c6
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497153"
---
# <a name="incident-management-overview"></a>ドキュメント管理の概要

## <a name="what-is-a-security-incident"></a>セキュリティ インシデントとは

Microsoft では、過失または違法な破壊、紛失、改ざん、不正開示、Microsoft によって処理される顧客データまたは個人情報へのアクセスにつながるセキュリティ違反を、オンライン サービスにおいて確認されたセキュリティ インシデントと定義します。 たとえば、Microsoft 365 インフラストラクチャへの無許可アクセスと顧客データの侵入はセキュリティ インシデントを構成しますが、サービスや顧客データの機密性、整合性、可用性に影響しないコンプライアンス イベントはセキュリティ インシデントとは見なされません。

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Microsoft はセキュリティ インシデントにどう対応しますか?

セキュリティ インシデントが発生した場合は常に、Microsoft のサービスと顧客データを保護するために、迅速かつ効果的に対応します。 Microsoft では、セキュリティ上の脅威を迅速かつ効率的に調査、格納、削除するように設計されたインシデント対応戦略を採用しています。

Microsoft クラウド サービスは、継続的に侵害の兆候を監視します。 セキュリティ監視と警告の自動化に加えて、すべての従業員は、潜在的なセキュリティ インシデントの兆候を認識して報告する年次トレーニングを受け取っています。 従業員、顧客、またはセキュリティ監視ツールによって検出された疑わしいアクティビティは、調査のためにサービス固有のセキュリティ対応チームにエスカレートされます。 サービス固有のセキュリティ応答チームを含むすべてのサービス運用チームは、インシデント対応 24x7x365 でリソースを利用できるよう、深いオンコールローテーションを維持します。 Microsoft のオンコールローテーションを使用すると、広範囲にわたるイベントや同時イベントを含む、いつでもまたは規模で効果的なインシデント対応を実装できます。

疑わしいアクティビティが検出およびエスカレートされると、サービス固有のセキュリティ応答チームは、分析、格納、根絶、および回復のプロセス **を開始します**。 これらのチームは、潜在的なインシデントの分析を調整して、顧客や顧客データへの影響を含め、その範囲を決定します。 この分析に基づいて、サービス固有のセキュリティ対応チームは、影響を受けたサービス チームと一緒に、脅威を含め、インシデントの影響を最小限に抑え、環境からの脅威を根絶し、既知の安全な状態に完全に回復する計画を策定します。 関連するサービス チームは、サービス固有のセキュリティ対応チームからのサポートを受けて計画を実装し、脅威が正常に排除され、影響を受けるサービスが完全に回復します。

インシデントが解決された後、サービス チームは、今後同様のインシデントを防止、検出、および対応するために、インシデントから学んだすべての教訓を実装します。 セキュリティ インシデント (特に、顧客に影響を与えるインシデント、またはデータ侵害の結果として発生するインシデント) を選択すると、完全なインシデントが事後分析後に発生します。 事後検討は、技術的過失、手続き上の失敗、手動エラー、およびインシデントの原因となった可能性がある、またはインシデント対応プロセス中に特定されたその他のプロセスの欠陥を特定するように設計されています。 事後に特定された改善は、サービス固有のセキュリティ対応チームとの連携によって実装され、将来のインシデントを防止し、検出および応答機能を向上させるのに役立ちます。

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>セキュリティインシデントまたはプライバシー インシデントについて、お客様に通知される方法と時間

Microsoft が顧客データの不正な損失、開示、または変更に関するセキュリティ違反に気付いた場合、Microsoft は、オンライン サービス条項 (OST) のデータ保護追加条項 (DPA) に示されている 72 時間以内に影響を受けるお客様に通知します。 正式なセキュリティ インシデント宣言が発生すると、通知のタイムライン コミットメントが始まります。 セキュリティ インシデントが宣言されると、通知プロセスは、過度な遅延を発生させずに、可能な限り迅速に実行されます。

通知には、侵害の性質、ユーザーへの影響のおおよその説明、および軽減手順 (該当する場合) が含まれます。 Microsoft の調査が最初の通知時に完了していない場合、通知には、次の手順と後続の通信のタイムラインも示されます。

データ侵害を含むがこれらに限定されない Microsoft に影響を与える可能性があるインシデントに気付いた場合、お客様は、DPA で定義されているインシデントを Microsoft に速やかに通知する責任があります。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 インシデント管理に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | IR-4: インシデント処理 <br> IR-6: インシデント報告 <br> IR-8: インシデント対応計画 | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: 情報セキュリティ インシデントと改善の管理 | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: 情報セキュリティ インシデントと改善の管理 | 2020 月 2 月 22 日 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: PII に関するデータ侵害の通知  | 2020 月 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26: セキュリティ インシデント レポート <br> CA-47: インシデント対応 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12: サービス レベル契約 (SLA) <br> CA-13: インシデント対応ガイド <br> CA-15: サービス正常性通知  <br>  <br> CA-26: セキュリティ インシデント レポート <br> CA-29: オンコール エンジニア <br> CA-47: インシデント対応 | 2020 年 12 月 24 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: インシデントの報告  | 2020 年 12 月 24 日  |

## <a name="resources"></a>リソース

- [オンライン サービスの使用条件 (OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [データ保護の追加 (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Microsoft Cloud Incident Management Implementation Guidance for Azure and Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365 - サードパーティの脆弱性評価 :Office 365 ~ 2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
