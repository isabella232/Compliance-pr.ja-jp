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
ms.openlocfilehash: 7ceceb59d0afcbc72fac9758f3de500082b8b365
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508629"
---
# <a name="architecture-overview"></a>アーキテクチャの概要

## <a name="what-is-microsoft-365"></a>Microsoft 365 とは

Microsoft 365 は、クラウド powered、サブスクリプションベースの Office のバージョン、Windows 10、Enterprise Mobility + Security、コンプライアンスに対応しています。 Microsoft 365 のお客様は、Outlook や Windows などのクライアントを入手できます。また、Exchange Online、Microsoft Teams、SharePoint Online などのユーザーに代わって Microsoft がホストするサービスも利用できます。 サービスのすべてのコンポーネントはサブスクリプションモデルの一部として定期的に更新されるため、お客様は「永続」の製品を利用できます。 Microsoft はお客様の代わりにサービスインフラストラクチャを管理します。つまり、Microsoft は顧客データを格納するインフラストラクチャをセキュリティで保護する責任を負います。

スケールに関しては、現在、100万台のコンピューターを使用して Microsoft 365 サービスに電源を供給しています。 これらのサービスを利用するインフラストラクチャは、サービス固有のハードウェアおよび Azure、Windows および Linux の仮想化された環境、マルチテナントおよび専用のプラットフォームに大きく異なります。 Microsoft 365 はグローバル企業であり、Microsoft のインフラストラクチャは世界中のデータ センターに分散されており、お客様はデータの常駐および権利に関する要件を満たすことができます。

要約すると、サービスは複雑で、驚異的な規模で稼働し、多くの Microsoft のエンジニアが構築して管理する必要があります。 このインフラストラクチャをすべて安全に保つための最優先事項です。

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>Microsoft 365 では、顧客テナント間の分離をどのようにしていますか?

Microsoft のクラウドサービスは、すべてのテナントが他のすべてのテナントに敵意を与える可能性があることを前提として構築されています。 テナントを相互に適切に分離するために、Microsoft はさまざまな分離テクノロジと制御を実装しています。 これらのコントロールは、テナント間での情報漏洩または承認されていない顧客データへのアクセスを防止するために設計されており、1つのテナントのアクションが別のテナントのサービスに悪影響を及ぼすことを防ぐためのものです。

お客様のコンテンツは、Microsoft 365 テナント内の Azure Active Directory (Azure AD) を使用して論理的に分離されています。 Microsoft 365 のユーザー認証は、ユーザー ID を確認するだけでなく、ユーザー アカウントが含まれるテナントの ID も確認します。これにより、ユーザーはテナント環境外のデータにアクセスできなくなります。 Azure AD の論理的分離を補足するために、お客様のコンテンツは常に保存され、転送中で暗号化されます。 個別のサービスによって、テナント分離の追加層が提供される場合もあります。たとえば、テナントデータの SharePoint Online 分離が、暗号化された個別のデータベースに分かれています。

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Microsoft 365 は、単一点障害を回避するための復元性の高いサービスを示していますか?

Microsoft は、クラウドサービスを設計および構築して信頼性を最大化し、通常の運用における障害や課題の影響をお客様にもたらす悪影響を最小限に抑えます。 この戦略は、地理的に分散したデータセンターを接続するネットワークの設計から始まります。 Microsoft のネットワークアーキテクチャには、直接 interconnections と複数のネットワークパスが含まれています。 Microsoft 365 サービスでは、この冗長性を活用して、サービス品質を向上するために障害を回避するトラフィックを自動的にルーティングします。

サービスレベルでは、Microsoft 365 の復元戦略によってソフトウェアの復元性が優先されます。 可能な限り、サービスの正常性監視を使用してサービスをアクティブ/アクティブ構成に展開することで、ユーザーの介入なしに多くの一般的な障害やエラーを検出し、回復することができます。 アクティブ/アクティブ構成に加えて、Microsoft 365 サービスは、サービスが別のフォールトゾーンに展開されるようにすることにより、フォールトトレランスが向上し、1つの領域内の障害が他の領域の可用性に影響を与えることを防ぐことができます。

データの回復性は、Microsoft 365 サービスのデータの整合性と可用性を保護することにより、サービスの回復性を補完します。 サービスでは、ローカル記憶域の冗長性と geo 冗長を使用して、顧客データのコピーを別の障害ゾーンにレプリケートします。 ある障害ゾーンでデータが破損または失われた場合、可用性を失うことなく別の障害ゾーンでデータにアクセスできます。 自動整合性チェックは、多くの種類の物理的または論理的な破損によって影響を受けるデータを自動的に復元します。 また、Microsoft 365 は、Exchange Online および SharePoint Online でユーザーが誤って削除または変更したデータを復元するためのツールをお客様に提供します。

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Microsoft 365 は、依存関係を追跡し、許可されていない外部システム接続を防止する方法を教えてください。

Microsoft 365 サービスチームは、重要なシステムコンポーネントとその依存関係をビジネス継続性管理の一部として識別します。 さらに、Microsoft 365 は、ネットワークファイアウォール構成で許可された接続のみが許可されていることを確認するために、すべての外部システム接続を記録し、追跡します。 Microsoft 365 のシステム、依存関係、および外部接続については、「Microsoft 365 の情報セキュリティアーキテクチャ」で説明されています。 情報セキュリティアーキテクチャと、対応するデータフロー図の両方が、少なくとも、システムに大幅な変更が加えられたときに、年単位で確認および更新されます。

Microsoft 365 アーキテクチャは定期的に検証されており、クラウドベースのツールを使用して自動的に自動的に使用し、セキュリティ原則に沿って配置し、分離と復元の機能を継続的にテストしています。 アーキテクチャ検証は、目的の状態からサービスの現在の状態が drifted されているインスタンスを自動的に識別し、レビューと軽減のための逸脱を指摘します。 アーキテクチャ検証の目的は、サービスインフラストラクチャのセキュリティ機能が期待どおりに機能し続けるようにすることです。

## <a name="related-external-regulations--certifications"></a>関連する外部規制 & 証明書

Microsoft のオンラインサービスは、社外の規制と証明書に準拠するために定期的に監査されます。 Microsoft 365 のアーキテクチャに関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: 情報フローの適用 <br> CP-9: 情報システムのバックアップ <br> PL-8: 情報セキュリティアーキテクチャ <br> SC-7: 境界保護 <br> SC-22: アーキテクチャとプロビジョニング | 2020年9月24日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 6: 情報セキュリティの組織 <br> 13.1: ネットワークセキュリティ管理 <br> 17.2: 重複 | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 6: 情報セキュリティの組織 <br> 13.1: ネットワークセキュリティ管理 | 2020 月 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-37: テナントの分離 <br> CA-49: バックアップポリシー <br> CA-51: データレプリケーション | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-05: データフロー図 <br> CA-37: テナントの分離 <br> CA-49: バックアップポリシー <br> CA-51: データレプリケーション | 2019 年 9 月 30 日 |