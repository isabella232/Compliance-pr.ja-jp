---
title: NIST SP 800-171
description: Microsoft クラウド サービスは NIST SP 800-171 ガイドラインに準拠し、非プラットフォーム情報システムで制御された未分類情報 (CUI) を保護します。
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
ms.openlocfilehash: 19b312d1b9f31683d775049010d390710554df01
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385667"
---
# <a name="nist-sp-800-171"></a>NIST SP 800-171

## <a name="about-nist-sp-800-171"></a>NIST SP 800-171 について

米国国立標準技術研究所 (NIST) は、連邦政府機関の情報および情報システムの保護に役立つ測定基準とガイドラインを推進し、維持しています。 管理された未分類情報 (CUI) の管理に関するエグゼクティブ オーダー 13556 に応答して [、NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final) *、非* 分類情報システムおよび組織で制御された未分類情報の保護を公開しました。 CUI は、デジタルと物理の両方の情報として定義され、政府 (またはその代わりにエンティティ) によって作成され、分類されていないが依然として機密性が高く、保護が必要です。

NIST SP 800-171 は、もともと 2015 年 6 月に公開され、その後、進化するサイバー脅威に対応して何度も更新されています。 CUI に安全にアクセスし、送信し、非公式の情報システムおよび組織に保存する方法に関するガイドラインを提供します。要件は、次の 4 つの主要なカテゴリに分類されます。

- 管理と保護のためのコントロールとプロセス
- IT システムの監視と管理
- エンド ユーザーの明確なプラクティスと手順
- 技術的および物理的なセキュリティ対策の実装

## <a name="microsoft-and-nist-sp-800-171"></a>Microsoft および NIST SP 800-171

認定されたサード パーティの評価組織である Kratos Secureinfo および Coalfire は、Microsoft と提携して、スコープ内クラウド サービスが CUI を処理する際に、非統合情報システムおよび組織の NIST SP 800-171「Protecting Controlled *Unclassified Information (CUI)」* の条件を満たしているのを証明しました。 [FedRAMP](offering-fedramp.md)要件の Microsoft の実装は、Microsoft のスコープ内クラウド サービスが、既に導入されているシステムとプラクティスを使用して NIST SP 800-171 の要件を満たすか、それを超える要件を満たしていることを確認するのに役立ちます。

NIST SP 800-171 の要件は、FedRAMP が使用する標準である NIST SP 800-53 のサブセットです。 NIST SP 800-171 の付録 D は、CUI セキュリティ要件を、FedRAMP プログラムの下で既に評価および承認されている NIST SP 800-53 の関連するセキュリティ制御に直接マッピングします。

米国政府の CUI (研究機関、コンサルティング会社、製造請負業者) を処理または保存するエンティティは、NIST SP 800-171 の厳しい要件に準拠する必要があります。 この構成証明により、Microsoft のスコープ内クラウド サービスは、Microsoft が完全に準拠しているという保証を受け、CUI ワークロードの展開を探しているお客様に対応できます。 たとえば、情報システムでスコープ内の Microsoft クラウド サービスを使用して「対象となる防御情報」を処理、保存、または送信するすべての DoD 請負業者は、NIST SP 800-171 のセキュリティ要件に準拠する必要がある米国国防総省 DFARS 条項を満たしています。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft のスコープ内クラウド プラットフォームと&サービス

- Azure Commercial, Azure Government
- Dynamics 365 米国政府機関
- Intune
- Office 365米国のGovernment Community Cloud (GCC)、Office 365 GCC DoD

## <a name="azure-dynamics-365-and-nist-sp-800-171"></a>Azure、Dynamics 365、NIST SP 800-171

Azure、Dynamics 365、その他のオンライン サービスのコンプライアンスの詳細については [、「Azure NIST SP 800-171](/azure/compliance/offerings/offering-nist-800-171)の提供」を参照してください。

## <a name="office-365-and-nist-sp-800-171"></a>Office 365 NIST SP 800-171

### <a name="office-365-cloud-environments"></a>Office 365クラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365とスコープ内サービス

次の表を使用して、サービスとサブスクリプションOffice 365を決定します。

| **適用対象** | **スコープ内サービス** |
|:------------------|:----------------------|
| **GCC** | アクティビティ フィード サービス、Bing サービス、Delve、Exchange Online、インテリジェント サービス、Microsoft Teams、Office 365 カスタマー ポータル、Office Online、Office サービス インフラストラクチャ、Office 利用状況レポート、OneDrive for Business、People Card、SharePoint Online、Skype for Business、Windows Ink |
| **GCC High** | Activity Feed Service, Bing Services, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, 
SharePointオンライン、Skype for Business、Windows Ink |
| **DoD** | Activity Feed Service, Bing Services, Exchange Online, Intelligent Services, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, Microsoft Teams, SharePoint Online, Skype for Business, Windows Ink |

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**組織で Microsoft コンプライアンスと NIST SP 800-171 を使用できますか?**

はい。 Microsoft のお客様は、FedRAMP 標準に関する独立したサード パーティ評価組織 (3PAO) からのレポートに記載されている監査されたコントロールを、独自の FedRAMP および NIST リスク分析および資格の取り組みの一環として使用できます。 これらのレポートは、Microsoft がスコープ内クラウド サービスに実装したコントロールの有効性を証明します。 お客様は、CUI ワークロードが NIST SP 800-171 ガイドラインに準拠している必要があります。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

### <a name="resources"></a>リソース

- [Microsoft DoD 認定は NIST 800-171 の要件を満たしています](offering-DoD-DISA-L2-L4-L5.md)
- [NIST 800-171 コンプライアンス:サイバーセキュリティ ドキュメントから始まる](https://www.nist800171.com/)
- [Microsoft Cloud Services FedRAMP の承認](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [NIST 800-171 3.3 監査と説明責任とOffice 365 GCC高](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [Microsoft と NIST サイバーセキュリティ フレームワーク](offering-nist-csf.md)
- [Microsoft Government クラウド](https://www.microsoft.com/enterprise/government)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
