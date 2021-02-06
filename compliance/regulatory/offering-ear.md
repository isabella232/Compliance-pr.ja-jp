---
title: 米国輸出管理規則 (EAR)
description: Microsoft クラウド サービスは、米国輸出管理規制 (EAR) の対象となるお客様がコンプライアンス要件を満たして、輸出管理リスクを管理するのに役立ちます。
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
ms.openlocfilehash: fbc8166770a3ad2539264bbf76319116a2c306a9
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120006"
---
# <a name="us-export-administration-regulations-ear"></a>米国輸出管理規則 (EAR)

## <a name="about-the-ear"></a>EAR について

米国商務省は、米国産業安全局 (BIS) を通じて輸出管理規制 [(EAR) を実施しています](https://www.bis.doc.gov/)。 EAR は、ほとんどの商用商品、ソフトウェア、およびテクノロジの輸出と再エクスポートに広範に制御を課します。これらの項目には、商用および商業目的と商業目的、および特定の防御項目の両方に使用できる "デュアル使用" 項目が含まれます。

BIS ガイダンスでは、データまたはソフトウェアがクラウドにアップロードされた場合、またはユーザー ノード間で転送される場合、顧客はクラウド プロバイダーではなく、そのデータまたはソフトウェアの転送、保管、およびアクセスが EAR に準拠していることを保証する責任を負う 「エクスポート者」です。

[BIS](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file)によると、エクスポートとは、保護された技術または技術データを国外の宛先に転送すること、または米国内の外部の人物 (指定されたエクスポートとも呼ばれる) にリリースすること *のことです。* EAR は、次の条件を広く管理します。

- 米国からエクスポートします。
- 米国の原点のアイテムと、米国の原点コンテンツの最小限の部分を超える特定の外部原点アイテムを再エクスポートまたは再送信します。
- 他の国からの個人への転送または開示。

EAR の対象となる項目は、Commerce Control List (CCL) で確認できます。各項目には、一意のエクスポートコントロール分類番号 [(ECCN)](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn)が割り当てられます。 CCL に記載されていない項目は、EAR99 として指定され、ほとんどの商用製品の EAR99 では、ライセンスをエクスポートする必要はなされません。 ただし、製品の宛先、エンド ユーザー、または使用終了によっては、たとえ EAR99 アイテムに対しても BIS エクスポート ライセンスが必要な場合があります。

2016 年 6 月に公開された最終規則では、FIPS 140-2 検証済み暗号化モジュールを使用してエンドツーエンドで暗号化され、意図的に禁則された国またはロシアのフェデレーションに保存されていない場合、未分類の技術データおよびソフトウェアの伝送と保管にも、EAR ライセンス要件は適用されないと明確にしました。 [](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations)

## <a name="microsoft-and-the-ear"></a>Microsoft と EAR

Microsoft のテクノロジ、製品、およびサービスは、米国輸出管理規則 (EAR) の対象です。 EAR、Microsoft Azure、Microsoft Azure Government、および Microsoft Office 365 Government (GCCHigh および DoD 環境) のコンプライアンス認証は提供されませんが、対象となるお客様が輸出管理リスクを管理し、コンプライアンス要件を満たすために役立つ重要な機能とツールを提供しています。

米国商務省 (EAR を適用) は、Microsoft などのクラウド サービス プロバイダーではなく、お客様が独自の顧客データをエクスポートしたと見なされる立場に位置付けされています。 お客様のほとんどのデータは、"テクノロジ" や "技術データ" とは見なされませんが、MICROSOFT の対象クラウド サービスは、お客様が直面する潜在的な輸出管理リスクを管理し、大幅に軽減するのに役立つ構造です。 Microsoft は一般に、対象となるお客様に対して政府機関向けクラウド サービスの使用を推奨していますが、排他的ではありません。 適切な計画により、お客様は次のツールと独自の内部手順を使用して、米国の輸出管理に完全に準拠できます。

- **データの場所に関するコントロール**。 お客様は、データの保存場所を確認し、堅牢なツールにアクセスしてストレージを制限できます。 したがって、データが米国に保存され、制御された技術や技術データが米国外に転送されるのを最小限に抑える可能性があります。 さらに、顧客データは非準拠の場所に保存されません。データが「意図的に保存」されている場所に関する EAR の禁止事項と一致します。Azure データセンターは、25 グループ D:5 の国またはロシア連邦に存在しない。
- **エンドツーエンドの暗号化**。 MICROSOFT のスコープ内クラウド サービスは、EAR で指定された物理的な保管場所に対してエンドツーエンドの暗号化セーフ を利用することで、エクスポート制御リスクから保護できる暗号化機能を提供します。 また、送信中および[](https://aka.ms/Azure-Encryption-Overview)保存中のデータを暗号化するためのさまざまなオプションと、暗号化オプションの中から選択できる柔軟性を顧客に提供します。
- **承認されていないと見なされたエクスポートを防ぐためのツールとプロトコル**。 暗号化を使用すると、米国以外のユーザーが暗号化されたデータにアクセスできる場合でも、暗号化されている間にデータを読み取りまたは理解できない場合は何も明らかにならないので、EAR の下で見なされるエクスポート (または再エクスポートと見なされる) 可能性から保護できます。したがって、制御されたデータの "解放" はありません。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure および Azure Government](https://aka.ms/AzureCompliance)
- [Office 365 Government (GCC-High および DoD)](https://aka.ms/Office-365-Export-Controls)
- Intune

## <a name="how-to-implement"></a>実装方法

米国の輸出管理の概要と、お客様が EAR に基づく義務を評価するためのガイダンス。

- [Azure](https://aka.ms/Azure-Export-Controls)
- [Office 365](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**Microsoft クラウド サービスを使用する場合、エクスポート コントロールに準拠するには、どのような操作を行う必要がありますか。**

EAR では、データが Microsoft クラウドなどのクラウド サーバーにアップロードされると、クラウド サービス プロバイダーではなく、データを所有する顧客が、エクスポート者と見なされます。 このため、データの所有者 (つまり、Microsoft のお客様) は、Microsoft クラウドの使用が米国の輸出管理に与える影響を慎重に評価し、使用または保存するデータが EAR コントロールの対象となる可能性があるかどうかを判断する必要があります。また、適用される場合は、どのコントロールが適用されるのかを判断する必要があります。 Azure および [Office](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers) [365](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI) クラウド サービスが、お客様が米国のエクスポート コントロールに完全に準拠する方法について説明します。

**Microsoft のテクノロジ、製品、およびサービスは、EAR の対象ですか?**

ほとんどの Microsoft テクノロジ、製品、サービスは、次のいずれかです。

- EAR の対象ではなされていないので、Commerce Control List には含め、ECCN はありません。
- または、MICROSOFT による自己分類の対象となる EAR99 または 5D992 Mass Market の対象であり、ライセンス不要 (NLR) としてライセンスなしで非禁用国にエクスポートされる場合があります。

しかし、いくつかの Microsoft 製品には、ライセンスが必要な場合と不要な ECCN が割り当てられている場合があります。 輸出の目的で適切なライセンスの種類と対象となる国を決定するには、EAR または法律弁護士に相談してください。

**EAR と武器国際交通規則 (ITAR) の違いは何ですか?**

最も広範なアプリケーションを持つ主要な米国のエクスポート コントロールは、米国商務省が管理するE EAR です。 EAR は、商用アプリケーションと商用アプリケーションの両方を持つデュアル用途のアイテム、および純粋に商用アプリケーションを持つアイテムに適用されます。

また、米国には、最も機密性の高いアイテムとテクノロジを管理する ITAR などの、個別の、より専門的な輸出管理規制があります。 米国国務省によって管理され、関連する技術データを含む多くの国防総省、およびインテリジェンス項目 ("防御記事" とも呼ばれる) のエクスポート、一時インポート、再エクスポート、転送に対して制御を課します。

## <a name="resources"></a>リソース

- [Microsoft 製品のエクスポート: 概要](https://www.microsoft.com/exporting/overview.aspx)
- [Microsoft 製品のエクスポート: FAQ](https://www.microsoft.com/exporting/faq.aspx)
- [Microsoft 製品のエクスポート: 製品の参照](https://www.microsoft.com/exporting/exporting-information.aspx)
- [暗号化に関するエクスポートの制限](/windows/uwp/security/export-restrictions-on-cryptography)
- [Microsoft および FIPS 140-2](offering-fips-140-2.md)
- [Microsoft と ITAR](offering-itar.md)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
