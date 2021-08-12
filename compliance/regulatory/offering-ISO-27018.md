---
title: クラウドで個人データを保護するための ISO/IEC 27018 実施基準
description: Microsoft は、クラウド プライバシーに関するこの実施基準を順守した初のクラウド プロバイダーです。
keywords: Microsoft 365、コンプライアンス、サービス
localization_priority: Priority
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
ms.openlocfilehash: 6683d038027ac940ec480af6baca58c7f6bae0d682b023e1bee4259344862019
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54289365"
---
# <a name="isoiec-27018-code-of-practice-for-protecting-personal-data-in-the-cloud"></a>クラウドで個人データを保護するための ISO/IEC 27018 実施基準

## <a name="isoiec-27018-overview"></a>ISO/IEC 27018 の概要

国際標準化機構 (ISO) は中立的な非政府組織で、国際基準を自主的に策定する世界最大の組織です。 ISO/IEC 27000 基準ファミリは、すべての形態および規模の組織が情報資産のセキュリティを確保できるよう支援します。

2014 年、ISO は、ISO/IEC 27001 の補遺として、クラウド プライバシーに関する初めての国際実施基準である ISO/IEC 27018:2014 を採用しました。 EU データ保護法に基づいて、個人を特定できる情報 (PII) の処理者の役割を担うクラウド サービス プロバイダー (CSP) に、PII 保護のためのリスク評価と最新制御の実装に関する特定のガイダンスを提供します。

Microsoft と ISO/IEC 27018

Microsoft Azure と Azure Germany は、年に 1 回以上、ISO/IEC 27001 および ISO/IEC 27018 への準拠に関して、第三者の公認認定機関の監査を受けています。この機関は、該当するセキュリティ コントロールが導入されていて、効果的に運用されていることを独自に検証します。 このコンプライアンスの検証プロセスの一環として、監査人は、適用宣言書で、対象となる Microsoft クラウド サービスおよび法人向けテクニカル サポート サービスに、Azure で PII を保護するための ISO/IEC 27018 制御が組み込まれていることを確認します。 コンプライアンスを確保し続けるために、Microsoft クラウド サービスは年 1 回第三者による審査を受ける必要があります。

ISO/IEC 27001 基準と ISO/IEC 27018 の実施基準への準拠が、(この実施基準を採用した初めての主要クラウド プロバイダーである) Microsoft のプライバシー ポリシーと手順が堅牢で、高い水準が維持されていることを証明しています。

