---
title: Microsoft 365 Yammerエンタープライズ アクセス制御
description: この記事では、実稼働環境でのエンタープライズ アクセス制御Yammerについて簡単に説明します。
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
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 916f26d5f2defdfb21cb9babe3a64cf618e8cd4a
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120366"
---
# <a name="yammer-enterprise-access-controls"></a>Yammerアクセス制御 

実稼働環境への物理的および論理的Yammerアクセスは、一部のユーザー (インフラストラクチャと運用) に制限されます。 他の Microsoft 365 エンジニアと同様に、Yammerエンジニアは顧客データに常にアクセスできます。 制限された数の承認者を持つロックボックスと同様に、承認ベースの Just-In-Time アクセス制御システムを使用してアクセスを要求する必要があります。 承認者は要求を確認し (たとえば、要求が必要性、業務事例、時間などに基づいて正当かどうかを確認する)、要求を承認または拒否します。 要求が承認されると、定義された限られた時間に対して JIT アクセスが許可されます。 アクセス時間を超えると、アクセスは自動的に期限切れになります。

他の Microsoft 365 サービスと同様に、Yammer環境へのすべてのアクセスは多要素認証を使用します。 すべてのアクセスとコマンドの履歴はユーザーに関連付けされ、セキュリティ チームによって定期的にログYammer確認されます。

管理と管理の詳細Yammer、管理者向けヘルプ [Yammer参照してください](/yammer/yammer-landing-page)。