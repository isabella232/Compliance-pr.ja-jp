---
title: アーキテクチャの概要
description: アーキテクチャの詳細については、Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 97fe615296f03c8f72dbf23d886501988686b53a
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947223"
---
# <a name="architecture-overview"></a>アーキテクチャの概要

## <a name="what-are-microsoft-online-services"></a>Microsoft オンライン サービスとは

Microsoft オンライン サービスは、Azure、Dynamics 365、および Microsoft が提供するクラウドベースのサービスをMicrosoft 365。  各サービスは、一般的なビジネス運用と生産性のニーズに固有のソリューションを提供し、小規模企業から大企業、政府に至るまで、世界中のお客様にサービスを提供します。 Microsoft の独立して管理されたネットワーク インフラストラクチャによって接続されたグローバルに分散されたデータセンターは、オンライン サービスをサポートするバックボーンとして機能し、ほぼすべての状況で可用性を維持し、大規模な世界的な需要に拡大する機能を提供します。

すべての Microsoft オンライン サービスは、管理するサービス インフラストラクチャと顧客のデータを保護する目的が同じですが、各オンライン サービスは個別のビジネス ユニットによって運用されます。 多くの場合、セキュリティ制御は、すべてのサービスで同じ方法で実装されますが、場合によっては、顧客の約束とコンプライアンスの義務を果たすために異なるアプローチを取っています。

## <a name="what-is-azure"></a>Azure とは

Microsoft Azureは、Microsoft およびサード パーティの管理データセンターのグローバル ネットワークを通じてアプリケーションを構築、展開、および管理するためのクラウド コンピューティング プラットフォームです。 サービスとしてのプラットフォーム (PaaS) とサービスとしてのインフラストラクチャ (IaaS) クラウド サービス モデルの両方をサポートし、クラウド サービスを顧客のオンプレミス リソースと統合するハイブリッド ソリューションを実現します。 Microsoft Azure、さまざまな製品やサービス、地域、業界にまたがる多くの顧客、パートナー、政府機関をサポートしています。 Microsoft Azureは、セキュリティ、機密性、およびコンプライアンス要件を満たして設計されています。

## <a name="what-is-dynamics-365"></a>Dynamics 365 とは

Dynamics 365 は、顧客関係管理 (CRM) 機能とその拡張機能を Enterprise リソース計画 (ERP) 機能と統合するオンライン ビジネス アプリケーション スイートです。 これらのエンドツーエンドのビジネス アプリケーションは、顧客が関係を収益に変え、顧客を獲得し、ビジネスの成長を加速するのに役立ちます。 Dynamics 365 は、Azure のインフラストラクチャ上に構築されたサービスとしてのソフトウェア (SaaS) スイートであり、グローバルに分散したデータセンターを通じて世界中のお客様が利用できます。

## <a name="what-is-microsoft-365"></a>Microsoft 365 とは

Microsoft 365は、クラウドベースのサブスクリプション ベースのバージョンの Office、Windows 10、Enterprise Mobility + Security、およびコンプライアンスです。 Microsoft 365顧客は Outlook や Windows などのクライアントを取得し、microsoft が代わりにホストするサービス (Exchange Online、Microsoft Teams、SharePoint Online など) を利用できます。 サービスのすべてのコンポーネントは、サブスクリプション モデルの一部として定期的に更新され、お客様に "常緑" 製品が提供されます。 Microsoft は、お客様に代わってサービス インフラストラクチャを管理します。つまり、Microsoft は顧客データを格納するインフラストラクチャをセキュリティ保護する責任を負います。

規模に関して、Microsoft は現在、100 万台近くのコンピューターを使用して、サービスのMicrosoft 365しています。 これらのサービスに電力を供給するインフラストラクチャは、Azure、Windows、Linux、マルチテナントおよび専用プラットフォームのサービス固有のハードウェア環境と仮想化環境によって大きく異なります。 Microsoft 365 はグローバル企業であり、Microsoft のインフラストラクチャは世界中のデータ センターに分散されており、お客様はデータの常駐および権利に関する要件を満たすことができます。

## <a name="how-do-microsoft-online-services-ensure-isolation-between-customer-tenants"></a>Microsoft オンライン サービスが顧客テナント間の分離を保証する方法

Microsoft のクラウド サービスは、すべてのテナントが他のすべてのテナントに対して敵対的である可能性があるという前提で構築されています。 テナントを適切に分離するために、Microsoft はさまざまな分離テクノロジとコントロールを実装しています。 これらのコントロールは、テナント間の情報漏洩や顧客データへの不正アクセスを防止し、あるテナントのアクションが別のテナントのサービスに悪影響を及ぼすのを防ぐために設計されています。

顧客コンテンツは、テナント内で論理的に分離され、Azure Active Directory (Azure AD) を使用します。 Microsoft Online Services のユーザー認証では、ユーザー ID だけでなく、ユーザー アカウントが含むテナント ID も検証され、ユーザーはテナント環境外のデータにアクセスできません。 Azure コンテンツの論理的な分離をAD、顧客コンテンツは常に保存時および転送中に暗号化されます。 個々のサービスでは、個別の暗号化されたデータベース内のテナント データSharePointのオンライン分離など、テナント分離の層が追加される場合があります。

