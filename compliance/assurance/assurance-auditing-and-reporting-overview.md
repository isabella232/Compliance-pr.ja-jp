---
title: Microsoft クラウド サービスでの監査とレポート作成
description: 監査機能とレポート機能の概要は、Office 365、Microsoft 365、およびサービス アシュアランス内にあります。
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
- M365-analytics
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: f45977c9afa14d8bca25c0b812e0a390cee82c9a468e6ffe0d601855ee64ed1f
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54289255"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a>Microsoft クラウド サービスでの監査とレポート作成

Microsoft クラウド サービスには、テナント内のユーザーと管理アクティビティを追跡するために使用できるいくつかの監査機能とレポート機能、Exchange Online および SharePoint Online テナント構成設定に加えた変更、およびドキュメントなどのアイテムに対するユーザーによる変更が含まれます。 Microsoft クラウド サービスで利用可能な監査情報とレポートを使用して、ユーザー エクスペリエンスの効率的な管理、リスクの軽減、コンプライアンス義務の履行を行います。

## <a name="security--compliance-centers"></a>セキュリティ & コンプライアンス センター

[Microsoft 365 セキュリティ](https://protection.office.com)& コンプライアンス センター [、Microsoft 365](https://security.microsoft.com)セキュリティ センター、[および Microsoft 365](https://compliance.microsoft.com)コンプライアンス センターは、組織内のデータを保護するためのワンストップ ポータルであり、多くの監査およびレポート機能が含まれます。 これらのセンターは、データ保護またはコンプライアンスのニーズに対応し、ユーザーと管理者のアクティビティを監査するのに役立ちます。 これらのセンターには、サブスクリプション管理者アカウントを使用してアクセスできます。

これらのセンターには、いくつかの機能にアクセスするナビゲーション ウィンドウが含まれます。

- **アラート:** アラートの管理、セキュリティ関連のアラートの表示、および高度なアラートの管理 [](/cloud-app-security/what-is-cloud-app-security)を、Cloud App Security。
- **アクセス許可:** コンプライアンス管理者 [、電子情報開示](/microsoft-365/security/office-365-security/grant-access-to-the-security-and-compliance-center) マネージャーなどのアクセス許可を組織内のユーザーに割り当て、これらのセンターでタスクを実行できます。 各センターのほとんどの機能にアクセス許可を割り当てるが、その他のアクセス許可は、Exchange管理センターと管理センター SharePointする必要があります。
- **脅威の管理:**[Microsoft 365](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)の Basic Mobility と Security を使用してデバイス管理ポリシーを作成および適用し、組織のデータ損失防止 [(DLP)](/microsoft-365/compliance/data-loss-prevention-policies)ポリシーを設定し、電子メール フィルター、マルウェア対策、DomainKeys Identified Mail (DKIM)、安全な添付ファイル、安全なリンク、OAuth アプリを構成できます。
- **データ ガバナンス:** 他のシステムから [電子メールまたは](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84)SharePoint データを Microsoft 365 にインポートし、アーカイブ [](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)メールボックスを構成し、組織内 [](/microsoft-365/compliance/retention-policies)の電子メールや他のコンテンツの保持ポリシーを設定できます。
- **検索&調査:** Exchange Online [](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a)メールボックス、[](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)グループとパブリック フォルダー、SharePoint Online、および OneDrive for Business 間のアクティビティをすばやく掘り下げられるコンテンツ検索、監査ログ、検疫、および電子情報開示ケース管理ツールを提供します。 [](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da)
- **レポート:** オンライン、SharePoint、OneDrive for Business、Azure Exchange OnlineのレポートにすばやくアクセスAD。 [](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a)
- **サービスアシュアランス:** Microsoft が Microsoft 365、Azure、Microsoft Dynamics CRM Online、Microsoft Intune、その他のクラウド サービスのグローバル標準に準拠してセキュリティ、プライバシー、コンプライアンスを維持する方法に関する情報を提供します。 また、サードパーティの ISO、SOC、その他の監査レポートへのアクセス、および Microsoft 365 のサード パーティ監査者によってテストおよび検証されたさまざまなコントロールに関する詳細を提供する監査コントロールも含まれます。

## <a name="service-assurance"></a>サービス アシュアランス

規制業界の多くの組織は、広範なコンプライアンス要件の対象となります。 多くの場合、お客様はリスク評価を実行するために、データのセキュリティとプライバシーを維持する方法Microsoft 365詳細な情報を必要とします。 Microsoft は、クラウド サービスにおける顧客データのセキュリティとプライバシーに取り組み、運用の透過的なビューを提供し、独立したコンプライアンス レポートと評価に簡単にアクセスすることで、顧客の信頼を得る取り組みです。

サービス アシュアランスは、運用の透明性と、Microsoft が顧客データのセキュリティ、プライバシー、コンプライアンスを管理する方法に関する情報を提供Microsoft 365。 データの暗号化、データの復元、セキュリティ インシデント管理など、Microsoft 365 トピックに関するホワイト ペーパー、FAQ、その他の資料のライブラリと共に、サード パーティの監査レポートが含まれています。 お客様は、この情報を使用して、独自の規制リスク評価を実行できます。 コンプライアンス担当者は、"Service Assurance User" ロールを割り当て、ユーザーにサービス アシュアランスへのアクセスを許可できます。 テナント管理者は、独立監査人などの外部ユーザーに、サービス アシュアランス ダッシュボードの情報へのアクセス権を、MICROSOFT CLOUD SERVICE[信頼ポータル (STP) から](https://aka.ms/STP)提供することもできます。

## <a name="onedrive-for-business-admin-center"></a>OneDrive for Business管理センター

管理Microsoft OneDrive管理センターを使用すると、組織のユーザー設定を 1 か所OneDrive for Business簡単に管理できます。 管理センターで OneDriveするには、管理センターへのアクセス onedrive.com 必要です。 組織のグローバル管理者または管理者ロールを持つカスタム管理者SharePoint必要があります。 [管理センター OneDrive for Businessにアクセスします [https://admin.onedrive.com](https://admin.onedrive.com/) 。

主な機能には、監査ログの検索、DLP の操作、保持、電子情報開示、アラート処理などの重要なシナリオに対する適切な管理センターへのリンクを管理者に提供するコンプライアンス領域が含まれます。

## <a name="related-links"></a>関連リンク

- [Microsoft 365 のレポート作成機能](assurance-reporting-features.md)
- [Microsoft 365 のエンジニアリングのための内部ログ記録](assurance-internal-logging.md)
