---
title: ロシアの個人データのローカライズ要件
description: 個人データの収集、ロシア市民の個人データの記録、システム化、蓄積、ストレージ、明確化、および抽出が、Microsoft サービス およびロシアにあるデータベースでどのように実行されるのかについて説明します。
keywords: Microsoft 365、コンプライアンス、サービス
ms.localizationpriority: medium
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
ms.openlocfilehash: 093ec578cd83dc6c52485101d232d9ccff88489e
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482802"
---
# <a name="russian-personal-data-localization-requirements"></a>ロシアの個人データのローカライズ要件

2015 年 9 月 1 日現在、個人データ事業者と見なされる組織は、個人データを収集する際に、ロシア市民の個人データの記録、システム化、蓄積、ストレージ、明確化 (更新、変更)、および抽出が、ロシアにあるデータベース ('個人データローカライズ要件') を介して実行される必要があります。<sup>1</sup>

Microsoft サービス (教育機関を含むがこれに限定されない) (以下、「顧客」と呼ぶ)、Microsoft Azure、Microsoft 365、Dynamics 365、Power Platform などの個人データ処理を可能にする組織は、ロシアの外部にあるデータ処理センターから提供されます (詳細については[、Microsoft Trust Center](https://www.microsoft.com/trust-center)を参照してください)。

顧客情報システムによって処理される情報の種類と内容に基づいて、Microsoft クラウド製品を使用するシステムを含むそのようなシステムは、個人データ情報システム ('PDIS', 'ISPD') とみなされる可能性があります。 お客様が、そのアーキテクチャと処理された情報の種類を通じて PDIS と見なされるシステムで Microsoft サービス を使用する場合、Microsoft は、次に示す利用可能なソリューションを検討する顧客を招待します。 提供されるシナリオはすべて、標準的なビジネス サービスの追加オプションとして、お客様が利用できます。

コンプライアンスを担当し、個人データのローカライズに適用される法的要件を分析および評価し、独自の裁量で、PDIS の個人データ処理がロシアの個人データ法に準拠することを確認するための十分な措置を独自に決定する PDIS の個人データオペレーターとしてお客様である必要があります。<sup>2</sup>

## <a name="subscribing-to-microsoft-services"></a>サブスクリプションのMicrosoft サービス

### <a name="microsoft-id-management"></a>Microsoft ID の管理

Microsoft は、ユーザーに対してサブスクリプションを検討Microsoft サービス。Microsoft Azure、Microsoft 365、Dynamics 365、および Power プラットフォームを使用して、Microsoft クラウド ソリューション プロバイダー (CSP) パートナーを使用します。 詳細については、CSP パートナーのこの [リストを参照してください](https://pinpoint.microsoft.com/search?type=services&campaign=691)。

### <a name="managing-user-identity-and-access-for-microsoft-services"></a>ユーザー ID とアクセスの管理Microsoft サービス

Microsoft サービス、Microsoft Azure、Microsoft 365、Dynamics 365、Power Platform などのユーザー検証およびアクセス管理は、Azure Active Directory [(Azure Active Directory)](https://azure.microsoft.com/services/active-directory/)を通じて実行されます。 Microsoft のお客様が Microsoft クラウド サービス (Windows Server Active Directory (AD) や他の ID 管理システムなど) にローカル ID 管理システムを使用している場合、お客様はそのようなシステムを Azure AD Connect を介して Azure Active Directory (Azure Active Directory) と迅速に統合する機会があります。 詳細については、「Azure AD Connect」[を参照してください](/azure/active-directory/cloud-provisioning/)。 Microsoft のお客様は、サードパーティ ベンダーのアプリケーションとソリューションを使用して、ユーザーを管理し、ローカル ID システムを Azure サーバーと統合AD。

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

## <a name="questions-and-support"></a>質問とサポート

技術的および請求に関する質問については、以下の Microsoft サポート リソースを参照してください。 その他の質問や説明については、Microsoft プライバシー チームにお [問い合わせください](https://support.microsoft.com/gp/privacy-page)。

### <a name="microsoft-azure"></a>Microsoft Azure

- **Web** サイト : [Microsoft Azureサポート](https://aka.ms/GetAzureSupport)
- **フリーダイヤル**: 8 800 200 8001
- **ローカル通話**: 495 916 7171
- **オンライン サポート**: Azure portal を介してクエリ [を送信する](https://portal.azure.com)

### <a name="microsoft-365"></a>Microsoft 365

- **フリーダイヤル**: 8 10 800 2548 1044
- **ローカル通話**: 499 922 8623
- **オンライン サポート**: 管理センターからクエリを [送信する](https://portal.office.com/)

### <a name="dynamics-365"></a>Dynamics 365

- **フリーダイヤル**: 8 10 800 2548 1044
- **ローカル通話**: 499 922 8623
- **オンライン サポート**: Dynamics サポート ポータルを介して [クエリを送信する](https://dynamics.microsoft.com/support/)

### <a name="power-platform"></a>Power Platform

- **フリーダイヤル**: 8 10 800 2548 1044
- **ローカル通話**: 499 922 8623
- **オンライン サポート**: Power Platform サポート経由で [クエリを送信する](/power-platform/admin/get-help-support)

> [!NOTE]
> <sup>1</sup> 連邦法 No. 242-FZ (エディション 12.31.2014 年版) '07.21.2014 年の日付の「情報および通信ネットワークにおける個人データ処理の手順の明確化に関するロシア連邦の特定の立法行為への修正の入力について」 <br>
> <sup>2</sup> 連邦法 No. 07.27 の個人データに関する 152-FZ。 2006<br>
