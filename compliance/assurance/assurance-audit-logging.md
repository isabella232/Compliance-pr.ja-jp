---
title: 監査ログの概要
description: 監査ログの詳細については、Microsoft 365
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
ms.openlocfilehash: 11695a941e5d5e6740833ab19bf2d68ac487c1c5
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947230"
---
# <a name="audit-logging-overview"></a>監査ログの概要

## <a name="how-do-microsoft-online-services-employ-audit-logging"></a>Microsoft オンライン サービスで監査ログを使用する方法

Microsoft オンライン サービスでは、監査ログを使用して、承認されていないアクティビティを検出し、Microsoft 担当者に説明責任を提供します。 監査ログは、システム構成の変更とアクセス イベントに関する詳細をキャプチャし、アクティビティの責任者、アクティビティがいつどこで行ったか、アクティビティの結果を特定するための詳細を示します。 ログの自動分析は、疑わしい動作のほぼリアルタイム検出をサポートします。 潜在的なインシデントは、詳細な調査のために適切な Microsoft セキュリティ対応チームにエスカレートされます。

Microsoft Online Services の内部監査ログは、次のようなさまざまなソースからのログ データをキャプチャします。

- イベント ログ
- AppLocker ログ
- パフォーマンス データ
- System Centerデータ
- 通話詳細レコード
- エクスペリエンス データの品質
- IIS Web Server ログ
- SQL Serverログ
- Syslog データ
- セキュリティ監査ログ

## <a name="how-do-microsoft-online-services-centralize-and-report-on-audit-logs"></a>Microsoft オンライン サービスは、監査ログを一元管理してレポートする方法を説明します。

さまざまな種類のログ データが Microsoft サーバーから、ほぼリアルタイム (NRT) 分析用の独自のセキュリティ監視ソリューション、および長期ストレージ用の内部ビッグ データ コンピューティング サービス (Cosmos) または Azure Data Explorer (Kusto) にアップロードされます。 このデータ転送は、自動ログ管理ツールを使用した承認済みポートおよびプロトコル上の FIPS 140-2 検証済み TLS 接続を使用して行われます。

ログは、ルールベース、統計、および機械学習の方法を使用して NRT で処理され、システム パフォーマンス インジケーターと潜在的なセキュリティ イベントを検出します。 機械学習モデルは、検出機能を継続的に向上させるために、Cosmosまたは Kusto に格納されている受信ログ データと履歴ログ データを使用します。 セキュリティ関連の検出では、アラートが生成され、インシデントが発生する可能性がある場合はオンコール エンジニアに通知し、該当する場合は自動修復アクションをトリガーします。 サービス チームは、自動化されたセキュリティ監視に加えて、分析ツールとダッシュボードを使用して、データの相関関係、対話型クエリ、およびデータ分析を行います。 これらのレポートは、サービスの全体的なパフォーマンスを監視および改善するために使用されます。

セキュリティ監視とアラートの詳細については、「セキュリティ監視の概要 [」を参照してください](assurance-security-monitoring.md)。

![データ フローの監査。](../media/assurance-audit-data-flow.png)

## <a name="how-do-microsoft-online-services-protect-audit-logs"></a>Microsoft オンライン サービスで監査ログを保護する方法

Microsoft オンライン サービスで監査レコードを収集および処理するために使用されるツールでは、元の監査レコードのコンテンツや時間の順序に対する永続的または不可逆的な変更は許可されません。 ユーザーまたは Kusto に保存されている Microsoft Cosmosサービス データへのアクセスは、承認された担当者に制限されます。 さらに、Microsoft は監査ログの管理を、監査機能を担当するセキュリティ チーム メンバーの限定されたサブセットに制限します。 セキュリティ チームの担当者は、管理者または Kusto Cosmosアクセス権を持つ必要があります。 管理アクセスには Just-In-Time (JIT) アクセスの承認が必要であり、ユーザーのログメカニズムに対する変更Cosmos記録および監査されます。 監査ログは、インシデント調査をサポートし、規制要件を満たすのに十分な時間保持されます。 サービス チームによって決定される監査ログ データ保持の正確な期間。ほとんどの監査ログ データは、90 日間、Cosmos 180 日間保持されます。

## <a name="how-do-microsoft-online-services-protect-user-personal-data-that-may-be-captured-in-audit-logs"></a>Microsoft Online Services は、監査ログに取り込む可能性が高いユーザーの個人データを保護する方法を説明します。

ログ データをアップロードする前に、自動ログ管理アプリケーションはスクラブ サービスを使用して、テナント情報やユーザー個人データなどの顧客データを含むフィールドを削除し、それらのフィールドをハッシュ値に置き換える。 匿名化およびハッシュ化されたログは、書き換え後、そのログにアップロードCosmos。 すべてのログ転送は、TLS 暗号化接続 (FIPS 140-2) を使用して行われます。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 監査ログに関連するコントロールの検証については、次の表を参照してください。

### <a name="azure-and-dynamics-365"></a>Azure と Dynamics 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: ログと監視 | 2020 年 12 月 2 日 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: ログと監視 | 2020 年 12 月 2 日 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: ログと監視 | 2020 年 12 月 2 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | VM-1: セキュリティ イベントログとコレクション | 2021 年 3 月 31 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | C5-6: ログへのアクセス制限 <br> VM-1: セキュリティ イベントログとコレクション | 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AU-2: 監査イベント <br> AU-3: 監査レコードの内容 <br> AU-4: ストレージ容量の監査 <br> AU-5: 監査処理の失敗に対する応答 <br> AU-6: 監査レビュー、分析、およびレポート <br> AU-7: 監査の削減とレポート生成 <br> AU-8: タイム スタンプ <br> AU-9: 監査情報の保護  <br> AU-10: 否認不可 <br> AU-11: 監査レコードの保持 <br> AU-12: 監査の生成  | 2020 年 9 月 24 日 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: ログと監視 | 2021 年 4 月 20 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: データセンターログ <br> CA-60: 監査ログ | 2020 年 12 月 24 日 |