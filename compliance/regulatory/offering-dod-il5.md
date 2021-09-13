---
title: 国防総省 (DoD) 影響レベル 5 (IL5)
description: Microsoft が国防総省 (DoD) の影響レベル 5 (IL5) 標準を満たす方法について説明します。
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
ms.openlocfilehash: c0c987dc5fbe2bee60508f0fab7dbdb8dce97857
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59161039"
---
# <a name="department-of-defense-dod-impact-level-5-il5"></a>国防総省 (DoD) 影響レベル 5 (IL5)

## <a name="dod-il5-overview"></a>DoD IL5 の概要

国防情報システム局 (DISA) は、DoD クラウド コンピューティング セキュリティ要件ガイド (SRG) の開発と保守を担当する米国国防総省 [(DoD)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)の機関です。 SRG は、クラウド サービス プロバイダー (CSP) のセキュリティ態勢を評価するために DoD が使用するベースライン セキュリティ要件を定義し、CSP が DoD ミッションをホストできる DoD 暫定承認 (PA) を付与する決定をサポートします。 以前に公開された DoD クラウド セキュリティ モデル (CSM) を組み込み、取り消し、取り消し、DoD リスク管理フレームワーク (RMF) にマップします。

DISA は、CSP の使用を計画および承認する DoD 機関および部門を案内します。 また、CSP が SRG に準拠するための CSP 製品を評価します。認証プロセスでは、CSP は DoD 標準への準拠に関するドキュメントを提供できます。 必要に応じて DoD 暫定承認 (PA) が発行されます。そのため、DoD 機関やサポート組織は、完全な承認プロセスを独自に行わずにクラウド サービスを使用し、時間と労力を節約できます。

[SRG セクション 3.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#3.2InformationImpactLevels) Information *Impact Levels* によると、IL5 の情報は次の内容をカバーします。

- IL4 よりも高いレベルの保護を必要とする制御された未分類情報 (CUI)
    - [CUI レジストリは](https://www.archives.gov/cui)、エグゼクティブ ブランチによって保護されている特定のカテゴリの情報を提供します。たとえば、20 を超えるカテゴリ グループが[CUI](https://www.archives.gov/cui/registry/category-list)カテゴリ リストに含まれています。
    - [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) *Nonfederal Systems and Organizations* の管理された未分類情報の保護は、連邦政府機関が連邦以外の組織と締結した契約または他の契約で使用することを目的としています。

- 国家セキュリティ システム (NSS)
    - [NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf)情報システムを国家セキュリティ システムとして識別するためのガイドラインは、NSS の定義を提供します。
    - [CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) Security *Categorization and Control Selection for* National Security Systemsでは、連邦政府機関が国家のセキュリティ情報を分類するために適用する必要があるセキュリティ基準に関するガイダンスを提供します。

商用クラウド コンピューティング サービスの取得と使用に関するガイダンスの更新に関する[2014 年 12 月 15](https://www.esi.mil/contentview.aspx?id=585)日の DoD CIO メモでは、「FedRAMP は、すべての DoD クラウド サービスの最小セキュリティ ベースラインとして機能する」と示されています。 SRG は、すべての情報影響レベル (IL) で FedRAMP モデレート ベースラインを使用し、一部ではハイ ベースラインと見なします。

[SRG セクション 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *FedRAMP* セキュリティ コントロールの DoD の使用では、FedRAMP High PA は、DoD FedRAMP+ コントロールとコントロール拡張 (C/CEs) と SRG の要件を補完して、IL5 での DoD PA の授与に向けて CSP を評価するために使用されます。 FedRAMP High PA の基礎としてどの C/CE ベースラインを使用する場合でも、DOD PA を IL5 で授与する前に、追加の考慮事項や要件を評価および承認する必要があります。 具体的には、表 2 の SRG セクション [5.1.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD FedRAMP+* セキュリティコントロール/拡張機能の状態では、DoD IL5 PA には FedRAMP High ベースラインを超える 10 の追加 C/CEs が必要です。

さらに [、SRG セクション 5.2.2.3](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL5* の場所と分離の要件に従って、レベル 5 PA に対して次の要件 (特に) を設定する必要があります。

- DoD と連邦政府機関のテナント/ミッション間の仮想/論理的な分離で十分です。 テナント/ミッション システム間の仮想/論理的な分離が必要です。
- DoD/非連邦政府機関以外のテナント (パブリック、地方/州政府のテナント) からの物理的な分離が必要です。
- CSP は、DoD およびコミュニティの情報への潜在的なアクセスを、米国市民である CSP 従業員に制限します。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- Azure
- Dynamics 365 Customer Service
- Microsoft Defender for Endpoint (以前の Microsoft Defender Advanced Threat Protection)
- Microsoft Graph
- Microsoft Stream
- Office 365 米国防総省
- Power Automate (以前の Microsoft Flow)
- Power BI

## <a name="azure-dynamics-365-and-dod-il5"></a>Azure、Dynamics 365、DoD IL5

Azure、Dynamics 365、その他のオンライン サービスのコンプライアンスの詳細については [、「Azure DoD IL5](/azure/compliance/offerings/offering-dod-il5)の提供」を参照してください。

## <a name="office-365-and-dod-il5"></a>Office 365 DoD IL5

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **DoD** | アクティビティ フィード サービス、Bing サービス、Exchange Online、Exchange Online Protection、インテリジェント サービス、Microsoft Teams、Office 365 カスタマー ポータル、Office Online、Office サービス インフラストラクチャ、Office 利用状況レポート、OneDrive for Business、People Card、SharePoint Online、Skype for Business、Windows Ink |

### <a name="attestation-documents"></a>構成証明のドキュメント

米国政府のお客様は、Office 365アクセス要求フォームを提出することにより[、FedRAMP Marketplace](https://marketplace.fedramp.gov/#!/products?sort=productName&productNameSearch=azure)から直接米国政府機関の FedRAMP ドキュメントを要求できます。 FedRAMP から直接 FedRAMP セキュリティ パッケージにアクセスするには、.gov または .mil の電子メール アドレスが必要です。

System Security Plan (SSP)、継続的監視レポート、Plan of Action and Milestones (POA M) などの FedRAMP ドキュメントと DoD ドキュメントを選択すると、NDA の下のお客様や、Service Trust Portal Audit Reports \& [- FedRAMP Reports](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3) セクションからの保留中のアクセス許可を利用できます。 サポートについては、Microsoft アカウント担当者にお問い合わせください。

### <a name="resources"></a>リソース

- [Microsoft Government ソリューション](https://www.microsoft.com/enterprise/government)
- [DoD Cloud Computing セキュリティ要件ガイド](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [FedRAMP ドキュメント](https://www.fedramp.gov/documents/)
- [DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Information Technology (IT) の DoD リスク管理フレームワーク (RMF)*
- [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final)情報システムと組織のリスク管理フレームワーク *:* セキュリティLife-Cycleプライバシーに関するシステムLife-Cycleアプローチ
- [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53)情報システムと組織のセキュリティと *プライバシー制御*
- [NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf)情報システムを国家セキュリティ システムとして識別 *するためのガイドライン*
- [CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *セキュリティ分類と* 国家セキュリティ システムの制御選択
- [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final)非 *federal* システムおよび組織での制御された未分類情報の保護
- 管理された未分類情報 (CUI) [レジストリと](https://www.archives.gov/cui) CUI [カテゴリ リスト](https://www.archives.gov/cui/registry/category-list)。
