---
title: ロシアの個人データのローカライズ要件
description: 個人データの収集、ロシア市民の個人データの記録、システム化、蓄積、保存、説明、抽出が、ロシアにある Microsoft サービスおよびデータベースでどのように実行されるのかについて説明します。
keywords: Microsoft 365、コンプライアンス、サービス
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 6ee6dc8a6132e76bd39487fbb51e03509e7d2a95
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50119896"
---
# <a name="russian-personal-data-localization-requirements"></a>ロシアの個人データのローカライズ要件

2015 年 9 月 1 日の現在、個人データオペレーターと見なされる組織は、個人データの収集、ロシア市民の個人データの記録、システム化、収集、保存、説明 (更新、変更)、抽出を、ロシアにあるデータベース (「個人データのローカライズ要件」) を通じて実行する必要があります。<sup>1</sup>

Microsoft Azure、Microsoft 365、Dynamics 365、Power Platform などの個人データ処理を有効にしている組織 (教育機関を含むが、これらに限定されない) (以下「お客様」と呼ばれる) が利用できる Microsoft サービスは、ロシアの外部にあるデータ処理センターから提供されます (詳細については [、Microsoft セキュリティ](https://www.microsoft.com/trust-center)センターを参照してください)。

顧客情報システムによって処理される情報の種類とコンテンツに基づいて、そのようなシステム (Microsoft クラウド製品を使用するシステムを含む) は、個人データ情報システム ('PDIS'、'ISPD') と見なされる場合があります。 お客様が、そのアーキテクチャと処理される情報の種類を通じて PDIS と見なされるシステムで Microsoft サービスを使用する場合、Microsoft は、以下に示す利用可能なソリューションの中でお客様に検討を招待します。 提供されるシナリオはすべて、標準的なビジネス サービスの追加オプションとして、お客様が利用できます。

コンプライアンスを担当し、個人データのローカライズに適用される法的要件を分析および評価する PDIS の個人データオペレーターであるお客様であり、独自の判断で、PDIS での個人データ処理がロシアの個人データ法に準拠していることを確認するための十分な手段を個別に決定する必要があります。<sup>2</sup>

## <a name="subscribing-to-microsoft-services"></a>Microsoft サービスのサブスクライブ

### <a name="microsoft-id-management"></a>Microsoft ID の管理

Microsoft は、Microsoft サービスへのサブスクライブを検討する顧客を招待します。Microsoft クラウド ソリューション プロバイダー (CSP) パートナー経由の Microsoft Azure、Microsoft 365、Dynamics 365、および Power Platform。 詳しくは、CSP パートナーの [一覧をご覧ください](https://pinpoint.microsoft.com/search?type=services&campaign=691)。

### <a name="managing-user-identity-and-access-for-microsoft-services"></a>Microsoft サービスのユーザー ID とアクセスの管理

Microsoft Azure、Microsoft 365、Dynamics 365、Power Platform などの Microsoft サービスの場合、ユーザーの検証とアクセス管理は [Azure Active Directory (Azure Active Directory)](https://azure.microsoft.com/services/active-directory/)を通じて実行されます。 Microsoft のお客様が Microsoft クラウド サービス (Windows Server Active Directory (AD) や他の ID 管理システムなど) にローカル ID 管理システムを使用している場合、お客様は Azure AD Connect を介してそのようなシステムを Azure Active Directory (Azure Active Directory) と迅速に統合する機会があります。 詳細については [、Azure AD Connect を参照してください](/azure/active-directory/cloud-provisioning/)。 Microsoft のお客様は、サードパーティ ベンダーのアプリケーションとソリューションを使用して、ユーザーを管理し、ローカル ID システムを Azure AD に統合する場合があります。

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

## <a name="questions-and-support"></a>質問とサポート

技術的および課金に関する質問については、以下の Microsoft サポート リソースを参照してください。 その他の質問や説明については、Microsoft プライバシー チームにお [問い合わせください](https://support.microsoft.com/gp/privacy-page)。

### <a name="microsoft-azure"></a>Microsoft Azure

- **Web サイト**: [Microsoft Azure サポート](https://aka.ms/GetAzureSupport)
- **フリー ダイヤル**: 8 800 200 8001
- **ローカル通話**: 495 916 7171
- **オンライン サポート**: Azure ポータル経由でクエリを [送信する](https://portal.azure.com)

### <a name="microsoft-365"></a>Microsoft 365

- **フリー ダイヤル**: 8 10 800 2548 1044
- **ローカル通話**: 499 922 8623
- **オンライン サポート**: 管理センターからクエリを [送信する](https://portal.office.com/)

### <a name="dynamics-365"></a>Dynamics 365

- **フリー ダイヤル**: 8 10 800 2548 1044
- **ローカル通話**: 499 922 8623
- **オンライン サポート**: Dynamics サポート ポータルから [クエリを送信する](https://dynamics.microsoft.com/support/)

### <a name="power-platform"></a>Power Platform

- **フリー ダイヤル**: 8 10 800 2548 1044
- **ローカル通話**: 499 922 8623
- **オンライン サポート**: Power Platform サポート経由で [クエリを送信する](/power-platform/admin/get-help-support)

> [!NOTE]
> <sup>1</sup> 連邦法いいえ 242-FZ (エディションの日付は 12.31.2014) '07.21.2014 日付の情報および通信ネットワークでの個人データ処理の手順を明確化するロシア連邦の特定の立法上の行為に修正を進める <br>
> <sup>2</sup> 連邦法いいえ 07.27 現在の個人データに対する 152- 的な保護。 2006<br>
