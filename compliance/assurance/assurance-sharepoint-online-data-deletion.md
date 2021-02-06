---
title: Microsoft 365 SharePoint Online のデータ削除
description: 削除されたコンテンツの保存場所や保存期間など、SharePoint Online でのデータ削除のしくみについて説明します。
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
- SPO_Content
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 89281b32dbc577f935224396fd358ed753348ea1
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120746"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a>Microsoft 365 での SharePoint Online データの削除

SharePoint Online は、アプリケーション データベース内に抽象コードとしてオブジェクトを格納します。 ユーザーがファイルを SharePoint Online にアップロードすると、そのファイルは逆アセンブルされ、アプリケーション コードに変換され、複数のデータベースの複数のテーブルに格納されます。 SharePoint Online では、顧客がアップロードするコンテンツはすべてチャンクに分割され、暗号化され (複数の AES 256 ビット キーを使用する可能性があります)、データセンター全体に分散されます。 チャンク化と暗号化プロセスの詳細については [、「Microsoft Cloud](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)での暗号化」を参照してください。 

SharePoint Online では、元の場所からアイテムを削除した後、アイテムは 93 日間保持されます。 ユーザーがサイトのごみ箱から削除したり、ごみ箱を空にしたりしない限り、サイトのごみ箱に残されます。 その場合、アイテムはサイト コレクションのごみ箱に移動し、残りの 93 日間は保存されます。 削除済みアイテムの復元については [、「SharePoint](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) サイトのごみ箱のアイテムを復元する」および「サイト コレクションのごみ箱から削除済みアイテムを復元する」を [参照してください](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b)。 ごみ箱の保持時間は SharePoint Online では構成できません。

サイト コレクションを削除すると、コレクション内のサイトの階層と、その中のすべてのコンテンツも削除されます。

- ドキュメントおよびドキュメント ライブラリ
- リストとリスト データ
- サイトの構成設定
- サイトまたはサブサイトに関連するロールおよびセキュリティ情報
- トップ レベル Web サイトのサブサイト、コンテンツ、ユーザー情報

誤ってサイト コレクションを削除した場合は、SharePoint 管理センターを使用してグローバル管理者または SharePoint 管理者がサイト コレクションを復元できます。

削除されたサイト コレクションは 93 日間保持されます。 93 日を過ぎると、リスト、ライブラリ、ページ、サブサイトなど、サイトおよびサイトのすべてのコンテンツと設定が完全に削除されます。

完全削除は、ユーザーがサイト コレクションのごみ箱から削除済みアイテムを削除した場合、保持期間とバックアップ期間が経過した場合、または管理者が [Remove-SPODeletedSite](/powershell/module/sharepoint-online/remove-spodeletedsite)コマンドレットを使用してサイト コレクションを完全に削除した場合に発生します。 ユーザーが SharePoint Online からコンテンツを完全に削除 (または完全に削除) すると、削除されたチャンクのすべての暗号化キーも削除されます。 以前に削除されたチャンクを格納したディスク上のブロックは、未使用としてマークされ、再使用できます。
