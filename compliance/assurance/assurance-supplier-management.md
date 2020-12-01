---
title: サプライヤー管理の概要
description: Microsoft 365 のサプライヤ管理について
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH'
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: e46a7d2121a3ed1f314a3126c51911248362ff59
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508840"
---
# <a name="supplier-management-overview"></a>サプライヤー管理の概要

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>Microsoft は、サプライヤーに関連するリスクをどのように管理していますか?

Microsoft は、お客様のニーズを満たすために、サードパーティ企業と提携しています。 これらのサードパーティ企業は、サプライヤーまたはサブプロセッサと呼ばれます。 Microsoft のサプライヤーのセキュリティとプライバシーについては、Microsoft と提携してオンラインサービスを提供しているすべてのサプライヤーに対する全社的な要件セットである [ベンダーセキュリティとプライバシー保証 (SSPA) プログラム](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)によって管理されています。 この SSPA プログラムには、サプライヤーベースの総合的なガバナンスと管理が備わっていますが、Microsoft 365 などの個々のビジネス単位では、サプライヤーの追加要件を維持することができます。

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>Microsoft のサプライヤーセキュリティおよびプライバシー保証 (SSPA) プログラムは、どのようにお客様のデータを保護しますか?

SSPA は、Microsoft の調達、企業の外部および法的な訴訟、および企業のセキュリティとのパートナーシップを通じて、サプライヤーが Microsoft のプライバシーとセキュリティの原則に従うようにします。 SSPA の範囲は、個人データまたは Microsoft の機密データを処理するすべてのサプライヤーを対象としています。 SSPA program の登録には、Microsoft のデータ保護要件 (DPR) に準拠しています。 DPR は、Microsoft との契約を開始する前に、サプライヤーが実装する必要があるセキュリティとプライバシーの統制で構成されています。 すべての登録されたサプライヤーは、DPR へのコンプライアンスに対して自己証明を行います。

DPR の要件は、6つの個別のデータ処理カテゴリに基づいてスコープが設定されています。サプライヤーは、SSPA での登録の一部として承認できます。 これらのカテゴリは、サプライヤーが Microsoft に提供するサービスに関連付けられているリスクを識別するために使用されます。 サプライヤーのデータ処理プロファイルは、適切なデータ保護を提供するために範囲内で考慮される DPR コントロールを決定します。 高いリスクと見なされるデータを処理するサプライヤーは、すべての DPR 要件に準拠している必要があります。また、コンプライアンスを個別に確認する必要もあります。 Microsoft 購入ツールでは、そのサプライヤーの調達を許可する前に、DPR の適用可能な部分への準拠を含む、すべてのサプライヤーの SSPA 状態を検証します。

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>Microsoft にサービスを提供するサブプロセッサの種類

「Subprocessor」とは、microsoft がプロセッサとして microsoft の個人データを処理するという、Microsoft が関与するサードパーティのことです。 Microsoft のサブプロセッサは、3つの異なるカテゴリに分類されます。 お客様が Microsoft に代わって顧客データを処理する前に、SSPA に準拠していることを示す必要があります。

