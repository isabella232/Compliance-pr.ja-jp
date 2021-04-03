---
title: 医療保険の携行性と責任に関する法律と HITECH 法 (Health Insurance Portability and Accountability (HIPAA) & HITECH Acts)
description: Microsoft は、医療保険の携行性と責任に関する法律のビジネス アソシエイト契約 (BAA) を提供しています。
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
ms.openlocfilehash: dbd05b64deb7b74a590a09f81004968e6cf3a84d
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497786"
---
# <a name="health-insurance-portability-and-accountability-hipaa--hitech-acts"></a>医療保険の携行性と責任に関する法律と HITECH 法 (Health Insurance Portability and Accountability (HIPAA) & HITECH Acts)

## <a name="hipaa-and-the-hitech-act-overview"></a>HIPAA と HITECH 法の概要

健康保険の携行性と責任に関する法律 (HIPAA) は、個人を特定できる健康情報の使用、開示、および保護に関する要件を定めた米国の医療法です。 対象となるエンティティ、医師のオフィス、病院、医療保険者、その他の医療会社に適用され、患者の保護された健康情報 (PHI) にアクセスできるだけでなく、クラウド サービスや IT プロバイダーなどのビジネスアソシエイトが、その代わりに PHI を処理します。 (ほとんどの対象事業体は、クレームやデータ処理などの機能を単独では実行しません。それらの機能の実行については、ビジネス関係者に依存しています。)

法律は、4 つの一般的な分野での PHI の使用および普及を規制しています。

- プライバシー。患者の機密性を対象とします。
- セキュリティ。物理的、技術的、および管理面での保護を含む情報の保護を扱います。
- 識別子。これは、調査目的で収集された場合に公開できない情報の種類です。
- 医療関連の取引におけるデータの電子送信のためのコード。適格性および保険金の請求や支払いを含みます。

HIPAA の範囲は、経済的および臨床的健全性のための健康情報技術 (HITECH) 法の制定により拡張されました。HIPAA および HITECH 法のルールには以下が含まれます。

- 個人が各自の個人情報の使用をコントロールする権利に焦点を当てる HIPAA プライバシー ルールは、PHI の機密性を対象とし、その使用と開示を制限します。
- HIPAA セキュリティ ルール。管理面、技術的、および物理的な保護の基準を設定し、電子 PHI を不正なアクセス、使用、および開示から保護します。 また、ビジネス アソシエイト契約 (BAA) などの組織の要件も含まれます。

HITECH 違反の通知に関する最終ルール。セキュリティ保護されていない PHI 違反が発生した場合、個人および政府に通知する必要があります。

## <a name="microsoft-and-hipaa-and-the-hitech-act"></a>Microsoft と HIPAA および HITECH 法

HIPAA の規制では、対象となるエンティティとそのビジネスアソシエイト (この場合、クラウド サービスを含むサービスを含む) を対象エンティティに提供する場合は、それらのビジネスアソシエイトが PHI を適切に保護するために契約を締結する必要があります。 これらの契約 (BAA) は、ビジネス アソシエイトが PHI を処理する方法を明確にし、制限し、HIPAA および HITECH 法に定めるセキュリティおよびプライバシーに関する規定を各当事者が遵守するよう定める。BAA が設定された後、Microsoft のお客様 (対象エンティティ) は、そのサービスを使用して PHI を処理および保存できます。

現在、HIPAA または HITECH 法のコンプライアンスに関する公式の認定資格はありません。 ただし、BAA の対象となるこれらの Microsoft サービスは、Microsoft ISO/IEC 27001 認定の独立監査人によって実施された監査を受けています。

Microsoft エンタープライズ クラウド サービスも FedRAMP 評価の対象です。 Microsoft Azure と Microsoft Azure Government は、FedRAMP 合同認定委員会から規定業務認可を受けました。Microsoft Dynamics 365 U.S. Government は、米国保健福祉省の Microsoft Office 365 U.S. Government と同様に、米国住宅都市開発省からエージェンシー業務認可を受けました。

