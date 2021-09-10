---
title: Baseline Informatiebeveiliging Rijksdienst 標準 (BIR 2012)
description: Microsoft クラウド サービスは、オランダの公的機関が BIR 2012 標準に準拠するのを支援します。
keywords: Microsoft 365、コンプライアンス、サービス
ms.localizationpriority: high
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
ms.openlocfilehash: d0f7bd0db5d71c91a163e05e582ad8c227a8aa22
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947821"
---
# <a name="baseline-informatiebeveiliging-rijksdienst-standard-bir-2012"></a>Baseline Informatiebeveiliging Rijksdienst 標準 (BIR 2012)

## <a name="bir-2012-overview"></a>BIR 2012 の概要

オランダの官公庁から業務を受託する組織は、Baseline Informatiebeveiliging Rijksdienst 標準 (BIR 2012) に準拠する必要があります。 
BIR 2012 は、ISO 27001 および ISO 27002 に基づく標準フレームワークを提供します。 Microsoft Azure または Office 365 を使用する場合、これらのクラウド サービスの BIR 2012 統制の一部はマイクロソフトにより、共同責任モデルを踏まえた形で管理されます。 そのため、BIR 2012 に準拠する必要のある組織は、ご利用中の Microsoft の基礎サービスが BIR 2012 に準拠しているか判断する必要があります。

BIR カバレッジ レポートでは、BIR 標準のどの領域が既存の ISO 27001 認証にカバーされているかを解説するガイダンスが提供されています。ISO 27001 認証は、Microsoft クラウド サービスに適用されています。 ISO 27001 でカバーされないその他の BIR 統制の領域に関しては、その他の独立した認証、監査文書、契約に関する陳述書が参照されます。

## <a name="microsoft-and-bir-2012"></a>Microsoft と BIR 2012

Microsoft は BIR 2012 の規制の対象外ですが、政府部門に関連する業務を行うお客様がクラウド サービスをお探しの場合、マイクロソフトの既存の認証を、BIR 2012 への準拠の判断材料としてお使いいただけます。 Azure と Office 365 はさまざまな独立した保証や認証を受けており、そのうちのいくつかは BIR 2012 に深くかかわるものです。

[Microsoft クラウドのダウンロード: Azure および Office 365 BIR-2012 ベースラインのカバレッジ ユーザー ガイド](https://go.microsoft.com/fwlink/p/?linkid=2099461)

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- Azure
- Intune
- Office 365

## <a name="office-365-and-bir-2012"></a>Office 365 と BIR 2012

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **商用** | Azure Information Protection、Bookings、Exchange Online Protection、Exchange Online、Kaizala、Microsoft Analytics、Microsoft Booking、Microsoft Graph、Microsoft Teams、Microsoft To Do for Web、MyAnalytics、Office 365 Cloud App Security、Office 365 グループ、Office 365 ビデオ、Office Delve、OneDrive for Business、Planner、Power Apps、Power Automate、Power BI for Office 365、PowerApps、SharePoint Online、Skype for Business、StaffHub、Stream、Sway、Yammer Enterprise |

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

Microsoft の独立した第三者監査機関によって、現在の Azure および Office 365 の認定と構成証明 (ISO/IEC 27001 や SOC 2 Type 2 など) で、Microsoft が担当する BIR 2012 をどの程度カバーできているかを分析しました。 その結果を示すレポートから、BIR 2012 標準に記載されているコントロールに対するこれらの既存の認定と構成証明のマッピングを確認できます。 このレポートは、BIR 2012 に準拠した方法で Azure を採用するのに役立つツールとしてご利用いただけます。 このレポートでは、Microsoft によってカバーされている BIR 2012 コントロールと、お客様が実装する必要のあるコントロールとが明確に示されています。 「Microsoft Cloud: Azure および Office 365 BIR 2012 ベースラインのカバレッジ」レポートは、[Service Trust Portal での監査レポートに関するページの「GRC 評価レポート」](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)セクションからダウンロードできます。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**Microsoft は BIR 2012 の認証を取得していますか?**

BIR コンプライアンスの義務は、政府部門に適用されます。 BIR コンプライアンスでは、組織が情報セキュリティ管理システムを実行し、適切な技術的および組織的な手段により対処することが求められています。 Microsoft はクラウド サービス プロバイダーとしての役割において、BIR コンプライアンスの準拠を目指してはおらず、また技術的に実現することはできません。 お客様が Microsoft クラウド サービスを導入または利用する場合、それらのサービスが BIR 評価の対象範囲に含まれている可能性があります。 しかし、組織は独自の (さらなる) 統制、選択事項、プロセスを取り入れなくてはならず、それらは総合的な BIR の評価の一部となります。 レポートの目的は、政府部門が BIR 2012 に準拠する形で Microsoft クラウド サービスを導入できるのを実証することにあります。

**Microsoft クラウド サービスを利用する顧客は BIR 2012 に準拠しますか?**

BIR コンプライアンスへの準拠は、お客様がその責任を負います。 クラウド サービス ベンダーを利用する場合、お客様は通常、ベンダーの保証を求め、独自の (さらなる) テクノロジ、組織の決定事項や選択事項、そしてプロセスを取り入れます。 この取り組みは結果的に、BIR コンプライアンスに関して、総合的な評価はお客様が実施することになり、その内容は審査または認定のため、第三者の監査人に提出されます。 BIR カバレッジ レポートでは、Microsoft クラウド サービスがどの BIR 統制の対象となるかを示すインサイトが提供されていますが、そこではエンド ツー エンドのコンプライアンスは取り上げられていません。

**BIR カバレッジ レポートで BIR 2012 コンプライアンスが 100% カバーされていないということは、同コンプライアンスへの準拠は不可能だということですか?**

Microsoft クラウド サービスでは、オランダ国内の組織が持つ BIR コンプライアンスのニーズを支援する、多くの統制を提供しています。 ただし、組織は自身で選択した実施事項、さらなる技術統制、そして管理プロセスに関しては、ベンダーによるそれらの保証を補完する必要があります。 同レポートでは既に、適用可能なすべての統制の 91% 以上が直接カバーされています。 カバーされていない規制に関しては、Microsoft がレポートにおいて、準拠する方法に関するガイダンスを提供しています。

**BIR カバレッジ レポートは法的拘束力を持つ文書ですか?**

いいえ。 BIR カバレッジ レポートは、お客様の社内的な BIR 保証プロセスをサポートするツールであり、BIR コンプライアンスの実行可能性への信頼と信任を確立するためのものです。 レポートは説明として提供され、法的な免責事項があります。

**このレポートを共有することはできますか?**

レポートは機密保持契約の元でお客様に提供され、お客様の参照のみを前提としており、また Microsoft の [Service Trust Platform](https://www.microsoft.com/TrustCenter/STP/default.aspx) 以外のチャネルを介した複製および開示はできません。 お客様はレポートを、コンプライアンスまたは保証プロセスの一環として、社内外の監査人と共有することができます。

## <a name="resources"></a>リソース

- [ISO-IEC 27001](offering-iso-27001.md)
- [Security prescription national 2013 (BVR)](https://wetten.overheid.nl/BWBR0033512/2013-06-01)
- [Prescription information security national 2007 (VIR)](https://wetten.overheid.nl/BWBR0022141/2007-07-01)
- [ベースライン情報のセキュリティ (BIR)](https://www.earonline.nl/index.php/BIR_2012)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
