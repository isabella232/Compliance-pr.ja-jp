---
title: 転送中のデータの暗号化
description: この記事では、Microsoft が転送中の Microsoft 365 顧客データを暗号化する方法について簡単に説明します。
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
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
ms.openlocfilehash: 227f74140ecd9b6283b92e8b0e87bd70912ec8e3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497249"
---
# <a name="encryption-for-data-in-transit"></a>転送中のデータの暗号化

保存中の顧客データの保護に加え、Microsoft では暗号化技術を使用してお客様の送信中の顧客データを保護します。 データは転送中です。

- クライアント コンピューターが Microsoft サーバーと通信する場合。
- Microsoft サーバーが別の Microsoft サーバーと通信する場合。そして
- Microsoft サーバーが Microsoft 以外のサーバー (たとえば、サード パーティの電子メール サーバーに電子メールを配信する Exchange Online など) と通信する場合。

Microsoft サーバー間のデータセンター間通信は TLS または IPsec を使用して行い、すべての顧客向けサーバーがクライアント コンピューターと TLS を使用してセキュリティで保護されたセッションをネゴシエートします (たとえば、Exchange Online では TLS 1.2 を使用し、256 ビットの暗号強度が使用されます (FIPS 140-2 レベル 2 検証)。 (365 [でサポート](/microsoft-365/compliance/technical-reference-details-about-encryption) される TLS 暗号スイートの一覧については、「暗号化に関するテクニカル リファレンスOffice参照してください)。これは、Outlook、Skype for Business、Microsoft Teams、Outlook on the web (HTTP、POP3 など) などのクライアントで使用されるプロトコルに適用されます。

パブリック証明書は、送信された情報の機密性を保護するための内部 Microsoft ツールである SSLAdmin を使用して Microsoft IT SSL によって発行されます。 Microsoft IT によって発行される証明書の長さは 2048 ビット以上であり、Webtrust コンプライアンスでは、証明書が Microsoft が所有するパブリック IP アドレスにのみ発行されるのを確認するために SSLAdmin が必要です。 この条件を満たしない IP アドレスは、例外プロセスを通じてルーティングされます。

使用されている TLS のバージョン、前方秘密 (FS) が有効かどうか、暗号スイートの順序など、すべての実装の詳細が一般に公開されています。 これらの詳細を確認する方法の 1 つは [、Qualys SSL Labs などのサードパーティの Web サイトを使用する方法です](https://www.ssllabs.com)。 以下に、次のサービスの情報を表示する Qualys の自動テスト ページへのリンクを示します。

- [Office 365 ポータル](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype for Business (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype for Business (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Exchange Online Protection の場合、URL はテナント名によって異なります。ただし、すべてのお客様が Microsoft 365 をテストするには **、microsoft-com.mail.protection.outlook.com。**