## <a name="how-do-microsoft-online-services-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Microsoft オンライン サービスは、単一障害点を回避する回復力のあるサービスを設計する方法を説明します。

Microsoft は、信頼性を最大化し、障害や通常の運用に対する課題に直面しているお客様への悪影響を最小限に抑えるために、クラウド サービスを設計および構築します。 この戦略は、地理的に分散したデータセンターを接続するネットワークの設計から始まります。 Microsoft のネットワーク アーキテクチャには、直接相互接続と複数のネットワーク パスが含まれています。 Microsoft オンライン サービスでは、この冗長性を使用して、サービス品質を向上させるために、障害に関するトラフィックを自動的にルーティングします。

可能な限り、Microsoft オンライン サービスは、サービスの正常性監視を自動化したアクティブ/アクティブ構成に展開され、サービスは人間の介入なしに多くの一般的な障害や障害を検出して回復できます。 アクティブ/アクティブ構成に加えて、Microsoft オンライン サービスは、サービスが個別のフォールト ゾーンに展開され、あるゾーンの障害が他のゾーンの可用性に影響を与えなかねない状態でフォールト トレランスを向上します。

データの復元は、Microsoft オンライン サービスのデータの整合性と可用性を保護することで、サービスの回復性を補完します。 弊社のサービスでは、ローカル ストレージの冗長性と地理的冗長性を使用して、顧客データのコピーを異なる障害領域にレプリケートします。 ある障害ゾーンでデータが破損または失われた場合、可用性を失うことなく別の障害ゾーンでデータにアクセスできます。 自動整合性チェックは、さまざまな種類の物理的または論理的な破損の影響を受けたデータを自動的に復元します。 また、Microsoft は、お客様が誤って削除または変更したデータを、オンラインやオンラインなどのサービスで復元Exchange Online提供SharePointしています。

## <a name="how-do-microsoft-online-services-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Microsoft Online Services は、依存関係を追跡し、承認されていない外部システム接続を防止する方法を説明します。

Microsoft オンライン サービス チームは、重要なシステム コンポーネントとその依存関係をビジネス継続性管理の一部として識別します。 さらに、Microsoft は、すべての外部システム接続を文書化して追跡し、ネットワーク ファイアウォール構成で許可された接続のみを許可します。 Microsoft オンライン サービス システム、依存関係、および外部接続は、Microsoft オンライン サービスの情報セキュリティ アーキテクチャに記載されています。 情報セキュリティアーキテクチャと対応するデータ フロー図は、少なくとも年に一度、またシステムに大きな変更が加わるたびに確認および更新されます。

Microsoft Online Services アーキテクチャは、クラウド ベースのツールを使用してセキュリティ原則との整合を検証し、継続的に分離と復元機能をテストするために、定期的に自動的に検証されます。 アーキテクチャ検証は、サービスの現在の状態が目的の状態から逸脱しているインスタンスを自動的に特定し、レビューと軽減のための偏差にフラグを立て動作します。 アーキテクチャの検証の目的は、サービス インフラストラクチャのセキュリティ機能が期待通り機能し続ける必要があります。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 アーキテクチャに関連するコントロールの検証については、次の表を参照してください。

### <a name="azure-and-dynamics-365"></a>Azure と Dynamics 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: 情報セキュリティの組織 <br> A.13.1: ネットワーク セキュリティ管理 <br> A.17.2: 冗長性 | 2020 年 12 月 2 日 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: 情報セキュリティの組織 <br> A.13.1: ネットワーク セキュリティ管理 <br> A.17.2: 冗長性 | 2020 年 12 月 2 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | BC-1: ビジネス継続性計画 <br> BC-3: BCDR プロシージャ <br> BC-4: BCDR テスト <br> BC-5: ビジネス継続性リスク評価 <br> BC-6: サードパーティのビジネス継続性 <br> BC-7: データセンターのビジネス継続性の手順 <br> BC-8: データセンターのビジネス継続性テスト <br> BC-9: データセンターの復元性評価 <br>  DS-6: 重要なコンポーネントの冗長性 <br> DS-7: 顧客データのレプリケーション <br> DS-14: 顧客サービスの復元 <br> DS-16: 顧客データの分離 | 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-4: 情報フローの適用 <br> CP-9: 情報システムのバックアップ <br> PL-8: 情報セキュリティ アーキテクチャ <br> SC-7: 境界保護 <br> SC-22: アーキテクチャとプロビジョニング | 2020 年 9 月 24 日 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: 情報セキュリティの組織 <br> A.13.1: ネットワーク セキュリティ管理 <br> A.17.2: 冗長性 | 2021 年 4 月 20 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: テナントの分離 <br> CA-49: バックアップ ポリシー <br> CA-51: データ レプリケーション | 2020 年 12 月 24 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: データ フロー図 <br> CA-37: テナントの分離 <br> CA-49: バックアップ ポリシー <br> CA-51: データ レプリケーション | 2020 年 12 月 24 日 |