- **Microsoft クラウド サービスの顧客がデータの保存場所を把握している。** ISO/IEC 27018 では、認定 CSP が、データの保存先の国を顧客に知らせる必要があります。したがって、Microsoft クラウド サービスの顧客には、適用される情報セキュリティ ルールに従うために必要な可視性が提供されています。
- **お客様のデータは、明確な同意がない限りマーケティングや広告に使用されない。** CSP によっては、顧客データを自身の商業目的でターゲットを絞った広告などに使用することがあります。 Microsoft では対象となるエンタープライズ クラウド サービスに ISO/IEC 27018 を採用しているため、明確な同意がない限り、お客様のデータがこのような目的で使用されることありません。その点に関しては、お客様は安心して利用できます。また、このような同意が、クラウド サービスの使用条件になることもありません。
- **Microsoft の顧客は PII の状況を把握できる。** ISO/IEC 27018 には、適正な期間内に個人情報の返却、移行、および安全な破棄を可能にするポリシーが必要です。 顧客データにアクセスする必要がある他の企業と連携する場合、Microsoft ではこうした二次処理者の身元を積極的に開示します。
- **顧客データの開示に対する要求には法的拘束力がある場合にのみ応じる。** Microsoft がこうした要求に応じる必要がある場合 (犯罪捜査の場合など)、法律で禁止されていない限り、必ずお客様に通知します。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- Azure、Azure Government、Azure ドイツ
- Azure DevOps Services
- [Dynamics 365、Dynamics 365、Dynamics 365 ドイツ](https://aka.ms/d365-compliance-list)
- Intune
- Microsoft Cloud App Security
- Microsoft Professional Services: Azure、Dynamics 365、Intune と、Microsoft 365 for business の Medium Business および Enterprise のお客様への Premier およびオンプレミス サポート
- Microsoft Graph
- Microsoft Healthcare Bot
- [Microsoft マネージド デスクトップ](/microsoft-365/managed-desktop/intro/compliance)
- Microsoft 脅威エキスパート
- Microsoft Stream
- Office 365、Office 365 米国政府、Office 365 米国防総省
- Office 365 Germany
- OMS Service Map
- Power Automate (旧称 Microsoft Flow): スタンドアロン サービス、または Office 365 や Dynamics 365 ブランド プランあるいはスイートに搭載されているサービスとしてのクラウド サービス
- Power Apps クラウド サービス: スタンドアロン サービス、または Office 365 や Dynamics 365 ブランド プランあるいはスイートに搭載されているサービス
- Power BI クラウド サービス: スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに搭載されているサービス
- Power BI Embedded
- Power Virtual Agents
- Microsoft Defender for Endpoint: エンドポイントの検出と応答、自動の調査と修復、セキュリティ スコア

## <a name="azure-dynamics-365-and-iso-isoiec-27018"></a>Azure、Dynamics 365、ISO ISO/IEC 27018

Azure、Dynamics 365、およびその他のオンライン サービス コンプライアンスの詳細については、[Azure ISO/IEC 27018 サービス](/azure/compliance/offerings/offering-iso-27018)を参照してください。

## <a name="office-365-and-iso-isoiec-27018"></a>Office 365 と ISO ISO/IEC 27018

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **Office 365** | Access Online、Azure Active Directory、Azure Communications Service、コンプライアンス マネージャー、カスタマー ロックボックス、Delve、Exchange Online Protection、Exchange Online、Forms、Griffin、Identity Manager、Lockbox (Torus)、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 Customer Portal、Office 365 Microservices (Kaizala、ObjectStore、Sway、PowerPoint Online Document Service、Query Annotation Service、School Data Sync、Siphon、Speech、StaffHub、eXtensible Application Program を含むがこれらに限定されない)、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、Office Services Infrastructure、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、Project Online、カスタマー キーによるサービスの暗号化、SharePoint Online、Skype for Business、Stream |
| **GCC** | Azure Active Directory、Azure Communications Service、コンプライアンス マネージャー、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream |
| **GCC High** | Azure Active Directory、Azure Communications Service、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business |
| **DoD** | Azure Active Directory、Azure Communications Service、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power BI、SharePoint Online、Skype for Business |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365 監査、レポート、証明書

Microsoft クラウド サービスおよび法人向けテクニカル サポート サービスは、年 1 回、ISO/IEC 27001 の認定プロセスの一環として、ISO/IEC 27018 実施基準に関する監査を受けています。

- [Office 365: ISO 27001、27018、27017 監査評価レポート](https://aka.ms/o365isoreport)
- [Yammer ISO 27018 監査評価レポート](https://aka.ms/YammerISO27018Auditreport)

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**ISO/IEC 27018 はだれに適用されますか?**

この実施基準は、他の組織との契約の下で PII を処理する CSP に適用されます。 また、Microsoft では、これらの CSP のサポートにも適用されます。

**"個人情報管理者" と "個人情報処理者" の違いは何ですか?**

ISO/IEC 27018 のコンテキストでは、次のような違いがあります。

- 「管理者」は、個人情報の収集、保持、処理、または使用を管理します。他の企業に代わって個人情報を管理する管理担当者も含まれます。
- 「処理者」は、管理者に代わって情報を処理します。情報の使用方法または処理の目的に関する決定を下すことはありません。 (ユーザーのベンダーである) Microsoft は、エンタープライズ クラウド サービスを提供する際に、情報処理者の役割を果たします。

**Office 365 の ISO/IEC 27018 コンプライアンス情報はどこで確認できますか?**

- [Office 365](https://aka.ms/Office365-Cert) の BSI (Microsoft が ISO/IEC 27018 に準拠していることを検証した独立監査人) からの ISO/IEC 27018 証明書を確認できます。

**Microsoft のコンプライアンスを自分の組織の認定プロセスに利用できますか?**

はい。ISO/IEC 27018 への準拠が、お客様のビジネスおよび Microsoft の対象企業向けクラウド サービスへの展開において重要である場合、Microsoft の ISO/IEC 27018 への準拠証明書と Microsoft の ISO/IEC 27001 への準拠認証をコンプライアンス評価に使用できます。

ただし、コンプライアンスや、組織内の統制およびプロセスに関して、実装を評価する査定人の手配の責任は、審査を受ける組織が負うものとします。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

### <a name="resources"></a>リソース

- [ISO/IEC 27018:2014 実施基準](https://aka.ms/ISO.IEC_27018.2014)
- [Microsoft Common Controls Hub コンプライアンス フレームワーク](https://www.microsoft.com/trustcenter/common-controls-hub)
- [Microsoft エンタープライズ クラウドおよびテクニカル サービスのデータ アクセス ポリシー](https://www.microsoft.com/trustcenter/Privacy/Who-can-access-your-data-and-on-what-terms)
- [Microsoft オンライン サービス条件](https://aka.ms/Online-Services-Terms)
- [Microsoft Government クラウド](https://go.microsoft.com/fwlink/p/?linkid=2087246)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
