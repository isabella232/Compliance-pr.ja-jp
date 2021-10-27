---
title: サプライヤー管理の概要
description: サプライヤー管理の詳細については、Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH'
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 8367f147e9d0e02ad76d97c665ad66559a743d06
ms.sourcegitcommit: 1f30616328d7deb04e41dcbd44a330ea937fe94f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/26/2021
ms.locfileid: "60582507"
---
# <a name="supplier-management-overview"></a>サプライヤー管理の概要

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>Microsoft は、サプライヤーに関連するリスクを管理する方法を説明します。

Microsoft は、お客様のニーズを満たすのに役立つサードパーティ企業と提携しています。 これらのサードパーティ企業は、サプライヤーまたはサブプロセッサと呼ばれます。 Microsoft のサプライヤーのセキュリティとプライバシーは、Microsoft と提携してオンライン サービスを提供するために、Microsoft と提携しているすべてのサプライヤーに対する企業全体の要件である、Supplier [Security and Privacy Assurance (SSPA)](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)プログラムによって管理されます。 SSPA プログラムは、サプライヤー ベースの包括的なガバナンスと管理を提供しますが、個々のビジネス ユニットは、サプライヤーに対する追加の要件を維持する場合があります。

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>Microsoft のサプライヤー セキュリティおよびプライバシー アシュアランス (SSPA) プログラムが顧客データを保護する方法

SSPA は、サプライヤーが Microsoft のプライバシーとセキュリティの原則を遵守するための、Microsoft の調達、企業の外部および法務、および企業セキュリティのパートナーシップです。 SSPA の範囲は、個人データまたは Microsoft 機密データを処理するすべてのサプライヤーを対象とします。 SSPA プログラムの登録には、Microsoft のデータ保護要件 (DPR) への準拠が含まれます。 DPR は、Microsoft との契約作業を開始する前に、サプライヤーが実装する必要があるセキュリティとプライバシーの制御で構成されています。 登録されているすべてのサプライヤーは、毎年 DPR に準拠する自己証明を行います。

DPR 要件の範囲は、SSPA への登録の一環として、サプライヤーが承認できる 6 つの異なるデータ処理カテゴリに基づいて行います。 これらのカテゴリは、サプライヤーが Microsoft に提供するサービスに関連するリスクを特定するために使用されます。 サプライヤーのデータ処理プロファイルは、適切なデータ保護を提供するためにスコープ内と見なされる DPR コントロールを決定します。 リスクが高いと見なされるデータを処理するサプライヤーは、すべての DPR 要件に準拠する必要があります。また、コンプライアンスの独立した検証を提供する必要があります。 Microsoft の購入ツールは、そのサプライヤーの調達を許可する前に、DPR の該当する部分への準拠を含むすべてのサプライヤーの SSPA 状態を検証します。

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>Microsoft にサービスを提供するサブプロセッサの種類

「サブプロセッサ」とは、Microsoft がプロセッサである Microsoft 個人データの処理を含む、Microsoft が関与する第三者です。 Microsoft のサブプロセッサは、3 つの異なるカテゴリに分類されます。 Microsoft の代わりに顧客データを処理する前に、SSPA への準拠を示す必要があります。

