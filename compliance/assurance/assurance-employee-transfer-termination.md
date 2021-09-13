---
title: Microsoft 従業員の異動と退職
description: Microsoft の従業員の転送と終了のプロセスについて詳しくは、Microsoft 365
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
ms.openlocfilehash: 2450a075d1ae3922cf047e92109a399d10d269ac
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160276"
---
# <a name="microsoft-employee-transfer-and-termination"></a>Microsoft 従業員の異動と退職

Microsoft は、他のすべての組織と同様に、通常の業務の一環として従業員の転送と終了を処理します。 従業員が役職を変更したり、会社を離れる場合は、不適切なアクセスを不適切な方法で取り消す必要があります。 効率的なアクセス変更とアクセス取り消しを容易にするために、Microsoft は標準化された手順と自動化されたプロセスを使用して、人事情報システム (HRIS) と IDM (IDM) システムを調整します。 これら 2 つのシステム間の自動オーケストレーションは、運用の一貫性を維持し、Microsoft のオンライン サービスとデータを保護し、特権の不気味を防止し、インサイダーの脅威に関連するリスクを軽減するために不可欠です。

Microsoft のオンライン サービスは、エンジニアの運用環境への管理アクセスを常に行わずに動作するように設計されています。 Microsoft では、Just-In-Time (JIT) Just-Enough-Access (JEA) モデルを使用して、必要に応じてサービスをサポートするために必要な一時的なアクセスをエンジニアに提供します。 JIT アクセスにサービス チーム アカウントを要求して使用するには、IDM ツールを使用して資格を要求し、維持する必要があります。 従業員が転送または終了すると、サービス チーム アカウントと関連する資格が自動的に変更され、不適切なアクセスが防止されます。

## <a name="transfer-and-reassignment"></a>転送と再割り当て

従業員の転送は、従業員のマネージャーによる転送トランザクション要求によって開始されます。 マネージャーは要求を作成し、オファーレタープロセスのグローバル人材獲得に従事します。 従業員が新しい役割のオファーを受け入れると、人事サービスは人事コア ツールの転送を完了し、IDM がトリガーして、すべての従業員の適格性の有効期限を設定します。 従業員は、資格を保持するために、要求を提出し、新しいマネージャーから承認を受ける必要があります。 要求の送信またはマネージャーの承認の受信に失敗すると、転送された従業員の資格が取り消されます。 特定のセキュリティ上の影響を含む転送では、システム アクセスとセキュリティ グループ メンバーシップが直ちに再評価され、新しい役割が反映されます。

## <a name="termination"></a>退職

Microsoft は、明確に定義されたポリシーと手順を使用して、従業員の退職時に、Microsoft のシステムとリソースへの物理的および論理的アクセスを即座に取り消します。 従業員が通知を行った場合、従業員のマネージャーは終了日を HRIS に入力します。 従業員の最後の勤務日の後、HRIS は従業員を終了としてマークし、IDM に情報を共有し、すべてのサービス チーム アカウントと資格を自動的に削除します。

不本意な終了の場合、人事担当者は従業員のマネージャーと一緒に適切な手順に従って従業員を終了およびオフボードします。 任意の終了と同様に、終了情報は HRIS に入力され、有効な日付調整、アクセスの削除、および役割外への移行に関連するその他の手順など、必要な手順が実行されます。
