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
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 5cca0c3cf70a0fe2c660c0b168a157056e1d4c56942fdeee2b71e7448c1dc50b
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54291015"
---
# <a name="identity-and-access-management-overview"></a>ID およびアクセス管理の概要

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>実稼働システムMicrosoft 365、または悪意のあるアクセスから保護する方法

Microsoft 365は、Microsoft のエンジニアが顧客コンテンツにアクセスせずにサービスを運用できるよう設計されています。 既定では、Microsoft 365エンジニアは顧客のコンテンツに対してゼロ スタンディング アクセス (ZSA) を持ち、実稼働環境への特権アクセスはありません。 Microsoft 365は、Just-In-Time (JIT) Just-Enough-Access (JEA) モデルを使用して、サービス チーム のエンジニアに、Microsoft 365 をサポートするためにそのようなアクセスが必要な場合に、一時的に実稼働環境への特権アクセスを提供します。 JIT アクセス モデルは、従来の永続的な管理者アクセスを、必要に応じた特権ロールへの一時的な昇格をエンジニアが要求するプロセスへと置き換えます。

運用サービスをサポートするためにサービス チームに割り当てられたエンジニアは、IDM (IdM) を使用してサービス チーム アカウントの適格性を要求します。 適格性の要求は、エンジニアがすべてのクラウド スクリーニング要件に合格し、必要なトレーニングを完了し、アカウントを作成する前に適切な管理承認を受けた場合に、一連の人事チェックをトリガーします。 すべての資格要件を満たしている場合にのみ、要求した環境のサービス チーム アカウントを作成できます。 サービス チーム アカウントの資格を維持するには、担当者は役割ベースのトレーニングを毎年実施し、2 年ごとに再審査を行う必要があります。 これらのチェックを完了または合格すると、資格が自動的に取り消されます。

サービス チーム アカウントは、常に管理者特権を付与したり、顧客コンテンツにアクセスしたりすることはできません。 エンジニアは、Microsoft 365 サービスをサポートするために追加のアクセスを必要とする場合、Lockbox というアクセス管理ツールを使用して、必要なリソースへの一時的な昇格されたアクセスを要求します。 ロックボックスは、割り当てられたタスクを完了するために必要な最小限の特権、リソース、時間への昇格したアクセス権を制限します。 承認されたレビューアーが JIT アクセス要求を承認すると、エンジニアには、割り当てられた作業を完了するために必要な権限のみを持つ一時的なアカウントが付与されます。 この一時アカウントには多要素認証が必要であり、承認された期間が経過すると自動的に削除されます。

JEA は、JIT アクセスの要求時に IDM の適格性とロックボックス の役割によって適用されます。 エンジニアの適格性の範囲内の資産へのアクセス要求だけが受け入れ、承認者に渡されます。 ロックボックスは、許可されたしきい値を超える要求を含む、エンジニアの適格性とロックボックスの役割の範囲を超える JIT 要求を自動的に拒否します。  

## <a name="how-does-microsoft-365-use-role-based-access-control-rbac-with-lockbox-to-enforce-least-privilege"></a>Lockbox でMicrosoft 365アクセス制御 (RBAC) を使用して最小特権を強制する方法

サービス チーム アカウントは、常に管理者特権を付与したり、顧客コンテンツにアクセスしたりすることはできません。 制限付き管理者特権に対する JIT 要求は、Lockbox を介して管理されます。 Lockbox は RBAC を使用して、エンジニアが行う JIT 昇格要求の種類を制限し、最小特権を強制するための追加の保護層を提供します。 RBAC は、サービス チーム アカウントを適切な役割に制限することで、職務の分離を強制するのにも役立ちます。
サービスをサポートするエンジニアには、その役割に基づいてセキュリティ グループへのメンバーシップが付与されます。 セキュリティ グループのメンバーシップでは、特権アクセスは付与されません。 代わりに、セキュリティ グループを使用すると、システムをサポートするために必要な場合、エンジニアは Lockbox を使用して JIT 昇格を要求できます。 エンジニアが行う特定の JIT 要求は、セキュリティ グループのメンバーシップによって制限されます。

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>実稼働システムMicrosoft 365リモート アクセスを処理する方法

