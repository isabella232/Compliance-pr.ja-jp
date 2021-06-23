---
title: Police-Assured セキュリティで保護された施設 (PASF) 英国
description: Microsoft ビジネス クラウド サービスは、データを処理してクラウドにPolice-Assuredセキュリティで保護された施設を要求する英国の法執行機関をサポートします。
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
ms.openlocfilehash: d28d224b756f79f5129b042bbc8aa0c8a27f2e6a
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088986"
---
# <a name="police-assured-secure-facilities-pasf-united-kingdom"></a>Police-Assured セキュリティで保護された施設 (PASF) 英国

## <a name="about-pasf"></a>PASF について

英国ホーム Office の国家ポリシング情報リスク管理チーム (NPIRMT) (セキュリティ、移民、および法律と命令を担当する省) は、警察情報の保存とアクセスが標準を満たしているという責任を負います。 国家ポリ [シング](http://library.college.police.uk/docs/APP-National-Policing-Information-Risk-Management-Policy.pdf)情報リスク管理ポリシーを通じて、警察情報システムをクラウドに移行するリスクを評価している英国全体の法執行機関の中心的な基準と管理を設定します。 このポリシーでは、保護的にマークされた、または他の機密性の高い法執行情報を保存および処理する英国のすべての国内警察サービスが、リスク評価に追加の一歩を踏み出す必要があります。データが保存されるデータセンターの物理的な検査です。 データセンターの評価が成功すると、それが PASF と判断されます。

現地の警察サービスのデューデリジェンス レビューを支援するために、NPIRMT は Azure データセンターの PASF 監査を実行し、準拠している必要があります。 ローカル警察サービスは、この NPIRMT 評価を使用して、独自のレビューをサポートできます。 NPIRMT ポリシー ガイドラインを使用して、各警察サービスの上級情報リスク所有者は、特定のアプリケーションのコンテキストで個々のデータセンターの適合性を評価し、その後 NPIRMT に承認を求め提出します。

## <a name="microsoft-and-pasf"></a>Microsoft と PASF

英国のナショナル ポリシング情報リスク管理チーム (NPIRMT) は、英国の Microsoft Azure データセンターの物理インフラストラクチャに関する包括的なセキュリティ評価を完了し、修復アクションなしで NPIRMT 要件に準拠していることを結論付けしました。 この物理的な監査が成功すると、Microsoft ビジネス クラウド サービスは、Police-Assured Secure Facilities (PASF) がクラウドでデータを処理および保存する必要がある英国全体の警察をサポートできます。

Microsoft では、セキュリティに対する総合的な防御のアプローチを採用しています。 英国のデータセンター (すべての Microsoft データセンターと同様) は、クラウド[](https://azure.microsoft.com/overview/trusted-cloud/)サービス プロバイダーの国際的に認められた標準の最も包括的なポートフォリオに準拠し、一貫してこれらの要件を満たしていることを証明されています。 このコンプライアンスには [、ISO/IEC 27001](offering-iso-27001.md) 情報セキュリティ管理標準および [ISO/IEC 27018](offering-iso-27018.md)クラウドでの個人データ保護に関するプラクティスのコードの実装に関する認定が含まれます。

これらの認定は、データセンターの物理的なセキュリティを保護するために取る措置によって裏付けされています。 データセンターの設計、構築、運用の方法から始まる層的なアプローチを採用し、顧客データが保存されている領域への物理的なアクセスを厳密に制御します。 Microsoft が管理するデータセンターには、施設の境界、建物の境界、建物内、およびデータセンターフロアで必要なアクセス承認を受け、広範なレベルの保護があります。 この構造は、承認されていないユーザーがデータおよびデータセンター リソースに物理的にアクセスするリスクを軽減します。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Dynamics 365](https://download.microsoft.com/download/E/1/9/E1977163-7A86-4812-AC18-C03ADC958AAF/Microsoft_Dynamics_365_Cloud_Service_Compliance_Datasheet.pdf)
- [Microsoft 365](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=9f756cce-b15d-45a9-94d7-6a583dee4401&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

NPIRMT は、毎年 1 つの Azure データセンターを監査し、英国の 4 つの Microsoft データセンターを毎年循環します。 Microsoft データセンターが PASF である NPIRMT 評価は、Azure および他の Microsoft クラウド サービスに対して独自のリスク評価を行っている法執行機関のお客様に対して、Home Office を通じて入手できます。

## <a name="how-to-implement"></a>実装方法

- [Azure UK Official Blueprint](/azure/governance/blueprints/samples/ukofficial-uknhs): 英国のお客様が Azure での準拠ワークロードの IaaS および PaaS 展開を加速するのに役立ちます。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**英国の警察署は、独自のリスク評価の一環として Azure PASF 評価を使用できますか?**

はい。 法執行機関は、Azure の NPIRMT 評価を使用して、クラウドに移行する前に、独自のローカル リスク評価をサポートできます。

## <a name="resources"></a>リソース

- [ナショナル ポリシング認定ポリシー](http://library.college.police.uk/docs/APP-National-Policing-Accreditation-Policy-2013.pdf)
- [Azure の施設、オンプレミス、および物理的なセキュリティ](https://azure.microsoft.com/blog/azure-layered-approach-to-physical-security/)
- [Microsoft および ISO/IEC 27001:2013 ISM 標準](offering-iso-27001.md)
- [Microsoft オンライン サービス条件](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=31)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
