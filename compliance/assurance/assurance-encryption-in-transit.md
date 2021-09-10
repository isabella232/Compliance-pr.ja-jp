---
title: 転送中のデータの暗号化
description: この記事では、Microsoft が転送中の顧客データを暗号化Microsoft 365説明します。
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: ebeface33b0d5ba419773c13305c277d681e8400
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947310"
---
# <a name="encryption-for-data-in-transit"></a>転送中のデータの暗号化

保存中の顧客データの保護に加え、Microsoft では暗号化技術を使用してお客様の送信中の顧客データを保護します。 データは転送中です。

- クライアント コンピューターが Microsoft サーバーと通信する場合。
- Microsoft サーバーが別の Microsoft サーバーと通信する場合。そして
- Microsoft サーバーが Microsoft 以外のサーバーと通信する場合 (たとえば、Exchange Onlineメールをサード パーティの電子メール サーバーに配信する場合など)。

Microsoft サーバー間のデータセンター間通信は TLS または IPsec を使用して行い、すべての顧客向けサーバーはクライアント コンピューターと TLS を使用してセキュリティで保護されたセッションをネゴシエートします (たとえば、Exchange Online では TLS 1.2 を使用し、256 ビットの暗号強度が使用されます (FIPS 140-2 レベル 2 検証)。 (暗号化[でサポートされる](/microsoft-365/compliance/technical-reference-details-about-encryption)TLS 暗号スイートの一覧については、「暗号化に関するテクニカル リファレンスの詳細」を参照Office 365)。これは、Outlook、Skype for Business、Microsoft Teams、Outlook on the web などのクライアントで使用されるプロトコル (HTTP、POP3 など) に適用されます。

パブリック証明書は、送信された情報の機密性を保護するための内部 Microsoft ツールである SSLAdmin を使用して Microsoft IT SSL によって発行されます。 Microsoft IT によって発行される証明書の長さは 2048 ビット以上であり、Webtrust コンプライアンスでは、証明書が Microsoft が所有するパブリック IP アドレスにのみ発行されるのを確認するために SSLAdmin が必要です。 この条件を満たしない IP アドレスは、例外プロセスを通じてルーティングされます。

使用されている TLS のバージョン、前方秘密 (FS) が有効かどうか、暗号スイートの順序など、すべての実装の詳細が一般に公開されています。 これらの詳細を確認する方法の 1 つは [、Qualys SSL Labs などのサードパーティの Web サイトを使用する方法です](https://www.ssllabs.com)。 以下に、次のサービスの情報を表示する Qualys の自動テスト ページへのリンクを示します。

- [Office 365ポータル](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype for Business (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype for Business (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

たとえばExchange Online Protection URL はテナント名によって異なります。ただし、すべてのお客様は、アプリを使用Microsoft 365テスト **microsoft-com.mail.protection.outlook.com。**
