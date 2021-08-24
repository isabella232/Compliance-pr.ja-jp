---
title: 金融業界規制当局 (FINRA) ルール 4511(c) 米国
description: 独立した評価会社は、Azure と Office 365が FINRA Rule 4511 レコードの保持と不変のストレージ要件を満たすのに役立つ可能性を検証しました。
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
ms.openlocfilehash: e5c253fe5a2b4995dffc7059717d74fecdc73935
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "58479769"
---
# <a name="financial-industry-regulatory-authority-finra-rule-4511c-united-states"></a>金融業界規制当局 (FINRA) ルール 4511(c) 米国

## <a name="about-finra-rule-4511"></a>FINRA ルール 4511 について

金融 [業界規制当局 (FINRA)](https://www.finra.org/#/) は、米国で 4,500 社を超える証券会社を監督する最大の独立機関規制証券会社です。 これは、米国議会によって「ブローカー-ディーラー業界が公平かつ正直に運営されるのを確認することで、アメリカの投資家を保護する」という承認を受けた。

2011 年、米国セキュリティおよび Exchange 委員会 (SEC) は、電子ストレージ メディア上の書籍およびレコードの保持に関する SEC ルールの FINRA 導入を承認しました。 [FINRA ルール 4511(c)](https://www.finra.org/sites/default/files/NoticeDocument/p123548.pdf)は、「FINRA ルールに従って行う必要があるすべての書籍およびレコードは、SEA (証券Exchange法) ルール 17a-4 に準拠する形式およびメディアで保持される必要があります」と指定します。

また、FINRA ルール 4511(c) では、該当する FINRA または SEA ルールの下で指定された保持期間がない書籍およびレコードを少なくとも 6 年間保持する必要があります。 実質的に、ブックとレコードがアカウントに関連する場合、保持期間はアカウントの閉鎖後 6 年と義務付けされます。 それ以外の場合、保持期間は、そのような書籍およびレコードが作成された後の 6 年間です。

## <a name="microsoft-and-finra-rule-4511c"></a>Microsoft および FINRA ルール 4511(c)

世界で最も厳しく規制されている業界の 1 つを代表する金融サービスの顧客は、金融取引の保持や、消えられない変更不可の状態での関連する通信など、複雑な規定の対象となります。 その中には、電子ストレージ メディアに書籍やレコードを保持する規制対象の厳しい要件を規定する金融業界規制当局 (FINRA) の規則 4511 があります。 保存されるレコードは、指定された保持期間の後まで変更または削除する機能を持つ改ざん防止である必要があります。

Microsoft Azureポリシー ロックStorageと Microsoft Office 365 保持ロックを使用した不変 BLOB の使用は、金融機関が FINRA ルール 4511(c) の不変ストレージ要件を満たすのに役立ちます。

## <a name="microsoft-azure"></a>Microsoft Azure

Azure の FINRA Rule 4511(c) への準拠を評価するために、Microsoft はレコード管理と情報ガバナンスを専門とする独立した評価会社である Cohasset Associates を保持しました。 結果のレポートである[SEC 17a-4(f) & CFTC 1.31 (c-d)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)コンプライアンス評価: Microsoft Azure Storage は、SEC ルール 17a-4(f) の形式およびメディア要件に従う FINRA ルール 4511(c) に対する Azure 準拠を包含します。

Cohasset は、時間ベースの BLOB を消去不可で書き換えできない (WORM) 形式で保持するために使用される場合に、ポリシー ロック オプションを指定した[Azure Immutable Blob Storage](/azure/storage/blobs/storage-blob-immutable-storage)が関連する FINRA ストレージ要件を満たしていることを検証しました。 各 BLOB (レコード) は、必要な保持期間が満了し、関連付けられた法的保持が解放されるまで、変更、上書き、または削除から保護されます。

機密性の高いワークロードを持つソフトウェア プロバイダーとパートナーは、レコード保持と不変ストレージのワンストップ ショップ クラウド ソリューションとして Azure Immutable Blob Storage を利用できます。 金融機関は、コンプライアンスを維持しながら、これらの機能を利用して独自のアプリケーションを構築できます。

## <a name="microsoft-365"></a>Microsoft 365

[FINRA Rule 4511(c)](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d)の要件に対して、Cohasset は Microsoft 365 にアーカイブ機能が含まれており、ブローカー-ディーラを含む規制対象のお客様が、レコード保持の SEC 要件に準拠する方法でデータを保存できると検証しました。 メール、ボイスメールMicrosoft 365共有ドキュメント、インスタント メッセージ、サードパーティデータなど、さまざまなデータを保持するのに役立ちます。 特に、Microsoft 365 でのアーカイブを使用すると、ユーザーは、グローバルまたは詳細なメッセージング保持ポリシーを設定して、定義された期間以降のデータを書き換え不可の消去可能な形式で保存できます。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

### <a name="azure--finra-rule-4511c"></a>Azure & FINRA ルール 4511(c)

- [SEC 17a-4(f) & CFTC 1.31 (c-d) コンプライアンス評価のAzure Storage](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)

### <a name="office-365--finra-rule-4511c"></a>Office 365 & FINRA ルール 4511(c)

[アーカイブ、Office 365保持、および SEC ルール 17a-4 準拠](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)

## <a name="how-to-implement"></a>実装方法

- **金融サービス規制**: クラウド コンピューティングおよび Microsoft オンライン サービスに関する米国の主要な規制原則のコンプライアンス マップ。 [詳細情報](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- **リスク評価およびコンプライアンス ガイド**: Microsoft クラウド サービスのリスク評価および規制機関の通知のガバナンス モデルを作成します。 [詳細情報](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- **金融ユース ケース**: 金融サービス向けの Azure ソリューションを構築するためのユース ケースの概要、チュートリアル、およびその他のリソース。 [詳細情報](/azure/industry/financial/)

## <a name="resources"></a>リソース

- [Microsoft 金融サービス コンプライアンス プログラム](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Microsoft 法人向けクラウド サービスおよび金融サービス](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Azure における金融サービス コンプライアンス](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Azure 金融サービス クラウド リスク評価ツール](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office 365アイテム保持ポリシー](/office365/securitycompliance/retention-policies)
- [Microsoft 金融サービスのブログ](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
