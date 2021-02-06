---
title: 連邦金融機関審査会 (FFIEC)
description: Microsoft は、金融サービスクライアントが連邦金融機関審査会 (FFIEC) の監査要件に準拠するのに役立ちます。
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
ms.openlocfilehash: 73a23d89876ee6c4c11a98a95d8f2bd491642b60
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120886"
---
# <a name="federal-financial-institutions-examination-council-ffiec"></a>連邦金融機関検査委員会 (FFIEC)

## <a name="ffiec-overview"></a>FFIEC の概要

連邦金融機関検査委員会 (FFIEC) は、米国の金融機関に対する米国連邦政府の審査を担当する 5 つの銀行規制機関で構成される正式な機関です。 FFIEC 審査担当者教育Office、FFIEC メンバー機関のフィールド検査者を対象とした IT 検査ハンドブックを公開しています。

[FFIEC 監査 IT 検査](https://ithandbook.ffiec.gov/it-booklets/audit.aspx)ハンドブックには、金融機関と TSP の両方の IT 監査プログラムの品質と有効性を評価するための、これらの検査担当者向けガイダンスが含されています。 具体的には、独立監査レポートの例として、米国認定公的会計員協会 (AICPA) の SOC 1、SOC 2、SOC 3 の構成証明レポートに言及しています。 ただし、FFIEC では、金融機関がこれらのレポートに含まれる情報だけに頼らず [、FFIEC](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx)アウトソーシング テクノロジ サービス IT 検査ハンドブックで詳細に説明されている検証と監視の手順も使用してください。

## <a name="microsoft-and-ffiec"></a>Microsoft と FFIEC

Microsoft Azure、Microsoft Power BI、および Microsoft Office 365 は、金融サービス機関向けのクラウド サービスの提供に関する厳しい要件を満たして構築されています。 サポートの一環として、情報技術に関する FFIEC 監査要件への準拠と、FFIEC コンプライアンスの義務を遵守する際に Azure SOC 構成証明を使用する機能に関するガイダンスを提供します。

金融機関の顧客が Azure に対する FFIEC コンプライアンス要件を満たすのを支援するために、Microsoft は [FFIEC](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint)規制サービスワークロード用の Azure Security and Compliance Blueprint を開発しました。 Azure クラウド サービスの使用に関するガイダンスと、お客様が FFIEC 要件とリスク評価ガイドラインに準拠する際の考慮事項について説明します。

FFIEC 要件への準拠を支援するために、Microsoft クラウド サービスは、独立した CPA 企業によって作成された [SOC](offering-SOC.md) 構成証明レポートを提供します。 たとえば、SOC 1 Type 2 の構成証明は、SAS 70 に取って代わる AICPA SSAE 18 標準 (AT-C Section 105 を参照) に基づいており、財務報告の特定のコントロールに関する報告に適しています。 SOC レポートには、指定された監視期間中に関連するコントロール目標を達成する際の Microsoft コントロールの有効性に関する監査者の意見が含まれます。 金融機関は、Azure、Power BI、および Office 365 に展開された資産に対する FFIEC 固有のコンプライアンス義務を遵守するときに、この正式な監査を使用できます。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure](https://aka.ms/AzureCompliance)
- Intune
- [Office 365](https://go.microsoft.com/fwlink/p/?LinkID=2077751)
- Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに搭載されているサービス)

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

Azure および Office 365 SOC 構成証明レポート。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**SoC 標準に準拠している Microsoft を使用して、教育機関の FFIEC コンプライアンスの義務を果たできますか?**

これらの義務を果たすために、Microsoft は上記の SOC 基準への準拠に関する具体的な情報を提供します。 ただし、最終的には、サービスが教育機関に適用される特定の法律および規制に準拠するかどうかを判断する必要があります。 FFIEC は、'監査レポートまたはレビューのユーザーは、TSP の内部制御環境を検証するために、レポートに含まれる情報だけに依存しろというのではないというアドバイスも示しています。 FFIEC IT 検査ハンドブックのアウトソーシング テクノロジの小[](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx)冊子で詳しい説明に従って、他の検証および監視手順を使用する必要があります。

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

## <a name="resources"></a>リソース

- [連邦金融機関審査会 (FFIEC)](https://www.ffiec.gov/)
- [米国におけるクラウド コンピューティングと規制の原則のコンプライアンス マップ](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- [FFIEC 監査 IT 検査ハンドブック](https://ithandbook.ffiec.gov/it-booklets/audit.aspx)
- [FFIEC アウトソーシング テクノロジ サービス IT 検査ハンドブック](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx)
- [Azure Security and Compliance FFIEC Financial Services Blueprint](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint)

## <a name="other-microsoft-resources-for-financial-services"></a>金融サービス向けのその他の Microsoft リソース

- [Microsoft 金融サービス コンプライアンス プログラム](https://www.microsoft.com/download/details.aspx?id=55332)
- [Azure における金融サービス コンプライアンス](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Microsoft 法人向けクラウド サービスおよび金融サービス](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [クラウド コンピューティングの共同責任](https://aka.ms/sharedresponsibility)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
