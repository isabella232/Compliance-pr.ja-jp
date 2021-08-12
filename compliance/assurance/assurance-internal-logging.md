---
title: Microsoft 365エンジニアリングの内部ログMicrosoft 365する
description: この記事では、エンジニアリング チームの内部ログMicrosoft 365説明します。
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
ms.openlocfilehash: 1811b118ffdbfce72ba7b387c499d7ce68be2911417611c3ae4fa39624511daf
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290975"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Microsoft 365 のエンジニアリングのための内部ログ記録

Microsoft は、お客様が利用できるイベントとログ データに加えて、ユーザーが使用できる内部ログ データ収集システムMicrosoft 365しています。 Microsoft 365 サーバーから、ほぼリアルタイム (NRT) 分析用の独自のセキュリティ監視ソリューション、および長期ストレージ用の内部のビッグ データ コンピューティング サービス (Cosmos) に、さまざまな種類のログ データがアップロードされます。 このデータ転送は、Office データ ローダー (ODL) と呼ばれる独自のオートメーション ツールを使用して、承認済みポートおよびプロトコル上の FIPS 140-2 検証済み TLS 接続を使用して行われます。 監査レコードを収集Microsoft 365処理するために使用されるツールでは、元の監査レコードのコンテンツや時間の順序に対する永続的または不可逆的な変更は許可されません。

サービス チームは、Cosmos を集中リポジトリとして使用して、アプリケーションの使用状況の分析、システムと運用パフォーマンスの測定、および問題やセキュリティの問題を示す可能性のある異常やパターンを探します。 各サービス チームは、以下を含むベースラインをアップロードします。

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

アップロードする前に、ODL アプリケーションはスクラブ サービスを使用して、テナント情報やエンドユーザー識別可能な情報など、顧客データを含むフィールドを削除し、それらのフィールドをハッシュ値に置き換える。 スクラブされたログは、Cosmosおよび潜在的なセキュリティ イベントとパフォーマンス インジケーターのログを分析する NRT セキュリティ監視ソリューションにアップロードされます。 監査ログ のデータ保持期間は、Cosmosチームによって決まります。ほとんどの監査ログ データは、セキュリティ インシデント調査をサポートし、規制保持要件を満たすために 90 日以上保持されます。

ユーザーにMicrosoft 365データへのアクセスは、Cosmos担当者に制限されます。 Microsoft は、監査ログの管理を、監査機能を担当するセキュリティ チーム メンバーの限定されたサブセットに制限します。 セキュリティ チームは、管理者に対する永続的なアクセス権を持Cosmos、すべての変更が記録および監査されます。

NRT 分析の後、各サービス チームは、データの相関関係、対話型クエリ、およびデータ分析に分析ツールとダッシュボードを使用できます。 これらのレポートは、サービスの全体的なパフォーマンスを監視および改善するために使用されます。
