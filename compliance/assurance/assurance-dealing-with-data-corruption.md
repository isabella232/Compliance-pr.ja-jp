---
title: Microsoft 365 データの破損に対処する
description: この記事では、Microsoft 365 のデータ破損と、データの防止と回復に対する Microsoft の取り組みについて説明します。
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
ms.openlocfilehash: 9e9f0951f7e349cc70bc96bb6a2d62275848cf04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497589"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a>Microsoft 365 でのデータ破損の処理

大規模なクラウド サービスを実行する難しい側面の 1 つは、大量のデータと独立したシステムを考えると、データの破損を処理する方法です。 データの破損は、次の原因で発生する可能性があります。

- アプリケーションまたはインフラストラクチャのバグ、アプリケーションの状態の一部またはすべてが壊れている
- データの紛失やデータの読み取りが行えなくなっているハードウェアの問題
- 人的操作上のエラー
- 悪意のあるハッカーと不満を持つ従業員
- データが失われる外部サービスのインシデント

データの整合性に対する復元性が高いということは、データ破損インシデントが少なくなっていることを意味します。Microsoft は、破損の発生を防ぐための Microsoft 365 保護メカニズムと、破損が発生した場合にデータを回復できるシステムとプロセスを組み込み込み、 データの破損に対する復元性を高めるエンジニアリング リリース プロセスのさまざまな段階にチェックとプロセスが存在します。

- システム設計
- コードの編成と構造
- コード レビュー
- 単体テスト、統合テスト、およびシステム テスト
- トリップ ワイヤーのテスト/ゲート

Microsoft 365 の実稼働環境では、データセンター間のピア レプリケーションによって、データのライブ コピーが常に複数存在します。 標準のイメージとスクリプトを使用して、失われたサーバーを回復し、レプリケートされたデータを使用して顧客データを復元します。 組み込みのデータ復元チェックとプロセスにより、Microsoft は、SharePoint Online の組み込みレプリケーションと内部コード リポジトリ ツール Source Depot を使用して、Microsoft 365 情報システムのドキュメント (セキュリティ関連のドキュメントを含む) のバックアップのみを保持します。 システムドキュメントは SharePoint Online に保存され、Source Depot にはシステムイメージとアプリケーション イメージが含まれています。 SharePoint Online と Source Depot の両方がバージョン管理を使用し、ほぼリアルタイムでレプリケートされます。
