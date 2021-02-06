---
title: Microsoft 365 でのデータの保持、削除、および破棄
description: データの保持、削除、破棄に関する Microsoft 365 の Microsoft ポリシーの概要。
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
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 025e2c422c05dbffdf5a510f93809beaed3fe09d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120656"
---
# <a name="data-retention-deletion-and-destruction-in-microsoft-365"></a>Microsoft 365 でのデータの保持、削除、および破棄

Microsoft は、削除後に顧客データを保持する期間を指定する Microsoft 365 のデータ処理標準ポリシーを用意しています。 一般に、顧客データが削除されるシナリオは 2 つあります。

- **アクティブな** 削除 : テナントにアクティブなサブスクリプションが設定され、ユーザーまたは管理者がデータを削除するか、管理者がユーザーを削除します。
- **パッシブ削除**: テナント サブスクリプションが終了します。

## <a name="data-retention"></a>データの保持

これらの各削除シナリオについて、次の表に、データカテゴリと分類別の最大データ保持期間を示します。

| データ カテゴリ | データ分類 | 説明 | 例 | 保持期間 |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| 顧客データ | 顧客コンテンツ| 管理者とユーザーが直接提供/作成したコンテンツ <br><br> Microsoft 365 のサービスを使用する際に Microsoft データ センターで作成および保存されたテキスト、サウンド、ビデオ、画像ファイル、およびソフトウェアすべてが含まれます。 | ユーザーがデータを作成できる最も一般的に使用される Microsoft 365 アプリケーションの例には、Word、Excel、PowerPoint、Outlook、OneNote があります。 <br><br> 顧客コンテンツには、顧客が所有/提供するシークレット (パスワード、証明書、暗号化キー、ストレージ キー) も含まれます。 | **アクティブな削除シナリオ:** 最大 30 日 <br><br> **パッシブ削除シナリオ:** 最大 180 日 |
| 顧客データ | エンド ユーザーを特定できる情報 (EUII) | Microsoft サービスのユーザーを識別するために使用できるデータ。 EUII に顧客コンテンツが含まれている | ユーザー名または表示名 (DOMAIN\UserName) <br><br> ユーザー プリンシパル名 (name@domain) <br><br>  ユーザー固有の IP アドレス | **アクティブ削除シナリオ:** 最大 180 日 (テナント管理者の操作のみ) <br><br> **パッシブ削除シナリオ:** 最大 180 日 |
| 個人データ <br> (顧客データに含まれていないデータ) | エンド ユーザーの仮名識別子 (EUPI) | Microsoft によって作成され、Microsoft サービスのユーザーに関連付けらた識別子。 マッピング テーブルなどの他の情報と組み合わせると、EUPI はエンド ユーザーを識別します。 <br><br> EUPI には、お客様によってアップロードまたは作成された情報が含まれているのではありません。 | ユーザー GUID、PUID、または SID <br><br> セッション ID | **アクティブな削除シナリオ:** 最大 30 日 <br><br> **パッシブ削除シナリオ:** 最大 180 日 |

## <a name="subscription-retention"></a>サブスクリプションの保持

アクティブなサブスクリプションの用語では、サブスクライバーは Microsoft 365 に保存されている顧客データにアクセス、抽出、または削除できます。 有料サブスクリプションが終了または終了した場合、Microsoft は Microsoft 365 に保存されている顧客データを機能制限付きアカウントに 90 日間保持し、サブスクライバーがデータを抽出できます。 90 日間の保持期間が終了すると、Microsoft はアカウントを無効にし、顧客データを削除します。 Microsoft 365 のサブスクリプションの期限切れまたは終了後 180 日以内に、Microsoft はアカウントを無効にし、すべての顧客データをアカウントから削除します。 データの最大保存期間が経過すると、そのデータは商業的に回復できなくなります。

無料試用版の場合、アカウントはほとんどの国と地域で 30 日間の猶予状態に移動します。 この猶予期間中に、Microsoft 365 を購入できます。 Microsoft 365 を購入しない場合は、試用版をキャンセルするか、猶予期間が終了するまでそのままにしておくことができます。そのようにすると、試用版のアカウント情報とデータは削除されます。

## <a name="expedited-deletion"></a>迅速な削除

サブスクリプションについては、サブスクライバーは Microsoft サポートに連絡して、サブスクリプションのデプロビジョニングの迅速化を要求できます。 このプロセスでは、管理者が Microsoft から提供されたロックアウト コードを入力してから 3 日後にすべてのユーザー データが削除されます。 これには、SharePoint Online と Exchange Online のデータが保持されているか、非アクティブなメールボックスに格納されています。

プロビジョニングの迅速化の詳細については、「サブスクリプションをキャンセルする」を [参照してください](/microsoft-365/commerce/subscriptions/cancel-your-subscription)。

## <a name="related-links"></a>関連リンク

- [データの破棄](assurance-data-destruction.md)
- [Office 365 での不変性](assurance-data-immutability.md)
- [Exchange Online でのデータ削除](assurance-exchange-online-data-deletion.md)
- [SharePoint Online でのデータ削除](assurance-sharepoint-online-data-deletion.md)
