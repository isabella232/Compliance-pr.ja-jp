---
title: Project Server での GDPR 対応
description: オンプレミスの Project Server で一般データ保護規則 (GDPR) の要件に対応する方法について説明します。
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
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
hideEdit: true
ms.openlocfilehash: ddbf22523caf1869d0253599216fff07ee14f751
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51495951"
---
# <a name="gdpr-for-project-server"></a>Project Server での GDPR 対応

Project Server では、Project Web App でユーザー データをエクスポートしたり編集したりするために、カスタム スクリプトが使用されます。基本的な処理は、次のとおりです。

1.  ファーム内で Project Web App のサイトを検索します。

2.  各サイトの中で、ユーザーが含まれているプロジェクトを検索します。

3.  確認対象となるタイプのデータをエクスポートし、確認します。

4.  必要に応じてデータを編集します。

これらの手順について、以下の記事で詳細に説明します。

- [Project Server からユーザー データをエクスポートする](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [Project Server からユーザー データを削除する](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


Project Server は SharePoint Server 上に構築されており、SharePoint ULS のログおよび利用状況データベースにイベントのログが出力されることに注意してください。詳細は「[SharePoint Server での GDPR への対応](gdpr-for-sharepoint-server.md)」をご覧ください。
