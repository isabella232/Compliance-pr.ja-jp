---
title: ISO/IEC 27017:2015 情報セキュリティ コントロールの実施基準
description: Microsoft クラウド サービスでは、情報セキュリティ コントロールに関するこの実施基準が採用されています。
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
ms.openlocfilehash: efd0e2c90018c8fb32e39f83bdafa7f02bf0f230
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482932"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a>ISO/IEC 27017:2015 情報セキュリティ コントロールの実施基準

## <a name="iso-iec-27017-overview"></a>ISO-IEC 27017 の概要

ISO/IEC 27017:2015 実施基準は、組織が ISO/IEC 27002:2013 に基づいてクラウド コンピューティング情報セキュリティ管理システムを実装するときにクラウド サービス情報セキュリティ コントロールを選択するためのリファレンスとして使用することを意図しています。 また、クラウド サービス プロバイダーが、一般に受け入れられている保護コントロールを実装するためのガイダンス資料としても使用できます。

この国際的な基準には、ISO/IEC 27002 に基づくクラウド特有の実装ガイダンスも提供されています。さらに、ISO/IEC 27002: 2013 の 5 項から 18 項で示されるコントロール、実装ガイダンスおよび各種情報に対するクラウド特有の情報セキュリティの脅威とリスクに対応するための追加コントロールも示されています。 具体的にはこの基準では ISO/IEC 27002 の 37 のコントロールに関するガイダンスを提供すると同時に、ISO/IEC 27002 では取り上げられていない 7 つの新しいコントロールにも言及しています。 これらの新しいコントロールは、次の重要な分野に対応しています。

- クラウド コンピューティング環境で共有される役割と責任
- 契約終了時におけるクラウド サービスのお客様の資産の削除と返却
- お客様の仮想環境を他のお客様の仮想環境から保護および分離すること
- ビジネス ニーズに応じた仮想マシンの要塞化要件
- クラウド コンピューティング環境の管理運用の手順
- クラウド コンピューティング環境内の関連アクティビティに対する監視手段の提供
- 仮想ネットワークと物理ネットワークのセキュリティ管理の連携

## <a name="microsoft-and-isoiec-27017"></a>Microsoft と ISO/IEC 27017

ISO/IEC 27017 は、クラウド サービス プロバイダーとクラウド サービスお客様の両方にガイダンスを提供している点で独特です。 また、クラウド サービスお客様がクラウド サービス プロバイダーに期待できることに関する実際的な情報も示しています。 お客様が ISO/IEC 27017 から直接得られるメリットとして、クラウドにおける共同責任を理解できます。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- [Azure、Azure Government、Azure Germany](https://aka.ms/AzureCompliance)
- Microsoft Cloud App Security
- [Dynamics 365、Dynamics 365、Dynamics 365 ドイツ](https://aka.ms/d365-compliance-list)
- Intune
- Microsoft Defender for Endpoint
- Microsoft Graph
- Microsoft Healthcare Bot
- [Microsoft マネージド デスクトップ](/microsoft-365/managed-desktop/intro/compliance)
- Office 365、Office 365 米国政府、Office 365 米国防総省、Office 365 Germany
- Power Automate (旧称 Microsoft Flow) スタンドアロン サービス、または Office 365 や Dynamics 365 ブランド プランあるいはスイートに搭載されているサービスとしてのクラウド サービス
- Power Apps クラウド サービス (スタンドアロン サービス、または Office 365 および Dynamics 365 ブランド プランあるいはスイートに搭載されているサービス)
- Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに組み込まれているサービス)
- Power BI Embedded

## <a name="azure-dynamics-365-and-iso-270172015"></a>Azure、Dynamics 365、ISO 27017:2015

Azure、Dynamics 365、およびその他のオンライン サービス コンプライアンスの詳細については、[Azure ISO 27017 サービス](/azure/compliance/offerings/offering-iso-27017)を参照してください。

## <a name="office-365-and-iso-270172015"></a>Office 365 と ISO 27017:2015

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **商用** | Access Online、Azure Active Directory、Azure Communications Service、コンプライアンス マネージャー、カスタマー ロックボックス、Delve、Exchange Online、Exchange Online Protection、Forms、Griffin、Identity Manager、Lockbox (Torus)、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 Customer Portal、Office 365 Microservices (Kaizala、ObjectStore、Sway、PowerPoint Online Document Service、Query Annotation Service、School Data Sync、Siphon、Speech、StaffHub、eXtensible Application Program を含むがこれらに限定されない)、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、Office Services Infrastructure、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、Project Online、カスタマー キーによるサービスの暗号化、SharePoint Online、Skype for Business、Stream |
| **GCC** | Azure Active Directory、Azure Communications Service、コンプライアンス マネージャー、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream |
| **GCC High** | Azure Active Directory、Azure Communications Service、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business |
| **DoD** | Azure Active Directory、Azure Communications Service、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power BI、SharePoint Online、Skype for Business |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365 監査、レポート、証明書

Microsoft クラウド サービスは、年 1 回、ISO/IEC 27001:2013 の認定プロセスの一環として、ISO/IEC 27017:2015 実施基準に関する監査を受けています。

- [Office 365: ISO 27001、27018、27017 監査評価レポート](https://aka.ms/o365isoreport)

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**この標準はだれに適用されますか?**

この実施基準では、クラウド サービス プロバイダーとクラウド サービスお客様の両方にコントロールと実装のガイダンスが提供されています。 ISO/IEC 27002:2013 と似た構成になっています。

**ISO/IEC 27017:2015 に関するMicrosoftコンプライアンス情報はどこで確認できますか?**

Azure、Intune、Power BI の [ISO/IEC 27017:2015 認定証](https://aka.ms/azureiso27017)をダウンロードできます。

**Microsoft サービスの ISO/IEC 27017 コンプライアンスを私の組織の認定プロセスに利用できますか?**

はい。 ビジネスで求められているのが、Microsoft の適用エンタープライズ クラウド サービスのいずれかに展開されている実装の認定である場合は、Microsoft の関連認定をコンプライアンス評価で利用できます。 ただし、コンプライアンスや、組織内の統制およびプロセスに関して、実装を評価する査定人の手配の責任は、審査を受ける組織が負うものとします。

**該当する監査レポートのコピーはどのようにして入手できますか?**

[Service Trust Portal](https://aka.ms/stphelp) では、独立している第三者監査レポートと他の関連資料が提供されています。 このポータルを利用して、お客様の規制要件に役立つ資料をダウンロードおよび確認できます。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

### <a name="resources"></a>リソース

- [ISO/IEC 27017:2015 実施基準](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [Microsoft オンライン サービス条件](https://aka.ms/Online-Services-Terms)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
