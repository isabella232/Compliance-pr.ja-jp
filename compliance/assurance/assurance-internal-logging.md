---
title: Microsoft 365 エンジニアリングの Microsoft 365 内部ログ
description: この記事では、Microsoft 365 エンジニアリング チームの内部ログがどのように機能するのかについて説明します。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 110a61c27a00380eede4d4f2303acfb025a27a1f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497069"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Microsoft 365 のエンジニアリングのための内部ログ記録

お客様が利用できるイベントとログ データに加えて、Microsoft 365 のエンジニアが Microsoft 365 エンジニアが利用できる内部ログ データ収集システムもあります。 さまざまな種類のログ データが Microsoft 365 サーバーから Cosmos と呼ばれる内部のビッグ データ コンピューティング サービスにアップロードされます。 各サービス チームは、それぞれのサーバーから Cosmos データベースに監査ログをアップロードして、集約と分析を行います。 このデータ転送は、Office データ ローダー (ODL) と呼ばれる独自のオートメーション ツールを使用して、特に承認されたポートおよびプロトコル上の FIPS 140-2 検証済みの TLS 接続を使用して行われます。 Microsoft 365 で監査レコードの収集と処理に使用されるツールでは、元の監査レコードのコンテンツや時間の順序に対する永続的または不可逆的な変更は許可されません。

サービス チームは、Cosmos を集中リポジトリとして使用して、アプリケーションの使用状況の分析、システムと運用パフォーマンスの測定、問題やセキュリティの問題を示す可能性のある異常やパターンを探します。 各サービス チームは、分析する内容に応じて、次のようなログのベースラインを Cosmos にアップロードします。

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

データを Cosmos にアップロードする前に、ODL アプリケーションはスクラブ サービスを使用して、テナント情報やエンドユーザー識別可能な情報など、顧客データを含むフィールドを難読化し、それらのフィールドをハッシュ値に置き換える。 匿名化ログとハッシュ ログが書き換え、次に Cosmos にアップロードされます。 サービス チームは、Cosmos のデータに対してスコープ付きクエリを実行して、相関関係、アラート、レポート作成を行います。 Cosmos の監査ログ データ保持期間は、サービス チームによって決まります。ほとんどの監査ログ データは、セキュリティ インシデント調査をサポートし、規制保持要件を満たすために 90 日以上保持されます。

Cosmos に格納されている Microsoft 365 データへのアクセスは、承認された担当者に制限されます。 Microsoft は、監査機能の管理を、監査機能を担当するサービス チーム メンバーの限定されたサブセットに制限します。 これらのチーム メンバーは、Cosmos からデータを変更または削除する機能を持たなく、Cosmos のログメカニズムに対する変更はすべて記録および監査されます。

各サービス チームは、特定のアプリケーションに特定の分析を実行する権限を与え、分析のためにログ データにアクセスします。 たとえば、Microsoft 365 セキュリティ チームは、独自のイベント ログ パーサーを介して Cosmos のデータを使用して、Microsoft 365 の実稼働環境で疑わしいアクティビティに関するアクション可能なレポートを関連付け、警告し、生成します。 このデータからのレポートは、脆弱性を修正し、サービスの全体的なパフォーマンスを向上させるために使用されます。 特定のアラートまたはレポートで詳細な調査が必要な場合、サービス担当者はデータを Microsoft 365 サービスにインポートしなおす必要があります。 Cosmos からインポートされる特定のログは暗号化され、サービス担当者は復号化キーにアクセスできないので、ターゲット ログは、スコープ設定された結果を承認されたサービス担当者に返す暗号化解除サービスをプログラムで渡されます。 この演習で見つかった脆弱性は、Microsoft の標準的なセキュリティ インシデント管理チャネルを使用して報告およびエスカレートされます。