- **テクノロジー** サブプロセッサーは、特定の Microsoft Online Services の提供に使用するテクノロジーを提供します。 顧客がこれらのサービスのいずれかを展開した場合、そのサービスに対して特定されたサブプロセッサは、そのサービスの提供を支援しながら、顧客データまたは個人データを処理、保存、またはアクセスできます。
- **Ancillary** サブプロセッサは、オンライン サービスをサポート、運用、および保守するサービスを提供します。 お客様がこれらのサービスのいずれかを展開した場合、特定されたサブプロセッサは、関連サービスを提供しながら、制限された顧客データまたは個人データを処理、保存、またはアクセスできます。
- **スタッフ拡張サブ** プロセッサは、2 つの異なる形式を取ります。どちらのシナリオでも、個人データは Microsoft の施設、Microsoft システムにのみ存在し、Microsoft のポリシーと監督の対象となります。

    - スタッフ増強の 1 つ目の形式は、Microsoft Online Services のサポート、運用、保守を行うスタッフを提供するものです。 これらのサブプロセッサーに対しては、その責任を果たす間に、顧客データや個人データが露呈されてしまう場合があります。 たとえば、サブプロセッサーが Microsoft のサーバー上でリモート トラブルシューティングを実行している間に、サーバーのクラッシュ ダンプ ログ内の顧客データ スニペットが露呈してしまう場合があります。
    - 2 番目の形式のスタッフ拡張では、Microsoft のオンライン サービスをサポート、運用、および保守するために、Microsoft のフルタイムの従業員と並べて作業するサブプロセッサが含まれる。 これらのサブプロセッサーに対しては、Microsoft のフルタイム従業員との共同業務の一環として、仮名化されたデータが露呈してしまう可能性があります。

Microsoft のデータ保護要件 (DPR) に準拠してアクセス制御を実装するには、テクノロジと関連サブプロセッサが必要です。 これらの要件は、Microsoft がオンライン サービス条項 (OST) で顧客に対して行う契約上のコミットメントを満たすか、それを超えています。 スタッフ拡張作業を実行するサプライヤーは、Microsoft の正社員と同じアクセス制御の対象です。

## <a name="how-does-microsoft-onboard-suppliers"></a>Microsoft は、どのようにサプライヤーをオンボードしますか?

サードパーティのサプライヤーは、オンボーディング プロセスの一環として Microsoft Master Agreement に署名する必要があります。 この契約は、Microsoft とそのサプライヤー間の関係を管理し、サプライヤー関係の一貫した管理を保証します。 オンボーディングの一環として、サプライヤーは SSPA に登録し、すべてのデータ処理カテゴリで承認される前に、該当する要件を満たす必要があります。 Microsoft ビジネス ユニットは、契約のデータ処理アクティビティが、サプライヤーが承認されたデータ処理カテゴリと一致する場合にのみ、サプライヤーとの契約を作成できます。

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>Microsoft は、データを処理するサプライヤーに対する変更を顧客に通知する方法を説明します。

Microsoft Online Service Data Protection Addendum (DPA) に基づき、Microsoft はサブプロセッサの追加に関する通知期間に関して追加のコミットメントを行います。 通知のタイム フレームは、サブプロセッサが Microsoft に代わって処理するデータの種類によって異なります。 DPA に記載されている通り、Microsoft は顧客データを処理する新しいサブプロセッサの少なくとも 6 か月前にお客様に通知を提供します。 その他の個人データに関して、Microsoft は少なくとも 30 日間の通知を提供します。 通知は、サブプロセッサ リストのMicrosoft Online Services [によって提供されます](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=ede6342e-d641-4a9b-9162-7d66025003b0&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List)。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 サプライヤー管理に関連するコントロールの検証については、以下の表を参照してください。

### <a name="azure-and-dynamics-365"></a>Azure と Dynamics 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|  
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: サプライヤー関係の情報セキュリティ | 2020 年 12 月 2 日 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: サプライヤー関係の情報セキュリティ | 2020 年 12 月 2 日 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A.8.1: 外注 PII 処理の開示 | 2020 年 12 月 2 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | SOC2-25: サプライヤーのリスク管理 <br> C5-2: サプライヤー リスク プロファイルのレビュー| 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | CA-3: システム相互接続 <br> IA-4: 識別子の管理 <br> PS-6: アクセス契約 <br> PS-7: サードパーティの人事セキュリティ <br> SA-4: 取得プロセス <br> SA-9: 外部情報システム サービス <br> SA-12: サプライ チェーン保護 | 2020 年 9 月 24 日 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: サプライヤー関係の情報セキュリティ | 2021 年 4 月 20 日 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.8.1: 外注 PII 処理の開示 | 2020 年 12 月 24 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-53: サードパーティの監視 | 2020 年 12 月 24 日 |

## <a name="resources"></a>リソース

- [Supplier Security Privacy and Assurance Program](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)
