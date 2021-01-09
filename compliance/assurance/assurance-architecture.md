---
title: アーキテクチャの概要
description: Microsoft 365 のアーキテクチャについて
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
ms.openlocfilehash: e1b4e9701e76c1e758f683750c8ebfeda2bc1f1f
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787491"
---
# <a name="architecture-overview"></a>アーキテクチャの概要

## <a name="what-is-microsoft-365"></a>Microsoft 365 とは

Microsoft 365 は、クラウドベースのサブスクリプション ベースバージョンの Office、Windows 10、Enterprise Mobility + Security、および Compliance です。 Microsoft 365 のお客様は、Outlook や Windows などのクライアントを利用できます。また、Exchange Online、Microsoft Teams、SharePoint Online など、Microsoft が代わりにホストするサービスも利用できます。 サービスのすべてのコンポーネントは、サブスクリプション モデルの一部として定期的に更新され、お客様に "常緑" 製品が提供されます。 Microsoft は、お客様の代わりにサービス インフラストラクチャを管理します。つまり、Microsoft は顧客データを格納するインフラストラクチャをセキュリティで保護する責任を負います。

規模に関して、現在、Microsoft 365 サービスを提供するために 100 万台近くのコンピューターを使用しています。 これらのサービスを活用するインフラストラクチャは、Azure、Windows、Linux、マルチテナントおよび専用プラットフォームのサービス固有のハードウェア環境と仮想化環境で大きく異なります。 Microsoft 365 はグローバル企業であり、Microsoft のインフラストラクチャは世界中のデータ センターに分散されており、お客様はデータの常駐および権利に関する要件を満たすことができます。

つまり、サービスは複雑で、驚く規模で実行され、何千人もの Microsoft エンジニアが構築と保守を行う必要があります。 このインフラストラクチャはすべて安全に保つのが最優先です。

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>Microsoft 365 では、どのように顧客テナント間の分離を確保していますか?

Microsoft のクラウド サービスは、すべてのテナントが他のすべてのテナントに対して敵対的である可能性があるという前提に基づいて構築されています。 テナントを適切に分離するために、Microsoft はさまざまな分離テクノロジと制御を実装しています。 これらのコントロールは、テナント間の顧客データへの情報漏洩や不正アクセスから保護し、あるテナントのアクションが別のテナントのサービスに悪影響を及ぼすのを防ぐことを目的として設計されています。

顧客のコンテンツは、Azure Active Directory (Azure AD) を使用して Microsoft 365 テナント内で論理的に分離されています。 Microsoft 365 のユーザー認証は、ユーザー ID を確認するだけでなく、ユーザー アカウントが含まれるテナントの ID も確認します。これにより、ユーザーはテナント環境外のデータにアクセスできなくなります。 Azure AD の論理的な分離を補完するために、お客様のコンテンツは保存中および転送中に常に暗号化されます。 また、個別のサービスでは、別の暗号化されたデータベースでのテナント データの SharePoint Online 分離など、テナント分離の追加のレイヤーを提供することもできます。

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Microsoft 365 では、単一障害点を回避する回復力のあるサービスを設計する方法について説明します。

Microsoft は、信頼性を最大限に高め、障害や通常の運用に対する課題に直面した場合のお客様への悪影響を最小限に抑えるため、クラウド サービスを設計および構築します。 この戦略は、地理的に分散したデータセンターを接続するネットワークの設計から始まります。 Microsoft のネットワーク アーキテクチャには、直接接続と複数のネットワーク パスが含まれています。 Microsoft 365 サービスは、この冗長性を活用して、サービス品質を向上させるために障害を回避するトラフィックを自動的にルーティングします。

サービス レベルでは、Microsoft 365 の回復戦略によってソフトウェアの回復性が優先されます。 可能な限り、サービスはアクティブ/アクティブな構成で展開され、サービスの正常性の監視が自動化され、人の介入なしにサービスが多くの一般的な障害や障害を検出して回復できます。 アクティブ/アクティブ構成に加えて、Microsoft 365 サービスは、サービスが別々の障害ゾーンに展開され、あるゾーンの障害が他のゾーンの可用性に影響を及ぼすのを防ぐことで、フォールト トレランスを向上します。

データの回復性は、Microsoft 365 サービスのデータの整合性と可用性を保護することにより、サービスの回復性を補完します。 サービスでは、ローカルストレージの冗長性と地理的冗長性を使用して、顧客データのコピーを異なる障害ゾーンにレプリケートします。 ある障害ゾーンでデータが破損または失われた場合、可用性を失うことなく別の障害ゾーンでデータにアクセスできます。 自動整合性チェックは、さまざまな種類の物理的または論理的破損の影響を受けたデータを自動的に復元します。 Microsoft 365 では、Exchange Online と SharePoint Online でお客様が誤って削除または変更したデータを復元するためのツールも提供します。

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Microsoft 365 は、どのように依存関係を追跡し、承認されていない外部システム接続を防止しますか?

Microsoft 365 サービス チームは、ビジネス継続性管理の一環として、重要なシステム コンポーネントとその依存関係を特定します。 さらに、Microsoft 365 は、すべての外部システム接続を文書化して追跡し、ネットワーク ファイアウォール構成で承認された接続のみが許可されます。 Microsoft 365 システム、依存関係、および外部接続については、Microsoft 365 の情報セキュリティ アーキテクチャに記載されています。 情報セキュリティ アーキテクチャと対応するデータ フロー図は、少なくとも年に 1 回、およびシステムに大幅な変更が加わるたびにレビューおよび更新されます。

Microsoft 365 アーキテクチャは、クラウド ベースのツールを使用して定期的に自動的に検証され、セキュリティの原則との整合を検証し、分離および復元機能を継続的にテストします。 アーキテクチャ検証は、サービスの現在の状態が目的の状態から離れたインスタンスを自動的に識別し、レビューと軽減のずれにフラグを設定します。 アーキテクチャ検証の目標は、サービス インフラストラクチャのセキュリティ機能が引き続き期待通り機能し続け提供を行うという点です。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 Microsoft 365 のアーキテクチャに関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: 情報フローの適用 <br> CP-9: 情報システムのバックアップ <br> PL-8: 情報セキュリティ アーキテクチャ <br> SC-7: 境界保護 <br> SC-22: アーキテクチャとプロビジョニング | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: 情報セキュリティの組織 <br> A.13.1: ネットワーク セキュリティ管理 <br> A.17.2: 冗長性 | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: 情報セキュリティの組織 <br> A.13.1: ネットワーク セキュリティ管理 | 2020 月 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: テナントの分離 <br> CA-49: バックアップ ポリシー <br> CA-51: データ レプリケーション | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: データ フロー図 <br> CA-37: テナントの分離 <br> CA-49: バックアップ ポリシー <br> CA-51: データ レプリケーション | 2020 年 12 月 24 日 |