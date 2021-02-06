---
title: 転送中のデータの暗号化
description: この記事では、Microsoft が送信中に Microsoft 365 の顧客データを暗号化する方法の簡単な説明を見つける必要があります。
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
ms.openlocfilehash: b6d6ae53ef2ade842e0e9205c01b44fe17891a97
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120536"
---
# <a name="encryption-for-data-in-transit"></a>転送中のデータの暗号化

保存中の顧客データの保護に加え、Microsoft では暗号化技術を使用してお客様の送信中の顧客データを保護します。 データは転送中です。

- クライアント コンピューターが Microsoft サーバーと通信する場合
- Microsoft サーバーが別の Microsoft サーバーと通信する場合そして
- Microsoft サーバーが Microsoft 以外のサーバーと通信する場合 (たとえば、Exchange Online がサード パーティの電子メール サーバーに電子メールを配信する場合)。

Microsoft サーバー間のデータ センター間通信は TLS または IPsec を使用して行われるので、すべての顧客向けサーバーはクライアント コンピューターとの TLS を使用してセキュリティで保護されたセッションをネゴシエートします (たとえば、Exchange Online は TLS 1.2 を使用し、256 ビット暗号強度が使用されます (FIPS 140-2 レベル 2 検証)。 (Office [](/microsoft-365/compliance/technical-reference-details-about-encryption) 365 でサポートされている TLS 暗号スイートの一覧については、暗号化に関するテクニカル リファレンスOffice参照してください)。これは、Outlook、Skype for Business、Microsoft Teams、Web 上の Outlook (HTTP、POP3 など) などのクライアントで使用されるプロトコルに適用されます。

パブリック証明書は、送信される情報の機密性を保護する内部の Microsoft ツールである SSLAdmin を使用して、Microsoft IT SSL によって発行されます。 Microsoft IT によって発行される証明書の長さは 2048 ビット以上であり、Webtrust コンプライアンスでは、証明書が Microsoft が所有するパブリック IP アドレスにのみ発行されるのを確認するために SSLAdmin が必要です。 この条件を満たしない IP アドレスは、例外処理によってルーティングされます。

使用されている TLS のバージョン、Forward Secrecy (FS) が有効かどうか、暗号スイートの順序など、すべての実装の詳細が一般に公開されています。 これらの詳細を確認する 1 つの方法は [、Qualys SSL Labs](https://www.ssllabs.com)などのサードパーティの Web サイトを使用する方法です。 次のサービスの情報を表示する Qualys の自動テスト ページへのリンクを以下に示します。

- [Office 365 ポータル](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype for Business (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype for Business (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Exchange Online Protection では、URL はテナント名によって異なります。However, all customers can test Microsoft 365 using **microsoft-com.mail.protection.outlook.com**.
