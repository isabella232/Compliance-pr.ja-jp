---
title: コモディティ先物取引委員会 (CFTC) ルール 1.31(c-d) 米国
description: 独立した評価会社は、Azure と Office 365が CFTC ルール 1.31 レコードの保持と不変のストレージ要件を満たすのに役立つ可能性を検証しました。
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
ms.openlocfilehash: 8bb9f380d57e932576c969f10512f508de7c6ada
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160879"
---
# <a name="commodity-futures-trading-commission-cftc-rule-131c-d-united-states"></a>コモディティ先物取引委員会 (CFTC) ルール 1.31(c-d) 米国

## <a name="about-cftc-rule-13c-d"></a>CFTC ルール 1.3(c-d) について

米国 [の](https://www.cftc.gov/) 独立機関であるコモディティ先物取引委員会 (CFTC) は、コモディティ先物とオプション市場、さらに最近ではスワップ市場を規制しています。  
  
長年の CFTC ルール 1.31 は、SEC ルール 17a-4(f) によって確立されたレコード保持要件を定義します。 さらに、電子記録を 5 年間保持し、最初の 2 年間は元のレコードを "容易にアクセス可能" に保ち、保持期間全体の間、委員会または米国司法省による検査を受け入れ可能にすることが指定されています。  
  
2017 年 [、CFTC](https://www.cftc.gov/sites/default/files/idc/groups/public/@lrfederalregister/documents/file/2017-11014a.pdf)は、レコードの保守方法に柔軟性を提供する、より少ない標準の原則に基づく標準を採用するために、レコードキーピング規則を修正し、最新化するルールを改訂しました。 この改訂により、ルールはテクノロジの中立性を高め、規制対象のエンティティは「レコードキーピング プロセスの信頼性を確保する」というセーフガードを維持しながら、ビジネスに最も適したテクノロジを選択できます。 改訂されたルールは、組織が元のレコードを 2 年間維持する要件を削除しますが、5 年間のメンテナンス期間を保持します。これは、CFTC と SEC の両方によって規制されている企業のプラクティスを調和します。

## <a name="microsoft-and-cftc-rule-131c-d"></a>Microsoft および CFTC ルール 1.31(c-d)

世界で最も厳しく規制されている業界の 1 つを代表する金融サービスの顧客は、金融取引の保持や、消えられない変更不可の状態での関連する通信など、複雑な規定の対象となります。 最も基準の 1 つは、電子ストレージ メディアで書籍やレコードを保持する規制対象エンティティに対する厳しい要件を規定する、米国商品先物取引委員会 (CFTC) の規則 1.31 です。 保存されるレコードは、指定された保持期間の後まで変更または削除する機能を持つ改ざん防止である必要があります。 Microsoft Azureポリシー ロックStorage保持ロック付き Microsoft Office 365 を使用した不変 BLOB の使用は、金融機関が CFTC ルール 1.31(c-d) のストレージ要件を満たすのに役立ちます。

### <a name="microsoft-azure"></a>Microsoft Azure

CfTC ルール 1.31(c-d) に対する Azure コンプライアンスを評価するために、Microsoft はレコード管理と情報ガバナンスを専門とする独立した評価会社である Cohasset Associates を保持しました。 結果のレポートでは[、CFTC 1.31 (c) (d)](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)コンプライアンス評価: Microsoft Azure Storage 、 Cohasset は、時間ベースの BLOB を消去不可で書き換えできない (WORM) 形式で保持するために使用される場合、ポリシー ロック オプションを使用して[Azure Immutable](/azure/storage/blobs/storage-blob-immutable-storage) Blob Storage が CFTC ルールの原則に基づく要件を満たしていることを検証しました。 各 BLOB (レコード) は、必要な保持期間が満了し、関連付けられた法的保持が解放されるまで、変更、上書き、または削除から保護されます。 機密性の高いワークロードを持つソフトウェア プロバイダーとパートナーは、レコード保持のための一Storageショップ クラウド ソリューションとして Azure Immutable Blob Storage を利用できます。 金融機関は、コンプライアンスを維持しながら、これらの機能を利用して独自のアプリケーションを構築できます。

### <a name="microsoft-365"></a>Microsoft 365

[CFTC 1.31(c)-(d)](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d)の要件に対して、Cohasset は、Microsoft 365 には、ブローカー-ディーラを含む規制対象の顧客がレコード保持の SEC 要件に準拠する方法でデータを保存できるアーカイブ機能が含まれると検証しました。 メール、ボイスメールMicrosoft 365共有ドキュメント、インスタント メッセージ、サードパーティデータなど、さまざまなデータを保持するのに役立ちます。 特に、Microsoft 365 でのアーカイブを使用すると、ユーザーは、グローバルまたは詳細なメッセージング保持ポリシーを設定して、定義された期間以降のデータを書き換え不可の消去可能な形式で保存できます。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- [Azure](https://aka.ms/AzureCompliance)
- [Office 365](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

- [Azure & CFTC ルール 1.31: SEC 17a-4(f) & CFTC 1.31(c-d) コンプライアンス評価 Azure Storage](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)
- Office 365 & CFTC ルール 1.31: Office 365、データ保持、および SEC ルール 17a-4 準拠のアーカイブ

## <a name="how-to-implement"></a>実装方法

- [金融サービス規制](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides): クラウド コンピューティングおよび Microsoft オンライン サービスに関する米国の主要な規制原則のコンプライアンス マップ。
- [リスク評価およびコンプライアンス ガイド](https://aka.ms/RiskGovernanceGuide): Microsoft クラウド サービスのリスク評価および規制機関の通知のガバナンス モデルを作成します。
- [金融ユース ケース](/azure/industry/financial/): 金融サービス向けの Azure ソリューションを構築するためのユース ケースの概要、チュートリアル、およびその他のリソース。

## <a name="resources"></a>リソース

- [Microsoft 金融サービス コンプライアンス プログラム](https://aka.ms/FSCP-Print)
- [Microsoft 法人向けクラウド サービスおよび金融サービス](https://www.microsoft.com/trustcenter/cloudservices/financialservices)
- [Azure における金融サービス コンプライアンス](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Microsoft Office 365アイテム保持ポリシー](/office365/securitycompliance/retention-policies)
- [Microsoft 金融サービスのブログ](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
