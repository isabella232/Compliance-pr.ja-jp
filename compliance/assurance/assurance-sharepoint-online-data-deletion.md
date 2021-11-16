---
title: Microsoft 365 SharePoint Online データの削除
description: 削除されたコンテンツが保存される場所や期間など、SharePoint Online でデータ削除がどのように機能するかを学習します。
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
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 3545a6e5746553e59603fbf68432ee4705a21f3f
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160772"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a>Microsoft 365 での SharePoint Online データの削除

SharePoint Online は、オブジェクトを抽象化されたコードとしてアプリケーション データベース内に格納します。 ユーザーがファイルを SharePoint Online にアップロードすると、そのファイルは分解されてアプリケーションコ ードに変換され、複数のデータベースにまたがる複数のテーブルに保存されます。 SharePoint Online では、顧客がアップロードするすべてのコンテンツがチャンクに分割され、暗号化され (複数の AES 256 ビット キーを使用する可能性があります)、データ センター全体に配布されます。 チャンク化と暗号化プロセスの詳細については、「[Microsoft Cloud での暗号化](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)」を参照してください。 

SharePoint Online では、アイテムは元の場所から削除したときから 93 日間保持されます。 その期間ずっと、誰かがそこから削除するか、そのごみ箱を空にしない限り、サイトのごみ箱にとどまります。 サイトのごみ箱から削除されたか、サイトのごみ箱が空にされた場合、アイテムはサイト コレクションのごみ箱に移動し、93 日間のうちの残りの日数だけサイト コレクションのごみ箱にとどまります。 削除されたアイテムの復元については、「[SharePoint サイトのごみ箱のアイテムを復元する](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
)」および「[サイト コレクションのごみ箱から削除したアイテムを復元する](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b)」を参照してください。 ごみ箱の保持時間は、SharePoint Online では構成できません。

サイト コレクションを削除すると、コレクション内のサイトの階層と、その中のすべてのコンテンツも削除されます。

- ドキュメントおよびドキュメント ライブラリ
- リストとリスト データ
- サイトの構成設定
- サイトまたはそのサブサイトに関するロールやセキュリティの情報
- トップレベル Web サイトのサブサイト、それらのコンテンツ、およびユーザー情報

サイト コレクションを誤って削除した場合は、SharePoint 管理センターを使用してグローバル管理者または SharePoint 管理者が復元できます。

削除されたサイト コレクションは 93 日間保持されます。 93 日を過ぎると、リスト、ライブラリ、ページ、サブサイトなど、サイトおよびサイトのすべてのコンテンツと設定が完全に削除されます。

ハード削除は、ユーザーがサイト コレクションのごみ箱から削除されたアイテムを削除したとき、保持期間とバックアップ期間が終了したとき、または管理者が [Remove-SPODeletedSite コマンドレット](/powershell/module/sharepoint-online/remove-spodeletedsite) を使用してサイト コレクションを完全に削除したときに発生します。 ユーザーが SharePoint Online からコンテンツを完全に削除 (完全に削除またはパージ) すると、削除されたチャンクのすべての暗号化キーも削除されます。 削除されたチャンクを以前に保存したディスク上のブロックは、未使用としてマークされ、再利用できます。
