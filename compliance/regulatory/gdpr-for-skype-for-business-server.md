---
title: Skype for Business Server の GDPR
description: オンプレミスの Skype for Business Server および Lync Server での GDPR の要件に対応する方法について説明します。
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.collection: MS-Compliance
hideEdit: true
ms.openlocfilehash: 945c9a90b117aca97b5b1af56e802e62bed91c9f700cddb595fc32bbe325559e
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54287966"
---
# <a name="gdpr-for-skype-for-business-server-and-lync-server"></a>Skype for Business Server および Lync Server の GDPR

Skype for Business Server および Lync Server のデータのほとんどは、Exchange Server に保存されます。それには、次のものが含まれます。

-   会話の履歴

-   ボイスメールの通知とトランスクリプション

-   会議の招待

[GDPR for Exchange Server](gdpr-for-exchange-server.md) について概要が示されている手順を使用して、GDPR 要求のこれらのデータ タイプを検索、エクスポート、削除します。

連絡先リストは、SQL Server のデータベースに保存されます。それらは、次の方法でエクスポートできます。

-   エンド ユーザー自身がグループ ヘッダーを右クリックして [コピー] を選択することにより、連絡先をエクスポートできます。この場合、そのグループのすべての連絡先がクリップボードにコピーされ、任意のアプリに貼り付けることができるようになります。

-   [Export-CsUserData](/powershell/module/skype/export-csuserdata) コマンドレットを使用することにより、このデータをエクスポートできます。

会議にアップロードされるコンテンツ (PowerPoint のファイルや配布資料など) または会議で生成されるコンテンツ (ホワイトボード、投票、Q/A など) は、ファイラーに保存されます。また、これらは、エンド ユーザーがまだ期限切れでない会議に再びログインして、アップロードされたコンテンツをダウンロードしたり、生成されたコンテンツの場合にはスクリーンショットを撮ってエクスポートすることもできます。

Exchange の予定表および連絡先リストにない MeetNow 会議および連絡先権限 (家族や同僚など) は、ユーザー データベース内にあります。Lync Server 2013 以降の場合は、[Export-CsUserData](/powershell/module/skype/export-csuserdata) コマンドレットを使用することにより、このデータをエクスポートできます。
