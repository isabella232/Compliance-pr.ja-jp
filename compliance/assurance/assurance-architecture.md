---
title: アーキテクチャの概要
description: Microsoft 365 のアーキテクチャの詳細
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 423e90164b3c13c53d45ca98c2e1a981968f23a8
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497692"
---
# <a name="architecture-overview"></a>アーキテクチャの概要

## <a name="what-is-microsoft-365"></a>Microsoft 365 とは

Microsoft 365 は、クラウドベースのサブスクリプション ベースのバージョンの Office、Windows 10、Enterprise Mobility + Security、および Compliance です。 Microsoft 365 のお客様は、Outlook や Windows などのクライアントを取得します。また、Exchange Online、Microsoft Teams、SharePoint Online など、Microsoft が代理でホストするサービスも利用できます。 サービスのすべてのコンポーネントは、サブスクリプション モデルの一部として定期的に更新され、お客様に "常緑" 製品が提供されます。 Microsoft は、お客様に代わってサービス インフラストラクチャを管理します。つまり、Microsoft は顧客データを格納するインフラストラクチャをセキュリティ保護する責任を負います。

規模については、現在、Microsoft 365 サービスに電力を供給するために、100 万台近くのコンピューターを使用しています。 これらのサービスに電力を供給するインフラストラクチャは、Azure、Windows、Linux、マルチテナントおよび専用プラットフォームのサービス固有のハードウェア環境と仮想化環境によって大きく異なります。 Microsoft 365 はグローバル企業であり、Microsoft のインフラストラクチャは世界中のデータ センターに分散されており、お客様はデータの常駐および権利に関する要件を満たすことができます。

つまり、サービスは複雑で、驚くべき規模で実行され、何千人もの Microsoft エンジニアがビルドと保守を行う必要があります。 このインフラストラクチャを安全に保つのが最優先事項です。

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>Microsoft 365 は、どのように顧客テナント間の分離を保証しますか?

Microsoft のクラウド サービスは、すべてのテナントが他のすべてのテナントに対して敵対的である可能性があるという前提で構築されています。 テナントを適切に分離するために、Microsoft はさまざまな分離テクノロジとコントロールを実装します。 これらのコントロールは、テナント間の情報漏洩や顧客データへの不正アクセスを防止し、あるテナントのアクションが別のテナントのサービスに悪影響を及ぼすのを防ぐために設計されています。

顧客コンテンツは、Azure Active Directory (Azure Active Directory)を使用して Microsoft 365 テナント内で論理的にAD。 Microsoft 365 のユーザー認証は、ユーザー ID を確認するだけでなく、ユーザー アカウントが含まれるテナントの ID も確認します。これにより、ユーザーはテナント環境外のデータにアクセスできなくなります。 Azure コンテンツの論理的な分離をAD、顧客コンテンツは常に保存時および転送中に暗号化されます。 また、個別のサービスでは、別の暗号化されたデータベース内のテナント データの SharePoint Online 分離など、テナント分離の層が追加される場合があります。

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Microsoft 365 は、単一障害点を回避する回復力のあるサービスを開発する方法を説明します。

Microsoft は、信頼性を最大化し、障害や通常の運用に対する課題に直面しているお客様への悪影響を最小限に抑えるために、クラウド サービスを設計および構築します。 この戦略は、地理的に分散したデータセンターを接続するネットワークの設計から始まります。 Microsoft のネットワーク アーキテクチャには、直接相互接続と複数のネットワーク パスが含まれています。 Microsoft 365 サービスは、この冗長性を活用して、サービス品質を向上させるために、障害に関するトラフィックを自動的にルーティングします。

サービス レベルでは、Microsoft 365 の復元戦略によって、ソフトウェアの復元性が優先されます。 可能な限り、サービスはアクティブ/アクティブ構成に展開され、サービスの正常性監視が自動化され、サービスは人間の介入なしに多くの一般的な障害や障害を検出して回復できます。 アクティブ/アクティブ構成に加えて、Microsoft 365 サービスは、サービスが個別のフォールト ゾーンに展開され、あるゾーンの障害が他のゾーンの可用性に影響を与えなかねない状態でフォールト トレランスを向上します。

データの回復性は、Microsoft 365 サービスのデータの整合性と可用性を保護することにより、サービスの回復性を補完します。 弊社のサービスでは、ローカル ストレージの冗長性と地理的冗長性を使用して、顧客データのコピーを異なる障害領域にレプリケートします。 ある障害ゾーンでデータが破損または失われた場合、可用性を失うことなく別の障害ゾーンでデータにアクセスできます。 自動整合性チェックは、さまざまな種類の物理的または論理的な破損の影響を受けたデータを自動的に復元します。 また、Microsoft 365 は、Exchange Online および SharePoint Online でユーザーが誤って削除または変更したデータを復元するためのツールを顧客に提供します。

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Microsoft 365 は、どのように依存関係を追跡し、承認されていない外部システム接続を防止しますか?

Microsoft 365 サービス チームは、ビジネス継続性管理の一環として、重要なシステム コンポーネントとその依存関係を識別します。 さらに、Microsoft 365 は、すべての外部システム接続をドキュメントおよび追跡して、ネットワーク ファイアウォール構成で許可された接続のみを許可します。 Microsoft 365 システム、依存関係、および外部接続は、Microsoft 365 の情報セキュリティ アーキテクチャに記載されています。 情報セキュリティアーキテクチャと対応するデータ フロー図は、少なくとも年に一度、またシステムに大きな変更が加わるたびに確認および更新されます。

Microsoft 365 アーキテクチャは、クラウドベースのツールを使用してセキュリティ原則との整合を検証し、分離と復元機能を継続的にテストするために、定期的に自動的に検証されます。 アーキテクチャ検証は、サービスの現在の状態が目的の状態から逸脱しているインスタンスを自動的に特定し、レビューと軽減のための偏差にフラグを立て動作します。 アーキテクチャの検証の目的は、サービス インフラストラクチャのセキュリティ機能が期待通り機能し続ける必要があります。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 Microsoft 365 のアーキテクチャに関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: 情報フローの適用 <br> CP-9: 情報システムのバックアップ <br> PL-8: 情報セキュリティ アーキテクチャ <br> SC-7: 境界保護 <br> SC-22: アーキテクチャとプロビジョニング | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: 情報セキュリティの組織 <br> A.13.1: ネットワーク セキュリティ管理 <br> A.17.2: 冗長性 | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: 情報セキュリティの組織 <br> A.13.1: ネットワーク セキュリティ管理 | 2020 月 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: テナントの分離 <br> CA-49: バックアップ ポリシー <br> CA-51: データ レプリケーション | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: データ フロー図 <br> CA-37: テナントの分離 <br> CA-49: バックアップ ポリシー <br> CA-51: データ レプリケーション | 2020 年 12 月 24 日 |