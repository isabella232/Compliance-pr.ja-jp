---
title: Office Server の GDPR
description: Office オンプレミスのサーバーで一般データ保護規則 (GDPR) の要件に対応する方法について説明します。
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: high
titleSuffix: Microsoft GDPR
ms.collection: MS-Compliance
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: f514a966b576f15b2eeba1ae36c5cb88f3e91bd8
ms.sourcegitcommit: 9766d656d0e270f478437bd39c0546ad2e4d846f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/27/2021
ms.locfileid: "58678636"
---
# <a name="gdpr-for-office-on-premises-servers"></a>オンプレミス サーバー上の Office の GDPR

一般データ保護規則 (GDPR) により、組織が個人データを保護し、データ主体要求に適切に応答するための要件が導入されます。このシリーズの記事では、オンプレミスのワークロードのために推奨されるアプローチを示します。

- [SharePoint Server](gdpr-for-sharepoint-server.md)

- [Exchange Server](gdpr-for-exchange-server.md)

- [Skype for Business Server](gdpr-for-skype-for-business-server.md)

- [Project Server](gdpr-for-project-server.md)

- [Office Web Apps Server および Office Online Server](gdpr-for-office-online-server.md)

- [オンプレミス ファイル共有](gdpr-for-on-premises-file-shares.md)

GDPR について、また Microsoft による支援方法の詳細については、[Microsoft セキュリティ センター](https://www.microsoft.com/trust-center/privacy/gdpr-overview
)を参照してください。

オンプレミス データで何らかの作業を実行する前に、法律およびコンプライアンスのチームに問い合わせて、ガイダンス情報を入手し、個人データを処理する際の既存の分類スキーマやアプローチについて確認してください。Microsoft では、[https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>) の Microsoft GDPR Data Discovery Toolkit で、分類スキーマの開発と拡張の推奨事項を提供しています。このツールキットでは、オンプレミス データをクラウドに移行するためのアプローチも記述されています。クラウドでは、必要に応じて、より洗練されたデータ ガバナンス機能を使用できます。このセクションの記事では、意図的にオンプレミスのままにするデータに関する推奨事項が示されています。

次の図に、これらのワークロードそれぞれで、個人データを検出、分類、保護、監視するために使用する推奨機能のリストを示します。詳細については、このセクションの記事を参照してください。

![ワークロード全体で個人データを検出、分類、保護、監視する機能を説明する図。](../media/gdpr-for-office-servers-image1.png)

## <a name="illustration-description"></a>図の説明

次の表では、図での例と同じものを見やすいように記載しています。

****

|Action|Windows Server ファイル共有|SharePoint Server|Exchange Server|Skype for Business|Project Server|
|---|---|---|---|---|---|
|検索|Azure Information Protection スキャナー<sup>\*</sup>|検索センターまたは eDiscovery (データが分類された後) <br/><br/> Azure Information Protection スキャナー<sup>\*</sup>|Exchange 電子情報開示ポータル|Exchange 電子情報開示ポータル|検出およびエクスポートのための SQL スクリプト|
|分類|Azure Information Protection スキャナー<sup>\*</sup> <br/><br/> Office 365 の機密情報の種類|Azure Information Protection スキャナー<sup>\*</sup> <br/><br/> Office 365 の機密情報の種類|Exchange 保持タグおよびアイテム保持ポリシー|Exchange 保持タグおよびアイテム保持ポリシー||
|保護||Exchange Server データ損失防止ルール <br/><br/> アクセス許可、ライブラリの IRM による保護|Exchange Server データ損失防止ルール <br/><br/> IRM と Exchange Server との統合|||
|監視する|SIEM ツールとのログ統合|SIEM ツールとのログ統合|SIEM ツールとのログ統合|SIEM ツールとのログ統合|SIEM ツールとのログ統合|
|

<sup>\*</sup> 保護機能によってファイルが暗号化されることに注意してください。結果として、SharePoint Server では、保護されたファイルの機密情報の種類を検索できなくなります。
