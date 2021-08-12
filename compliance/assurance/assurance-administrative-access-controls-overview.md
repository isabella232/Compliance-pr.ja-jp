---
title: 管理アクセス制御 (Microsoft 365
description: この記事では、管理アクセス制御とデータ分類の概要について説明します。Microsoft 365。
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
hideEdit: true
ms.openlocfilehash: 06bdd239e2845d3495a40fc83bd33cbb0e43dbdb3d025bd8fa77b5d5451a680c
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54289265"
---
# <a name="administrative-access-controls-in-microsoft-365"></a>管理アクセス制御 (Microsoft 365 

Microsoft は、Microsoft による顧客コンテンツへのアクセスを意図的に制限しながら、Microsoft 365操作を自動化するシステムとコントロールに多額の投資を行っています。 人間がサービスを管理し、ソフトウェアがサービスを運用します。 この構造により、Microsoft は大規模なMicrosoft 365を管理し、顧客コンテンツに対する内部脅威のリスクを管理できます。

既定では、Microsoft のエンジニアは、管理者特権がゼロで、ユーザーのコンテンツに対する永続的なアクセスMicrosoft 365。 Microsoft のエンジニアは、限られた時間の間、お客様のコンテンツへのアクセスを制限、監査、およびセキュリティで保護することができます。 アクセスは、サービスの運用に必要な場合にのみ、Microsoft 上級管理職のメンバーによって承認された場合にのみ行います。 Customer Lockbox ライセンスのお客様の場合、お客様は、ユーザーがホストするコンテンツへのアクセス承認をMicrosoft 365。

Microsoft は、複数の形式のクラウド配信を使用してオンライン サービスを提供します。

- **パブリック クラウド:** 北米、南アメリカ、ヨーロッパ、アジア、オーストラリアなどMicrosoft 365、Azure、その他のサービスのマルチテナント バージョンが含まれます。
- **国のクラウド:** 中国の Microsoft 365 (21Vianet が運用) やドイツの Microsoft 365 (Microsoft が運用していますが、ドイツのデータ トラスティであるドイツテレコムが顧客データを含むシステムへの Microsoft のアクセスを制御および監視するモデル) など、米国外のすべての主権および第三者が運用するクラウドが含まれています。
- **政府機関のクラウド:** 米国Microsoft 365顧客が利用できるサービスと Azure サービスが含まれます。

この記事では、以下のサービスMicrosoft 365提供しています。

- [Exchange Online](/Exchange/exchange-online)
- [Exchange Online Protection](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [SharePoint Online](/sharepoint/sharepoint-online)
- [OneDrive for Business](/OneDrive/onedrive)
- [Skype for Business](/SkypeForBusiness/skype-for-business-online)
- [Microsoft Teams](/MicrosoftTeams/Teams-overview)
- [Yammer](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a>Microsoft 365アクセス制御

アクセス制御の目的で、Microsoft はデータMicrosoft 365顧客データまたは他の種類のデータとして分類します。

### <a name="customer-data"></a>顧客データ

顧客データは、サービスを利用する際に顧客が提供または代理して提供Microsoft 365です。 このデータは、以下を含む、ユーザーが直接作成またはアップロードMicrosoft 365顧客コンテンツです。

- メール
- SharePointオンライン コンテンツ
- インスタント メッセージ
- 予定表アイテム
- Documents
- 連絡先
- エンド ユーザー識別可能な情報 (EUII) (ユーザーに固有のデータ、または個々のユーザーにリンクできるが、顧客コンテンツは含められないデータ)

### <a name="other-types-of-data"></a>その他の種類のデータ

その他の種類のデータには、次のものがあります。

- **アカウント データ:** 管理データ (管理者がサービスをサインアップまたは購入するときに提供する情報)、支払いデータ (クレジット カードの詳細など、支払い手段に関する情報) が含まれます。
- **組織的に識別可能な情報:** テナントを識別するために使用されるデータ、利用状況データ、および個々のユーザーにリンクできない、または顧客コンテンツに含まれていないデータが含まれます。
- **システム メタデータ:** 構成設定、システム状態、Microsoft IP アドレス、サブスクリプションとテナントに関する技術情報を含むサービス ログが含まれます。

Microsoft は、お客様データまたはアクセス制御データへの未承認のアクセスを誰も持たなくするためのアクセス制御メカニズムを確立しました。 アクセス制御データは、顧客コンテンツまたは EUII、Microsoft パスワード、セキュリティ証明書、その他の認証関連データへのアクセスを含む、環境内の他の種類のデータまたは機能へのアクセスを管理します。 また、アクセス制御メカニズムは、未承認の物理、論理、またはリモート アクセスから、Microsoft 365保護します。

Microsoft が使用するアクセス制御には、次の 3 つのカテゴリMicrosoft 365。

- 分離の制御
- 担当者の制御
- テクノロジの制御

これらのコントロールを組み合わせると、ユーザーの悪意のあるアクションを防止して検出Microsoft 365。 Microsoft が使用する分離、人員、およびテクノロジコントロールに加えて、お客様が実装するコントロールという 4 番目のカテゴリのコントロールがあります。

Microsoft 365オンプレミス環境でデータを管理するのと同じ方法でデータを管理できます。 組織に自動的に組織をMicrosoft 365するユーザーは、グローバル管理者になります。 グローバル管理者は、管理ポータルのすべての機能にアクセスできます。

- ユーザーの作成または編集
- 管理者の役割を他のユーザーに割り当てる
- ユーザー パスワードをリセットする
- ユーザー ライセンスの管理
- ドメインの管理
- 顧客ロックボックス要求の承認

各組織で少なくとも 2 つの管理者アカウントを構成することをお勧めします。 大規模なエンタープライズ組織では、さまざまな機能を提供する特殊な管理者アカウントをお勧めします。

管理者の役割とアクセス許可の割り当てについては、「管理者ロールの割り当て [」および](/microsoft-365/admin/add-users/assign-admin-roles) 「管理者ロール [について」を参照してください](/microsoft-365/admin/add-users/about-admin-roles)。

## <a name="related-links"></a>関連リンク

- [分離のMicrosoft 365](assurance-isolation-in-microsoft-365.md)
- [Microsoft 就職前スクリーニング](assurance-pre-employment-screening.md)
- [Microsoft Cloud の背景チェック](assurance-cloud-background-check.md)
- [アクセス制御の監視と監査](assurance-monitoring-and-auditing-access-controls.md)
- [Yammer Enterprise でのアクセス制御](assurance-yammer-enterprise-access-controls.md)
