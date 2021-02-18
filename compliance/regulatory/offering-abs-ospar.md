---
title: シンガポール銀行協会 (ABS) 外部委託サービス プロバイダー監査レポート (OSPAR)
description: Microsoft Azure と Microsoft Dynamics 365 は、シンガポールの金融機関向けの外部委託サービス プロバイダー監査レポート (OSPAR) に準拠しています。
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
ms.openlocfilehash: 0d8c455842b07f3cbb41ee5979b1393a6c40dd3a
ms.sourcegitcommit: 4f70b1fe53943f9d919e7e1f449093b90b30f046
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "50276085"
---
# <a name="association-of-banks-in-singapore-abs-outsourced-service-providers-audit-report-ospar"></a>シンガポール銀行協会 (ABS) 外部委託サービス プロバイダー監査レポート (OSPAR)

## <a name="abs-ospar-overview"></a>ABS OSPAR 概要

金融機関がビジネス機能をアウトソーシングする場合、サービス プロバイダーは、金融機関が自ら管理するのと同じレベルのガバナンス、厳格さ、および一貫性を維持するようにする必要があります。

そのために、シンガポールで営業している国内および外国の銀行の利益を代表する非営利組織である[シンガポール銀行協会](https://www.abs.org.sg/about-us/our-role) (ABS) は、『[ABS Guidelines on Control Objectives and Procedures for Outsourced Service Providers (外部委託サービス プロバイダーの制御目標と手順に関する ABS ガイドライン)](https://abs.org.sg/docs/library/abs_outsource_guidelines.pdf)』 (ABS ガイドライン) を発行しました。 ABS ガイドラインは、シンガポールで営業している金融機関にサービスを提供するサービス プロバイダー向けの情報セキュリティ ガイダンスを定めています。 ガイドラインは、クラウド アウトソーシングの取り決めにおいて、サービス プロバイダーが特に重要なワークロードに対して実施する必要がある基本的な組織的制御を指定します。 外部委託サービス プロバイダー監査レポート (OSPAR) は、外部監査人が ABS ガイドラインで定められた基準に対してサービス プロバイダーの制御を検証するために使用されるフレームワークです。

## <a name="microsoft-and-abs-ospar"></a>Microsoft と ABS OSPAR

独立したサービス監査人が、Microsoft Azure と Microsoft Dynamics 365 のセキュリティ機能 (120 以上の Azure サービスと 10 の Dynamics 365 アプリケーションを含む) の厳密な監査を実施し、ABS ガイドラインへの準拠を評価しました。

監査人は、Azure と Dynamics 365 のセキュリティ制御が、該当する ABS の制御基準を満たすように適切に設計され、1 年間のテスト期間中に効果的に運用されたことを証明しました。

この ABS OSPAR 証明の達成は、Microsoft の対象サービスの一連のセキュリティ制御が ABS ガイドラインを満たしていることを意味し、これらのサービスは公式リストである [OSPAR 監査済みアウトソーシング サービス プロバイダー](https://abs.org.sg/docs/library/OSPAR_Audited_OSPs_16102020.pdf)に含まれています。 これにより、シンガポールに事業所を持つ金融サービス関連顧客に対して、Microsoft がガイドラインに準拠した金融サービス ソリューションを展開するための高い基準を満たしていることが保証されます。

## <a name="microsoft-and-in-scope-cloud-services"></a>Microsoft サービスと対象となるクラウド サービス

- [Azure](https://aka.ms/AzureCompliance)
- [Dynamics 365](https://go.microsoft.com/fwlink/p/?linkid=2051700)
- Intune
- Microsoft Cloud App Security
- Microsoft Graph
- [Microsoft マネージド デスクトップ](/microsoft-365/managed-desktop/intro/compliance)
- Microsoft Stream
- PowerApps クラウド サービス: スタンドアロン サービス、または Office 365 や Dynamics 365 ブランド プランあるいはスイートに搭載されているサービス
- Power Automate: スタンドアロン サービス、または Office 365 や Dynamics 365 ブランド プランあるいはスイートに搭載されているサービスとしてのクラウド サービス
- Power BI クラウド サービス: スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに搭載されているサービス
- Power Virtual Agents

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

監査は通常、12 か月に 1 回実行されます。

[Microsoft Azure and Dynamics 365 OSPAR Report (2020)](https://aka.ms/OSPAR-Report)

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**"重要な" アウトソーシングの取り決めとは何を意味し、その定義が重要である理由は何ですか?**

アウトソーシングの取り決めは、以下の状況において "重要" です。サービスの失敗または違反が金融機関の事業運営、または金融機関のリスクを管理し、適用される法律および規制を遵守する能力に重大な影響を与える可能性がある場合、または、顧客情報が含まれる場合で、顧客情報への不正アクセスまたは開示、紛失、または盗難が企業の顧客に重大な影響を与える場合です。 "顧客情報" の定義では、セキュリティで保護され、暗号化された情報は明示的に除外されることに注意してください。

この定義が重要である理由は、『MAS Outsourcing Guidelines』の一部の規定は、"重要なアウトソーシングの取り決め" にのみ適用されるためです。 これらの規定には、年次レビューの実施の義務、監査権に対処する必須契約条項、シンガポール国外へのアウトソーシングが MAS の監督業務に影響を与えないようにしなければならないことなどが含まれます。

## <a name="resources"></a>リソース

### <a name="abs-ospar-resources"></a>ABS OSPAR リソース

- [ABS Guidelines for Outsourced Service Providers](https://abs.org.sg/industry-guidelines/outsourcing)
- [シンガポールの金融機関向けのコンプライアンス チェックリスト](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=37557722-d5ed-419b-9365-2762982bacbf&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- [Microsoft and the Monetary Authority of Singapore (MAS) and Association of Banks in Singapore (ABS)](offering-mas-abs-singapore.md)

### <a name="other-microsoft-resources-for-financial-services"></a>金融サービス向けのその他の Microsoft リソース

- [Microsoft 金融サービス コンプライアンス プログラム](https://www.microsoft.com/download/details.aspx?id=55332)
- [Azure における金融サービス コンプライアンス](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Microsoft 法人向けクラウド サービスおよび金融サービス](https://www.microsoft.com/trustcenter/cloudservices/financialservices)
