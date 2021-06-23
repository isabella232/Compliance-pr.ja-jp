---
title: 証券およびExchange委員会 - 規制システムのコンプライアンスと整合性 (SCI)
description: SCI ルールは SCI エンティティに適用されます。このエンティティには、株式およびオプションの交換、登録された清算機関、代替取引システム (ATS) などの自己規制組織 (SOS) が含まれます。
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
ms.openlocfilehash: 06537749b60f40ab87211aa6efa65e8e88ed691b
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087536"
---
# <a name="securities-and-exchange-commission-regulation-systems-compliance-and-integrity-sci"></a>証券およびExchange委員会: 規制システムのコンプライアンスと整合性 (SCI)

## <a name="about-regulation-sci"></a>規制 SCI について

米国証券Exchange委員会 (SEC) は、米国連邦政府の独立機関であり、米国証券市場の主要な監督および規制当局です。 これは、連邦証券法に対する執行機関を制御し、新しい証券ルールを提案し、証券業界の市場規制を監督します。

2014 年 11 月、SEC は米国証券市場のテクノロジ インフラストラクチャを強化するために、規制システムコンプライアンスと整合性 [(SCI) (](https://www.sec.gov/rules/final/2014/34-73639.pdf) および SCI イベント報告用のフォーム SCI) を採用しました。 この規制は、システム停止の頻度を減らし、このようなインシデントが発生した場合の回復力を向上し、証券市場技術と規制の施行に関する SEC の監督を強化するように設計されています。

SCI ルールは SCI エンティティに適用されます。このエンティティには、株式およびオプションの交換、登録された清算機関、代替取引システム (ATS) などの自己規制組織 (SOS) が含まれます。 このルールは、主に主要な証券市場機能を直接サポートするシステム (取引、クリアランスと決済、注文ルーティング、市場データ、市場規制、市場監視) を規制します。

## <a name="microsoft-and-sec-regulation-sci"></a>Microsoft および SEC 規制 SCI

米国証券Exchange委員会 (SEC) は、米国証券市場を運営およびサポートする金融機関の技術インフラストラクチャを強化するために規制 SCI を採用しました。 SEC の監視の下で、その要件は、これらのシステムが高可用性、強力な復元性、低遅延 (遅延の少ないメッセージの量が多い) を確保するように設計されています。

この規制に準拠する必要がある米国の金融サービスのお客様を案内するために、Microsoft は sec Regulation Systems Compliance and Integrity Cloud Implementation Guide Microsoft Azure[を公開しました](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)。 このドキュメント内のガイダンス:

- 強力な復元性、高可用性、低遅延をサポートする Azure の全体的な機能の概要を示します。
- Azure が対応する制御領域と規制の側面を明確にします。 Azure の機能とサービスと SCI 要件のこのポイント バイ ポイント マッピングは、規制フレームワークに対する Azure コンプライアンスを測定します。 また、オンプレミスでの運用時に完全に所有していたセキュリティ責任を Azure に移行できる場所を理解するのにも役立ちます。 これらの機能は、Microsoft が Azure SLA で行う約束に裏付けされています。
- お客様が対処する責任である各規制 SCI 要件を指定し、これらの責任に対処するための Azure のドキュメントとサービスを提供します。

このドキュメントでは、重要な規制 SCI フォーカス領域の詳細なチェックリストを示します。 このチェックリストは、規制当局、顧客、およびリーダーシップが適用可能な規制要件に準拠していることを保証するために、金融機関が Azure を採用する方法を理解するのに役立ちます。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure](https://aka.ms/AzureCompliance)

## <a name="how-to-implement"></a>実装方法

- [規制 SCI 実装ガイド](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers): 規制マップ Azure の機能について説明し、コンプライアンスに関する共有の責任を詳細に説明します。
- [信頼性の高い Azure アプリケーションの設計](/azure/architecture/resiliency/): Azure アプリケーション設計の各ステップに信頼性を構築する方法の簡単な概要。
- [高可用性アプリケーションを設計](/azure/storage/common/storage-designing-ha-apps-with-ragrs)する: 開発者が、ユーザーのアプリケーションを高可用性Azure Storageする方法。
- [リスク評価およびコンプライアンス ガイド](https://aka.ms/RiskGovernanceGuide): Microsoft クラウド サービスのリスク評価および規制機関の通知のガバナンス モデルを作成します。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**クラウド テクノロジを使用する場合、共有責任とは何を意味しますか?**

コンピューティング環境がオンプレミスのデータセンターからクラウド内のデータセンターに移行するに伴い、セキュリティの責任もクラウド サービス プロバイダー (CSP) と顧客が共有します。 アプリケーションとソリューションごとに、その責任の量が顧客に及び CSP にどれだけ依存するかは、お客様が展開する Azure モデル (IaaS、SaaS、PaaS) によって異なります。 必要なセキュリティ制御の実装に対してどの程度責任を果たされるかを理解する必要があります。 ただし、Microsoft は、お客様がこの複雑な動的な操作を行うのに役立つガイダンスを提供します。 詳細については、「クラウド コンピューティングの [共有責任」を参照してください](https://gallery.technet.microsoft.com/Shared-Responsibilities-81d0ff91)。

**規制 SCI 要件を満たすために Azure を利用できる金融機関**

この規制の対象となる金融機関、または SCI エンティティは、Azure を展開できます。 SECは、その規制は、指定されたボリュームしきい値を超える NMS および非 NMS 株式を取引する「株式とオプションの交換、登録されたクリアリング機関、FINRA、MSRB、代替取引システム (ATSS)、統合市場データの普及者 (プラン プロセッサ)、および特定の除外クリアリング機関を含む、自己規制組織 (SOS) に適用される」と述べています。

## <a name="resources"></a>リソース

- [規制 SCI に関するよく寄せられる質問に対する SEC の応答](https://www.sec.gov/divisions/marketreg/regulation-sci-faq.shtml)
- [ビジネスの継続性と障害復旧 (BCDR): Azure のペアリングされた地域](/azure/best-practices-availability-paired-regions)
- [クラウド コンピューティングの規制原則とコンプライアンスのコンプライアンス マップMicrosoft Online Services](https://aka.ms/FinServ-Guide-US)
- [Microsoft Cloud Financial Services Compliance Program](https://aka.ms/FSCP-Print)
- [Azure における金融サービス コンプライアンス](https://aka.ms/FinServ-Compliance-Azure)
- [Microsoft Financial Services](https://aka.ms/FinServ-Compliance)
- [Microsoft および SEC ルール 17a-4](offering-SEC-17a-4.md)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
