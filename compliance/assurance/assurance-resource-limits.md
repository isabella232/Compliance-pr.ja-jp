---
title: Microsoft 365 リソース制限
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
hideEdit: true
ms.openlocfilehash: 54ea001e542cdd1ab078546cf96bd011e27ab1dc
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497501"
---
# <a name="service-resource-limits"></a>サービス リソースの制限

リソース制限は、クォータ (制限) と調整を使用して適用されます。 Azure Active Directory (Azure AD) と個々の Microsoft 365 サービスは両方を使用します。 制限はサービス固有であり、新しい機能が追加されるに応じ、時間の流中で変化します。 さまざまなサービスの現在の制限の詳細については、次のトピックを参照してください。

- [Azure ADサービスの制限と制限](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Exchange Online の制限](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [SharePoint Online ソフトウェアの境界と制限](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype for Business Limits](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [Yammer REST API とレート制限](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Sway のファイル サイズの制限](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

これらの制限に加えて、Azure ADおよび Microsoft 365 全体でいくつかの調整メカニズムが使用されます。 Microsoft のデータセンターのネットワーク リソースがサービスを使用する幅広い顧客に最適化されている場合、サービス内での調整は特に重要です。 調整メカニズムには、次のものが含まれます。

- Azure ADおよび Microsoft 365 機能のユーザー レベル調整は、1 人のユーザーが実行できるトランザクションまたは同時呼び出し (スクリプトまたはコードによる) の数を制限します。
- 既定の PowerShell 調整ポリシーは、テナントの作成時に各テナントに割り当てられます。 これらの設定は、1 人の管理者が同時に開くことができる PowerShell セッションの最大数など、他の項目に影響します。
- 各 Exchange Online のお客様には、EWS クライアント操作と、すべての Outlook クライアントに適用される調整用に調整される既定の Exchange Web サービス (EWS) ポリシーがあります。
