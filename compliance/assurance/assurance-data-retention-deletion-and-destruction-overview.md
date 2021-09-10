---
title: データの保持、削除、およびデータの破棄Microsoft 365
description: データの保持、削除、およびMicrosoft 365に関する Microsoft ポリシーの概要。
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: c851b235a70104720457d08c51529ee7b25c65e4
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947270"
---
# <a name="data-retention-deletion-and-destruction-in-microsoft-365"></a>データの保持、削除、およびデータの破棄Microsoft 365

Microsoft には、削除後に顧客データMicrosoft 365保持する期間を指定するデータ処理標準ポリシーがあります。 一般に、顧客データが削除されるシナリオは 2 つあります。

- **アクティブな削除**: テナントにアクティブなサブスクリプションが設定され、ユーザーまたは管理者がデータを削除するか、管理者がユーザーを削除します。
- **パッシブ削除**: テナント サブスクリプションが終了します。

## <a name="data-retention"></a>データ保持

これらの削除シナリオのそれぞれについて、次の表に、データ カテゴリと分類別の最大データ保持期間を示します。

| データ カテゴリ | データ分類 | 説明 | 例 | 保持期間 |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| 顧客データ | 顧客コンテンツ| 管理者とユーザーが直接提供/作成するコンテンツ <br><br> すべてのテキスト、サウンド、ビデオ、イメージ ファイル、および Microsoft データ センターで作成および保存されたソフトウェアが含まれています(Microsoft 365 | ユーザーがデータを作成できる最も一般的な Microsoft 365 アプリケーションの例には、Word、Excel、PowerPoint、Outlook、およびOneNote <br><br> 顧客コンテンツには、顧客が所有/提供するシークレット (パスワード、証明書、暗号化キー、ストレージ キー) も含まれます。 | **アクティブな削除シナリオ:** 最大 30 日間 <br><br> **パッシブ削除のシナリオ:** 最大 180 日間 |
| 顧客データ | エンド ユーザー識別可能な情報 (EUII) | Microsoft サービスのユーザーを識別または識別するために使用できるデータ。 EUII に顧客コンテンツが含まれている | ユーザー名または表示名 (DOMAIN\UserName) <br><br> ユーザー プリンシパル名 (name@domain) <br><br>  ユーザー固有の IP アドレス | **アクティブな削除シナリオ:** 最大 180 日 (テナント管理者のアクションのみ) <br><br> **パッシブ削除のシナリオ:** 最大 180 日間 |
| 個人データ <br> (顧客データに含まれていないデータ) | エンド ユーザー仮名識別子 (EUPI) | Microsoft によって作成された識別子は、Microsoft サービスのユーザーに関連付けされます。 マッピング テーブルなどの他の情報と組み合わせると、EUPI はエンド ユーザーを識別します。 <br><br> EUPI には、顧客がアップロードまたは作成した情報が含まれている | ユーザー GUID、PUID、または GUID <br><br> セッション ID | **アクティブな削除シナリオ:** 最大 30 日間 <br><br> **パッシブ削除のシナリオ:** 最大 180 日間 |

## <a name="subscription-retention"></a>サブスクリプションの保持

アクティブなサブスクリプションの用語では、サブスクライバーは、サブスクリプションに格納されている顧客データにアクセス、抽出、または削除Microsoft 365。 有料サブスクリプションが終了または終了した場合、Microsoft は Microsoft 365 に保存されている顧客データを 90 日間限定機能アカウントに保持し、購読者がデータを抽出できます。 90 日間の保持期間が終了すると、Microsoft はアカウントを無効にし、顧客データを削除します。 Microsoft 365 のサブスクリプションの期限切れまたは終了後 180 日以内に、Microsoft はアカウントを無効にし、すべての顧客データをアカウントから削除します。 データの最大保存期間が経過すると、そのデータは商業的に回復できなくなります。

無料試用版の場合、アカウントはほとんどの国と地域で 30 日間猶予状態に移動します。 この猶予期間中に、Microsoft 365 を購入できます。 Microsoft 365 を購入しない場合は、試用版をキャンセルするか、猶予期間が終了するまでそのままにしておくことができます。そのようにすると、試用版のアカウント情報とデータは削除されます。

## <a name="expedited-deletion"></a>迅速な削除

サブスクリプションについては、サブスクライバーは Microsoft サポートに連絡して、サブスクリプションのデプロビジョニングの迅速化を要求できます。 このプロセスでは、管理者が Microsoft から提供されたロックアウト コードを入力してから 3 日後にすべてのユーザー データが削除されます。 これには、SharePoint Online と Exchange Online のデータが保持されているか、非アクティブなメールボックスに格納されています。

迅速なプロビジョニング解除の詳細については、「サブスクリプションをキャンセル [する」を参照してください](/microsoft-365/commerce/subscriptions/cancel-your-subscription)。

## <a name="related-links"></a>関連リンク

- [データを有するデバイスの破棄](assurance-data-bearing-device-destruction.md)
- [Office 365 での不変性](assurance-data-immutability.md)
- [Exchange Online でのデータ削除](assurance-exchange-online-data-deletion.md)
- [SharePoint Online でのデータ削除](assurance-sharepoint-online-data-deletion.md)
