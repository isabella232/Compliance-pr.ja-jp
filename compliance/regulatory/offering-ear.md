---
title: 米国輸出管理規則 (EAR)
description: Microsoft クラウド サービスは、米国輸出管理規則 (EAR) の対象となるお客様がコンプライアンス要件を満たし、輸出管理リスクを管理するのに役立ちます。
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
ms.openlocfilehash: 859067495b6811b2264ab3a379f305d428771bce
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160116"
---
# <a name="us-export-administration-regulations-ear"></a>米国輸出管理規則 (EAR)

## <a name="about-the-ear"></a>EAR について

米国商務省は、産業セキュリティ局 (BIS) を通じて輸出管理規則 [(EAR) を施行しています](https://www.bis.doc.gov/)。 EAR は、商用および軍事目的と特定の防御アイテムの両方に使用できる「デュアル使用」アイテムを含む、ほとんどの商用製品、ソフトウェア、およびテクノロジの輸出と再輸出に関する管理を広く管理し、課します。

BIS ガイダンスでは、データまたはソフトウェアがクラウドにアップロードされた場合、またはユーザー ノード間で転送される場合、クラウド プロバイダーではなく顧客が、そのデータまたはソフトウェアの転送、保存、およびアクセスが EAR に準拠していることを確認する責任を負う「輸出者」です。

[BIS](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file)によると、エクスポートとは、保護されたテクノロジまたは技術データを外国の宛先に転送すること、または米国の外国の人物 (みなしエクスポートとも呼ばれます) へのリリースを指 *します*。 EAR は大まかに次の規則を適用します。

- 米国からのエクスポート。
- 米国起源のコンテンツのデ ミニミス部分を超える米国起源のアイテムと特定の外部起源アイテムを再エクスポートまたは再送信します。
- 他の国からの個人への転送または開示。

EAR の対象となるアイテムは、各アイテムに一意のエクスポート コントロール分類番号 (ECCN) が割り当てられているコマース コントロール リスト [(CCL) に記載されています](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn)。 CCL に記載されていないアイテムは EAR99 として指定され、ほとんどの EAR99 商用製品ではライセンスをエクスポートする必要がなされません。 ただし、アイテムの宛先、エンド ユーザー、またはエンド 使用によっては、EAR99 アイテムでも BIS エクスポート ライセンスが必要な場合があります。

2016 年 6 月に公開された最終規則は、FIPS 140-2 検証済みの暗号化モジュールを使用してエンドツーエンドで暗号化され、軍事禁輸国またはロシア連邦に意図的に保存されていない場合、未分類の技術データとソフトウェアの伝送と保存にも EAR ライセンス要件が適用されないと明らかにしました。 [](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations)

## <a name="microsoft-and-the-ear"></a>Microsoft と EAR

Microsoft のテクノロジ、製品、およびサービスは、米国輸出管理規則 (EAR) の対象となります。 EAR、Microsoft Azure、Microsoft Azure Government、および Microsoft Office 365 Government (GCCHigh および DoD 環境) のコンプライアンス認定は、対象となるお客様が輸出管理リスクを管理し、コンプライアンス要件を満たすのに役立つ重要な機能とツールを提供します。

EAR を適用する米国商務省は、Microsoft などのクラウド サービス プロバイダーではなく、顧客が自分の顧客データの輸出者であると見なされる立場を取っています。 ほとんどの顧客データは、EAR エクスポート制御の対象となる「テクノロジ」または「技術データ」とは見なされませんが、Microsoft のスコープ内クラウド サービスは、お客様が直面する潜在的な輸出管理リスクを管理し、大幅に軽減するために構成されています。 Microsoft は通常、対象となる顧客に対して政府機関のクラウド サービスの使用を推奨していますが、排他的ではありません。 適切な計画を立て、お客様は以下のツールと独自の内部手順を使用して、米国の輸出管理に完全に準拠することができます。

- **データの場所に関するコントロール**。 お客様は、データの保存場所を可視化し、ストレージを制限するための堅牢なツールにアクセスできます。 したがって、データが米国に保存され、管理されたテクノロジまたは技術データが米国外に転送されるのを最小限に抑える可能性があります。 さらに、顧客データは非準拠の場所に保存されません。データが 「意図的に保存される」場所に関する EAR 禁止事項と一致します。Azure データセンターは、25 グループ D:5 の国またはロシア連邦にはありません。
- **エンドツーエンドの暗号化**。 EAR で指定された物理的な記憶域の場所に対してエンドツーエンドの暗号化セーフ ハーバーを利用することで、Microsoft のスコープ内クラウド サービスは、エクスポート制御リスクから保護するのに役立つ暗号化機能を提供します。 また、転送中および[](https://aka.ms/Azure-Encryption-Overview)保存中のデータを暗号化するための幅広いオプションと、暗号化オプションの中から柔軟に選択できるオプションも提供します。
- **未承認のみなしエクスポートを防止するためのツールとプロトコル**。 また、暗号化を使用すると、米国以外のユーザーが暗号化されたデータにアクセスできる場合でも、暗号化されている間にデータを読み取りまたは理解できない場合は何も明らかにされません。したがって、制御されたデータの 'release" はありません。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- [Azure および Azure Government](https://aka.ms/AzureCompliance)
- [Office 365 Government (GCC-High および DoD)](https://aka.ms/Office-365-Export-Controls)
- Intune

## <a name="how-to-implement"></a>実装方法

米国の輸出管理の概要と、EAR に基づく義務を評価する顧客向けガイダンス。

- [Azure](https://aka.ms/Azure-Export-Controls)
- [Office 365](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**Microsoft クラウド サービスを使用する場合、エクスポートコントロールに準拠するために何を行う必要がありますか?**

EAR では、データが Microsoft クラウドなどのクラウド サーバーにアップロードされると、クラウド サービス プロバイダーではなく、データを所有している顧客が輸出者と見なされます。 そのため、データの所有者 (つまり、Microsoft のお客様) は、Microsoft クラウドの使用が米国の輸出管理に影響を与える可能性がある方法を慎重に評価し、使用または保存するデータが EAR コントロールの対象になる可能性があるかどうかを判断し、その場合は、どのコントロールが適用されるのかを判断する必要があります。 [Azure](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)とクラウド サービス[Office 365、米国](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI)の輸出管理に完全に準拠する方法について説明します。

**Microsoft のテクノロジ、製品、およびサービスは、EAR の対象ですか?**

ほとんどの Microsoft テクノロジ、製品、およびサービスは、次のいずれかです。

- EAR の対象となされないので、コマース コントロール リストに含め、ECCN はありません。
- または、MICROSOFT による自己分類の対象となる EAR99 または 5D992 Mass Market であり、ライセンス不要 (NLR) としてライセンスなしで非禁輸国にエクスポートできます。

つまり、いくつかの Microsoft 製品には、ライセンスが必要な場合と必要としない ECCN が割り当てられている場合があります。 輸出目的で適切なライセンスの種類と対象国を決定するには、EAR または法律顧問に相談してください。

**武器規制 (ITAR) における EAR と国際トラフィックの違いは何ですか?**

最も広範なアプリケーションを持つ米国の主要なエクスポート コントロールは、米国商務省によって管理される EAR です。 EAR は、商用アプリケーションと軍事アプリケーションの両方を持つデュアル使用アイテム、および純粋に商用アプリケーションを持つアイテムに適用できます。

また、米国には、最も機密性の高いアイテムとテクノロジを管理する ITAR などの、より専門的で専門的な輸出管理規制があります。 米国国務省によって管理され、関連する技術データを含む多くの軍事、防衛、およびインテリジェンスアイテム (「防衛記事」とも呼ばれる) の輸出、一時的な輸入、再輸出、および転送に対して制御を課します。

## <a name="resources"></a>リソース

- [Microsoft 製品のエクスポート: 概要](https://www.microsoft.com/exporting/overview.aspx)
- [Microsoft 製品のエクスポート: FAQ](https://www.microsoft.com/exporting/faq.aspx)
- [Microsoft 製品のエクスポート: 製品参照](https://www.microsoft.com/exporting/exporting-information.aspx)
- [暗号化に関するエクスポートの制限](/windows/uwp/security/export-restrictions-on-cryptography)
- [Microsoft および FIPS 140-2](offering-fips-140-2.md)
- [Microsoft と ITAR](offering-itar.md)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
