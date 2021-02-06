---
title: Microsoft 365 の管理アクセス制御
description: この記事では、Microsoft 365 の管理アクセス制御とデータ分類の概要について説明します。
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: d3d6cd30fbe682de979d5c04943c57cedc86552f
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120716"
---
# <a name="administrative-access-controls-in-microsoft-365"></a>Microsoft 365 の管理アクセス制御 

Microsoft は、Microsoft による顧客コンテンツへのアクセスを意図的に制限しながら、ほとんどの Microsoft 365 操作を自動化するシステムとコントロールに多額の投資を行っています。 人間がサービスを管理し、ソフトウェアがサービスを運用します。 この構造により、Microsoft は Microsoft 365 を大規模に管理し、顧客コンテンツに対する内部の脅威のリスクを管理できます。

既定では、Microsoft のエンジニアは、Microsoft 365 の顧客コンテンツに対する永続的な管理特権と永続的なアクセス権を持ち合っています。 Microsoft のエンジニアは、限られた期間、制限付き、監査、およびセキュリティで保護されたアクセスをお客様のコンテンツに持ち込む可能性があります。 アクセスは、サービス運用に必要な場合と、Microsoft 上級管理職のメンバーによって承認された場合にのみ行います。 カスタマー ロックボックスライセンスのお客様の場合、お客様は Microsoft 365 でホストされているコンテンツへのアクセス承認を提供します。

Microsoft は、複数の形式のクラウド配信を使用してオンライン サービスを提供しています。

- **パブリック クラウド:** Microsoft 365、Azure、および北米、南アメリカ、ヨーロッパ、アジア、オーストラリアなどにホストされているその他のサービスのマルチテナント バージョンが含まれます。
- **国内クラウド:** 中国の Microsoft 365 (21Vianet が運用) やドイツの Microsoft 365 (Microsoft が運用していますが、ドイツ のデータ トラスティである Deutsche Telekom が顧客データを含むシステムに対する Microsoft のアクセスを制御および監視するモデルの下で) など、米国外のすべての独立したクラウドと第三者が運用するクラウド (前に説明したクラウドを除く) が含まれます。
- **政府機関用クラウド:** 米国政府機関のお客様が利用できる Microsoft 365 および Azure サービスが含まれています。

この記事の目的上、Microsoft 365 サービスには以下が含まれます。

- [Exchange Online](/Exchange/exchange-online)
- [Exchange Online Protection](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [SharePoint Online](/sharepoint/sharepoint-online)
- [OneDrive for Business](/OneDrive/onedrive)
- [Skype for Business](/SkypeForBusiness/skype-for-business-online)
- [Microsoft Teams](/MicrosoftTeams/Teams-overview)
- [Yammer](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a>Microsoft 365 のアクセス制御

アクセス制御の目的で、Microsoft は Microsoft 365 データを顧客データまたは他の種類のデータとして分類します。

### <a name="customer-data"></a>顧客データ

顧客データとは、Microsoft 365 サービスを使用する際にお客様が提供または代理して提供するデータです。 このデータは、Microsoft 365 ユーザーによって直接作成またはアップロードされた顧客コンテンツです。以下が含まれる。

- メール
- SharePoint Online コンテンツ
- インスタント メッセージ
- 予定表アイテム
- ドキュメント
- 連絡先
- エンドユーザーを特定できる情報 (EUII) (ユーザーに固有のデータ、または個々のユーザーにリンク可能だが顧客コンテンツは含められないデータ)

### <a name="other-types-of-data"></a>その他の種類のデータ

その他の種類のデータは次のとおりです。

- **アカウント データ:** 管理データ (管理者がサービスをサインアップまたは購入するときに提供する情報)、支払いデータ (クレジット カードの詳細など、支払い方法に関する情報) が含まれます。
- **組織的に識別可能な情報:** テナントの識別に使用されるデータ、使用状況データが含まれます。個々のユーザーまたは顧客コンテンツにリンクできません。
- **システム メタデータ:** 構成設定、システム状態、Microsoft IP アドレス、およびサブスクリプションとテナントに関する技術情報を含むサービス ログが含まれます。

Microsoft は、顧客データやアクセス制御データへの未承認のアクセスを許可しないユーザーがいなか、アクセス制御メカニズムを確立しています。 アクセス制御データは、お客様のコンテンツや EUII、Microsoft パスワード、セキュリティ証明書、その他の認証関連データへのアクセスなど、環境内の他の種類のデータまたは機能へのアクセスを管理します。 アクセス制御メカニズムは、Microsoft 365 の実稼働環境への未承認の物理的アクセス、論理アクセス、またはリモート アクセスに対する保護も行います。

Microsoft 365 の運用に Microsoft が使用するアクセス制御には、次の 3 つのカテゴリがあります。

- 分離の制御
- 担当者の制御
- テクノロジの制御

これらのコントロールを組み合わせると、Microsoft 365 の悪意のある操作を防止および検出できます。 Microsoft が使用する分離、人員、および技術のコントロールに加えて、コントロールの第 4 のカテゴリがあります。コントロールは、お客様によって実装されます。

Microsoft 365 では、オンプレミス環境でデータを管理するのと同じ方法でデータを管理できます。 Microsoft 365 の組織にサインインしたユーザーは、自動的にグローバル管理者になります。 グローバル管理者は、管理ポータルのすべての機能にアクセスできます。次の機能を使用できます。

- ユーザーを作成または編集する
- 管理者ロールを他のユーザーに割り当てる
- ユーザー パスワードをリセットする
- ユーザー ライセンスを管理する
- ドメインの管理
- カスタマー ロックボックス要求を承認する

各組織で少なくとも 2 つの管理者アカウントを構成することをお勧めします。 大規模なエンタープライズ組織では、さまざまな機能を提供する専用の管理者アカウントをお勧めします。

管理者の役割とアクセス許可の割り当てについては、「管理者の役割の割り当て [」および](/microsoft-365/admin/add-users/assign-admin-roles) 「管理者の役割 [について」を参照してください](/microsoft-365/admin/add-users/about-admin-roles)。

## <a name="related-links"></a>関連リンク

- [Microsoft 365 での分離](assurance-isolation-in-microsoft-365.md)
- [Microsoft 就職前スクリーニング](assurance-pre-employment-screening.md)
- [Microsoft Cloud の背景チェック](assurance-cloud-background-check.md)
- [アクセス制御の監視と監査](assurance-monitoring-and-auditing-access-controls.md)
- [Yammer Enterprise でのアクセス制御](assurance-yammer-enterprise-access-controls.md)
