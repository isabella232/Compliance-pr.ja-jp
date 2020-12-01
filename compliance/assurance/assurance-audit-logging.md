---
title: 監査ログの概要
description: Microsoft 365 の監査ログについて
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
ms.openlocfilehash: 3714a5df73253d0814e1d4067248116cb6e10a40
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508624"
---
# <a name="audit-logging-overview"></a>監査ログの概要

## <a name="how-does-microsoft-365-employ-audit-logging"></a>Microsoft 365 で監査ログを採用する方法

Microsoft 365 では、監査ログを使用して、製品とサービスの権限のないアクティビティを検出し、Microsoft の担当者にアカウンタビリティを提供しています。 監査ログには、システム構成の変更とアクセスイベントに関する詳細が記録されます。ここでは、アクティビティの責任者、アクティビティが発生した時間と場所、およびアクティビティの結果を特定できます。 自動ログ分析は、不審な動作のほぼリアルタイム検出をサポートします。 潜在的なインシデントは、さらに調査を行うために Microsoft 365 セキュリティ対応チームにエスカレートされます。

Microsoft 365 内部監査ログは、次のようなさまざまなソースからのログデータをキャプチャします。

- イベントログ
- AppLocker ログ
- パフォーマンス データ
- System Center データ
- 通話詳細レコード
- Qoe (Quality of experience) データ
- IIS Web サーバーのログ
- SQL Server ログ
- Syslog データ
- セキュリティ監査ログ

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>Microsoft 365 は監査ログの集中管理とレポート作成を行いますか?

Microsoft 365 サーバーから、Cosmos と呼ばれる内部の大規模なデータコンピューティングサービスに、さまざまな種類のログデータがアップロードされています。 各サービスチームは、それぞれのサーバーからの監査ログを Cosmos データベースにアップロードして、集約と分析を行います。 このデータ転送は、Office データローダー (ODL) と呼ばれる独自の自動化ツールを使用して、承認されたポートおよびプロトコルで、FIPS 140-2 で検証された TLS 接続を介して行われます。

サービスチームは、ログの関連付け、警告、およびレポート用に、Cosmos のデータに対してスコープ指定されたクエリを実行します。 たとえば、Microsoft 365 セキュリティチームは、独自のイベントログパーサーを使用して Cosmos のデータを使用して、ログデータの関連付け、通知の送信、および Microsoft 365 運用環境での疑わしい可能性のあるアクティビティに対する実践的なレポートの生成を行います。 このデータからのレポートは、脆弱性を修正し、サービスの全体的なパフォーマンスを向上させるために使用されます。

## <a name="how-does-microsoft-365-protect-audit-logs"></a>Microsoft 365 で監査ログを保護する方法

Microsoft 365 で監査レコードを収集して処理するために使用されるツールでは、元の監査レコードのコンテンツや時間の順序を永続的に変更したり、取り消したりすることはできません。 Cosmos に格納されている Microsoft 365 データへのアクセスは、権限のある人物に制限されます。 Microsoft 365 では、監査機能の管理が、監査機能を担当するサービスチームメンバーの限定されたサブセットに制限されています。 これらのチームメンバーは、Cosmos のデータを変更または削除することはできません。また、Cosmos のログメカニズムに加えられたすべての変更は記録および監査されます。 監査ログは、インシデント調査をサポートし規制要件を満たすのに十分な期間保持されます。 Cosmos での監査ログデータの保持期間の正確な期間は、サービスチームによって決まります。ほとんどの監査ログデータは、90日間またはそれ以上保持されます。

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>Microsoft 365 は、監査ログに記録される可能性があるエンドユーザーの識別可能な情報を保護する方法を教えてください。

データを Cosmos にアップロードする前に、ODL アプリケーションはスクラブサービスを使用して、テナント情報やエンドユーザー識別情報などの顧客データを含むフィールドを難読化し、それらのフィールドをハッシュ値で置換します。 匿名化とハッシュ化されたログが書き直され、Cosmos にアップロードされます。

## <a name="related-external-regulations--certifications"></a>関連する外部規制 & 証明書

Microsoft のオンラインサービスは、社外の規制と証明書に準拠するために定期的に監査されます。 監査ログに関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: 監査イベント <br> AU-3: 監査レコードの内容 <br> AU-4: 監査ストレージ容量 <br> AU-5: 監査処理エラーに対する応答 <br> AU-6: 監査レビュー、分析、およびレポート <br> AU-7: 監査の削減とレポート生成 <br> AU-8: タイムスタンプ <br> AU-9: 監査情報の保護  <br> AU-10: 否認不可 <br> AU-11: 監査レコードの保持 <br> AU-12: 監査の生成  | 2020年9月24日 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.4: ログ記録と監視 | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.4: ログ記録と監視 | 2020 月 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-48: データセンターログ <br> CA-60: 監査ログ | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-48: データセンターログ <br> CA-60: 監査ログ | 2019 年 9 月 30 日 |