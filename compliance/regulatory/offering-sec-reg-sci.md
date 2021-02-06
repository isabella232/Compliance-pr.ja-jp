---
title: 証券取引委員会 - 規制システムのコンプライアンスと整合性 (SCI)
description: SCI ルールは、株式やオプションの交換、登録されたクリアリング 機関、代替取引システム (ATS) などの自己規制組織 (SOS) を含む SCI エンティティに適用されます。
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
ms.openlocfilehash: 049f0516598209411b0c5ca47eea39140762fd3d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50119876"
---
# <a name="securities-and-exchange-commission-regulation-systems-compliance-and-integrity-sci"></a>証券取引委員会: 規制システムのコンプライアンスと整合性 (SCI)

## <a name="about-regulation-sci"></a>規制 SCI について

米国証券取引委員会 (SEC) は、米国連邦政府の独立機関であり、米国証券市場の主要監督者および規制当局です。 連邦証券法に対する執行機関を務め、新しい証券規則を提案し、証券業界の市場規制を監督します。

米国証券市場の技術インフラストラクチャを強化するために、2014 年 11 月に、SEC は規制システムのコンプライアンスと整合性 [(SCI) (](https://www.sec.gov/rules/final/2014/34-73639.pdf) および SCI イベントの報告用のフォーム SCI) を採用しました。 この規制は、システム停止の頻度を減らし、そのようなインシデントが発生した場合の回復性を向上し、証券市場技術の SEC 監視と規制の実施を強化するように設計されています。

SCI ルールは、株式やオプションの交換、登録されたクリアリング機関、代替取引システム (ATS) などの自己規制組織 (SOS) を含む SCI エンティティに適用されます。 このルールでは、主に主要な証券市場機能 (取引、株式と受取り、注文ルーティング、市場データ、市場規制、市場の規制) を直接サポートするシステムを規制します。

## <a name="microsoft-and-sec-regulation-sci"></a>Microsoft および SEC 規制 SCI

米国証券取引委員会 (SEC) は、米国証券市場を運営およびサポートする金融機関の技術インフラストラクチャを強化するために、規制 SCI を採用しました。 SEC の監視の下で、その要件は、これらのシステムが高可用性、強力な回復性、および低待機時間 (少しの遅延でメッセージの量が多い) を確保するように設計されています。

この規制に準拠する必要がある米国の金融サービスのお客様を支援するために、Microsoft は [Microsoft Azure SEC Regulation Systems Compliance and Integrity Cloud Implementation Guide を公開しました](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)。 このドキュメント内のガイダンス:

- 強力な回復性、高可用性、低待機時間をサポートする Azure の全体的な機能の概要について説明します。
- Azure が対応するコントロール領域と規制の側面を明確にする。 Azure の機能とサービスと SCI 要件のこのポイント バイ ポイントマッピングは、規制フレームワークに対する Azure コンプライアンスを測定します。 また、オンプレミスでの運用時に完全に所有していたセキュリティの責任を Azure に移行できる場所を理解するのにも役立ちます。 これらの機能は、Microsoft が Azure SLA で行う約束に裏付けされています。
- お客様が対応する責任を負う各規制 SCI 要件を指定し、Azure のドキュメントとサービスを提供して、これらの責任に対処します。

このドキュメントでは、重要な規制 SCI フォーカス領域の詳細なチェックリストを示します。 このチェックリストは、金融機関が、該当する規制要件に準拠できる規制機関、顧客、およびリーダーシップを確保するために Azure を導入する方法を理解するのに役立ちます。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure](https://aka.ms/AzureCompliance)

## <a name="how-to-implement"></a>実装方法

- [規制 SCI 実装ガイド](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers): 規制に対する Azure の機能をマップし、コンプライアンスに関する共有責任の詳細を説明します。
- [信頼性の高い Azure アプリケーションの設計](/azure/architecture/resiliency/): Azure アプリケーション設計の各ステップに信頼性を組み込む方法の簡単な概要。
- [高可用性アプリケーションの設計](/azure/storage/common/storage-designing-ha-apps-with-ragrs): 開発者が Azure Storage アプリケーションを高可用性にするための方法。
- [リスク評価およびコンプライアンス ガイド](https://aka.ms/RiskGovernanceGuide): Microsoft クラウド サービスのリスク評価および規制機関の通知のガバナンス モデルを作成します。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**クラウド テクノロジを使用する場合、共有責任とは何を意味しますか。**

コンピューティング環境がオンプレミスのデータセンターからクラウド内のデータセンターに移行するに伴い、セキュリティの責任も移行します。クラウド サービス プロバイダー (CSP) と顧客は、その責任を共有しています。 すべてのアプリケーションとソリューションについて、その責任のどれだけが顧客に及び、CSP にどれだけ依存するかは、お客様が展開する Azure モデル (IaaS、SaaS、PaaS) によって異なります。 お客様は、必要なセキュリティコントロールの実装にどの程度責任を持つのかを理解する必要があります。 ただし、Microsoft は、お客様がこのような複雑な動的な作業を行うのを支援するガイダンスを提供します。 詳細については、「クラウド コンピューティング [の共有責任」を参照してください](https://gallery.technet.microsoft.com/Shared-Responsibilities-81d0ff91)。

**規制 SCI 要件を満たすために Azure を利用できる金融機関は何ですか?**

この規制の対象となる金融組織または SCI エンティティは、Azure を展開できます。 SEC は、規制が「株式およびオプションの交換、登録されたクリアリング機関、FINRA、MSRB、代替取引システム (ATSS)、NMS と非 NMS 株式を取引する特定のボリュームしきい値を超える取引、統合市場データの販売者 (計画処理者)、および特定の除外クリアリング機関を含む、自己規制組織 (SOS) に適用される」と述べています。

## <a name="resources"></a>リソース

- [規制 SCI に関してよく寄せられる質問に対する SEC の対応](https://www.sec.gov/divisions/marketreg/regulation-sci-faq.shtml)
- [ビジネス継続性と障害復旧 (BCDR): Azure ペアリング地域](/azure/best-practices-availability-paired-regions)
- [クラウド コンピューティングの規制原則とコンプライアンス のMicrosoft Online Services](https://aka.ms/FinServ-Guide-US)
- [Microsoft Cloud Financial Services Compliance Program](https://aka.ms/FSCP-Print)
- [Azure における金融サービス コンプライアンス](https://aka.ms/FinServ-Compliance-Azure)
- [Microsoft Financial Services](https://aka.ms/FinServ-Compliance)
- [Microsoft および SEC 規則 17a-4](offering-SEC-17a-4.md)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
