---
title: 米国内歳入サービス発行 1075
description: Microsoft には、米国内歳入サービス文書 1075 の要件を満たすコントロールがあります。
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
ms.openlocfilehash: 94e032efec2fd10f1d352f4f1b610916abe23cf7
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160647"
---
# <a name="us-internal-revenue-service-publication-1075"></a>米国内歳入サービス発行 1075

## <a name="us-internal-revenue-service-publication-1075-overview"></a>米国内歳入サービス発行 1075 の概要

Internal Revenue Service Publication 1075 (IRS 1075) は、連邦税情報 (FTI) にアクセスする米国政府機関とその代理人が、その機密性を保護するためにポリシー、プラクティス、およびコントロールを使用するためのガイダンスを提供します。 IRS 1075 は、外部政府機関が保有する FTI の損失、侵害、または誤用のリスクを最小限に抑えるためです。 たとえば、住民の納税申告書で FTI を処理する国税局、または FTI にアクセスする保健サービス機関は、その情報を保護するためのプログラムを用意している必要があります。  
  
FTI を保護するために、IRS 1075 では、アプリケーション、プラットフォーム、データセンター サービスのセキュリティとプライバシーの制御が規定されています。 たとえば、FTI の適切な処理、データ センターの請負業者の監視など、データセンター アクティビティのセキュリティを優先して、エントリを制限します。 FTI を受け取る政府機関がこれらの管理を確実に適用するために、IRS は、これらの機関とその請負業者の定期的なレビューを含むセーフガード プログラムを確立しました。

## <a name="microsoft-and-us-internal-revenue-service-publication-1075"></a>Microsoft and US Internal Revenue Service Publication 1075

Microsoft Azure政府機関Microsoft Office 365[](https://products.office.com/government/office-365-web-services-for-government)米国政府機関向けクラウド サービスは、適切な管理を行う契約上のコミットメントと、Microsoft 代理店のお客様が IRS 1075 の実質的な要件を満たすために必要なセキュリティ機能を提供します。  
  
政府機関向けこれらの Microsoft クラウド サービスは、お客様がソリューションを構築および運用できるプラットフォームを提供しますが、お客様は、これらの特定のソリューションが IRS 1075 に従って運用され、したがって IRS 監査の対象となるかどうかを判断する必要があります。  
  
政府機関がコンプライアンスの取り組みを支援するために、Microsoft は次の作業を行います。

- 政府機関が自分の責任を理解し、さまざまな IRS コントロールが Azure Government および米国政府機関の機能にマップOffice 365ガイダンスを提供します。 IRS 1075 セーフガード セキュリティ レポート (SSR) は、Microsoft サービス が適用可能な IRS コントロールを実装する方法を徹底的に文書化し、Azure Government および Office 365 米国政府機関の FedRAMP パッケージに基づいて作成されます。 IRS 1075 と FedRAMP の両方が NIST 800-53 に基づくため、IRS 1075 のコンプライアンス境界は FedRAMP 認証と同じです。
- IRS は、すべての IRS セーフガード ドキュメントのリリースを明示的に承認する必要があります。そのため、NDA の下の政府機関のお客様だけが SSR を確認できます。
- クラウド サービスの独立した評価者が作成した監査レポートと監視情報を利用できます。
- IRS Azure Government コンプライアンスに関する考慮事項と Office 365 米国政府機関のコンプライアンスに関する考慮事項について説明します。これは、IRS 1075 に準拠する方法で政府機関が Microsoft Cloud for Government サービスを使用する方法を概説します。 NDA の下の政府機関のお客様は、これらのドキュメントを要求できます。
- 必要に応じて、お客様に Microsoft の件名の専門家または社外の監査人と通信する機会を提供します (費用負担)。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

FedRAMP 認証は、NIST ガイドライン (低、中、高) に基づいて 3 つの影響レベルで付与されます。 これらは、機密性、整合性、または可用性の喪失が組織に与える影響をランク付けします 。低 (限定的な効果)、中程度 (重大な悪影響)、および高 (重大または致命的な影響)。

- Azure および Azure Government
- Dynamics 365 米国政府機関
- Office 365 Office 365米国政府
- Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに組み込まれているサービス)

## <a name="azure-dynamics-365-and-irs-1075"></a>Azure、Dynamics 365、IRS 1075

Azure、Dynamics 365、その他のオンライン サービスコンプライアンスの詳細については [、「Azure IRS 1075](/azure/compliance/offerings/offering-irs-1075)製品」を参照してください。

## <a name="office-365-and-irs-1075"></a>Office 365 IRS 1075

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **GCC** | アクティビティ フィード サービス、Bing サービス、Delve、Exchange Online Protection、Exchange Online、インテリジェント サービス、Microsoft Teams、Office 365 カスタマー ポータル、Office Online、Office サービス インフラストラクチャ、Office 利用状況レポート、OneDrive for Business、People Card、SharePoint Online、Skype for Business、Windows Ink |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365 監査、レポート、証明書

IRS 1075 の実質的な要件への準拠は、毎年 FedRAMP 監査の対象となります。

- [FedRAMP 認証](https://marketplace.fedramp.gov/#/product/azure-government?sort=productName&productNameSearch=azure)

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**Microsoft は IRS 1075 の要件にどう対処しますか?**

Microsoft は、セキュリティ、プライバシー、運用管理、および NIST 800-53 rev を定期的に監視します。中程度の影響情報システムの FedRAMP ベースラインで必要な 4 つのコントロール。 継続的な監視レポートを通じて四半期ごとにこの情報にアクセスできます。 Azure Government および Office 365米国政府機関のお客様は、サービス信頼ポータルを通じてこの機密性の高いコンプライアンス[情報にアクセスできます](https://aka.ms/stphelp)。

さらに、Microsoft は、Azure Government および Office 365 米国政府機関のマスター コントロール セットに IRS 1075 コントロールを含め、毎年監査を行う予定です。

**FedRAMP パッケージまたは System Security Plan を確認できますか?**

はい、組織が Azure Government および米国政府機関の適格性要件を満Office 365場合。 これらのドキュメントを確認するには、Microsoft アカウント担当者に直接お問い合わせください。 また、準拠するクラウド サービス プロバイダーの FedRAMP リストを参照できます。

**Azure またはパブリック クラウド環境Office 365、IRS 1075 に準拠できますか?**

いいえ。 FTI を格納および処理できる環境は、Azure Government または米国政府機関Office 365環境のみです。 政府機関のお客様は、これらの環境を使用する資格要件を満たす必要があります。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

### <a name="resources"></a>リソース

- [IRS 文書 1075](https://www.irs.gov/pub/irs-pdf/p1075.pdf)
- [IRS セーフガード プログラム](https://www.irs.gov/uac/Safeguards-Program)
- [Microsoft Common Controls Hub コンプライアンス フレームワーク](https://www.microsoft.com/trust-center/compliance/compliance-overview)
- [Microsoft Cloud for Government](https://azure.microsoft.com/global-infrastructure/government/)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
