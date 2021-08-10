---
title: Microsoft 365 Yammerアクセス制御
description: この記事では、実稼働環境でのアクセス制御Yammer Enterprise概要について説明します。
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
ms.openlocfilehash: d9a3604bd987170ea266871cf4c384c0e071817dc10640eb01e560debb5d9664
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54291645"
---
# <a name="yammer-enterprise-access-controls"></a>Yammerアクセス制御 

実稼働環境への物理的Yammer論理的なアクセスは、少人数のユーザー (インフラストラクチャと運用) に制限されます。 他のエンジニアMicrosoft 365同様に、Yammerエンジニアは顧客データに常にアクセスできます。 承認者の数が限られている Lockbox に似た承認ベースの Just-in-time アクセス制御システムを使用してアクセスを要求する必要があります。 承認者は要求を確認し (たとえば、要求が必要性、ビジネス ケース、時間などに基づいて正当かどうかを確認します)、要求を承認または拒否します。 要求が承認された場合、JIT アクセスは、定義された期間限定で付与されます。 アクセス時間を超えると、アクセスは自動的に期限切れになります。

他の Microsoft 365サービスと同様に、すべてのアクセスは、Yammer多要素認証を使用します。 すべてのアクセス履歴とコマンド履歴はユーザーに属性付けされ、セキュリティ チームによって定期的にログYammerされます。

管理と管理の詳細Yammer、管理者のヘルプYammer[参照してください](/yammer/yammer-landing-page)。