---
title: ドキュメント管理の概要
description: Microsoft 365 のインシデント管理について
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
ms.openlocfilehash: 24ecad99115705f293f765edb84345dad8ff8c93
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787316"
---
# <a name="incident-management-overview"></a>ドキュメント管理の概要

## <a name="what-is-a-security-incident"></a>セキュリティ インシデントとは

Microsoft では、過失または違法な破壊、紛失、改ざん、不正開示、Microsoft によって処理される顧客データまたは個人情報へのアクセスにつながるセキュリティ違反を、オンライン サービスにおいて確認されたセキュリティ インシデントと定義します。 たとえば、Microsoft 365 インフラストラクチャへの不正アクセスや顧客データの取り出しはセキュリティ インシデントを構成しますが、サービスや顧客データの機密性、整合性、可用性に影響しないコンプライアンス イベントはセキュリティ インシデントとは見なされません。

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Microsoft はセキュリティ インシデントに対してどのように対応しますか?

セキュリティ インシデントが発生した場合は常に、Microsoft のサービスと顧客データを迅速かつ効果的に保護するために対応します。 Microsoft では、セキュリティの脅威を迅速かつ効率的に調査、阻止、削除するためのインシデント対応戦略を採用しています。

Microsoft クラウド サービスは、侵害の兆候を継続的に監視します。 セキュリティの監視と警告の自動化に加えて、すべての従業員は、潜在的なセキュリティ インシデントの兆候を認識して報告する年間トレーニングを受け取っています。 従業員、顧客、またはセキュリティ監視ツールによって検出された不審なアクティビティは、調査のためにサービス固有のセキュリティ対応チームにエスカレートされます。 サービス固有のセキュリティ対応チームを含むすべてのサービス運用チームは、インシデント対応 24x7x365 でリソースを利用できるよう、深いオンコールローテーションを維持します。 Microsoft のオンコールローテーションにより、Microsoft は広範囲にわたるイベントや同時イベントを含め、いつでもまたは規模に応じて効果的なインシデント対応をマウントできます。

不審なアクティビティが検出およびエスカレートされると、サービス固有のセキュリティ対応チームは、分析、格納、参加、回復のプロセス **を開始します**。 これらのチームは、潜在的なインシデントの分析を調整して、顧客や顧客データへの影響を含め、その範囲を決定します。 この分析に基づいて、サービス固有のセキュリティ対応チームは、影響を受けたサービス チームと作業して、脅威を含め、インシデントの影響を最小限に抑え、環境からの脅威を改善し、既知の安全な状態に完全に回復する計画を策定します。 関連するサービス チームは、脅威が正常に排除され、影響を受けるサービスが完全な回復を受けることを保証するために、サービス固有のセキュリティ対応チームのサポートを受けて計画を実装します。

インシデントが解決された後、サービス チームは、今後の同様のインシデントの防止、検出、対応を向上するために、インシデントから学んだすべてのレッスンを実装します。 セキュリティ インシデント(特に、お客様に影響を与えるインシデントやデータ侵害の可能性があるインシデント) を選択すると、事後に完全なインシデントが発生します。 事後検討は、技術的過失、手続き上の失敗、手動エラー、およびインシデントの原因となった可能性がある、またはインシデント対応プロセス中に特定されたその他のプロセスの欠陥を特定するように設計されています。 事後分析中に特定された改善点は、サービス固有のセキュリティ対応チームによる調整によって実装され、今後のインシデントを防止し、検出および対応機能を向上させるのに役立ちます。

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>セキュリティインシデントやプライバシー インシデントについて、お客様に通知する方法と時間

Microsoft は、お客様データの不正な損失、開示、または変更に関連するセキュリティ違反を認識した場合は、72 時間以内に、オンライン サービス使用条件 (OST) のデータ保護に関する追加条項 (DPA) に示されている通り、影響を受けたお客様に通知します。 正式なセキュリティ インシデント宣言が発生すると、通知のタイムライン コミットメントが始まります。 セキュリティ インシデントが宣言されると、通知プロセスは、過度な遅延を発生させずに、可能な限り迅速に実行されます。

通知には、違反の性質の説明、ユーザーへの影響の概算、軽減手順 (該当する場合) が含まれます。 最初の通知の時点で Microsoft の調査が完了しなかった場合、通知には、その後の通信の次の手順とタイムラインも示されます。

お客様がデータ侵害を含むがこれらに限定されないなど、Microsoft に影響を与える可能性があるインシデントを認識した場合、お客様は DPA で定義されているインシデントを Microsoft に速やかに通知する責任があります。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 インシデント管理に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | IR-4: インシデント処理 <br> IR-6: インシデントレポート <br> IR-8: インシデント対応計画 | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: 情報セキュリティ インシデントと改善の管理 | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: 情報セキュリティ インシデントと改善の管理 | 2020 月 2 月 22 日 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: PII に関連するデータ侵害の通知  | 2020 月 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26: セキュリティ インシデントレポート <br> CA-47: インシデント対応 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12: サービス レベル契約 (SLA) <br> CA-13: インシデント対応ガイド <br> CA-15: サービス正常性通知  <br>  <br> CA-26: セキュリティ インシデントレポート <br> CA-29: オンコール エンジニア <br> CA-47: インシデント対応 | 2020 年 12 月 24 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: インシデントの報告  | 2020 年 12 月 24 日  |

## <a name="resources"></a>リソース

- [オンライン サービスの使用条件 (OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [データ保護に関する追加処理 (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Azure および Office 365 向け Microsoft Cloud Incident Management 実装ガイダンス](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365 - Office 365 - 2019 のサードパーティの脆弱性評価](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
