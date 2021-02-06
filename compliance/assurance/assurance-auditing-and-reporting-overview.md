---
title: Microsoft クラウド サービスでの監査とレポート
description: Office 365、Microsoft 365、およびサービス アシュアランス内の監査およびレポート機能の概要。
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
ms.openlocfilehash: 4cb9f68f2c5861905a4246582a3b4530c30988ca
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120706"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a>Microsoft クラウド サービスでの監査とレポート

Microsoft クラウド サービスには、テナント内のユーザーおよび管理アクティビティを追跡するために使用できる監査およびレポート機能がいくつか含まれています。たとえば、Exchange Online と SharePoint Online のテナント構成設定に加えた変更、ドキュメントや他のアイテムに対するユーザーによる変更が含まれます。 Microsoft クラウド サービスで利用可能な監査情報とレポートを使用して、ユーザー エクスペリエンスの効率的な管理、リスクの軽減、コンプライアンスの義務の履行を行います。

## <a name="security--compliance-centers"></a>セキュリティ & コンプライアンス センター

[Microsoft 365 セキュリティ](https://protection.office.com)& コンプライアンス センター [、Microsoft 365](https://security.microsoft.com)セキュリティ センター、および Microsoft [365 コンプライアンス](https://compliance.microsoft.com)センターは、組織内のデータを保護するための 1 つの停止ポータルであり、多くの監査およびレポート機能が含まれます。 これらのセンターは、データ保護またはコンプライアンスのニーズに対応し、ユーザーと管理者のアクティビティを監査するのに役立ちます。 これらのセンターには、サブスクリプション管理者アカウントを使用してアクセスできます。

これらのセンターには、いくつかの機能にアクセスするナビゲーション ウィンドウが含まれます。

- **アラート:** Cloud App Security を使用して、アラートの管理、セキュリティ関連のアラートの表示、高度な [アラートの管理を行えます](/cloud-app-security/what-is-cloud-app-security)。
- **アクセス許可:** コンプライアンス管理者 [、](/microsoft-365/security/office-365-security/grant-access-to-the-security-and-compliance-center) 電子情報開示マネージャーなどのアクセス許可を組織内のユーザーに割り当て、これらのセンターでタスクを実行できます。 各センターのほとんどの機能にアクセス許可を割り当てるが、その他のアクセス許可は Exchange 管理センターと SharePoint 管理センターを使用して構成する必要があります。
- **脅威の管理:**[Microsoft 365](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)の Basic Mobility and Security を使用してデバイス管理ポリシーを作成して適用し、組織のデータ損失防止 [(DLP)](/microsoft-365/compliance/data-loss-prevention-policies)ポリシーを設定し、電子メール フィルター、マルウェア対策、DomainKeys Identified Mail (DKIM)、安全な添付ファイル、安全なリンク、OAuth アプリを構成できます。
- **データ ガバナンス:** 電子メールまたは SharePoint データを他のシステムから [Microsoft 365](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84)にインポートしたり、アーカイブ [](/microsoft-365/compliance/retention-policies)メールボックスを構成したり、組織内の電子メールや他のコンテンツの保持ポリシーを設定したりできます。 [](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)
- **検索&調査:** コンテンツ [検索、](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a)[監査ログ](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)、検疫、および電子 [](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da)情報開示ケース管理ツールを提供し、Exchange Online メールボックス、グループとパブリック フォルダー、SharePoint Online、OneDrive for Business 間でのアクティビティをすばやく詳細に確認できます。
- **レポート:** SharePoint Online、OneDrive for Business、Exchange Online、Azure AD のレポートにすばやくアクセスできます。 [](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a)
- **サービス アシュアランス:** Microsoft が Microsoft 365、Azure、Microsoft Dynamics CRM Online、Microsoft Intune、その他のクラウド サービスのグローバル標準に対するセキュリティ、プライバシー、コンプライアンスを維持する方法について説明します。 また、サードパーティの ISO、SOC、その他の監査レポートへのアクセス、および Microsoft 365 のサード パーティ監査人によってテストおよび検証されたさまざまなコントロールに関する詳細を提供する監査コントロールも含まれます。

## <a name="service-assurance"></a>サービス アシュアランス

規制対象業界の多くの組織は、広範なコンプライアンス要件の対象となります。 お客様自身のリスク評価を実行するには、Microsoft 365 がデータのセキュリティとプライバシーを維持する方法に関する詳細な情報が必要な場合があります。 Microsoft は、クラウド サービス内の顧客データのセキュリティとプライバシーに取り組み、運用の透過的なビューと、独立したコンプライアンス レポートと評価への簡単なアクセスを提供することで、顧客の信頼を得る取り組みです。

サービス アシュアランスは、運用の透明性と、Microsoft が Microsoft 365 の顧客データのセキュリティ、プライバシー、コンプライアンスを維持する方法に関する情報を提供します。 データの暗号化、データの回復性、セキュリティ インシデント管理など、Microsoft 365 のトピックに関するホワイト ペーパー、FAQ、その他の資料のライブラリと共に、サードパーティ監査レポートが含まれています。 お客様は、この情報を使用して、独自の規制リスク評価を実行できます。 コンプライアンス責任者は、"サービス アシュアランス ユーザー" ロールを割り当て、ユーザーにサービス アシュアランスへのアクセスを許可できます。 テナント管理者は [、Microsoft Cloud Service Trust Portal](https://aka.ms/STP) (STP) を通じて、サービス アシュアランス ダッシュボードの情報へのアクセス権を、独立監査人などの外部ユーザーに提供することもできます。

## <a name="onedrive-for-business-admin-center"></a>OneDrive for Business 管理センター

Microsoft OneDrive 管理センターは、組織の OneDrive for Business の設定をすばやく簡単に 1 か所で管理するのに役立ちます。 OneDrive 管理センターを使用するには、アプリへのアクセスonedrive.com必要です。 また、組織のグローバル管理者か、SharePoint 管理者ロールを持つカスタム管理者である必要があります。 OneDrive for Business 管理センターにアクセスします [https://admin.onedrive.com](https://admin.onedrive.com/) 。

主要な機能には、監査ログの検索、DLP の操作、保持、電子情報開示、警告などの主要なシナリオに適した管理センターへのリンクを管理者に提供するコンプライアンス領域が含まれます。

## <a name="related-links"></a>関連リンク

- [Microsoft 365 のレポート作成機能](assurance-reporting-features.md)
- [Microsoft 365 のエンジニアリングのための内部ログ記録](assurance-internal-logging.md)
