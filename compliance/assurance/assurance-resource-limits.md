---
title: Microsoft 365リソースの制限
description: この記事では、アプリケーション内のさまざまなアプリケーションのリソース制限に関する情報をMicrosoft 365。
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
ms.openlocfilehash: 2f64b1201077e25d28d99f49b573912078e4e428ccb51011e17934b1440f75ac
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290545"
---
# <a name="service-resource-limits"></a>サービス リソースの制限

リソース制限は、クォータ (制限) と調整を使用して適用されます。 Azure Active Directory (Azure AD) と個々のサービスMicrosoft 365両方を使用します。 制限はサービス固有であり、新しい機能が追加されるに応じ、時間の流中で変化します。 さまざまなサービスの現在の制限の詳細については、次のトピックを参照してください。

- [Azure ADサービスの制限と制限](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Exchange Online の制限](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [SharePointオンライン ソフトウェアの境界と制限](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype for Business制限](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [YammerREST API とレート制限](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Sway のファイル サイズの制限](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

これらの制限に加えて、Azure サーバーとサーバー全体でいくつかの調整AD使用Microsoft 365。 Microsoft のデータセンターのネットワーク リソースがサービスを使用する幅広い顧客に最適化されている場合、サービス内での調整は特に重要です。 調整メカニズムには、次のものが含まれます。

- Azure ADおよび Microsoft 365機能のユーザー レベル調整は、1 人のユーザーが実行できるトランザクション数または同時呼び出し数 (スクリプトまたはコード別) を制限します。
- 既定の PowerShell 調整ポリシーは、テナントの作成時に各テナントに割り当てられます。 これらの設定は、1 人の管理者が同時に開くことができる PowerShell セッションの最大数など、他の項目に影響します。
- 各Exchange Onlineには、EWS クライアント操作に合Exchange Web サービス (EWS) の既定のポリシーと、すべてのクライアントに適用される調整Outlookがあります。
