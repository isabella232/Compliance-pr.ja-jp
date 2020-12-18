---
title: NIST SP 800-171
description: Microsoft クラウド サービスは NIST SP 800-171 のガイドラインに準拠して、非Federal information systems の未分類の制御された情報 (CUI) を保護します。
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
ms.openlocfilehash: 51a09772498da0ffc4c7d135e8b9ae103364a984
ms.sourcegitcommit: 9d00734702fec0e76f6b001e31ff0a6eb60cae6f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/18/2020
ms.locfileid: "49712085"
---
# <a name="nist-sp-800-171"></a>NIST SP 800-171

## <a name="about-nist-sp-800-171"></a>NIST SP 800-171 について

米国標準技術協会 (NIST) は、連邦機関の情報および情報システムを保護するための測定基準とガイドラインを推進および維持しています。 管理下にある未分類情報 (CUI) の管理に関する Executive Order 13556 に対して [、NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final) *、非* 分類情報システムおよび組織の制御された未分類情報の保護を公開しました。 CUI は、デジタルと物理の両方の情報として定義され、政府 (またはその代わりにエンティティ) によって作成され、分類されていない場合でも機密性が高く、保護が必要です。

NIST SP 800-171 はもともと 2015 年 6 月に公開され、その後、進化するサイバー脅威に対応して何度か更新されています。 また、非Federal information systems and organizations に CUI を安全にアクセス、送信、および保存する方法に関するガイドラインを示します。その要件は、主に次の 4 つのカテゴリに分類されます。

- 管理と保護のためのコントロールとプロセス
- IT システムの監視と管理
- エンド ユーザーの明確なプラクティスと手順
- 技術的および物理的なセキュリティ対策の実装

## <a name="microsoft-and-nist-sp-800-171"></a>Microsoft および NIST SP 800-171

認定された第三者評価機関である、Microsoft と協力して、範囲内のクラウド サービスが CUI の処理時に NIST SP 800-171 の *CUI (Nonfederal Information Systems and Organizations の* 制御対象未分類情報 (CUI) を保護する) の条件を満たしているか証明しました。 [FedRAMP](offering-fedramp.md)要件の Microsoft 実装は、Microsoft の対象クラウド サービスが、既に実施されているシステムとプラクティスを使用して、NIST SP 800-171 の要件を満たすか、それを超過していることを確認するのに役立ちます。

NIST SP 800-171 の要件は、FedRAMP が使用する標準である NIST SP 800-53 のサブセットです。 NIST SP 800-171 の付録 D では、CUI のセキュリティ要件と、範囲内のクラウド サービスが FedRAMP プログラムで既に評価および承認されている NIST SP 800-53 の関連するセキュリティ コントロールに直接対応しています。

米国政府機関の CUI を処理または保存するエンティティ (調査機関、コンサルティング会社、製造請負業者) は、NIST SP 800-171 の厳しい要件に準拠する必要があります。 この構成証明は、Microsoft が完全に準拠しているという保証を得て、CUI ワークロードの展開を探しているお客様に Microsoft の対象クラウド サービスが対応できるという意味です。 たとえば、情報システム内の対象となる Microsoft クラウド サービスを使用して「対象となる防御情報」を処理、保存、または送信する DoD 請負業者はすべて、NIST SP 800-171 のセキュリティ要件に準拠する必要がある米国国防総省 DFARS 条項を満たしています。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure Government](https://aka.ms/AzureCompliance)
- [Azure Commercial](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/)
- [Dynamics 365 U.S. Government](https://aka.ms/d365-compliance-list)
- Intune
- [Office 365 米国政府機関コミュニティ クラウド (GCC)、Office 365 GCC High、DoD](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

- [Azure Government Attestation of Compliance with NIST SP 800-171](https://aka.ms/Azure-NIST-800-171)

## <a name="how-to-implement"></a>実装方法

- [Azure Blueprint のサンプル](https://docs.microsoft.com/azure/governance/blueprints/samples/): NIST ベースのコントロールに準拠するワークロードの実装のサポートを受け取る。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**組織で NIST SP 800-171 に準拠している Microsoft を使用できますか?**

はい。 Microsoft のお客様は、FedRAMP 標準に関する独立した第三者評価組織 (3PAO) からのレポートに記載されている監査されるコントロールを、FedRAMP および NIST リスク分析および資格認定作業の一環として使用できます。 これらのレポートは、Microsoft が範囲内のクラウド サービスに実装したコントロールの有効性を証明します。 お客様は、CUI ワークロードが NIST SP 800-171 ガイドラインに準拠している必要があります。

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager) は、[Microsoft 365 コンプライアンス センター](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center) の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンス マネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンス マネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンス マネージャーで評価をする方法](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments) について説明します。

## <a name="resources"></a>リソース

- [Microsoft DoD 認定は NIST 800-171 の要件を満たしています](offering-DoD-DISA-L2-L4-L5.md)
- [NIST 800-171 コンプライアンスの開始とサイバーセキュリティ に関するドキュメント](https://www.nist800171.com/)
- [Microsoft Cloud Services FedRAMP の承認](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [NIST 800-171 3.3 監査とアOffice 365 GCC High](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [Microsoft と NIST サイバーセキュリティ フレームワーク](offering-nist-csf.md)
- [Microsoft Government クラウド](https://www.microsoft.com/enterprise/government)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
