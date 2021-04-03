---
title: 監査ログの概要
description: Microsoft 365 での監査ログの詳細
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
ms.openlocfilehash: dc56d0413811d59309c974931e1fa50ee184e94a
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497679"
---
# <a name="audit-logging-overview"></a>監査ログの概要

## <a name="how-does-microsoft-365-employ-audit-logging"></a>Microsoft 365 では監査ログを使用する方法を説明します。

Microsoft 365 では、監査ログを使用して、製品およびサービスの未承認のアクティビティを検出し、Microsoft 担当者に説明責任を提供します。 監査ログは、システム構成の変更とアクセス イベントに関する詳細をキャプチャし、アクティビティの責任者、アクティビティがいつどこで行ったか、アクティビティの結果を特定するための詳細を示します。 ログの自動分析は、疑わしい動作のほぼリアルタイム検出をサポートします。 潜在的なインシデントは、詳細な調査のために Microsoft 365 セキュリティ対応チームにエスカレートされます。

Microsoft 365 の内部監査ログは、次のようなさまざまなソースからログ データをキャプチャします。

- イベント ログ
- AppLocker ログ
- パフォーマンス データ
- System Center データ
- 通話詳細レコード
- エクスペリエンス データの品質
- IIS Web Server ログ
- SQL Serverログ
- Syslog データ
- セキュリティ監査ログ

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>Microsoft 365 では、監査ログを一元化してレポートする方法について説明します。

さまざまな種類のログ データが Microsoft 365 サーバーから Cosmos と呼ばれる内部のビッグ データ コンピューティング サービスにアップロードされます。 各サービス チームは、それぞれのサーバーから Cosmos データベースに監査ログをアップロードして、集約と分析を行います。 このデータ転送は、Office Data Loader (ODL) と呼ばれる独自のオートメーション ツールを使用して、承認済みポートおよびプロトコル上の FIPS 140-2 検証済み TLS 接続を使用して行われます。

サービス チームは、ログの相関関係、アラート、レポート作成のために、Cosmos のデータに対してスコープ付きクエリを実行します。 たとえば、Microsoft 365 セキュリティ チームは、Cosmos のデータと独自のイベント ログ パーサーを使用して、ログ データの関連付け、アラートの送信、Microsoft 365 の実稼働環境での疑わしいアクティビティに関するアクション可能なレポートの生成を行います。 このデータからのレポートは、脆弱性を修正し、サービスの全体的なパフォーマンスを向上させるために使用されます。

## <a name="how-does-microsoft-365-protect-audit-logs"></a>Microsoft 365 は監査ログを保護する方法を説明します。

Microsoft 365 で監査レコードの収集と処理に使用されるツールでは、元の監査レコードのコンテンツや時間の順序に対する永続的または不可逆的な変更は許可されません。 Cosmos に格納されている Microsoft 365 データへのアクセスは、承認された担当者に制限されます。 Microsoft 365 は、監査機能の管理を、監査機能を担当するサービス チーム メンバーの限定されたサブセットに制限します。 これらのチーム メンバーは、Cosmos からデータを変更または削除する機能を持たなく、Cosmos のログメカニズムに対する変更はすべて記録および監査されます。 監査ログは、インシデント調査をサポートし、規制要件を満たすのに十分な時間保持されます。 Cosmos の監査ログ データ保持の正確な期間は、サービス チームによって決まります。ほとんどの監査ログ データは 90 日以上保持されます。

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>Microsoft 365 は、監査ログに記録される可能性があるエンド ユーザー識別可能な情報を保護する方法を説明します。

データを Cosmos にアップロードする前に、ODL アプリケーションはスクラブ サービスを使用して、テナント情報やエンドユーザー識別可能な情報など、顧客データを含むフィールドを難読化し、それらのフィールドをハッシュ値に置き換える。 匿名化ログとハッシュ ログが書き換え、次に Cosmos にアップロードされます。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 監査ログに関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: 監査イベント <br> AU-3: 監査レコードの内容 <br> AU-4: ストレージ容量の監査 <br> AU-5: 監査処理の失敗に対する応答 <br> AU-6: 監査レビュー、分析、およびレポート <br> AU-7: 監査の削減とレポート生成 <br> AU-8: タイム スタンプ <br> AU-9: 監査情報の保護  <br> AU-10: 否認不可 <br> AU-11: 監査レコードの保持 <br> AU-12: 監査の生成  | 2020 年 9 月 24 日 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: ログと監視 | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: ログと監視 | 2020 月 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: データセンターログ <br> CA-60: 監査ログ | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: データセンターログ <br> CA-60: 監査ログ | 2020 年 12 月 24 日|