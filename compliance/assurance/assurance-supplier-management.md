---
title: サプライヤー管理の概要
description: Microsoft 365 のサプライヤー管理について
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
ms.openlocfilehash: 4da4775332989c4a40738777dfae7318e27086f0
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787376"
---
# <a name="supplier-management-overview"></a>サプライヤー管理の概要

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>Microsoft では、サプライヤーに関連するリスクを管理する方法について説明します。

Microsoft は、お客様のニーズを満たすためにサード パーティ企業と提携しています。 これらのサード パーティ企業は、サプライヤーまたはサブプロセッサと呼ばれます。 Microsoft のサプライヤーのセキュリティとプライバシーは、マイクロソフトのオンライン サービスを提供するために Microsoft と提携しているすべてのサプライヤーに対する企業全体の要件である、サプライヤー セキュリティ/プライバシー アシュアランス [(SSPA)](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)プログラムによって管理されます。 SSPA プログラムは、サプライヤー ベースの包括的なガバナンスと管理を提供しますが、Microsoft 365 などの個々の事業単位は、サプライヤーに対する追加の要件を維持する場合があります。

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>Microsoft のサプライヤー セキュリティ/プライバシー アシュアランス (SSPA) プログラムは、どのように顧客データを保護しますか?

SSPA は、サプライヤーが Microsoft のプライバシーとセキュリティの原則を確実に遵守するための、Microsoft 調達、企業の外部および法務、および企業のセキュリティの間のパートナーシップです。 SSPA の範囲は、個人データまたは Microsoft 機密データを処理するすべてのサプライヤーを対象とします。 SSPA プログラムの登録には、Microsoft のデータ保護要件 (DPR) への準拠が含まれます。 DPR は、マイクロソフトとの契約作業を開始する前に、サプライヤーが実装する必要があるセキュリティとプライバシーのコントロールで構成されています。 登録しているすべてのサプライヤーは、毎年 DPR に準拠する自己証明を行います。

DPR 要件は、SSPA への登録の一環として、サプライヤーが承認できる 6 つの異なるデータ処理カテゴリに基づいて範囲指定されます。 これらのカテゴリは、仕入先が Microsoft に提供するサービスに関連するリスクを特定するために使用されます。 供給者のデータ処理プロファイルは、適切なデータ保護を提供するために範囲内と見なされる DPR コントロールを決定します。 より高いリスクと見なされるデータを処理するサプライヤーは、すべての DPR 要件に準拠する必要があります。また、コンプライアンスの独立した検証を提供する必要がある場合があります。 Microsoft の購入ツールは、そのサプライヤーの調達を許可する前に、DPR の該当する部分への準拠を含む、すべてのサプライヤーの SSPA ステータスを検証します。

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>Microsoft にサービスを提供するサブプロセッサの種類は何ですか?

「サブプロセッサ」とは、マイクロソフトが処理者である Microsoft 個人データの処理を含む、Microsoft が関与する第三者です。 Microsoft のサブプロセッサは、3 つの異なるカテゴリに分類されます。 それぞれが、Microsoft に代わって顧客データを処理する前に、SSPA への準拠を実証する必要があります。

- **テクノロジー** サブプロセッサーは、特定の Microsoft Online Services の提供に使用するテクノロジーを提供します。 お客様がこれらのサービスの 1 つを展開した場合、そのサービスに対して特定された副処理者は、そのサービスの提供を支援しながら、顧客データまたは個人データを処理、保存、またはアクセスできます。
- **付帯サブプロセッサは** 、オンライン サービスをサポート、運用、および保守するサービスを提供します。 お客様がこれらのサービスの 1 つを展開した場合、特定された副処理者は、付帯サービスの提供中に、限定的な顧客データまたは個人データを処理、保存、またはアクセスできます。
- **スタッフ オーグメント** サブプロセッサは、2 つの異なる形式を取ります。どちらのシナリオでも、個人データは Microsoft の施設、Microsoft システムにのみ存在し、Microsoft のポリシーと監督の対象となります。

    - スタッフ増強の 1 つ目の形式は、Microsoft Online Services のサポート、運用、保守を行うスタッフを提供するものです。 これらのサブプロセッサーに対しては、その責任を果たす間に、顧客データや個人データが露呈されてしまう場合があります。 たとえば、サブプロセッサーが Microsoft のサーバー上でリモート トラブルシューティングを実行している間に、サーバーのクラッシュ ダンプ ログ内の顧客データ スニペットが露呈してしまう場合があります。
    - 2 番目の形式のスタッフオーグメントには、Microsoft のフルタイム従業員と並べて作業し、Microsoft オンライン サービスのサポート、運用、および保守を行う副処理者が含まれる。 これらのサブプロセッサーに対しては、Microsoft のフルタイム従業員との共同業務の一環として、仮名化されたデータが露呈してしまう可能性があります。

Microsoft のデータ保護要件 (DPR) に準拠してアクセス制御を実装するには、テクノロジと付帯サブプロセッサが必要です。 これらの要件は、Microsoft がオンライン サービス使用条件 (OST) で顧客に対して行う契約上のコミットメントを満たすか、超過しています。 スタッフの拡張作業を行うサプライヤーは、Microsoft のフルタイム従業員と同じアクセス制御の対象です。

## <a name="how-does-microsoft-onboard-suppliers"></a>Microsoft はサプライヤーをオンボードする方法を説明します。

サード パーティのサプライヤーは、オンボーディング プロセスの一環として Microsoft マスター契約に署名する必要があります。 この契約は、Microsoft とそのサプライヤー間の関係を管理し、サプライヤーとの関係を一貫して管理します。 オンボーディングの一環として、サプライヤーは SSPA に登録し、該当する要件を満たす必要があります。その後、データ処理カテゴリの承認を受けることができます。 Microsoft のビジネス 単位は、契約のデータ処理アクティビティが、仕入先が承認されたデータ処理カテゴリと一致する場合にのみ、仕入先との契約を作成できます。

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>Microsoft は、データを処理するサプライヤーへの変更を顧客に通知する方法を説明します。

Microsoft Online Service Data Protection Addendum (DPA) に基づき、マイクロソフトは、サブプロセッサの追加に関する通知期間に関する追加のコミットメントを行います。 タイム フレームは、サブプロセッサが Microsoft に代わって処理するデータの種類によって異なります。 DPA で説明したように、Microsoft は、顧客データを処理する新しいサブプロセッサの少なくとも 6 か月前にお客様に通知を提供します。 その他の個人データに関して、Microsoft は少なくとも 30 日間の通知を行います。 通知は、サブプロセッサ リストの更新 [Microsoft Online Services提供されます](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=926b2cf5-6b6e-43ca-9bc3-f73e961aad5f&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List)。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 仕入先管理に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CA-3: システムの相互接続 <br> IA-4: 識別子の管理 <br> PS-6: アクセス契約 <br> PS-7: サードパーティの担当者のセキュリティ <br> SA-4: 取得プロセス <br> SA-9: 外部情報システム サービス <br> SA-12: サプライ チェーン保護 | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: サプライヤー関係の情報セキュリティ | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: サプライヤー関係の情報セキュリティ | 2020 月 2 月 22 日 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A.8.1: 下請け PII 処理の開示 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-53: サードパーティの監視 | 2020 年 12 月 24 日 |

## <a name="resources"></a>リソース

- [サプライヤー のセキュリティプライバシーおよび保証プログラム](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)
