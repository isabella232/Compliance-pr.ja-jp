---
title: Microsoft 365データの破損に対処する
description: この記事では、データの破損と、Microsoft 365を防止および回復するために Microsoft が行った取り組みについて説明します。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
ms.openlocfilehash: 860a150760e080df4a577d73478a75ac94b8700b
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160295"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a>データ破損のMicrosoft 365

大規模なクラウド サービスを実行する難しい側面の 1 つは、大量のデータと独立したシステムを考えると、データの破損を処理する方法です。 データの破損は、次の原因で発生する可能性があります。

- アプリケーションまたはインフラストラクチャのバグ、アプリケーションの状態の一部またはすべてが壊れている
- データの紛失やデータの読み取りが行えなくなっているハードウェアの問題
- 人的操作上のエラー
- 悪意のあるハッカーと不満を持つ従業員
- データが失われる外部サービスのインシデント

データの整合性に対する復元性が高いということは、データ破損インシデントの数が少ないので、破損を防ぐための Microsoft 365 保護メカニズムと、破損が発生した場合にデータを回復できるシステムとプロセスが組み込まれております。 データの破損に対する復元性を高めるエンジニアリング リリース プロセスのさまざまな段階にチェックとプロセスが存在します。

- システム設計
- コードの編成と構造
- コード レビュー
- 単体テスト、統合テスト、およびシステム テスト
- トリップ ワイヤーのテスト/ゲート

このMicrosoft 365環境では、データセンター間のピア レプリケーションによって、データのライブ コピーが常に複数存在します。 標準のイメージとスクリプトを使用して、失われたサーバーを回復し、レプリケートされたデータを使用して顧客データを復元します。 組み込みのデータ復元チェックとプロセスにより、Microsoft は SharePoint Online の組み込みレプリケーションと内部コード リポジトリ ツール Source Depot を使用して、Microsoft 365 情報システムのドキュメント (セキュリティ関連のドキュメントを含む) のバックアップのみを保持します。 システムドキュメントはオンラインSharePoint、Source Depot にはシステムイメージとアプリケーション イメージが含まれています。 オンラインSharePoint Source Depot の両方でバージョン管理が使用され、ほぼリアルタイムでレプリケートされます。