- **テクノロジー** サブプロセッサーは、特定の Microsoft Online Services の提供に使用するテクノロジーを提供します。 お客様がこれらのサービスのいずれかを展開している場合、そのサービスに対して識別されたサブプロセッサは、お客様のデータまたは個人データに対して処理、保存、またはその他のアクセスを行うことができます。
- **補助** サブプロセッサは、オンラインサービスをサポート、運用、および管理するサービスを提供します。 お客様がこれらのサービスのいずれかを展開している場合、識別されたサブプロセッサによって、担当者のサービスを提供しながら、限定された顧客データや個人データへのアクセス、保存、その他のアクセスが可能です。
- **スタッフの補強** サブプロセッサには、次の2つの形式があります。どちらの場合も、個人データは microsoft の施設にのみ存在し、microsoft のシステムでは、microsoft のポリシーと監督の対象となります。

    - スタッフ増強の 1 つ目の形式は、Microsoft Online Services のサポート、運用、保守を行うスタッフを提供するものです。 これらのサブプロセッサーに対しては、その責任を果たす間に、顧客データや個人データが露呈されてしまう場合があります。 たとえば、サブプロセッサーが Microsoft のサーバー上でリモート トラブルシューティングを実行している間に、サーバーのクラッシュ ダンプ ログ内の顧客データ スニペットが露呈してしまう場合があります。
    - 2番目の形式のスタッフ強化には、microsoft online services をサポート、運用、および管理するために、Microsoft フルタイムの従業員と並行して作業するサブプロセッサが含まれます。 これらのサブプロセッサーに対しては、Microsoft のフルタイム従業員との共同業務の一環として、仮名化されたデータが露呈してしまう可能性があります。

Microsoft のデータ保護要件 (DPR) に準拠してアクセス制御を実装するには、テクノロジおよび補助サブプロセッサが必要です。 これらの要件は、Microsoft がオンラインサービス利用規約 (OST) でお客様に提供する契約のコミットメントを超える、または超過します。 スタッフ増強作業を実施するサプライヤーは、Microsoft フルタイムの従業員に対して同じアクセス制御を実施します。

## <a name="how-does-microsoft-onboard-suppliers"></a>マイクロソフトは、どのようにしてサプライヤーを選定しますか?

サードパーティのサプライヤーは、オンボードプロセスの一部として Microsoft マスターアグリーメントに署名する必要があります。 この契約は、Microsoft とそのサプライヤーとの関係を制御し、サプライヤーとの関係を一貫して管理することを保証します。 オンボードの一部として、サプライヤーは SSPA に登録し、任意のデータ処理カテゴリに対して承認される前に、該当するすべての要件を満たす必要があります。 Microsoft のビジネスユニットは、納入業者が承認されているデータ処理カテゴリと契約のデータ処理カテゴリが一致している場合にのみ、サプライヤーとの契約を作成できます。

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>Microsoft は、データを処理するサプライヤーの変更についてお客様に通知しますか?

Microsoft Online Service Data Protection 補遺 (DPA) により、Microsoft は、サブプロセッサの追加に関する通知期間について追加のコミットメントを行います。 通知タイムフレームは、Microsoft の代わりにサブプロセッサが処理するデータの種類によって異なります。 DPA に記載されているように、Microsoft はお客様のデータを処理する新しいサブプロセッサを事前に、少なくとも6か月間お客様に通知することを確約します。 その他の個人データについては、Microsoft は少なくとも30日間の通知を提供します。 メモは、 [Microsoft Online Services サブプロセッサリスト](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=926b2cf5-6b6e-43ca-9bc3-f73e961aad5f&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List)の更新プログラムによって提供されます。

## <a name="related-external-regulations--certifications"></a>関連する外部規制 & 証明書

Microsoft のオンラインサービスは、社外の規制と証明書に準拠するために定期的に監査されます。 次の表を参照して、サプライヤ管理に関連するコントロールの検証を行います。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CA-3: System interconnections <br> IA-4: 識別子管理 <br> -6: アクセス許可 <br> -7: サードパーティのスタッフのセキュリティ <br> SA-4: 買収プロセス <br> 南アメリカ-9: 外部情報システムサービス <br> SA-12: サプライチェーン保護 | 2020年9月24日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 「15.1: サプライヤーとの関係における情報セキュリティ」 | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 「15.1: サプライヤーとの関係における情報セキュリティ」 | 2020 月 2 月 22 日 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  (8.1): 下請けの PII 処理の公開 | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-53: サードパーティ製の監視 | 2019 年 9 月 30 日 |

## <a name="resources"></a>リソース

- [サプライヤーセキュリティのプライバシーと保証プログラム](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)
