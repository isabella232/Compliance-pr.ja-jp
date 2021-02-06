---
title: 米国国防総省取得規則補足 (DFARS)
description: Microsoft Azure Government は、Defense Federal Acquisition Regulation (DFARS) の要件をサポートしています。
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
ms.openlocfilehash: a969d446296605fd3ea9b1d7b9225009e99f4471
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121286"
---
# <a name="defense-federal-acquisition-regulation-supplement-dfars"></a>米国国防総省取得規則補足 (DFARS)

## <a name="dfars-overview"></a>DFARS の概要

2016 年 10 月 21 日、国防総省 (DoD) は、米国国防総省取得規則 (DFARS) を修正し、情報システムが対象となる防御情報 (CDI) を処理、保存、または送信する防御請負業者に対して保護とサイバー インシデント報告の義務を課す最終規則を発行しました。  
  
最後の DFARS 条項 252.204-7012 (対象となる防御情報とサイバー インシデントレポートの保護) では、サイバー インシデント報告の要件とクラウド サービス プロバイダーに関する追加の考慮事項を含むセーフガードを指定しています。 DFARS 252.204-7012 では、すべての DoD 請負業者と防御産業基盤は、適切なセキュリティのための DFARS 要件に準拠する必要があります (2017 年 12 月 31 日より早く、

## <a name="microsoft-and-dfars"></a>Microsoft と DFARS

Microsoft Government Cloud サービスは、米国防総省の請負業者のお客様が、クラウド サービス プロバイダーに適用される 252.204-7012 の DFARS 条項に列挙されている DFARS 要件を満たすのに役立ちます。 防御請負業者が契約で DFARS 条項 252.204-7012 に準拠する必要がある場合、Microsoft は Azure Government および Office 365 U.S. Government Defense サービスのクラウド サービス プロバイダーに適用される要件をサポートできます。 どちらのサービスも、お客様が国防総省セキュリティ要件ガイドへの L5 認定を通じて DFARS 7012 条項に準拠するために必要な機能のサポートを示しています。  
  
Azure のセキュリティとコンプライアンスのブループリントを使用して DFARS の展開を加速する方法について説明します [。Azure をダウンロードする — Blueprint DFARS Customer Responsibilities Matrix](https://servicetrust.microsoft.com/ViewPage/Blueprint?command=Download&downloadType=Document&downloadId=7ed1b47c-b180-4323-9aec-21712d54b167&docTab=fc060920-cdb8-11e7-bacf-0bf52b09d912_DoD_Blueprint)

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

DoD 影響レベル 5 の対象サービス

- [Azure および Azure Government](https://aka.ms/AzureCompliance)
- [Office 365 U.S. Government and Office 365 U.S. Government Defense](https://go.microsoft.com/fwlink/p/?LinkID=2077751)

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

- [Microsoft Cloud Services Authorizations](https://marketplace.fedramp.gov/index.html#/products?status=Compliant&sort=productName)
- [2017 年 3 月 3 日に署名された Azure P-ATO レター](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=94ff5b42-4077-4612-8cf7-3194ded323dc&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)
- [その他の監査レポートを見る](https://aka.ms/auditreports)

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**Microsoft Azure Government および 365 U.S. Government Defense Officeサポートされている DFARS 要件は何ですか?**

Azure Government および Office 365 U.S. Government Defense は、クラウド サービス プロバイダーに適用される 252.204-7012 の DFARS 条項に列挙されている DFARS 要件に従って、当社の防御技術基盤および防御請負業者のお客様が DFARS 要件を満たします。

**独立評価者は、Azure Government および Office 365 U.S. Government Defense が DFARS 要件をサポートしていることを検証しましたか?**

はい。第三者評価機関は、Azure Government および Office 365 U.S. Government Defense クラウド サービスが DFARS 条項 252.204-7012 (未分類の制御された技術情報の保護) の該当する要件を満たしていることを証明しています。

**CUI (Controlled Unclassified Information) と対象となる防御情報 (CDI) の関係は何ですか?**

CUI は、法律、規制、または政府全体のポリシーに従ってコントロールを保護または普及する必要がある情報です。 [CUI レジストリは、承認済](https://www.archives.gov/cui/registry/category-list.html)みの CUI カテゴリとサブカテゴリを識別します。

CDI は、技術的な情報または (CUI レジストリに記載されている) その他の情報を管理します。この情報は、保護または流用の制御を必要とします。次のいずれかです。

- 契約、タスク注文、または配信注文でマークまたは他の方法で識別され、契約のパフォーマンスに関連して DoD によって、または DoD の代わりに契約者に提供されます。
- 契約のパフォーマンスをサポートするために、契約者によって、または代理で収集、開発、受信、送信、使用、または保存される

**すべての Microsoft サービスは、DFARS 規制の下で「対象となる防御情報」に適用される「適切なセキュリティ」要件を満たしていますか?**

2016 年 10 月、国防総省 (DoD) は、情報システムを通じて 「対象となる防御情報」を処理、保存、または送信する DoD 請負業者全員に適用される、国防総省入手規則補足 (DFARS) 条項を実施する最終的な規則を規定しました。 この規則では、このようなシステムは、NIST SP 800-171、非組織の非分類[](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-171.pdf)情報の保護、または DoD 契約責任者によって承認された「代替の、同じように効果的なセキュリティ対策」に定めるセキュリティ要件を満たす必要があるという定めがあります。 また、DoD 請負業者が外部のクラウド サービス プロバイダーを使用して対象となる防御情報を処理、保存、または送信する場合、そのようなプロバイダーは FedRAMP Moderate ベースラインと同等のセキュリティ要件を満たす必要があります。

次の Microsoft クラウド サービスは、FedRAMP の中程度の承認を受け、DFARS (Azure Government、Dynamics 365 U.S. Government、Office 365 U.S. Government、および Office 365 U.S. Government Defense) に対して適切です。

また、Microsoft は FedRAMP 認定の境界外の製品を提供しています。DoD の請負業者が「対象となる防御情報」の処理、保存、または送信に使用する可能性がある製品は、コンプライアンスの期限である 2017 年 12 月 31 日を満たすためにレビューを実施しています。 Microsoft は、DFARS 関連条項を満たすために、これらの内部および顧客向けサービスが NIST SP 800-171 または許容されるセキュリティ同等物に準拠する方法を文書化する取り組みです。

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

## <a name="resources"></a>リソース

- [米国国防総省取得規則補足 (DFARS)](https://www.acq.osd.mil/dpap/dars/dfarspgi/current/index.html)
- [Microsoft Cloud for Government](https://enterprise.microsoft.com/industries/government/start-your-microsoft-cloud-for-government-trial-today)
- [オンライン サービスの使用条件](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=31)
- [制御された未分類情報 (CUI)](https://www.archives.gov/cui/registry/category-list)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
