---
title: 米国商品先物取引委員会 (CFTC) 規則 1.31(c-d)
description: 独立した評価会社は、Azure および Office 365 が金融機関が CFTC Rule 1.31 のレコード保持および不変ストレージ要件を満たすのに役立つ可能性を検証しました。
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
ms.openlocfilehash: 474cd04d98dc91668e48d1999f4fbd91d81523ec
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121756"
---
# <a name="commodity-futures-trading-commission-cftc-rule-131c-d-united-states"></a>米国商品先物取引委員会 (CFTC) 規則 1.31(c-d)

## <a name="about-cftc-rule-13c-d"></a>CFTC Rule 1.3(c-d) について

米国 [連邦](https://www.cftc.gov/) 政府機関である商品先物取引委員会 (CFTC) は、商品先物市場とオプション市場、最近ではスワップ市場を規制しています。  
  
CFTC ルール 1.31 は、SEC Rule 17a-4(f) で確立されたレコード保持要件を定義します。 さらに、電子記録は 5 年間保持する必要があります。また、最初の 2 年間は元のレコードに "容易にアクセス可能" に保ち、保持期間中は委員会または米国の検査部門が検査できるように指定しています。  
  
2017 年 [、CFTC](https://www.cftc.gov/sites/default/files/idc/groups/public/@lrfederalregister/documents/file/2017-11014a.pdf)はレコード保持規則の修正と最新化を行い、記録の管理方法の柔軟性を高め、より基本的で基本的な基準を採用しました。 この変更により、ルールは中立的なテクノロジになります。これにより、規制対象エンティティは、"レコードキーピング プロセスの信頼性を確保する" というセーフガードを維持しながら、ビジネスに最も適したテクノロジを選択できます。 改訂されたルールは、組織が元のレコードを 2 年間保持する要件を削除しますが、CFTC と SEC の両方によって規制されている企業の慣行を規定する 5 年間のメンテナンス期間を保持します。

## <a name="microsoft-and-cftc-rule-131c-d"></a>Microsoft および CFTC Rule 1.31(c-d)

金融サービスのお客様は、世界で最も厳しく規制されている業界の 1 つであり、金融取引の保持や、消えられない変更できない状態での関連する通信など、複雑な規定の対象となります。 最も規定の 1 つは、米国商品先物取引委員会 (CFTC) の規則 1.31 です。これは、電子ストレージ メディアで書籍や記録を保持する規制対象エンティティに対する厳しい要件を規定しています。 保存されるレコードは、指定された保持期間が終了するまで変更または削除する機能を備えず、改ざん防止する必要があります。 ポリシー ロック付き Microsoft Azure 不変 BLOB ストレージと保持ロック付き Microsoft Office 365 は、金融機関が CFTC Rule 1.31(c-d) のストレージ要件を満たすのに役立ちます。

### <a name="microsoft-azure"></a>Microsoft Azure

CFTC Rule 1.31(c-d) に対する Azure コンプライアンスを評価するために、Microsoft はレコード管理と情報ガバナンスを専門とする独立した評価会社である Cohasset Associates を保持しました。 結果のレポートでは [、CFTC 1.31 (c–(d) コンプライアンス評価: Microsoft Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)、Cohasset は、時間ベースの BLOB を消去不可で書き換えできない (WORM) 形式で保持するために使用される場合に、ポリシー ロック オプションを使用した Azure [Immutable Blob](/azure/storage/blobs/storage-blob-immutable-storage) Storage が CFTC ルールの原則ベースの要件を満たしていることを検証しました。 各 BLOB (レコード) は、必要な保持期間が終了し、関連する法的情報保留が解放されるまで、変更、上書き、または削除から保護されます。 機密性の高いワークロードを持つソフトウェア プロバイダーとパートナーは、Azure 不変 Blob ストレージをレコード保持の 1 つの店舗クラウド ソリューションとして利用できます。 金融機関は、コンプライアンスを維持しながら、これらの機能を活用して独自のアプリケーションを構築できます。

### <a name="microsoft-365"></a>Microsoft 365

[CFTC 1.31(c)-(d)](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d)要件に関して、Cohasset は、Microsoft 365 に、ブローカー販売業者を含む規制対象顧客がレコード保持の SEC 要件に準拠する方法でデータを保存できるアーカイブ機能が含まれると検証しました。 Microsoft 365 の保持機能は、電子メール、ボイスメール、共有ドキュメント、インスタント メッセージ、サード パーティデータなど、幅広いデータを保持するのに役立ちます。 特に、Microsoft 365 のアーカイブを使用すると、グローバルまたは詳細なメッセージング保持ポリシーを設定して、定義された期間以降のデータを書き換え不可で消去できない形式で保存できます。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure](https://aka.ms/AzureCompliance)
- [Office 365](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

[Azure & CFTC Rule 1.31: SEC 17a-4(f) & CFTC 1.31(c-d) Compliance Assessment of Azure Storage

[Office 365 & CFTC Rule 1.31: archiving in Office 365, data retention, and SEC Rule 17a-4 compliance

## <a name="how-to-implement"></a>実装方法

- [金融サービス規制](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides): クラウド コンピューティングと Microsoft オンライン サービスに関する米国の主要な規制原則のコンプライアンス マップ。
- [リスク評価およびコンプライアンス ガイド](https://aka.ms/RiskGovernanceGuide): Microsoft クラウド サービスのリスク評価および規制機関の通知のガバナンス モデルを作成します。
- [金融ユース ケース](/azure/industry/financial/): 金融サービス向けの Azure ソリューションを構築するためのユース ケースの概要、チュートリアル、およびその他のリソース。

## <a name="resources"></a>リソース

- [Microsoft 金融サービス コンプライアンス プログラム](https://aka.ms/FSCP-Print)
- [Microsoft 法人向けクラウド サービスおよび金融サービス](https://www.microsoft.com/trustcenter/cloudservices/financialservices)
- [Azure における金融サービス コンプライアンス](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Microsoft Office 365 アイテム保持ポリシー](/office365/securitycompliance/retention-policies)
- [Microsoft 金融サービスのブログ](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
