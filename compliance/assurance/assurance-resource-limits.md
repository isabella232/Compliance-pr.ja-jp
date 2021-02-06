---
title: Microsoft 365 リソースの制限
description: この記事では、Microsoft 365 内のさまざまなアプリケーションのリソース制限に関する情報を確認できます。
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
ms.openlocfilehash: 632a0b78c5c5ba02a59f8863c2e751f009cc968e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120756"
---
# <a name="service-resource-limits"></a>サービス リソースの制限

リソースの制限は、クォータ (制限) と調整を使用して適用されます。 Azure Active Directory (Azure AD) と個々の Microsoft 365 サービスは両方を使用します。 制限はサービス固有であり、新しい機能が追加されるに応じ、時間の流中で変化します。 さまざまなサービスの現在の制限の詳細については、以下のトピックを参照してください。

- [Azure AD サービスの制限](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Exchange Online の制限](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [SharePoint Online ソフトウェアの境界と制限](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype for Business の制限](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [Yammer REST API とレート制限](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Sway でのファイル サイズの制限](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

これらの制限に加えて、Azure AD および Microsoft 365 全体でいくつかの調整メカニズムが使用されます。 サービス内の調整は特に重要です。Microsoft のデータセンター内のネットワーク リソースは、サービスを使用する広範な顧客に最適化されています。 調整メカニズムには、次のものが含まれます。

- Azure AD Microsoft 365 では、ユーザー レベルの調整が機能します。この調整によって、1 人のユーザーが実行できるトランザクションまたは (スクリプトまたはコードによる) 同時呼び出しの数が制限されます。
- 既定の PowerShell 調整ポリシーは、テナント作成時に各テナントに割り当てられます。 これらの設定は、1 人の管理者が同時に開くことができる PowerShell セッションの最大数など、他の項目に影響します。
- 各 Exchange Online のお客様には、EWS クライアント操作用に調整された既定の Exchange Web サービス (EWS) ポリシーと、すべての Outlook クライアントに適用される調整があります。
