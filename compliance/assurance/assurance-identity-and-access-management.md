---
title: ID およびアクセス管理の概要
description: ID とアクセス管理の詳細については、Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
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
ms.openlocfilehash: 933db3783c6672fa952f70f18c4815955bcedb21
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481959"
---
# <a name="identity-and-access-management-overview"></a>ID およびアクセス管理の概要

## <a name="how-do-microsoft-online-services-protect-production-systems-from-unauthorized-or-malicious-access"></a>Microsoft オンライン サービスは、承認されていないアクセスや悪意のあるアクセスから実稼働システムを保護する方法を説明します。

Microsoft オンライン サービスは、Microsoft のエンジニアが顧客コンテンツにアクセスせずにサービスを運用できる設計です。 既定では、Microsoft のエンジニアは、顧客コンテンツに対するゼロ スタンディング アクセス (ZSA) を持ち、実稼働環境への特権アクセスはありません。 Microsoft オンライン サービスは、Just-In-Time (JIT) Just-Enough-Access (JEA) モデルを使用して、Microsoft オンライン サービスをサポートするためにそのようなアクセスが必要な場合に、サービス チーム のエンジニアに一時的に実稼働環境への特権アクセスを提供します。 JIT アクセス モデルは、従来の永続的な管理者アクセスを、必要に応じた特権ロールへの一時的な昇格をエンジニアが要求するプロセスへと置き換えます。

運用サービスをサポートするためにサービス チームに割り当てられたエンジニアは、ID およびアクセス管理ソリューションを通じてサービス チーム アカウントの適格性を要求します。 適格性の要求は、エンジニアがすべてのクラウド スクリーニング要件に合格し、必要なトレーニングを完了し、アカウントを作成する前に適切な管理承認を受けた場合に、一連の人事チェックをトリガーします。 すべての資格要件を満たしている場合にのみ、要求した環境のサービス チーム アカウントを作成できます。 サービス チーム アカウントの資格を維持するには、担当者は役割ベースのトレーニングを毎年実施し、2 年ごとに再審査を行う必要があります。 これらのチェックを完了または合格すると、資格が自動的に取り消されます。

サービス チーム アカウントは、常に管理者特権を付与したり、顧客コンテンツにアクセスしたりすることはできません。 エンジニアが Microsoft オンライン サービスをサポートするために追加のアクセス権を必要とする場合、Lockbox という名前のアクセス管理ツールを使用して、必要なリソースへの一時的な昇格されたアクセスを要求します。 ロックボックスは、割り当てられたタスクを完了するために必要な最小限の特権、リソース、時間への昇格したアクセス権を制限します。 承認されたレビューアーが JIT アクセス要求を承認すると、エンジニアには、割り当てられた作業を完了するために必要な権限のみを持つ一時的なアカウントが付与されます。 この一時アカウントには多要素認証が必要であり、承認された期間が経過すると自動的に削除されます。

JEA は、JIT アクセスの要求時に、適格性とロックボックス の役割によって適用されます。 エンジニアの適格性の範囲内の資産へのアクセス要求だけが受け入れ、承認者に渡されます。 ロックボックスは、許可されたしきい値を超える要求を含む、エンジニアの適格性とロックボックスの役割の範囲を超える JIT 要求を自動的に拒否します。  

## <a name="how-do-microsoft-online-services-use-role-based-access-control-rbac-with-lockbox-to-enforce-least-privilege"></a>Microsoft オンライン サービスは、ロックボックスで役割ベースのアクセス制御 (RBAC) を使用して最小特権を強制する方法を説明します。

サービス チーム アカウントは、常に管理者特権を付与したり、顧客コンテンツにアクセスしたりすることはできません。 制限付き管理者特権に対する JIT 要求は、Lockbox を介して管理されます。 Lockbox は RBAC を使用して、エンジニアが行う JIT 昇格要求の種類を制限し、最小特権を強制するための追加の保護層を提供します。 RBAC は、サービス チーム アカウントを適切な役割に制限することで、職務の分離を強制するのにも役立ちます。
サービスをサポートするエンジニアには、その役割に基づいてセキュリティ グループへのメンバーシップが付与されます。 セキュリティ グループのメンバーシップでは、特権アクセスは付与されません。 代わりに、セキュリティ グループを使用すると、システムをサポートするために必要な場合、エンジニアは Lockbox を使用して JIT 昇格を要求できます。 エンジニアが行う特定の JIT 要求は、セキュリティ グループのメンバーシップによって制限されます。

## <a name="how-do-microsoft-online-services-handle-remote-access-to-production-systems"></a>Microsoft オンライン サービスは、実稼働システムへのリモート アクセスを処理する方法を説明します。

