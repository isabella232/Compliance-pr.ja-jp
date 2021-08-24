---
title: ニュージーランド政府機関向けクラウド コンピューティングのセキュリティとプライバシーに関する考慮事項
description: Microsoft NZ は、ニュージーランドのクラウド コンピューティング フレームワークで公開されている質問に対応します。
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
ms.openlocfilehash: 2e6dc7b7dcd59e3d82d6787b59f698c621f119bb
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "58480489"
---
# <a name="new-zealand-government-information-security-and-privacy-considerations-ispc"></a>ニュージーランド政府機関の情報セキュリティとプライバシーに関する考慮事項 (ISPC)

## <a name="new-zealand-government-information-security-and-privacy-considerations-overview"></a>ニュージーランド政府機関の情報セキュリティとプライバシーに関する考慮事項の概要

2015 年 10 月、ニュージーランド政府は、公共部門全体での情報技術の使用に関する「クラウド ファースト」ポリシーを再確認した、改訂された全政府 ICT 戦略を支持しました。 改訂された戦略は、NZ 政府最高情報責任者 (GCIO) の権限の下で開発および実装された「クラウド コンピューティング リスクと保証フレームワーク」を保持します。

政府は、クラウド サービスを評価および採用する際に、すべてのニュージーランド国家サービス機関がこのフレームワーク内で機能すると予想しています。 「クラウド コンピューティングの要件」は、政府機関がクラウド サービスを導入する際に行う必要がある操作と、政府のクラウド ポリシーの履歴の概要を示しています。

NZ 政府機関が潜在的なクラウド ソリューションに関する一貫した堅牢なデューデリジェンスを実施する際に支援するために、GCIO はクラウド コンピューティング: Information Security and [Privacy Considerations (ISPC)](https://www.digital.govt.nz/dmsdocument/1~cloud-computing-information-security-and-privacy-considerations/html)を公開しました。 このドキュメントには、データの主権、プライバシー、セキュリティ、ガバナンス、機密性、データ整合性、可用性、インシデント対応と管理に焦点を当てた 100 以上の質問が含まれている。 ISPC は、クラウド サービス プロバイダーが正式なコンプライアンスを実証する必要がある NZ 政府機関の標準を定義していない。 ただし、ドキュメントに記載されている質問の多くは、クラウド サービス プロバイダーがさまざまな関連基準に準拠する方法を理解することの重要性を示しています。

## <a name="microsoft-and-new-zealand-government-cloud-computing-security-and-privacy-considerations"></a>Microsoft およびニュージーランド政府機関向けクラウド コンピューティングのセキュリティとプライバシーに関する考慮事項

政府機関が Microsoft エンタープライズ クラウド サービスの分析と評価を行うのを支援するために、Microsoft ニュージーランドは、エンタープライズ クラウド サービスが Microsoft クラウド サービスが認定される標準にリンクすることで、「クラウド コンピューティング ISPC」に記載されている質問に対処する方法を示すドキュメントを作成しました。 これらの認定は、Microsoft が、プライバシーとセキュリティのリスクを効果的に軽減し、データ主権の懸念に対処するために、クラウド サービスが設計、構築、運用されるという公的および民間部門の両方の顧客に保証する方法の中心です。 [クラウド コンピューティング ISPC に対する Azure の応答は](https://azure.microsoft.com/resources/microsoft-azure-response-to-nz-gcio-cloud-computing-information-security-privacy-considerations/)、お客様がダウンロードできます。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- Azure および Azure Government
- [Dynamics 365](https://aka.ms/d365-compliance-list)
- Intune
- Office 365
- Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに組み込まれているサービス)

## <a name="office-365-and-ispc"></a>Office 365 ISPC

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **商用** | Exchange Online, SharePoint, Skype for Business |

>[!Note]
>Microsoft NZ は GCIO チームと連携して、「Office 365: SEEMail Integration and Reference Architecture」で説明されている Exchange Online と SEEMail を統合するリファレンス アーキテクチャを開発しました。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**フレームワークは誰に適用されますか?**

GCIO の義務に該当する組織、公的および非公的サービス部門、20 の地区の保健委員会、および 7 つのクラウン エンティティは、クラウド サービスの使用を決定する際にフレームワークに従う必要があります。

**代理店は、ICT システムの認定プロセスで、このフレームワークに対する Microsoft の応答を使用できますか?**

ニュージーランド情報セキュリティマニュアルの下で、機関が ICT システムの認定と[](https://go.microsoft.com/fwlink/p/?linkid=2099496)認定を受ける必要がある場合は、分析の一環としてこれらの応答を使用できます。

## <a name="resources"></a>リソース

- [オフショアホスト型生産性サービスのセキュリティ要件:Officeの準拠ガイドOffice 365](https://aka.ms/o365-gcio-conformance-guidance)
- [NZ Government ICT Strategy 2015](https://www.ict.govt.nz/strategy-and-action-plan/strategy/)
- [クラウド コンピューティング: 情報セキュリティとプライバシーに関する考慮事項 (ISPC)](https://www.digital.govt.nz/standards-and-guidance/technology-and-architecture/cloud-services/)
- [Microsoft オンライン サービス条件](https://aka.ms/Online-Services-Terms)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)

## <a name="microsoft-responses-to-cloud-computing-ipsc"></a>クラウド コンピューティング IPSC に対する Microsoft の応答

- [Azure](https://aka.ms/Azure-NZ-response)
- [Intune](https://aka.ms/Intune-NZ-response)
- [Office 365](https://aka.ms/O365-NZ-Response)
- [Power BI](https://download.microsoft.com/download/5/1/7/51726B9B-2E76-49C4-9D4F-A36BF025CB93/Response-to-GCIO-105-questions-Power-BI.pdf)
