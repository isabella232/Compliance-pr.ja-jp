---
title: インシデント管理の概要
description: Microsoft 365 でのインシデント管理について
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
ms.openlocfilehash: 6b5c77a2a81f8231ad620fbc40205457c6ba1a49
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507849"
---
# <a name="incident-management-overview"></a>インシデント管理の概要

## <a name="what-is-a-security-incident"></a>セキュリティ インシデントとは

Microsoft では、過失または違法な破壊、紛失、改ざん、不正開示、Microsoft によって処理される顧客データまたは個人情報へのアクセスにつながるセキュリティ違反を、オンライン サービスにおいて確認されたセキュリティ インシデントと定義します。 たとえば、Microsoft 365 インフラストラクチャおよびお客様データの exfiltration フィルターに対する権限のないアクセスはセキュリティインシデントを発生させますが、機密性、整合性、またはサービスや顧客データの可用性に影響を与えないコンプライアンスイベントはセキュリティインシデントとは見なされません。

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Microsoft はセキュリティインシデントにどのように対応しますか?

セキュリティインシデントが発生した場合、microsoft は迅速かつ効果的に Microsoft サービスと顧客データを保護することに努めます。 Microsoft は、セキュリティ上の脅威を迅速かつ効率的に調査、含める、および削除するために設計されたインシデント対応戦略を採用しています。

Microsoft クラウドサービスは、侵害の兆候を継続的に監視しています。 自動化されたセキュリティの監視と通知に加えて、すべての従業員は、潜在的なセキュリティインシデントの兆候を認識して報告するために毎年のトレーニングを受けます。 従業員、顧客、またはセキュリティ監視ツールによって検出された疑わしいアクティビティは、調査のためにサービス固有のセキュリティ対応チームにエスカレートされます。 サービス固有のセキュリティ対応チームを含む、すべてのサービス運用チームが、インシデント対応の24時間365日にリソースを利用できるようにするための、詳細な通話のローテーションを維持します。 Microsoft では、このようなオンコールローテーションにより、効果的なインシデント対応をいつでも、または同時実行イベントも含めて、いつでも、いつでもマウントできます。

疑わしい動作が検出されてエスカレートされると、サービス固有のセキュリティ対策チームは、 **分析、コンテインメント、eradication、および recovery** のプロセスを開始します。 これらのチームは、潜在的なインシデントの分析を調整して、顧客や顧客データへの影響など、その範囲を決定します。 この分析に基づいて、サービス固有のセキュリティ対応チームは、影響を受けるサービスチームと連携して、脅威を含んでいることを最小限に抑え、環境からの脅威を eradicate、既知の安全な状態に完全に復旧する計画を策定します。 関連するサービスチームは、サービス固有のセキュリティ対応チームからサポートを受けてプランを実装し、脅威が正常に削除され、サービスが完全な復旧を実行することを保証します。

インシデントが解決した後、サービスチームは、インシデントから学んだ教訓を実装して、将来の類似インシデントの防止、検出、および対応を強化します。 セキュリティインシデントを選択します (特にお客様に影響を与える、またはデータ違反が発生した場合は、インシデントの事後に関する問題が発生します)。 事後検討は、技術的過失、手続き上の失敗、手動エラー、およびインシデントの原因となった可能性がある、またはインシデント対応プロセス中に特定されたその他のプロセスの欠陥を特定するように設計されています。 事後処理中に特定された改善は、サービス固有のセキュリティ対応チームからの調整によって実装され、今後のインシデントを防ぎ、検出と応答の機能が向上します。

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>お客様がセキュリティまたはプライバシーインシデントを通知する方法とタイミング

Microsoft は、お客様のデータの不正な損失、開示、または変更に関するセキュリティ違反を認識した場合、Microsoft は、オンラインサービス利用規約 (OST) のデータ保護補遺 (DPA) に記載されているように、影響を受けるお客様に72時間以内に通知します。 正式なセキュリティ インシデント宣言が発生すると、通知のタイムライン コミットメントが始まります。 セキュリティ インシデントが宣言されると、通知プロセスは、過度な遅延を発生させずに、可能な限り迅速に実行されます。

通知には、違反の性質、ユーザーへのおおよその影響、および軽減手順 (該当する場合) の説明が含まれます。 最初の通知時に Microsoft の調査が完了していない場合は、次の手順と、以降の通信のためのタイムラインも通知されます。

お客様が Microsoft に影響を与える可能性があるインシデントを認識していて、データの漏洩に限定されているわけではない場合、お客様は DPA で定義されているようにインシデントを迅速に通知する責任を負います。

## <a name="related-external-regulations--certifications"></a>関連する外部規制 & 証明書

Microsoft のオンラインサービスは、社外の規制と証明書に準拠するために定期的に監査されます。 インシデント管理に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | IR-4: インシデント処理 <br> IR-6: インシデントレポート <br> IR-8: インシデント対応計画 | 2020年9月24日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 16.1: 情報セキュリティインシデントと改善の管理 | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 16.1: 情報セキュリティインシデントと改善の管理 | 2020 月 2 月 22 日 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | -PII: PII を含むデータ違反の通知  | 2020 月 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-26: セキュリティインシデントの報告 <br> CA-47: インシデント対応 | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-12: サービスレベル契約 (Sla) <br> CA-13: インシデント対応ガイド <br> CA-15: サービス正常性の通知  <br>  <br> CA-26: セキュリティインシデントの報告 <br> CA-29: オンプレ呼び出しエンジニア <br> CA-47: インシデント対応 | 2019 年 9 月 30 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-08: Reporting インシデント  | 2019 年 9 月 30 日  |

## <a name="resources"></a>リソース

- [オンライン サービスの使用条件 (OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [データ保護補遺 (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Azure および Office 365 の Microsoft クラウドインシデント管理実装ガイダンス](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365-サードパーティの脆弱性評価 Office 365-2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
