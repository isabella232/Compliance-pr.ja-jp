---
title: 国防総省 (DoD) 影響レベル 2 (IL2)
description: Microsoft が国防総省 (DoD) の影響レベル 2 (IL2) 標準を満たす方法について説明します。
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
ms.openlocfilehash: c57183a53c563fffa2bb3eb1cedb2fca23db26f4
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947892"
---
# <a name="department-of-defense-dod-impact-level-2-il2"></a>国防総省 (DoD) 影響レベル 2 (IL2)

## <a name="dod-il2-overview"></a>DoD IL2 の概要

国防情報システム局 (DISA) は、DoD クラウド コンピューティング セキュリティ要件ガイド (SRG) の開発と保守を担当する米国国防総省 [(DoD)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)の機関です。 SRG は、クラウド サービス プロバイダー (CSP) のセキュリティ態勢を評価するために DoD が使用するベースライン セキュリティ要件を定義し、CSP が DoD ミッションをホストできる DoD 暫定承認 (PA) を付与する決定をサポートします。 以前に公開された DoD クラウド セキュリティ モデル (CSM) を組み込み、取り消し、取り消し、DoD リスク管理フレームワーク (RMF) にマップします。

DISA は、CSP の使用を計画および承認する DoD 機関および部門を案内します。 また、CSP が SRG に準拠するための CSP 製品を評価します。認証プロセスでは、CSP は DoD 標準への準拠に関するドキュメントを提供できます。 必要に応じて DoD 暫定承認 (PA) が発行されます。そのため、DoD 機関やサポート組織は、完全な承認プロセスを独自に行わずにクラウド サービスを使用し、時間と労力を節約できます。

商用クラウド コンピューティング サービスの取得と使用に関するガイダンスの更新に関する[2014 年 12 月 15](https://www.esi.mil/contentview.aspx?id=585)日の DoD CIO メモでは、「FedRAMP は、すべての DoD クラウド サービスの最小セキュリティ ベースラインとして機能する」と示されています。 SRG は、すべての情報影響レベル (IL) で FedRAMP モデレート ベースラインを使用し、一部ではハイ ベースラインと見なします。

[SRG セクション 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *FedRAMP* セキュリティ コントロールの DoD の使用では、セクション 5.6.2 で説明されている人事セキュリティ要件に準拠した場合、FedRAMP モデレート PA と DoD レベル 2 PA を最小限に抑える CSP で IL2 情報がホストされる可能性があります。 ただし、この方法では、ミッション所有者の要求に応じて CSP が他のセキュリティ要件や統合要件を満たさないわけではありません。 [SRG セクション 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2 の* 場所と分離の要件に従って、DoD IL2 PA は FedRAMP モデレート PA で適切にカバーされ、IL2 PA の要件は追加的に評価されません。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- Azure
- Dynamics 365
- Microsoft Cloud App Security
- Microsoft Defender for Endpoint
- Microsoft Graph
- Microsoft Intune
- Microsoft Stream
- Office 365米国政府、米国Office 365 - 高
- Power Apps
- Power Automate
- Power BI

## <a name="azure-dynamics-365-and-dod-il2"></a>Azure、Dynamics 365、DoD IL2

Azure、Dynamics 365、その他のオンライン サービスコンプライアンスの詳細については [、「Azure DoD IL2 製品」を参照してください](/azure/compliance/offerings/offering-dod-il2)。

## <a name="office-365-and-dod-il2"></a>Office 365 DoD IL2

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **GCC** | アクティビティ フィード サービス、Bing サービス、Delve、Exchange Online Protection、Exchange Online、インテリジェント サービス、Microsoft Teams、Office 365 カスタマー ポータル、Office Online、Office サービス インフラストラクチャ、Office 利用状況レポート、OneDrive for Business、People Card、SharePoint Online、Skype for Business、Windows Ink |
| **GCC High** | アクティビティ フィード サービス、Bing サービス、Delve、Exchange Online Protection、Exchange Online、インテリジェント サービス、Microsoft Teams、Office 365 カスタマー ポータル、Office Online、Office サービス インフラストラクチャ、Office 利用状況レポート、OneDrive for Business、People Card、SharePoint Online、Skype for Business、Windows Ink |

### <a name="resources"></a>リソース

- [Microsoft Government ソリューション](https://www.microsoft.com/enterprise/government)
- [DoD Cloud Computing セキュリティ要件ガイド](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [FedRAMP ドキュメント](https://www.fedramp.gov/documents/)
- [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final)情報システムと組織のリスク管理フレームワーク *:* セキュリティLife-Cycleプライバシーに関するシステムLife-Cycleアプローチ
- [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53)情報システムと組織のセキュリティと *プライバシー制御*
- [DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Information Technology (IT) の DoD リスク管理フレームワーク (RMF)*
