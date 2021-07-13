---
title: Health Information Trust Alliance (HITRUST) Common Security Framework (CSF)
description: Azure と Office 365は、正常性情報信頼アライアンス (HITRUST) 共通セキュリティ フレームワーク (CSF) の認定を受けています。
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
ms.openlocfilehash: ef8f44309a8560341f456b3b2cace3b8038ae993
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384857"
---
# <a name="health-information-trust-alliance-hitrust-common-security-framework-csf"></a>Health Information Trust Alliance (HITRUST) Common Security Framework (CSF)

## <a name="hitrust-csf-overview"></a>HITRUST CSF の概要

Health Information Trust Alliance (HITRUST) は、医療業界の代表者が管理する組織です。 HITRUST は、医療組織とそのプロバイダーが一貫性のある合理化された方法でセキュリティとコンプライアンスを実証するための認定可能なフレームワークである Common Security Framework (CSF) を作成し、維持しています。

CSF は HIPAA と HITECH 法に基付け、個人を特定できる健康情報の使用、開示、および保護に関する要件を確立し、非準拠を強制する米国の医療法です。 HITRUST は、標準化されたコンプライアンス フレームワーク、評価、認定プロセスというベンチマークを提供し、クラウド サービス プロバイダーと対象となる正常性エンティティがコンプライアンスを測定できる基準を提供します。 また、CSF には、Payment Card Industry Data Security Standard[(PCI-DSS)、ISO/IEC](https://www.microsoft.com/trustcenter/compliance/pci) [27001](https://www.microsoft.com/trustcenter/compliance/iso-iec-27001) 情報セキュリティ管理標準、および最小許容リスク基準[(MARS-E)](https://www.microsoft.com/trustcenter/compliance/mars-e)など、既存のフレームワークからの医療固有のセキュリティ、プライバシー、その他の規制要件も組み込まれております。

CSF は、エンドポイント保護、モバイル デバイスセキュリティ、アクセス制御など、19 の異なるドメインに分かれています。 HITRUST は、これらのコントロールに対して IT サービスを認定します。 HITRUST は、組織、システム、および規制の要素に基づいて、組織のリスクに認定要件を適合します。

Health Information Trust Alliance (HITRUST) Common Security Framework (CSF)

HITRUST は、自己評価、CSF 検証、および CSF 認定の 3 つのレベルの保証またはレベルを提供します。 各レベルは、その下のレベルに対する厳しさが増して構築されます。 最高レベルの CSF 認定を受けた組織は、CSF のすべての認定要件を満たしています。 Microsoft AzureおよびOffice 365は、HITRUST CSF の認定を受ける最初のハイパースケール クラウド サービスです。 HITRUST 評価会社の Coalfire は、Azure と Office 365 が機密情報を保護するためのセキュリティ、プライバシー、および規制要件を実装する方法に基づいて評価を実施しました。 Microsoft は HITRUST 共有責任プログラムをサポートしています。

Azure Security and Compliance Blueprint を使用して HITRUST の展開を加速する方法について説明します。

[HITRUST Microsoft Azure (CRM) ブループリント v9.0d をダウンロードする](https://servicetrust.microsoft.com/ViewPage/Blueprint?command=Download&downloadType=Document&downloadId=3ccde498-4761-4be0-be8b-cd8d379a3a4f&docTab=fc060920-cdb8-11e7-bacf-0bf52b09d912_Healthcare_Blueprint)

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft のスコープ内クラウド プラットフォームと&サービス

- Azure および Azure Government
- Intune
- [Microsoft マネージド デスクトップ](/microsoft-365/managed-desktop/intro/compliance)
- Office 365

## <a name="azure-dynamics-365-and-hitrust"></a>Azure、Dynamics 365、HITRUST

Azure、Dynamics 365、その他のオンライン サービスコンプライアンスの詳細については [、「Azure HITRUST の提供」を参照してください](/azure/compliance/offerings/offering-hitrust)。

## <a name="office-365-and-hitrust"></a>Office 365 HITRUST

### <a name="office-365-cloud-environments"></a>Office 365クラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365とスコープ内サービス

次の表を使用して、サービスとサブスクリプションOffice 365を決定します。

| **適用対象** | **スコープ内サービス** |
|:------------------|:----------------------|
| **Office 365** | アクティビティ フィード サービス、Bing サービス、Delve、Exchange Online Protection、Exchange Online、Microsoft Teams、Office 365 カスタマー ポータル、Office Online、Office サービス インフラストラクチャ、Office 利用状況レポート、OneDrive for Business、People Card、SharePoint Online、Skype for Business、Windows Ink |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365、レポート、および証明書

HITRUST CSF 認定Office 365 2 年間有効です。

- [Office 365HITRUST 認定書](https://aka.ms/O365HITRUSTcertification)

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**一部のOffice 365サービスが、この認定の対象ではない理由**

Microsoft は、他のクラウド サービス プロバイダーと比較して最も包括的なサービスを提供します。 地域や業界全体にわたる広範なコンプライアンスの提供に対応するために、市場の需要、顧客からのフィードバック、製品ライフサイクルに基づく保証の取り組みの範囲にサービスが含まれます。 サービスが特定のコンプライアンスサービスの現在の範囲に含まれていない場合、組織は、コンプライアンス義務に基づいてリスクを評価し、そのサービスのデータを処理する方法を決定する責任があります。 お客様からのフィードバックを継続的に収集し、規制当局や監査人と一緒に取り組み、お客様のセキュリティとコンプライアンスのニーズに合わせてコンプライアンス範囲を拡大します。

**Microsoft 認定とは、組織が組織で認証を使用している場合Office 365 HITRUST CSF に準拠しているという意味ですか?**

データを SaaS Office 365に保存する場合、コンプライアンスを達成する責任は Microsoft と組織の間で共有されます。 Microsoft は、物理的なセキュリティ、ネットワーク制御、アプリケーション レベルの制御など、インフラストラクチャ制御の大部分を管理し、組織はアクセス制御を管理し、機密データを保護する責任を負います。 HITRUST Office 365は、Microsoft の制御フレームワークのコンプライアンスを示しています。 その上で、組織は HITRUST CSF の要件を満たすために、独自のデータ保護制御を実装および維持する必要があります。

**Microsoft は、組織が適切なコントロールを実装するためのガイダンスを提供Office 365?**

はい、組織がクラウド サービスを使用する際に複雑なコンプライアンス義務を果たすのに役立つ、Microsoft Cloud ソリューションをまたがったコンプライアンス スコアで、推奨される顧客のアクションを確認できます。 具体的には、HITRUST CSF の場合は、コンプライアンス スコアで NIST 800-53 および NIST CSF 評価を使用してリスク評価を実行することをお勧めします。 評価では、データ保護制御の実装に使用できる詳細なガイダンスと Microsoft ソリューションを提供します。 コンプライアンス スコアの詳細については、「Microsoft コンプライアンス [マネージャー」を参照してください](/microsoft-365/compliance/compliance-manager)。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 コンプライアンス マネージャーで [評価をビルドおよび管理する方法について学習します](/microsoft-365/compliance/compliance-manager-assessments)。

### <a name="resources"></a>リソース

- [HITRUST Alliance](https://hitrustalliance.net/)
- [HITRUST CSF 9.3](https://hitrustalliance.net/csf-license-agreement/)
- [CSF の理解と活用](https://hitrustalliance.net/understanding-leveraging-csf/)
- [HITRUST 共有責任プログラムの詳細](https://go.microsoft.com/fwlink/p/?linkid=2100268)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