Microsoft クラウドがお客様の HIPAA および HITECH 要件への準拠をどのように支援するかについては、「[Microsoft のお客様事例](https://customers.microsoft.com)」をご覧ください。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure および Azure Government](https://aka.ms/AzureCompliance)
- Microsoft Cloud App Security
- [Microsoft Cloud for Healthcare](https://aka.ms/MicrosoftCloudforHealthcareCompliance)
- Microsoft Healthcare Bot Service
- [Microsoft マネージド デスクトップ](/microsoft-365/managed-desktop/intro/compliance)
- Microsoft Stream
- Microsoft Professional Services: Azure、Dynamics 365、Intune と、Microsoft 365 for business の Medium Business および Enterprise のお客様への Premier およびオンプレミス サポート
- [Dynamics 365、Dynamics 365 U.S. Government](https://aka.ms/d365-compliance-list)
- Power Automate (旧称 Microsoft Flow) スタンドアロン サービス、または Office 365 や Dynamics 365 ブランド プランあるいはスイートに搭載されているサービスとしてのクラウド サービス
- Intune
- [Office 365、Office 365 U.S. Government、Office 365 U.S. Government Defense](https://go.microsoft.com/fwlink/p/?LinkID=2077751)
- Power Apps クラウド サービス (スタンドアロン サービス、または Office 365 や Dynamics 365 ブランド プランあるいはスイートに搭載されているサービス)
- Power BI クラウド サービス (スタンドアロン サービス、または Office 365 および Dynamics 365 ブランド プランあるいはスイートに組み込まれているサービス)
- Azure DevOps Services

## <a name="accelerate-your-deployment-of-hipaahitrust-solutions-on-azure"></a>Azure での HIPAA/HITRUST ソリューションの展開を加速する

Azure Security and [Compliance Blueprint: HIPAA/HITRUST Health Data](/azure/governance/blueprints/samples/hipaa-hitrust-9-2)and AI を使用して、クラウドのメリットを利用して正常性データ ソリューションを活用しましょう。 このブループリントは、HIPAA/HITRUST ソリューションの構築を今日から始めるためのツールとガイダンスを提供します。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**自分の所属組織は Microsoft と BAA を締結できますか ?**

Microsoft は、対象企業またはそのサプライヤーに、範囲内の Microsoft サービスを対象とする BAA を提供します。

Microsoft クラウド サービスの場合: [HIPAA ビジネス アソシエイト契約](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)は、HIPAA の対象事業体またはビジネス関係者であるすべての顧客が、オンライン サービスの使用条件を介して既定で利用できます。 この BAA の対象となるクラウド サービスの一覧については、この Web ページの「対象となる Microsoft のクラウド サービス」を参照してください。

Microsoft Professional Services サービスの場合: HIPAA ビジネス アソシエイト の修正は、Microsoft サービス担当者への要求に応じて、範囲内のMicrosoft Professional Services で利用できます。

**MICROSOFT に BAA を持つことで、組織が HIPAA および HITECH 法に準拠しているのですか?**

いいえ。 BAA を提供することにより、Microsoft は HIPAA コンプライアンスへの準拠の支援をしますが、Microsoft のサービスを使用するだけでは達成できません。 組織は、適切なコンプライアンス プログラムと内部プロセスを整備し、Microsoft サービスの特定の使用が HIPAA および HITECH 法と整合するように調整する責任があります。

**Microsoft は組織の BAA を変更できますか?**

Microsoft のサービスはすべての顧客に対して一貫しているため、HIPAA BAA を変更することはできません。したがって、すべてのお客様が同じ手順に従っていただく必要があります。 ただし、Microsoft の HIPAA 規制のお客様とそのサービス向け BAA を作成するために、Microsoft は米国の一流の医学部とその HIPAA プライバシー 弁護士、および他の公的および民間部門の HIPAA で覆われたエンティティと協力しました。

**監査人のレポートのコピーを取得する方法**

[Service Trust Portal](https://www.microsoft.com/trustcenter/STP/default.aspx) では、中立的な監査によるコンプライアンス レポートを提供しています。 貴社の監査人が Microsoft のクラウド サービスの監査結果と貴社の法的および規制要件を比較できるようにするために、ポータルで監査レポートをリクエストすることができます。

**HIPAA および HITECH 法への準拠に関する詳細を知るには、どうすればよいですか ?**

このタスクをサポートするために、Microsoft は次のガイドを公開しています。

- [Azure](/azure/governance/blueprints/samples/hipaa-hitrust/) 向けおよび [Dynamics 365 および Office 365](https://go.microsoft.com/fwlink/?LinkID=257510) 向けの *HIPAA/HITECH 法実装ガイダンス*。 プライバシー、セキュリティ、コンプライアンス責任者、および HIPAA および HITECH 法の実装を担当するその他の担当者向けに作成され、コンプライアンスを維持するために組織が実行できる具体的な手順について説明しています。
- 「[Practical guide to designing secure health solutions using Microsoft Azure (Microsoft Azure を使用して安全な健康ソリューションを設計するための実践ガイド)](https://aka.ms/azureindustrysecurity)」は、クラウド サービスを安全な方法で適切に導入するために必要なことをよりよく理解するために役立ちます。
- 「[Microsoft クラウドでの HIPAA セキュリティおよびプライバシー要件への対応](https://smb.blob.core.windows.net/smbproduction/Content/Microsoft_Cloud_Healthcare_HIPAA_Security_Privacy.pdf)」では、規制要件の概要を説明しています。 また、これらの要件に対応する方法論を使用して Microsoft のクラウド サービスがどのように構築されたのかについての詳細な分析と、コンプライアンス対応ソリューションを構築する方法に関するガイダンスも提供します。

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

## <a name="resources"></a>リソース

- [HIPAA オムニバス ルール](https://aka.ms/HIPAA-omnibus) (最終規制を修正する HIPAA ルール)
- [Microsoft Common Controls Hub コンプライアンス フレームワーク](https://www.microsoft.com/trustcenter/common-controls-hub)
- [Microsoft オンライン サービス条件](https://aka.ms/Online-Services-Terms)
- [Microsoft Government クラウド](https://go.microsoft.com/fwlink/p/?linkid=2087246)
- [Azure の HIPAA コンプライアンスについて](https://www.youtube.com/embed/6ptdye1LZ5k?autoplay=0) (2016 年 5 月 19 日)
- [Azure HIPAA HITRUST ブループリント サンプル](/azure/governance/blueprints/samples/hipaa-hitrust/)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
