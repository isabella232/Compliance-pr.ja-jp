---
title: コンプライアンス認証 - Cloud Security Alliance (CSA) STAR Self-Assessment
description: Microsoft の STAR Self-Assessment では、クラウド サービスにおいて Cloud Security Alliance の要件を満たす方法の詳細を説明しています。
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
ms.openlocfilehash: 6ff20d9ac81562353a5971386d0d498b44edfd3b
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "58479739"
---
# <a name="cloud-security-alliance-csa-star-self-assessment"></a>Cloud Security Alliance (CSA) STAR Self-Assessment

## <a name="csa-star-self-assessment-overview"></a>CSA STAR Self-Assessment の概要

Cloud Security Alliance (CSA) は、業界の実務者、企業、および他の重要な関係者の幅広い連合によって主導される非営利組織です。 最も安全なクラウド コンピューティング環境の確保に役立ち、IT 運用をクラウドに移行する際にクラウドのお客様が詳細な情報を得た上で決断できるようにするためのベスト プラクティスを定義することに尽力しています。  
  
2010 年に CSA はクラウド IT 運用を評価するためのツールのスイートである CSA Governance, Risk Management, and Compliance (GRC) スタックを公開しました。 これは、業界のベスト プラクティスや規格の順守状態、および規制への準拠状態について、クラウドのお客様がクラウド サービス プロバイダー (CSP) を評価できるように作成されています。  
  
2013 年に、CSA と British Standards Institution は Security, Trust & Assurance Registry (STAR) を発表しました。これは、CSP が CSA 関連の評価を公開できる無償の公的にアクセス可能なレジストリです。  
  
CSA STAR は、CSA GRC スタックの 2 つの主要なコンポーネントを基にしています。

- Cloud Controls Matrix (CCM): 16 のドメインを対象とする、基本のセキュリティ原則についての管理フレームワークです。クラウドのお客様が CSP の全体的なセキュリティ リスクを評価できるようにします。
- Consensus Assessments Initiative Questionnaire (CAIQ): CCM を基に、CSA ベスト プラクティスへの準拠状態を評価するためにお客様やクラウド監査機関が CSP に対して確認するとよい 140 項目以上の質問をまとめています。

STAR は 3 つのレベルの保証を提供します。CSA STAR Self-Assessment は、導入レベルである Level 1 の保証になり、すべての CSP が無料で使用できます。 それ以降の STAR プログラムの保証については、Level 2 では第三者による評価ベースの認定が必要になり、Level 3 では継続的な監視に基づく認定が必要になります。

## <a name="microsoft-and-csa-star-self-assessment"></a>Microsoft および CSA STAR Self-Assessment

STAR Self-Assessment の一環として、CSP は、CSA ベスト プラクティスへの準拠を示す 2 種類の異なるドキュメントを提出できます。1 つは回答を記入した CAIQ で、もう 1 つは CCM への準拠状態を記録したレポートです。 CSA STAR Self-Assessment の場合、Microsoft では Microsoft Azure 用に CAIQ と CCM ベースのレポートの両方を、Microsoft Dynamics 365 と Microsoft Office 365 用には CCM ベースのレポートを公開しています。  

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- Azure および Azure Government
- [Dynamics 365](https://aka.ms/d365-compliance-list)
- Office 365

## <a name="azure-dynamics-365-and-csa-star-self-assessment"></a>Azure、Dynamics 365、CSA STAR 自己評価

Azure、Dynamics 365、およびその他のオンライン サービス コンプライアンスの詳細については、[Azure CSA STAR 自己評価サービス](/azure/compliance/offerings/offering-csa-star-self-assessment)を参照してください。

## <a name="office-365-and-csa-star-self-assessment"></a>Office 365 と CSA STAR 自己評価

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **商用** |Exchange Online、Exchange Online Protection、Office 365 Customer Portal、Office Online、Office Services Infrastructure、OneDrive for Business、SharePoint Online、Skype for Business |

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**CSA CCM が対応しているのはどの業界標準ですか?**

CCM は、ISO 27001、PCI DSS、HIPAA、AICPA SOC 2、NERC CIP、FedRAMP、NIST など、業界で受け入れられているさまざまなセキュリティ基準、規制、管理フレームワークに対応しています。 最新のリストについては [CSA の Web サイト](https://cloudsecurityalliance.org/)にアクセスしてください。

**CSA STAR Self-Assessment が重要であるのはなぜですか?**

CSP は CSA STAR Self-Assessment を使用すると、透明性の高い方法で、CSA が発行したベスト プラクティスに準拠していることを文書化できます。 自己評価レポートは一般に公開されるため、クラウドのお客様が CSP のセキュリティ施策について確認し、同じ基準を使用して異なる CSP を比較検討できます。

**Office 365 が達成した CSA STAR の保証レベルは?**

- **レベル 1**: **CSA STAR 自己評価**: クラウド サービス プロバイダーにより提供される無償のサービスで、顧客がサービスのセキュリティを評価できるよう、プロバイダーが自社のセキュリティ制御を文書化したものです。

### <a name="office-365-resources"></a>Office 365 のリソース

- [Cloud Security Alliance](https://cloudsecurityalliance.org/)
- [Cloud Controls Matrix (CCM)](https://cloudsecurityalliance.org/group/cloud-controls-matrix/)
- [Consensus Assessments Initiative Questionnaire (CAIQ)](https://cloudsecurityalliance.org/group/consensus-assessments/)
- [CSA Security, Trust & Assurance Registry (STAR)](https://cloudsecurityalliance.org/star/)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)