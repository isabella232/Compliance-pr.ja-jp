---
title: Payment Card Industry (PCI) Data Security Standard (DSS)
description: Azure、SharePoint Online、OneDrive for Business は、Payment Card Industry Data Security Standards レベル 1 バージョン 3.2 に準拠します。
keywords: Microsoft 365、コンプライアンス、サービス
localization_priority: Priority
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
ms.openlocfilehash: 753d793d9024e766dcfda84c631744112b677229984226332517b911186b2679
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54294004"
---
# <a name="payment-card-industry-pci-data-security-standard-dss"></a>Payment Card Industry (PCI) Data Security Standard (DSS)

## <a name="pci-dss-overview"></a>PCI DSS の概要

Payment Card Industry (PCI) Data Security Standards (DSS) は、クレジット カードのデータを安全に管理して不正利用を防ぐ目的で策定されたグローバル情報セキュリティ基準です。 クレジット カード主要 5 社 (Visa、MasterCard、American Express、Discover、ジェーシービー (JCB)) によるカード支払いを受け付ける、あらゆる規模の組織が PCI DSS 基準に従う必要があります。 この PCI DSS への準拠は、支払いとカード所有者に関するデータを保存、処理、または転送するすべての組織に求められます。

## <a name="microsoft-and-pci-dss"></a>Microsoft と PCI DSS

Microsoft では、年 1 回、認定 Qualified Security Assessor (QSA) による PCI DSS 評価を実施しています。 監査人は、Microsoft Azure、Microsoft OneDrive for Business、および Microsoft SharePoint Online の環境を確認しました。これには、インフラストラクチャ、開発、運用、管理、サポート、および対象となるサービスの検証が含まれます。 PCI DSS では、取引量に応じて 4 つのレベルのコンプライアンスが指定されています。 Azure、OneDrive for Business および SharePoint Online は、PCI DSS Version 3.2 サービス プロバイダー レベル 1 (年間取引量が最も多く、600 万件を超える) 準拠として認定されています。

評価の結果、お客様が利用できる Attestation of Compliance (AoC) と Report on Compliance (RoC) が QSA によって発行されています。 コンプライアンスの有効期間は、監査に合格して、査定人から AoC を受け取ったときから始まり、その AoC に署名された日付の 1 年後に終了します。 

カード所有者環境またはカード処理サービスを開発しようとしているお客様は、基礎となる多くの部分でこれらの検証を使用できるため、独自の PCI DSS 証明を取得するために費やす労力とコストを削減できます。

Azure、OneDrive for Business、および SharePoint Online の PCI DSS コンプライアンス ステータスが、顧客がプラットフォームで構築またはホストするサービスの PCI DSS 認定を直ちに意味するわけではありません。これを理解しておくことが重要です。 PCI DSS 要件への対応についてはお客様自身が責任を負います。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- Azure および Azure Government
- Intune
- Microsoft Cloud App Security
- [Microsoft Defender for Endpoint](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- Microsoft Graph
- Office 365
- OneDrive for Business および SharePoint Online (米国のみ)
- PowerApps クラウド サービス (スタンドアロン サービス、または Office 365 および Dynamics 365 ブランド プランまたはスイートに搭載されているサービス)
- Power Automate (スタンドアロン サービス、または Office 365 および Dynamics 365 ブランド プランまたはスイートに搭載されているサービス)
- Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに搭載されているサービス)

## <a name="azure-dynamics-365-and-pci-dss"></a>Azure、Dynamics 365、PCI DSS

Azure、Dynamics 365、およびその他のオンライン サービス コンプライアンスの詳細については、[Azure PCI DSS サービス](/azure/compliance/offerings/offering-pci-dss)を参照してください。

## <a name="office-365-and-pci-dss"></a>Office 365 と PCI DSS

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **Office 365** | OneDrive for Business (米国)、SharePoint Online |

### <a name="office-365-audit-reports-and-certificates"></a>Office 365 監査、レポート、証明書

- [OneDrive for Business および SharePoint Online の PCI DSS Attestation of Compliance (AoC)](https://aka.ms/spo-pci)

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**Attestation of Compliance (AoC) の表紙に「2018 年 6 月」と記載されているのはなぜですか?**

この表紙に表示されている「2018 年 6 月」の日付は、AoC のテンプレートが発行された日付です。 評価の日付については、セクション 2 を参照してください。 

**PA DSS と PCI DSS の間にはどのような関係があるのですか?**

Payment Application Data Security Standard (PA DSS) は PCI DSS に準拠する一連の条件で、Visa の Payment Application Best Practices に代わるものであり、他の主要カード発行元のコンプライアンス要件が統合されています。 PA DSS は、カード承認または決済処理の一環として、カード所有者の支払いデータを保存、処理、または転送するサード パーティ アプリケーションを、ソフトウェア ベンダーが開発する際に役立ちます。 PCI DSS コンプライアンスを効率的に実現するには、小売り業者が PA DSS 認定アプリケーションを使用する必要があります。 PA DSS は Azure には適用されません。

**"取得者" とは何ですか? Azure では使用していますか?**

取得者とは、銀行、またはカード支払い取引を処理するその他の当事者です。 Azure がカード支払い処理をサービスとして提供することはないため、取得者を利用することはありません。

**PCI DSS はどのような組織や業者に適用されるのですか?**

PCI DSS は、規模や取引数に関係なく、カード会員データを受信、転送、または保存するすべての企業に適用されます。 つまり、お客様がクレジット カードまたはデビット カードを使用して企業に支払った場合は、必ず PCI DSS 要件が適用されます。 企業は、12 か月間の取引量合計に基づいて 4 つのレベルのいずれかで検証されます。 レベル 1 は年間取引件数が 600 万件を超える企業、レベル 2 は 100 ～ 600 万件、レベル 3 は 2 ～ 100 万件、レベル 4 は 2 万件未満の企業を対象としています。

**OneDrive for Business および SharePoint Online が米国以外で PCI DSS に準拠する計画はありますか?**

現在 OneDrive for Business および SharePoint Online は、米国内でのみ PCI-DSS に準拠しています。 Microsoft は、米国以外の地域が追加された場合は、他の地域の要件や予定を評価し、更新情報を提供します。

**OneDrive for Business および SharePoint Online の対象ついて**

現在のところ、OneDrive for Business および SharePoint Online にアップロードされたファイルとドキュメントのみが PCI DSS に準拠しています。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

### <a name="resources"></a>リソース

- [PCI Security Standards Council](https://www.pcisecuritystandards.org/)
- [PCI データ セキュリティ基準](https://www.pcisecuritystandards.org/documents/PCI_DSS_v3-1.pdf)
- [PCI DSS クイック レファレンス ガイド](https://www.pcisecuritystandards.org/documents/PCISSC%20QRG%20August%202014%20-print.pdf)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
