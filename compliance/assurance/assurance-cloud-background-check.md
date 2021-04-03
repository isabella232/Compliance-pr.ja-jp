---
title: Microsoft Cloud の背景チェック
description: この記事では、Microsoft 365 の Microsoft 人事審査の実施方法の概要について説明します。
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
ms.openlocfilehash: 2347d524bf1561b60eb40020636196332e2accd7
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497660"
---
# <a name="microsoft-cloud-background-check"></a>Microsoft Cloud の背景チェック

Microsoft Cloud バックグラウンド チェックは、米国で Microsoft 365 関連サービスを提供する従業員として採用される候補者に必要です。 顧客データにアクセスできる米国の Microsoft 従業員は、すべての Microsoft 365 サービスで必要な Microsoft Cloud バックグラウンド チェック プロセスに従う必要があります。 米国外では、プロセスは異なります。 たとえば、Microsoft Cloud for Germany は、Microsoft ではなく、データ トラスティ (ドイツの会社) が顧客データへのアクセスを制御するように設計されたデータ トラスティ承認モデルを使用します。 ドイツの Microsoft Cloud はドイツのデータセンターから配信され、データ トラスティの技術スタッフを含むオペレーション センター (OC) もドイツにあります。 データセンターと OC 施設の両方が、データ トラスティによって運用、保守、および制御されます。

現地の法律で許容される範囲で、Microsoft Cloud バックグラウンド チェックの一部として次のチェックが実行されます。

- 米国: 社会保障番号トレース
- 犯罪歴は、州、郡、および地方レベルでの重罪と軽犯罪、および米国で適切な場合は連邦レベルで最大 7 年をチェックします。 国際犯罪歴チェック (現地の法律に依存) は、米国以外の地域に適用されます。
- 外国資産管理 (OFAC) リストの Office、産業およびセキュリティ局 (BIS) リスト、および防衛貿易管理の debarred Persons (DDTC) リスト チェックの Office を含むグローバルな制裁と執行チェック。

Microsoft Cloud バックグラウンド チェックの結果は、従業員データベースに格納され、データセンターアクセス制御システムに接続されます。 Microsoft Cloud バックグラウンド チェックの有効期限が切れ、従業員が更新しない場合、Microsoft 365 サービスへのアクセスは取り消され、Microsoft Cloud バックグラウンド チェックが完了するまで使用できません。 Microsoft との雇用関係が終了すると、すべてのデータセンター アクセスが直ちに取り消されます。

米国の市民権は、Microsoft 365 米国政府機関サービスに物理的または論理的にアクセスできるすべての従業員について検証されます。 市民権を確認するために、従業員および/または新入社員候補者は、米国市民権を確認するドキュメントを確認する訓練を受けた米国市民権代理人と会います。 従業員または新入社員候補者は、必要なドキュメントを持参し、その地域の市民権代理人との会議で構成証明フォームに署名する必要があります。 会議は、実際に行う必要があります。 個人がシチズンシップ代理人と会い、必要なドキュメントと署名を提供すると、シチズンシップ代理人はドキュメントのコピーを Microsoft Staffing Operations に転送し、そのコピーを送信して記録保持します。

Microsoft 365 米国政府機関クラウドへの論理的なアクセス権を持つ担当者、または Azure U.S.政府機関への論理的または物理的なアクセス権を持つ担当者は、人事審査を含む FBI[](https://www.fbi.gov/services/cjis)の刑事司法情報サービス (CJIS) の連邦政府の要件を遵守する必要があります。 Microsoft 365 米国政府機関サービスをサポートする CJIS スクリーニングには、Microsoft Online Services CJIS サポート プログラムに登録されている州の CJIS システム機関指定の裁判官によって[](https://blogs.office.com/2013/10/23/california-and-microsoft-sign-cjis-security-policy-agreement/)審査された指紋ベースの犯罪背景チェックが含まれます。

## <a name="periodic-rescreening"></a>定期的な再スクリーン処理

特定の管理、セキュリティ、その他の役割 (顧客データへのアクセスを必要とする役割の従業員を含む) には、定期的な再スクリーン処理や追加のバックグラウンド チェックが必要になる場合があります (「クラウドバックグラウンドチェック」を参照)。