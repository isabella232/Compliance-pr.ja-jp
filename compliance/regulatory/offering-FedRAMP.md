---
title: Federal Risk and Authorization Management Program (FedRAMP)
description: Microsoft は、米国連邦リスク/承認管理プログラム P-ATOs および ATOs を付与されました。
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
ms.openlocfilehash: ccfeb35005250b29342e8fc80c1a1b2537a09908
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120326"
---
# <a name="federal-risk-and-authorization-management-program-fedramp"></a>Federal Risk and Authorization Management Program (FedRAMP)

## <a name="fedramp-overview"></a>FedRAMP の概要

米国連邦リスク/承認管理プログラム (FedRAMP) は、連邦情報セキュリティ管理法 (FISMA) に基づいてクラウド コンピューティング製品とサービスを評価、監視、承認するための標準化されたアプローチを提供し、連邦機関によるセキュリティで保護されたクラウド ソリューションの導入を促進するために確立されました。

現在Office管理および予算の管理機関では、すべての連邦政府機関が FedRAMP を使用してクラウド サービスのセキュリティを検証する必要があります。 (他の機関も採用しています。そのため、公的機関の他の分野でも役立ちます)。National Institute of Standards and Technology (NIST) SP 800-53 は、必須の標準を設定し、情報システムのセキュリティ カテゴリ (機密性、整合性、可用性) を確立して、組織の情報および情報システムが侵害された場合の組織への潜在的な影響を評価します。 FedRAMP は、クラウド サービス プロバイダー (CSP) がこれらの基準を満たしたと認定するプログラムです。

連邦機関にサービスを販売する必要がある場合は、FedRAMP コンプライアンスを実証するために次の 3 つの方法を実行できます。

- 共同承認委員会 (JAB) から運用暫定権限 (P-ATO) を獲得します。 JAB は、FedRAMP の主要なガバナンスおよび意思決定の本体です。 国防総省、ホームランド セキュリティ省、および一般サービス管理の代表者が役員を務めた。 このボードは、FedRAMP コンプライアンスを実証した CSP に P-ATO を付与します。
- 連邦機関から運用機関 (ATO) を受け取る。
- または、プログラムの要件を満たす CSP 提供パッケージの開発に個別に取り組みます。

これらの各パスには、FedRAMP Program Management Office (PMO) による厳格な技術的レビューと、プログラムの認定を受けた独立したサード パーティ組織による評価が必要です。

