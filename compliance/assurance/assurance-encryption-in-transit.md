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
# <a name="encryption-for-data-in-transit"></a><span data-ttu-id="d09ce-103">転送中のデータの暗号化</span><span class="sxs-lookup"><span data-stu-id="d09ce-103">Encryption for data-in-transit</span></span>

<span data-ttu-id="d09ce-104">保存中の顧客データの保護に加え、Microsoft では暗号化技術を使用してお客様の送信中の顧客データを保護します。</span><span class="sxs-lookup"><span data-stu-id="d09ce-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect customer data in transit.</span></span> <span data-ttu-id="d09ce-105">データは転送中です。</span><span class="sxs-lookup"><span data-stu-id="d09ce-105">Data is in transit:</span></span>

- <span data-ttu-id="d09ce-106">クライアント コンピューターが Microsoft サーバーと通信する場合</span><span class="sxs-lookup"><span data-stu-id="d09ce-106">when a client machine communicates with a Microsoft server;</span></span>
- <span data-ttu-id="d09ce-107">Microsoft サーバーが別の Microsoft サーバーと通信する場合そして</span><span class="sxs-lookup"><span data-stu-id="d09ce-107">when a Microsoft server communicates with another Microsoft server; and</span></span>
- <span data-ttu-id="d09ce-108">Microsoft サーバーが Microsoft 以外のサーバーと通信する場合 (たとえば、Exchange Online がサード パーティの電子メール サーバーに電子メールを配信する場合)。</span><span class="sxs-lookup"><span data-stu-id="d09ce-108">when a Microsoft server communicates with a non-Microsoft server (for example, Exchange Online delivering email to a third-party email server).</span></span>

<span data-ttu-id="d09ce-109">Microsoft サーバー間のデータ センター間通信は TLS または IPsec を使用して行われるので、すべての顧客向けサーバーはクライアント コンピューターとの TLS を使用してセキュリティで保護されたセッションをネゴシエートします (たとえば、Exchange Online は TLS 1.2 を使用し、256 ビット暗号強度が使用されます (FIPS 140-2 レベル 2 検証)。</span><span class="sxs-lookup"><span data-stu-id="d09ce-109">Inter-data center communications between Microsoft servers take place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (for example, Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated).</span></span> <span data-ttu-id="d09ce-110">(Office [](/microsoft-365/compliance/technical-reference-details-about-encryption) 365 でサポートされている TLS 暗号スイートの一覧については、暗号化に関するテクニカル リファレンスOffice参照してください)。これは、Outlook、Skype for Business、Microsoft Teams、Web 上の Outlook (HTTP、POP3 など) などのクライアントで使用されるプロトコルに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d09ce-110">(See [Technical reference details about encryption](/microsoft-365/compliance/technical-reference-details-about-encryption) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, Microsoft Teams, and Outlook on the web (for example, HTTP, POP3, etc.).</span></span>

<span data-ttu-id="d09ce-111">パブリック証明書は、送信される情報の機密性を保護する内部の Microsoft ツールである SSLAdmin を使用して、Microsoft IT SSL によって発行されます。</span><span class="sxs-lookup"><span data-stu-id="d09ce-111">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information.</span></span> <span data-ttu-id="d09ce-112">Microsoft IT によって発行される証明書の長さは 2048 ビット以上であり、Webtrust コンプライアンスでは、証明書が Microsoft が所有するパブリック IP アドレスにのみ発行されるのを確認するために SSLAdmin が必要です。</span><span class="sxs-lookup"><span data-stu-id="d09ce-112">All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and Webtrust compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft.</span></span> <span data-ttu-id="d09ce-113">この条件を満たしない IP アドレスは、例外処理によってルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="d09ce-113">Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="d09ce-114">使用されている TLS のバージョン、Forward Secrecy (FS) が有効かどうか、暗号スイートの順序など、すべての実装の詳細が一般に公開されています。</span><span class="sxs-lookup"><span data-stu-id="d09ce-114">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly.</span></span> <span data-ttu-id="d09ce-115">これらの詳細を確認する 1 つの方法は [、Qualys SSL Labs](https://www.ssllabs.com)などのサードパーティの Web サイトを使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="d09ce-115">One way to see these details is to use a third-party website, such as [Qualys SSL Labs](https://www.ssllabs.com).</span></span> <span data-ttu-id="d09ce-116">次のサービスの情報を表示する Qualys の自動テスト ページへのリンクを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="d09ce-116">Below are the links to automated test pages from Qualys that display information for the following services:</span></span>

- [<span data-ttu-id="d09ce-117">Office 365 ポータル</span><span class="sxs-lookup"><span data-stu-id="d09ce-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="d09ce-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="d09ce-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="d09ce-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="d09ce-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="d09ce-120">Skype for Business (SIP)</span><span class="sxs-lookup"><span data-stu-id="d09ce-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="d09ce-121">Skype for Business (Web)</span><span class="sxs-lookup"><span data-stu-id="d09ce-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="d09ce-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="d09ce-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="d09ce-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d09ce-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="d09ce-124">Exchange Online Protection では、URL はテナント名によって異なります。However, all customers can test Microsoft 365 using **microsoft-com.mail.protection.outlook.com**.</span><span class="sxs-lookup"><span data-stu-id="d09ce-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Microsoft 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
