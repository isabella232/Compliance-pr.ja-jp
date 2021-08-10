---
title: Federal Risk and Authorization Management Program (FedRAMP)
description: Microsoft は、米国連邦リスクおよび承認管理プログラム P-ATOs と ATOs を付与されました。
keywords: Microsoft 365、コンプライアンス、オファリング
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
ms.openlocfilehash: f613e35cfcfa6f15946572901cb0c9f3c7a5fa0407a970ccd3b4e19d8efc138a
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292774"
---
# <a name="federal-risk-and-authorization-management-program-fedramp"></a>Federal Risk and Authorization Management Program (FedRAMP)

## <a name="fedramp-overview"></a>FedRAMP の概要

米国連邦リスク承認管理プログラム (FedRAMP) は、連邦情報セキュリティ管理法 (FISMA) に基づくクラウド コンピューティング製品およびサービスの評価、監視、承認のための標準化されたアプローチを提供し、連邦政府機関によるセキュリティで保護されたクラウド ソリューションの導入を加速するために設立されました。

管理Office予算の管理および予算の管理では、すべての連邦政府機関が FedRAMP を使用してクラウド サービスのセキュリティを検証する必要があります。 (他の機関でも採用されていますので、公的機関の他の分野でも役立ちます。国立標準技術研究所 (NIST) SP 800-53 は、必須の標準を設定し、情報システムのセキュリティ カテゴリ (機密性、整合性、可用性) を確立し、情報システムと情報システムが侵害された場合に組織に及ぼす潜在的な影響を評価します。 FedRAMP は、クラウド サービス プロバイダー (CSP) がこれらの標準を満たしているという認定を行うプログラムです。

連邦政府機関にサービスを販売する必要がある AP は、FedRAMP コンプライアンスを実証するために 3 つの道を歩む可能性があります。

- 共同承認委員会 (JAB) から運用する暫定権限 (P-ATO) を取得します。 JAB は、FedRAMP の主要なガバナンスと意思決定の組織です。 国防総省、ホームランドセキュリティ省、および一般サービス管理局の代表者が役員を務めた。 このボードは、FedRAMP コンプライアンスを実証した P-ATO を CSP に付与します。
- 連邦政府機関から運用機関 (ATO) を受け取る。
- または、プログラム要件を満たす CSP 提供パッケージの開発に個別に取り組みます。

これらの各パスには、FedRAMP Program Management Office (PMO) による厳格な技術的レビューと、プログラムによって認定された独立したサードパーティ組織による評価が必要です。

FedRAMP 認証は、NIST ガイドライン (低、中、高) に基づいて 3 つの影響レベルで付与されます。 これらのレベルは、機密性、整合性、または可用性の喪失が組織に与える影響をランク付けします 。低 (限定的な効果)、中程度 (重大な悪影響)、および高 (重大または致命的な影響)。

## <a name="microsoft-and-fedramp"></a>Microsoft と FedRAMP

Azure Government、Dynamics 365 Government、および Office 365 米国政府機関を含む Microsoft の政府機関クラウド サービスは、米国連邦リスクおよび承認管理プログラム (FedRAMP) の厳しい要件を満たしています。

Microsoft Government クラウド サービスは、公的部門のお客様に、FedRAMP に準拠した豊富なサービスと [、FedRAMP High](https://aka.ms/fedrampblueprint)ブループリントを含む堅牢なガイダンスと実装ツールを提供し、FedRAMP High コントロールを実装する必要がある Azure が展開するアーキテクチャのコア セットを展開するのに役立ちます。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- Azure および Azure Government
- [Dynamics 365 米国政府機関](https://aka.ms/d365-compliance-list)
- Intune
- Office 365米国政府、米国Office 365 - 高、米国Office 365国防
- Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに搭載されているサービス)

## <a name="azure-dynamics-365-and-fedramp"></a>Azure、Dynamics 365、および FedRAMP

Azure、Dynamics 365、その他のオンライン サービスのコンプライアンスの詳細については [、「Azure FedRAMP の提供」を参照してください](/azure/compliance/offerings/offering-fedramp)。

## <a name="office-365-and-fedramp"></a>Office 365 FedRAMP

- Office 365およびOffice 365米国政府は米国保健福祉省 (DHHS) の ATO を持っています。
- Office 365米国政府機関は、米国国防情報システム局 (DISA) の P-ATO を持っています。 米国政府機関への展開をOffice 365、DISA P-ATO を使用して機関 ATO を生成し、その受け入れを文書化できます。
- Office 365 (エンタープライズおよびビジネス プラン) および Office 365 米国政府は、検査官の DHHS および Office からの中程度の影響レベルで FedRAMP Agency ATO を持っています。 Office 365米国政府は、この承認を取得した最初のクラウドベースの電子メールとコラボレーション サービスでした。

### <a name="office-365-cloud-environments"></a>Office 365 クラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **GCC** | アクティビティ フィード サービス、Bing サービス、Delve、Exchange Online、Exchange Online Protection、インフラストラクチャ、インテリジェント サービス、Microsoft Teams、Office 365 カスタマー ポータル、Office Online、Office サービス、Office 利用状況レポート、OneDrive for Business、People Card、SharePoint Online、Skype for Business、Windows Ink |
| **GCC High** | アクティビティ フィード サービス、Bing サービス、Exchange Online、Exchange Online Protection、インテリジェント サービス、Microsoft Teams、Office 365 カスタマー ポータル、Office Online、Office サービス インフラストラクチャ、Office 利用状況レポート、OneDrive for Business、People Card、SharePoint Online、Skype for Business、Windows Ink |
| **DoD** | アクティビティ フィード サービス、Bing サービス、Exchange Online Protection、Exchange Online、インテリジェント サービス、Microsoft Teams、Office 365 カスタマー ポータル、Office Online、Office サービス インフラストラクチャ、Office 利用状況レポート、OneDrive for Business、People Card、SharePoint Online、Skype for Business、Windows Ink |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365 監査、レポート、証明書

Microsoft は、P-ATO および ATO を維持するために、Microsoft のクラウド サービスを再認定する必要があります。 これを行うには、Microsoft はセキュリティ制御を継続的に監視および評価し、サービスのセキュリティがコンプライアンスに準拠している状態を示す必要があります。

- [Microsoft FedRAMP 監査レポート](https://aka.ms/MicrosoftFedRAMPAuditDocuments)  

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**Microsoft クラウド サービスは、連邦情報セキュリティ管理法 (FISMA) に準拠していますか?**

FISMA は、米国の連邦政府機関とそのパートナーが FISMA 要件に準拠している組織からのみ情報システムとサービスを調達する必要がある連邦法です。 FISMA 準拠を示すほとんどの機関とそのベンダーは、特別文書 800-53 rev 4 の NIST によって識別されるコントロールを満たす方法を参照しています。 FISMA プロセス (ただし、基になる標準自体ではない) は、2011 年に FedRAMP に置き換えられた。

**FedRAMP は誰に適用されますか?**

「FedRAMP は、低リスクおよび中程度のリスク影響レベルで連邦政府機関のクラウド展開とサービス モデルに必須です。 CSP に参加する連邦政府機関は、FedRAMP の仕様を満たす必要があります。 さらに、連邦政府が使用する製品やサービスにクラウド テクノロジを採用している企業は、ATO を取得する必要があります。

**代理店が独自のコンプライアンス作業を開始する場所**

FedRAMP を正常にナビゲートし、その要件を満たすために連邦政府機関が実行する必要がある手順の概要については [、「Get Authorized: Agency Authorization」を参照してください](https://www.fedramp.gov/agency-authorization/)。

**代理店の承認プロセスで Microsoft コンプライアンスを使用できますか?**

はい。 Microsoft クラウド サービスの認定を、連邦政府機関からの ATO を必要とするプログラムまたはイニシアチブの基礎として使用できます。 ただし、これらのサービス外のコンポーネントに対して独自の承認を行う必要があります。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

### <a name="resources"></a>リソース

- [連邦リスクと承認管理プログラム](https://www.fedramp.gov/)
- [FedRAMP セキュリティ評価フレームワーク](https://www.fedramp.gov/assets/resources/documents/FedRAMP_Security_Assessment_Framework.pdf)
- [Microsoft でのクラウドでのコンプライアンスの管理](https://www.microsoft.com/trustcenter/common-controls-hub)
- [Microsoft Government クラウド](https://go.microsoft.com/fwlink/p/?linkid=2087246)
