---
title: ID およびアクセス管理の概要
description: Microsoft 365 での ID とアクセス管理について
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
ms.openlocfilehash: c07801fe5ef571ddb4c9efcbfe04a7b3e5faedb6
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787476"
---
# <a name="identity-and-access-management-overview"></a>ID およびアクセス管理の概要

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>Microsoft 365 は、無許可または悪意のあるアクセスから実稼働システムを保護する方法を説明します。

Microsoft 365 は、Microsoft のエンジニアが顧客のコンテンツにアクセスすることなくサービスを運用できるよう設計されています。 既定では、Microsoft 365 のエンジニアは、お客様のコンテンツに対するゼロ 永続的アクセス (ZSA) を持ち、実稼働環境への特権アクセスはありません。 Microsoft 365 では、Just-In-Time (JIT) Just-Enough-Access (JEA) モデルを使用して、Microsoft 365 をサポートするためにそのようなアクセスが必要な場合に、サービス チーム エンジニアに、実稼働環境への一時的な特権アクセスを提供します。 JIT アクセス モデルは、従来の永続的な管理者アクセスを、必要に応じた特権ロールへの一時的な昇格をエンジニアが要求するプロセスへと置き換えます。

運用サービスをサポートするためにサービス チームに割り当てられたエンジニアは、IDM (Identity Management Tool) を通じてサービス チーム アカウントの資格を要求します。 適格性の要求により、一連の担当者チェックがトリガーされ、エンジニアがすべてのクラウド スクリーン処理要件に合格し、必要なトレーニングを完了し、アカウントを作成する前に適切な管理承認を受けた必要があります。 すべての資格要件を満たしている場合にのみ、要求した環境のサービス チーム アカウントを作成できます。

サービス チーム アカウントは、永続的な管理者特権や顧客コンテンツへのアクセス権を付与する必要はありません。 エンジニアが Microsoft 365 サービスをサポートするために追加のアクセス権を必要とする場合、ロックボックス (Lockbox) というアクセス管理ツールを使用して、必要なリソースへの一時的な昇格されたアクセスを要求します。 ロックボックスは、割り当てられたタスクを完了するために必要な最小限の特権、リソース、時間への昇格したアクセス権を制限します。 承認されたレビューアーが JIT アクセス要求を承認すると、エンジニアには、割り当てられた作業を完了するために必要な特権のみを持つ一時的なアカウントが付与されます。 この一時アカウントには多要素認証が必要であり、承認された期間が経過すると自動的に削除されます。

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>Microsoft 365 は、実稼働システムへのリモート アクセスを処理する方法を説明します。

Microsoft 365 システム コンポーネントは、運用チームから地理的に分離されたデータ センターに格納されます。 データセンターの担当者は、Microsoft 365 システムに論理的にアクセスできない。 その結果、Microsoft 365 サービス チームの担当者はリモート アクセスを使用して環境を管理します。 Microsoft 365 をサポートするためのリモート アクセスを必要とするサービスチームの担当者は、承認されたマネージャーからの承認後にのみリモート アクセスを許可されます。 すべてのリモート アクセスは、安全なリモート接続のために FIPS 140-2 互換 TLS を使用します。

Microsoft 365 は、サービス チームのリモート アクセスに Secure Admin Workstation (SAW) を使用して、Microsoft 365 環境を侵害から保護します。 これらのワークステーションは、USB ポートのロックダウンや、環境をサポートするために必要なものに SAW で使用可能なソフトウェアの制限など、実稼働データが意図的または意図せずに失われるのを防ぐことを目的として特別に設計されています。 SAW は、Microsoft のエンジニアによる顧客データの悪意のある侵害や不注意による侵害を検出および防止するために、密接に追跡および監視されています。

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>カスタマー ロックボックスによって、顧客コンテンツに対する保護がどのように追加されますか?

顧客は、カスタマー ロックボックスを有効にすることで、コンテンツにさらにレベルのアクセス制御を追加できます。 ロックボックス昇格要求に顧客コンテンツへのアクセスが含まれる場合、カスタマー ロックボックスは承認ワークフローの最終ステップとして顧客からの承認を必要とします。 これにより、組織は、これらの要求を承認または拒否するオプションが提供され、顧客に直接アクセス制御できます。 顧客がカスタマー ロックボックス要求を拒否した場合、要求されたコンテンツへのアクセスは拒否されます。 お客様が一定の期間に要求を拒否または承認しない場合、Microsoft が顧客のコンテンツにアクセスすることなく、要求は自動的に期限切れになります。 お客様が要求を承認すると、Microsoft による顧客コンテンツへの一時的なアクセスは記録され、監査可能であり、トラブルシューティング操作を完了するために割り当てられた時間が経過すると自動的に取り消されます。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 ID とアクセス制御に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: アカウント管理 <br> AC-3: アクセスの実施 <br> AC-5: 職務の分離 <br> AC-6: 最低特権 <br> AC-17: リモート アクセス | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: アクセス制御のビジネス要件 <br> A.9.2: ユーザー アクセス管理 <br> A.9.3: ユーザーの責任 <br> A.9.4: システムとアプリケーションのアクセス制御 <br> A.15.1: サプライヤー関係の情報セキュリティ | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.2: ユーザー アクセス管理 <br> A.9.4: システムとアプリケーションのアクセス制御 <br> A.15.1: サプライヤー関係の情報セキュリティ | 2020 月 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33: アカウントの変更 <br> CA-34: ユーザー認証 <br> CA-35: 特権アクセス <br> CA-36: リモート アクセス <br> CA-57: カスタマー ロックボックス Microsoft の管理承認 <br> CA-58: カスタマー ロックボックス サービス要求 <br> CA-59: カスタマー ロックボックス通知 <br> CA-61: JIT のレビューと承認 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32: 共有アカウント ポリシー <br> CA-33: アカウントの変更 <br> CA-34: ユーザー認証 <br> CA-35: 特権アクセス <br> CA-36: リモート アクセス <br> CA-53: サードパーティの監視 <br> CA-56: カスタマー ロックボックスのお客様の承認 <br> CA-57: カスタマー ロックボックス Microsoft の管理承認 <br> CA-58: カスタマー ロックボックス サービス要求 <br> CA-59: カスタマー ロックボックス通知 <br> CA-61: JIT のレビューと承認 | 2020 年 12 月 24 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15: カスタマー ロックボックス要求 | 2020 年 12 月 24 日 |