Microsoft 365 システム コンポーネントは、運用チームから地理的に分離されたデータ センターに格納されます。 データセンターの担当者は、システムに対して論理的Microsoft 365持つ必要があります。 その結果、サービス Microsoft 365担当者がリモート アクセスを通じて環境を管理します。 Microsoft 365 をサポートするためのリモート アクセスを必要とするサービスチームの担当者は、承認されたマネージャーからの承認後にのみリモート アクセスを許可されます。 すべてのリモート アクセスは、安全なリモート接続のために FIPS 140-2 互換 TLS を使用します。

Microsoft 365セキュリティで保護された管理ワークステーションをサービス チームのリモート アクセスに使用して、セキュリティで保護された環境Microsoft 365保護します。 これらのワークステーションは、USB ポートをロックダウンしたり、Secure Admin Workstation で使用できるソフトウェアを環境をサポートするために必要なソフトウェアを制限したりなど、意図的または意図しない実稼働データの損失を防ぐ目的で設計されています。 Secure Admin Workstations は、Microsoft のエンジニアによる悪意のある、または不注意な顧客データの侵害を検出および防止するために、密接に追跡および監視されています。

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>カスタマー ロックボックスは、顧客コンテンツに対する追加の保護を追加する方法を示します。

顧客は、Customer Lockbox を有効にすることで、コンテンツに追加レベルのアクセス制御を追加できます。 ロックボックス昇格要求に顧客コンテンツへのアクセスが含まれる場合、顧客ロックボックスは承認ワークフローの最終ステップとして顧客からの承認を必要とします。 このプロセスは、組織にこれらの要求を承認または拒否するオプションを提供し、顧客に直接アクセス制御を提供します。 顧客が Customer Lockbox 要求を拒否した場合、要求されたコンテンツへのアクセスは拒否されます。 お客様が一定の期間に要求を拒否または承認しない場合、Microsoft が顧客コンテンツにアクセスすることなく、要求は自動的に期限切れになります。 顧客が要求を承認すると、トラブルシューティング操作の完了に割り当てられた時間が経過すると、Microsoft の顧客コンテンツへの一時的なアクセスがログに記録され、監査され、自動的に取り消されます。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 ID とアクセス制御に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: アカウント管理 <br> AC-3: アクセスの適用 <br> AC-5: 職務の分離 <br> AC-6: 最小特権 <br> AC-17: リモート アクセス | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: アクセス制御のビジネス要件 <br> A.9.2: ユーザー アクセス管理 <br> A.9.3: ユーザーの責任 <br> A.9.4: システムとアプリケーションのアクセス制御 <br> A.15.1: サプライヤー関係の情報セキュリティ | 2021 年 4 月 20 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.2: ユーザー アクセス管理 <br> A.9.4: システムとアプリケーションのアクセス制御 <br> A.15.1: サプライヤー関係の情報セキュリティ | 2021 年 4 月 20 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33: アカウントの変更 <br> CA-34: ユーザー認証 <br> CA-35: 特権アクセス <br> CA-36: リモート アクセス <br> CA-57: カスタマー ロックボックス Microsoft の管理承認 <br> CA-58: 顧客ロックボックス サービス要求 <br> CA-59: カスタマー ロックボックス通知 <br> CA-61: JIT のレビューと承認 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32: 共有アカウント ポリシー <br> CA-33: アカウントの変更 <br> CA-34: ユーザー認証 <br> CA-35: 特権アクセス <br> CA-36: リモート アクセス <br> CA-53: サードパーティの監視 <br> CA-56: 顧客ロックボックスのお客様の承認 <br> CA-57: カスタマー ロックボックス Microsoft の管理承認 <br> CA-58: 顧客ロックボックス サービス要求 <br> CA-59: カスタマー ロックボックス通知 <br> CA-61: JIT のレビューと承認 | 2020 年 12 月 24 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15: 顧客ロックボックス要求 | 2020 年 12 月 24 日 |