FedRAMP の承認は、NIST ガイドラインに基づいて、低、中、および高の 3 つの影響レベルで付与されます。 これらのレベルは、機密性、整合性、または可用性の喪失が組織に与える可能性がある影響 (低 (限定的な影響)、中程度 (重大な悪影響)、および高 (重大または致命的な影響) をランク付けします。

## <a name="microsoft-and-fedramp"></a>Microsoft と FedRAMP

Azure Government、Dynamics 365 Government、Office 365 U.S. Government を含む Microsoft の政府機関向けクラウド サービスは、米国連邦政府のリスク/承認管理プログラム (FedRAMP) の厳しい要件を満たしています。米国連邦政府機関は、Microsoft Cloud のコスト削減と厳格なセキュリティの恩恵を受けることができます。

Microsoft 政府機関向けクラウド サービスは、公的機関のお客様に、FedRAMP に準拠した豊富なサービスと [、FedRAMP High blueprint](https://aka.ms/fedrampblueprint)などの堅牢なガイダンスと実装ツールを提供します。FedRAMP High の制御を実装する必要がある Azure が展開するアーキテクチャのコア セットを展開するのに役立ちます。

## <a name="microsoft-azure-p-atos"></a>Microsoft Azure P-ATOs

Azure および Azure Government は、FedRAMP 認定の最高レベルである共同承認機関から、高影響レベルで P-ATO を獲得しました。この機関は、Azure と Azure Government による機密性の高いデータの処理を承認します。

Azure および Azure Government の FedRAMP 監査には、スコープ内サービスのインフラストラクチャ、開発、運用、管理、サポートを含む情報セキュリティ管理システムが含まれていました。 P-ATO が付与された後も、CSP は、使用している政府機関からの承認 (ATO) を必要とします。 Azure の場合、政府機関は独自のセキュリティ承認プロセスで Azure P-ATO を使用し、FedRAMP 要件も満たす機関 ATO を発行する基盤として Azure P-ATO を利用できます。

Azure は、FedRAMP の影響度の高いレベルで、他のクラウド プロバイダーよりも多くのサービスを引き続きサポートしています。 また、Azure パブリック クラウドの FedRAMP High は多くの米国政府機関のお客様のニーズを満たしますが、より厳しい要件を持つ機関は、引き続き Azure Government に依存しています。これは、人員のスクリーン処理の強化など、追加の保護策を提供します。 Microsoft では [、Azure](/azure/azure-government/compliance/azure-services-in-fedramp-auditscope#azure-public-services-by-audit-scope) Government で現在 FedRAMP High 境界で利用可能なすべての Azure パブリック サービスと、現在の年に予定されているサービスを一覧表示しています。

## <a name="microsoft-dynamics-365-us-government-ato"></a>Microsoft Dynamics 365 U.S. Government ATO

Dynamics 365 U.S. Government は、米国住宅都市開発省 (HUD) によって、高い影響レベルで FedRAMP 機関 ATO を付与されました。 認定の対象範囲は Government Community Cloud に限定されます。Dynamics 365 U.S. Government のビジネスおよびエンタープライズ プランは、同じ厳格な FedRAMP コントロールのセットに従って動作します。

## <a name="microsoft-office-365-and-office-365-us-government-atos"></a>Microsoft Office 365 および Office 365 U.S. Government ATOs

- Office 365 および Office 365 U.S. Government には、米国保健省 (DHHS) の ATO があります。
- Office 365 U.S. Government Defense には、米国国防情報システム局 (DISA) の P-ATO があります。 Office 365 U.S. Government Defense を展開する場合は、DISA P-ATO を使用して、その承認を文書化する機関 ATO を生成できます。
- Office 365 (エンタープライズおよびビジネス プラン) および Office 365 U.S. Government には、インスペクター全般のDHHS Office からの中程度の影響レベルの FedRAMP 機関 ATO があります。 Office 365 米国政府機関は、この承認を得た最初のクラウドベースの電子メールおよびコラボレーション サービスでした。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure および Azure Government](https://go.microsoft.com/fwlink/p/?linkid=2095323)
- [Dynamics 365 U.S. Government](https://aka.ms/d365-compliance-list)
- Intune
- [Office 365 および Office 365 U.S. Governmen](https://go.microsoft.com/fwlink/p/?linkid=2077751)
- Office 365 米国防総省
- Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに組み込まれているサービス)
- Microsoft Defender ATP

> [!NOTE]
> Azure Government 内で Azure Active Directory を使用するには、Azure Government の外部に Azure パブリック クラウドに展開されているコンポーネントを使用する必要があります。

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

Microsoft は、P-ATO および ATO を維持するために、Microsoft のクラウド サービスを再認定する必要があります。 これを行うには、Microsoft は継続的にセキュリティコントロールを監視および評価し、サービスのセキュリティがコンプライアンスを維持する必要があります。

- [Microsoft クラウド サービス FedRAMP の承認</span>](https://marketplace.fedramp.gov/#/product/azure-government?sort=productName&productNameSearch=azure)
- [Microsoft FedRAMP 監査レポート</span>](https://aka.ms/MicrosoftFedRAMPAuditDocuments)  

他の FedRAMP レポートを受信するには、Azure Federal Documentation に [メールを送信します](mailto:AzFedDoc@microsoft.com)。

## <a name="quickly-deploy-your-fedramp-solutions-on-azure-government"></a>FedRAMP ソリューションを Azure Government に迅速に展開する

Microsoft では、ATO プロセスをガイドし、FedRAMP High blueprint を使用して FedRAMP ソリューションをすばやく展開できます。このブループリントは、FedRAMP High コントロールを実装する必要がある Azure が展開するアーキテクチャに対するポリシーのコア セットを実装するのに役立ちます。

[Azure FedRAMP High Blueprint の使用を開始する](https://aka.ms/fedrampblueprint)

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**Microsoft クラウド サービスは連邦情報セキュリティ管理法 (FISMA) に準拠していますか?**

FISMA は連邦法であり、米国連邦機関とそのパートナーは、FISMA の要件を満たす組織からのみ情報システムとサービスを調達する必要があります。 FISMA 準拠を示すほとんどの機関とそのベンダーは、NIST が Special Publication 800-53 rev 4 で識別するコントロールを満たす方法を指しています。 FISMA プロセス (ただし、基礎となる標準自体) は、2011 年に FedRAMP に置き換えられた。

**FedRAMP は誰に適用されますか?**

「FedRAMP は、低および中程度のリスク影響レベルでの連邦機関のクラウド展開とサービス モデルに必須です。」 CSP を利用する連邦政府機関は、FedRAMP の仕様を満たす必要があります。 さらに、連邦政府が使用する製品やサービスでクラウド テクノロジを採用している企業は、ATO を取得する必要があります。

**私のエージェンシーは、どこに独自のコンプライアンス活動を開始しますか?**

FedRAMP を正常にナビゲートし、その要件を満たすために連邦機関が実行する必要がある手順の概要については、「承認を取得 [する: 機関](https://www.fedramp.gov/agency-authorization/)の承認」にアクセスしてください。

**Microsoft コンプライアンスを私の機関の承認プロセスで使用できますか?**

はい。 Microsoft クラウド サービスの認定は、連邦政府機関からの ATO を必要とするプログラムまたはイニシアチブの基盤として使用できます。 ただし、これらのサービス外のコンポーネントに対して独自の承認を行う必要があります。

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

## <a name="resources"></a>リソース

- [連邦リスク/承認管理プログラム](https://www.fedramp.gov/)
- [FedRAMP セキュリティ評価フレームワーク](https://www.fedramp.gov/assets/resources/documents/FedRAMP_Security_Assessment_Framework.pdf)
- [Microsoft でのクラウドでのコンプライアンスの管理](https://www.microsoft.com/trustcenter/common-controls-hub)
- [Microsoft Government クラウド](https://go.microsoft.com/fwlink/p/?linkid=2087246)
- [Azure Compliance Offerings](https://aka.ms/azurecompliance)
