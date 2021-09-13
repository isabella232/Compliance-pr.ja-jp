---
title: NEN 7510
description: オランダ国内の組織は NEN 7510 標準に従い、患者の医療データの統制を実施する必要があります。
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
ms.openlocfilehash: 438780ab33c99bae410218bdb54265093105c16b
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160391"
---
# <a name="nen-7510"></a>NEN 7510

## <a name="nen-7510-overview"></a>NEN 7510 の概要

オランダ国内で患者の医療情報を取り扱う組織は、そのデータおよび組織への統制が NEN 7510 標準で定められた要件に適合していることを実証する必要があります。 Microsoft は NEN 7510 の規制の対象外ですが、医療分野のお客様は、Microsoft クラウドで構築されたソリューションに対して、NEN 7510 への準拠を確保する必要があります。 Microsoft のクラウド サービスは、定期的にさまざまな認証や監査を受けており、その中には NEN 7510 で指定された要件に密接に関わる要素が含まれています。

## <a name="microsoft-and-nen-75102011"></a>Microsoft と NEN 7510:2011

Microsoft では現在の認証と保証声明を分析し、[NEN 7510 カバレッジ レポート](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=15d5a5fa-fbb6-4ea6-8126-2a2c684ae789&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_GRC_Assessment_Reports) (Service Trust Platform でご利用いただけます)。それらの認証や保証声明は、Microsoft がクラウド サービス プロバイダーとして責任を負う NEN 7510 規制に対して対応付けられています。 この文書は、患者の医療情報の保管または処理に関連する Microsoft クラウド サービスの利用を NEN 7510 に準拠させるため、お客様がどの統制をさらに実施しなくてはならないか判断する上で役立ちます。

Azure セキュリティおよびコンプライアンス ブループリントを使用して NEN 7510 の展開を加速する方法を説明します。「[Microsoft クラウドをダウンロードする: Azure および Office 365 NEN7510-2011 標準範囲ユーザー ガイド](https://aka.ms/Azure-NEN7510-2011)」をダウンロードしてください。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- Azure および Azure Government
- Intune
- Office 365

## <a name="office-365-and-iso-27001"></a>Office 365 と ISO 27001

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **商用** | Azure Information Protection、Bookings、Delve、Exchange Online、Exchange Online Protection、Kaizala、Microsoft Analytics、Microsoft Booking、Microsoft Graph、Microsoft Teams、Microsoft To Do for Web、MyAnalytics、Office 365 Cloud App Security、Office 365 グループ、Office 365 ビデオ、OneDrive for Business、Planner、Power Apps、Power Automate、Power BI for Office 365、PowerApps、SharePoint Online、Skype for Business、StaffHub、Stream、Sway、Yammer Enterprise |

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

- [Azure および Office 365 NEN 7510:2011 標準範囲](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=15d5a5fa-fbb6-4ea6-8126-2a2c684ae789&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_GRC_Assessment_Reports)

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**Microsoft クラウド サービスを利用する顧客は NEN 7510 に準拠しますか?**

NEN コンプライアンスへの準拠は、医療組織 (「顧客」) がその責任を負います。 クラウド サービス ベンダーを利用する場合、お客様は通常、ベンダーの保証を求め、独自の (他の) テクノロジ、組織の決定事項や選択事項、そしてプロセスを取り入れます。 このことにより、結果的に NEN 7510 コンプライアンスに関して、総合的な評価は顧客が実施し、その内容は審査または認定のため、第三者の監査人に提出されることになります。 NEN 7510 カバレッジ レポートでは、Microsoft クラウド サービスの対象となる NEN 7510 制御に関するインサイトが提供されていますが、そのため、エンド ツー エンドのコンプライアンスは取り上げられていません。

**Microsoft は NEN 7510 に準拠していますか?**

NEN 7510 コンプライアンスの義務は、オランダの医療組織に適用されます。 NEN 7510 コンプライアンスでは、組織が情報セキュリティ管理システムを実行し、適切な技術的および組織的な手段により対処することが求められています。 Microsoft はクラウド サービス プロバイダーとしての役割において、NEN 7510 コンプライアンスの準拠を目指してはおらず、また技術的に実現することはできません。 顧客が Microsoft クラウド サービスを導入または利用する場合、それらのサービスが NEN 7510 評価の対象範囲に含まれている可能性があります。 ただし、組織は独自の (他の) 制御、選択事項、プロセスを取り入れる必要があり、これらは NEN7510 の総合評価に含まれます。 レポートの目的は、医療事業者が NEN 7510 に準拠する形で Microsoft クラウド サービスを導入できることを示すことにあります。

**NEN カバレージ レポートで NEN 7510 コンプライアンスが 100% カバーされていないということは、同コンプライアンスへの準拠は不可能だということですか?**

Microsoft クラウド サービスでは、オランダ国内の医療分野の組織が持つ NEN 7510 コンプライアンスのニーズを支援する、多くの制御を提供しています。 ただし、組織は自身で選択した実施事項、他の技術制御、そして管理プロセスに関しては、ベンダーによるそれらの保証を補完する必要があります。 同レポートでは既に、適用可能なすべての統制の 94% 以上が直接カバーされてています。 カバーされていない規制に関しては、Microsoft がレポートにおいて、準拠する方法に関するガイダンスを提供しています。

> [!NOTE]
> NEN 7510 では、すべての規制を実施することを主要な目的としてはいませんがその大部分をカバーする Microsoft のオンライン サービスは、すべての規制に対応する上で役立ちます。 NEN 7510 では、組織がどの規制が適用されるか判断するため、組織が利用できるリスクベースの情報セキュリティ システムの実行を義務付けています。

**NEN 7510 カバレッジ レポートは法的拘束力を持つ文書ですか?**

いいえ。 これは、お客様の社内的な NEN 7510 保証プロセスをサポートするツールであり、NEN 7510 コンプライアンスの実行可能性への信頼と信任を確立するためのものです。 独立監査人である KPMG によって作成されたこのレポートは、説明として提供され、法的な免責事項があります。

**Microsoft はレポートの作成に出資しましたか?**

Microsoft は自社の世界中の保証と NEN 7510 標準の統制との対応付けを実施しました。 その後、Microsoft は NEN 7510 に対応付けられた統制に関する独立した審査を、独立監査人である KPMG に委託しました。

**このレポートを共有することはできますか?**

レポートは機密保持契約 (NDA) の元でお客様に提供され、お客様の参照のみを前提としており、また Microsoft の Service Trust Portal 以外のチャネルを介した複製および開示はできません。

お客様はレポートを、コンプライアンスまたは保証プロセスの一環として、社内外の監査人と共有することができます。

## <a name="resources"></a>リソース

- [NEN について](https://www.nen.nl/About-NEN.htm)
- [NEN 7510:2011 標準](https://www.nen.nl/NEN-Shop-2/Standard/NEN-75102011-nl.htm)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
