---
title: Federal Risk and Authorization Management Program (FedRAMP)
description: Microsoft は、米国連邦リスクおよび承認管理プログラム P-ATOs と ATOs を付与されました。
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
ms.openlocfilehash: b8835b605ef41336828acbf2f60da71b9f8ac641
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496502"
---
# <a name="federal-risk-and-authorization-management-program-fedramp"></a>Federal Risk and Authorization Management Program (FedRAMP)

## <a name="fedramp-overview"></a>FedRAMP の概要

米国連邦リスク承認管理プログラム (FedRAMP) は、連邦情報セキュリティ管理法 (FISMA) に基づくクラウド コンピューティング製品およびサービスの評価、監視、承認のための標準化されたアプローチを提供し、連邦政府機関によるセキュリティで保護されたクラウド ソリューションの導入を加速するために設立されました。

管理Office予算の管理に関して、すべての連邦政府機関が FedRAMP を使用してクラウド サービスのセキュリティを検証する必要があります。 (他の機関でも採用されていますので、公的機関の他の分野でも役立ちます。国立標準技術研究所 (NIST) SP 800-53 は、必須の標準を設定し、情報システムのセキュリティ カテゴリ (機密性、整合性、可用性) を確立し、情報システムと情報システムが侵害された場合に組織に及ぼす潜在的な影響を評価します。 FedRAMP は、クラウド サービス プロバイダー (CSP) がこれらの標準を満たしているという認定を行うプログラムです。

連邦政府機関にサービスを販売する必要がある AP は、FedRAMP コンプライアンスを実証するために 3 つの道を歩む可能性があります。

- 共同承認委員会 (JAB) から運用する暫定権限 (P-ATO) を取得します。 JAB は、FedRAMP の主要なガバナンスと意思決定の組織です。 国防総省、ホームランドセキュリティ省、および一般サービス管理局の代表者が役員を務めた。 このボードは、FedRAMP コンプライアンスを実証した P-ATO を CSP に付与します。
- 連邦政府機関から運用機関 (ATO) を受け取る。
- または、プログラム要件を満たす CSP 提供パッケージの開発に個別に取り組みます。

これらの各パスには、FedRAMP Program Management Office (PMO) による厳格な技術的レビューと、プログラムによって認定された独立したサードパーティ組織による評価が必要です。

FedRAMP 認証は、NIST ガイドライン (低、中、高) に基づいて 3 つの影響レベルで付与されます。 これらのレベルは、機密性、整合性、または可用性の喪失が組織に与える影響をランク付けします 。低 (限定的な効果)、中程度 (重大な悪影響)、および高 (重大または致命的な影響)。

## <a name="microsoft-and-fedramp"></a>Microsoft と FedRAMP

Azure Government、Dynamics 365 Government、Office 365 米国政府を含む Microsoft の政府機関クラウド サービスは、米国連邦リスク承認管理プログラム (FedRAMP) の厳しい要件を満たしています。

Microsoft Government クラウド サービスは、公的部門のお客様に、FedRAMP に準拠した豊富なサービスと [、FedRAMP High](https://aka.ms/fedrampblueprint)ブループリントを含む堅牢なガイダンスと実装ツールを提供し、FedRAMP High コントロールを実装する必要がある Azure が展開するアーキテクチャのコア セットを展開するのに役立ちます。

## <a name="microsoft-azure-p-atos"></a>Microsoft Azure P-ATOs

Azure と Azure Government は、FedRAMP 認定の最高のバーである共同承認委員会から、高い影響レベルで P-ATO を取得し、Azure と Azure Government を使用して機密性の高いデータを処理することを承認しています。

Azure と Azure Government の FedRAMP 監査には、インスコープ サービスのインフラストラクチャ、開発、運用、管理、サポートを含む情報セキュリティ管理システムが含まれていました。 P-ATO が付与された後でも、CSP は、使用する政府機関からの承認 (ATO) を必要とします。 Azure の場合、政府機関は Azure P-ATO を独自のセキュリティ承認プロセスで使用し、FedRAMP 要件も満たす機関 ATO を発行する基礎として使用できます。

Azure は、FedRAMP High Impact レベルで他のクラウド プロバイダーよりも多くのサービスを引き続きサポートしています。 また、Azure パブリック クラウドの FedRAMP High は多くの米国政府機関のお客様のニーズを満たしますが、より厳しい要件を持つ機関は引き続き Azure Government に依存し、人員のスクリーニングの強化などの追加のセーフガードを提供します。 Microsoft は [、Azure](/azure/azure-government/compliance/azure-services-in-fedramp-auditscope#azure-public-services-by-audit-scope) Government で現在利用可能なすべての Azure パブリック サービスと FedRAMP High 境界、および現在の年に計画されているサービスを一覧表示します。

## <a name="microsoft-dynamics-365-us-government-ato"></a>Microsoft Dynamics 365 米国政府機関 ATO

Dynamics 365 米国政府は、米国住宅都市開発省 (HUD) によって高い影響レベルで FedRAMP Agency ATO を付与されました。 認定の範囲は Government Community Cloud に限定されています。Dynamics 365 米国政府機関および企業計画は、同じ厳格な FedRAMP コントロールのセットに従って動作します。

## <a name="microsoft-office-365-and-office-365-us-government-atos"></a>Microsoft Office 365 および Office 365 米国政府機関の ATOs

- Office 365 Office 365 米国政府は米国保健福祉省 (DHHS) の ATO を持っています。
- Office 365 米国政府機関は、米国国防情報システム局 (DISA) の P-ATO を持っています。 365 Office 365 米国政府機関の展開を希望する顧客は、DISA P-ATO を使用して、その受け入れを文書化する機関 ATO を生成できます。
- Office 365 (エンタープライズおよびビジネス プラン) と Office 365 米国政府は、検査官総長の DHHS Office からの中程度の影響レベルで FedRAMP Agency ATO を持っています。 Office 365 米国政府は、この承認を取得した最初のクラウドベースの電子メールおよびコラボレーション サービスでした。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure および Azure Government](https://go.microsoft.com/fwlink/p/?linkid=2095323)
- [Dynamics 365 米国政府機関](https://aka.ms/d365-compliance-list)
- Intune
- [Office 365 および Office 365 米国の管理人](https://go.microsoft.com/fwlink/p/?linkid=2077751)
- Office 365 米国防総省
- Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに組み込まれているサービス)
- Microsoft Defender for Endpoint

> [!NOTE]
> Azure Government 内で Azure Active Directory を使用するには、Azure Government の外部に展開されているコンポーネントを Azure パブリック クラウドで使用する必要があります。

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

Microsoft は、P-ATO および ATO を維持するために、Microsoft のクラウド サービスを再認定する必要があります。 これを行うには、Microsoft はセキュリティ制御を継続的に監視および評価し、サービスのセキュリティがコンプライアンスに準拠している状態を示す必要があります。

- [Microsoft クラウド サービスの FedRAMP 認証</span>](https://marketplace.fedramp.gov/#/product/azure-government?sort=productName&productNameSearch=azure)
- [Microsoft FedRAMP 監査レポート</span>](https://aka.ms/MicrosoftFedRAMPAuditDocuments)  

他の FedRAMP レポートを受信するには、Azure Federal Documentation に [メールを送信します](mailto:AzFedDoc@microsoft.com)。

## <a name="quickly-deploy-your-fedramp-solutions-on-azure-government"></a>Azure Government に FedRAMP ソリューションをすばやく展開する

Microsoft では、ATO プロセスをガイドし、FedRAMP High ブループリントを使用して FedRAMP ソリューションをすばやく展開し、FedRAMP High コントロールを実装する必要がある Azure 展開アーキテクチャのコア セットを実装するのに役立ちます。

[Azure FedRAMP High Blueprint の使用を開始する](https://aka.ms/fedrampblueprint)

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**Microsoft クラウド サービスは、連邦情報セキュリティ管理法 (FISMA) に準拠していますか?**

FISMA は、米国の連邦政府機関とそのパートナーが FISMA 要件に準拠している組織からのみ情報システムとサービスを調達する必要がある連邦法です。 FISMA 準拠を示すほとんどの機関とそのベンダーは、特別文書 800-53 rev 4 の NIST によって識別されるコントロールを満たす方法を参照しています。 FISMA プロセス (ただし、基になる標準自体ではない) は、2011 年に FedRAMP に置き換えられた。

**FedRAMP は誰に適用されますか?**

「FedRAMP は、低リスクおよび中程度のリスク影響レベルで連邦政府機関のクラウド展開とサービス モデルに必須です。 CSP に参加する連邦政府機関は、FedRAMP の仕様を満たす必要があります。 さらに、連邦政府が使用する製品やサービスにクラウド テクノロジを採用している企業は、ATO を取得する必要があります。

**代理店が独自のコンプライアンス作業を開始する場所**

FedRAMP を正常にナビゲートし、その要件を満たすために連邦政府機関が実行する必要がある手順の概要については [、「Get Authorized: Agency Authorization」を参照してください](https://www.fedramp.gov/agency-authorization/)。

**代理店の承認プロセスで Microsoft コンプライアンスを使用できますか?**

はい。 Microsoft クラウド サービスの認定を、連邦政府機関からの ATO を必要とするプログラムまたはイニシアチブの基礎として使用できます。 ただし、これらのサービス外のコンポーネントに対して独自の承認を行う必要があります。

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

## <a name="resources"></a>リソース

- [連邦リスクと承認管理プログラム](https://www.fedramp.gov/)
- [FedRAMP セキュリティ評価フレームワーク](https://www.fedramp.gov/assets/resources/documents/FedRAMP_Security_Assessment_Framework.pdf)
- [Microsoft でのクラウドでのコンプライアンスの管理](https://www.microsoft.com/trustcenter/common-controls-hub)
- [Microsoft Government クラウド](https://go.microsoft.com/fwlink/p/?linkid=2087246)
- [Azure コンプライアンス オファリング](https://aka.ms/azurecompliance)