Microsoft Online Services システム コンポーネントは、運用チームから地理的に分離されたデータセンターに収容されます。 データセンター担当者は、Microsoft オンライン サービス システムに論理的にアクセスできます。 その結果、Microsoft サービス チームの担当者はリモート アクセスを通じて環境を管理します。 Microsoft オンライン サービスをサポートするためにリモート アクセスを必要とするサービス チームの担当者は、承認されたマネージャーからの承認後にのみリモート アクセスを許可されます。 すべてのリモート アクセスは、安全なリモート接続のために FIPS 140-2 互換 TLS を使用します。

Microsoft オンライン サービスは、サービス チームのリモート アクセスに Secure Admin Workstations (SAW) を使用して、Microsoft オンライン サービス環境を侵害から保護します。 これらのワークステーションは、USB ポートをロックダウンしたり、Secure Admin Workstation で使用できるソフトウェアを環境をサポートするために必要なソフトウェアを制限したりなど、意図的または意図しない実稼働データの損失を防ぐ目的で設計されています。 Secure Admin Workstations は、Microsoft のエンジニアによる悪意のある、または不注意な顧客データの侵害を検出および防止するために、密接に追跡および監視されています。

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>カスタマー ロックボックスは、顧客コンテンツに対する追加の保護を追加する方法を示します。

顧客は、Customer Lockbox を有効にすることで、コンテンツに追加レベルのアクセス制御を追加できます。 ロックボックス昇格要求に顧客コンテンツへのアクセスが含まれる場合、顧客ロックボックスは承認ワークフローの最終ステップとして顧客からの承認を必要とします。 このプロセスは、組織にこれらの要求を承認または拒否するオプションを提供し、顧客に直接アクセス制御を提供します。 顧客が Customer Lockbox 要求を拒否した場合、要求されたコンテンツへのアクセスは拒否されます。 お客様が一定の期間に要求を拒否または承認しない場合、Microsoft が顧客コンテンツにアクセスすることなく、要求は自動的に期限切れになります。 顧客が要求を承認すると、トラブルシューティング操作の完了に割り当てられた時間が経過すると、Microsoft の顧客コンテンツへの一時的なアクセスがログに記録され、監査され、自動的に取り消されます。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 ID とアクセス制御に関連するコントロールの検証については、次の表を参照してください。

### <a name="azure-and-dynamics-365"></a>Azure と Dynamics 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: アクセス制御のビジネス要件 <br> A.9.2: ユーザー アクセス管理 <br> A.9.3: ユーザーの責任 <br> A.9.4: システムとアプリケーションのアクセス制御 <br> A.15.1: サプライヤー関係の情報セキュリティ | 2020 年 12 月 2 日 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: アクセス制御のビジネス要件 <br> A.9.2: ユーザー アクセス管理 <br> A.9.3: ユーザーの責任 <br> A.9.4: システムとアプリケーションのアクセス制御 <br> A.15.1: サプライヤー関係の情報セキュリティ | 2020 年 12 月 2 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | OA-2: プロビジョニング アクセス <br> OA-7: JIT アクセス <br> OA-21: Secure Admin ワークステーションと MFA | 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-2: アカウント管理 <br> AC-3: アクセスの適用 <br> AC-5: 職務の分離 <br> AC-6: 最小特権 <br> AC-17: リモート アクセス | 2020 年 9 月 24 日 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: アクセス制御のビジネス要件 <br> A.9.2: ユーザー アクセス管理 <br> A.9.3: ユーザーの責任 <br> A.9.4: システムとアプリケーションのアクセス制御 <br> A.15.1: サプライヤー関係の情報セキュリティ | 2021 年 4 月 20 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33: アカウントの変更 <br> CA-34: ユーザー認証 <br> CA-35: 特権アクセス <br> CA-36: リモート アクセス <br> CA-57: カスタマー ロックボックス Microsoft の管理承認 <br> CA-58: 顧客ロックボックス サービス要求 <br> CA-59: カスタマー ロックボックス通知 <br> CA-61: JIT のレビューと承認 | 2020 年 12 月 24 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32: 共有アカウント ポリシー <br> CA-33: アカウントの変更 <br> CA-34: ユーザー認証 <br> CA-35: 特権アクセス <br> CA-36: リモート アクセス <br> CA-53: サードパーティの監視 <br> CA-56: 顧客ロックボックスのお客様の承認 <br> CA-57: カスタマー ロックボックス Microsoft の管理承認 <br> CA-58: 顧客ロックボックス サービス要求 <br> CA-59: カスタマー ロックボックス通知 <br> CA-61: JIT のレビューと承認 | 2020 年 12 月 24 日 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15: 顧客ロックボックス要求 | 2020 年 12 月 24 日 |