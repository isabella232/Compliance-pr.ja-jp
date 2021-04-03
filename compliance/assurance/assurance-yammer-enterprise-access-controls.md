---
title: Microsoft 365 Yammerアクセス制御
description: この記事では、実稼働環境でのエンタープライズ Yammerの概要について説明します。
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
hideEdit: true
ms.openlocfilehash: df345d922bbd0c9106cf0714377803a9c0870d82
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497351"
---
# <a name="yammer-enterprise-access-controls"></a>Yammerアクセス制御 

実稼働環境への物理的および論理的Yammerアクセスは、少人数のユーザー (インフラストラクチャと運用) に制限されます。 他の Microsoft 365 エンジニアと同様に、Yammerエンジニアは顧客データに常にアクセスできます。 承認者の数が限られている Lockbox に似た承認ベースの Just-in-time アクセス制御システムを使用してアクセスを要求する必要があります。 承認者は要求を確認し (たとえば、要求が必要性、ビジネス ケース、時間などに基づいて正当かどうかを確認します)、要求を承認または拒否します。 要求が承認された場合、JIT アクセスは、定義された期間限定で付与されます。 アクセス時間を超えると、アクセスは自動的に期限切れになります。

他の Microsoft 365 サービスと同様に、すべてのアクセスは、Yammer多要素認証を使用します。 すべてのアクセス履歴とコマンド履歴はユーザーに属性付けされ、セキュリティ チームによって定期的にログYammerされます。

管理と管理の詳細Yammer、管理者のヘルプYammer [参照してください](/yammer/yammer-landing-page)。