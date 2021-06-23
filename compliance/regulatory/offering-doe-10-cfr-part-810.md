---
title: US DoE 10 CFR Part 810
description: 米国 DoE 10 CFR Part 810 の輸出管理要件の対象となるお客様は、Azure Government を使用できます。
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
ms.openlocfilehash: 1a16495f5cfe3e293910ebe84e6af566aea17621
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087546"
---
# <a name="us-doe-10-cfr-part-810"></a>US DoE 10 CFR Part 810

## <a name="microsoft-and-doe-10-cfr-part-810"></a>Microsoft と DoE 10 CFR Part 810

Microsoft Azure政府機関は、米国エネルギー省 (DoE) 10 CFR Part 810 の輸出管理要件に従って、次の 2 つの承認を受けるお客様をサポートできます。

- 共同承認委員会 (JAB) が発行する FedRAMP 高仮承認 (P-ATO)
- 国防総省 (DoD) 防御情報システム局からのレベル 4 と 5 の暫定承認

FedRAMP は、Azure Government が、厳格な NIST コントロールで設計されたコンピューティング、ストレージ、ネットワークなどのコア インフラストラクチャと仮想化テクノロジとサービスを提供する保証を提供する適切なベースラインを提供します。 これらは、お客様のデータ分離要件を満たすのに役立ち、お客様のオンプレミス環境への安全な接続を可能にします。

さらに、Azure Government は、Azure クラウドから物理的に分離された米国政府機関のコミュニティ クラウドです。 米国政府による特定のバックグラウンド スクリーニング要件に関する追加の保証を提供します。Azure 運用担当者の間で米国市民をスクリーニングするために情報やシステムへのアクセスを制限する特定の制御を含む。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure Government](https://aka.ms/AzureCompliance)
- Intune

## <a name="how-to-implement"></a>実装方法

- [NERC CIP Standards &](https://aka.ms/AzureNERC)クラウド コンピューティング : Azure または Azure Government にワークロードを展開する電気事業者および登録済みエンティティに関するガイダンス。

## <a name="about-doe-10-cfr-part-810"></a>DoE 10 CFR Part 810 について

米国エネルギー省 (DoE) 輸出管理規則 [10 CFR Part 810](https://www.govinfo.gov/content/pkg/FR-2015-02-23/pdf/2015-03479.pdf) は、未分類の核技術と支援の輸出を管理します。 これは、米国から輸出された核技術が平和的な目的でのみ使用されるのを保証するのに役立ちます。 改訂されたパート 810 (Final Rule) は 2015 年 3 月に有効であり、国家核セキュリティ局によって [管理されています](https://www.energy.gov/nnsa/national-nuclear-security-administration)。 セクション 810.6 では、「一般的に承認されている」機密性の高い核技術の支援と転送の規定と、特定の承認を必要とする (エンリッチメントや重水生産などの機密性の高い核技術に関する支援など) には、特定の DoE 認証が必要とされています。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**米国原子力規制委員会の 10 CFR Part 110 規制は Azure Government に適用されますか?**

いいえ。 米国[原子力規制委員会](https://www.nrc.gov/)(NRC) は[、10 CFR Part 110](https://www.nrc.gov/reading-rm/doc-collections/cfr/part110/)に基いて、原子力施設および関連機器および資材の輸出入を規制しています。 [](https://www.nrc.gov/about-nrc/ip/export-import.html) NRC は、DoE 管轄区域に該当するこれらの項目に関連する核技術と支援を規制するものではありません。 したがって、NRC 10 CFR Part 110 の規制は Azure Government には適用されません。

**DoE 10 CFR Part 810 に準拠している証拠を提供する方法**

組織が Azure Government にデータを展開している場合は、適切に制限された方法でデータを処理している証拠として、Azure Government FedRAMP High P-ATO を利用できます。 ただし、クラウド サービスの使用を含む、独自のシステムの DoE 承認を取得する責任があります。

**Azure Government に展開されたデータを分類する責任は何ですか?**

Azure Government にデータを展開する顧客は、独自のセキュリティ分類プロセスを担当します。 DoE 輸出管理の対象となる顧客データの場合、分類システムは、米国原子力法第 148 条によって確立された非分類制御核情報 (UCNI) コントロールによって [拡張されます](https://www.epa.gov/laws-regulations/summary-atomic-energy-act)。

## <a name="resources"></a>リソース

- [Azure Cloud Services と米国のエクスポート コントロール](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- [Microsoft と FedRAMP](offering-fedramp.md)
- [Microsoft と DoD](offering-dod-disa-l2-l4-l5.md)
- [Microsoft Government クラウド](https://www.microsoft.com/enterprise/government)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
