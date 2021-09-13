---
title: Microsoft 365 SharePointデータの削除
description: 削除されたコンテンツの保存場所やSharePointなど、オンラインでのデータ削除のしくみについて説明します。
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
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160772"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a>SharePointオンライン データの削除 (Microsoft 365

SharePointOnline は、アプリケーション データベース内に抽象化されたコードとしてオブジェクトを格納します。 ユーザーがファイルを SharePoint Online にアップロードすると、そのファイルは逆アセンブルされ、アプリケーション コードに変換され、複数のデータベースの複数のテーブルに格納されます。 SharePoint Online では、顧客がアップロードするコンテンツはすべてチャンクに分割され、暗号化され (複数の AES 256 ビット キーを使用する可能性があります)、データセンター全体に分散されます。 チャンク処理と暗号化プロセスの詳細については [、「Microsoft Cloud での暗号化」を参照してください](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)。 

[SharePointオンライン] では、アイテムを元の場所から削除した後、アイテムは 93 日間保持されます。 ユーザーがサイトのごみ箱から削除したり、ごみ箱を空にしたりしない限り、サイトのごみ箱に残されます。 その場合、アイテムはサイト コレクションのごみ箱に移動し、残りの 93 日間は保存されます。 削除済みアイテムの復元の詳細については[、「SharePoint](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
)サイトのごみ箱のアイテムを復元する」および「サイト コレクションのごみ箱から削除済みアイテムを復元する」を[参照してください](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b)。 ごみ箱の保持時間は、オンラインで構成SharePointできません。

サイト コレクションを削除すると、コレクション内のサイトの階層と、その中のすべてのコンテンツも削除されます。

- ドキュメントおよびドキュメント ライブラリ
- リストとリスト データ
- サイト構成の設定
- サイトまたはサブサイトに関連する役割とセキュリティ情報
- トップ レベルの Web サイトのサブサイト、そのコンテンツ、およびユーザー情報

サイト コレクションを誤って削除した場合は、管理者が管理センターを使用して、SharePointまたはSharePointできます。

削除されたサイト コレクションは 93 日間保持されます。 93 日を過ぎると、リスト、ライブラリ、ページ、サブサイトなど、サイトおよびサイトのすべてのコンテンツと設定が完全に削除されます。

ハード削除は、ユーザーがサイト コレクションのごみ箱から削除済みアイテムを削除した場合、保持期間とバックアップ期間が経過した場合、または管理者が [Remove-SPODeletedSite](/powershell/module/sharepoint-online/remove-spodeletedsite)コマンドレットを使用してサイト コレクションを完全に削除した場合に発生します。 ユーザーが SharePoint Online からコンテンツをハード削除 (完全に削除、または削除) すると、削除されたチャンクのすべての暗号化キーも削除されます。 以前に削除されたチャンクを格納したディスク上のブロックは、未使用としてマークされ、再使用できます。
