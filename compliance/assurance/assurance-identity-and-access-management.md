---
title: Id およびアクセス管理の概要
description: Microsoft 365 での id およびアクセス管理について
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
ms.openlocfilehash: b62219faa5bc55ef4bef9557d953caf1a2f95fc7
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507836"
---
# <a name="identity-and-access-management-overview"></a>Id およびアクセス管理の概要

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>Microsoft 365 は、運用システムを無許可または悪意のあるアクセスから保護する方法を教えてください。

Microsoft 365 は、Microsoft のエンジニアがお客様のコンテンツにアクセスせずにサービスを運用できるように設計されています。 既定では、Microsoft 365 エンジニアは、お客様のコンテンツへのゼロのアクセス (ZSA) を持ち、運用環境への特権アクセスはありません。 Microsoft 365 では、ジャストインタイム (JIT) だけで十分にアクセスできる (JEA) モデルを使用して、Microsoft 365 のサポートに必要な場合に運用環境への一時的な特権によるアクセスをサービスチームのエンジニアに提供します。 JIT アクセス モデルは、従来の永続的な管理者アクセスを、必要に応じた特権ロールへの一時的な昇格をエンジニアが要求するプロセスへと置き換えます。

サービスチームに割り当てられているエンジニア。 Id 管理ツール (IDM) を使用してサービスチームアカウントの運用サービス要求の適格性をサポートします。 資格の要求によって、エンジニアがすべてのクラウドスクリーンの要件を満たしていることを確認し、必要なトレーニングを完了し、アカウントを作成する前に適切な管理の承認を受けられるようにします。 すべての資格要件を満たしている場合にのみ、要求した環境のサービス チーム アカウントを作成できます。

サービスチームアカウントは、管理者特権または顧客コンテンツへのアクセスを許可しません。 エンジニアが Microsoft 365 サービスをサポートするために追加のアクセスを必要とする場合は、ロックボックスと呼ばれるアクセス管理ツールを使用して、必要なリソースへの昇格された一時的なアクセス権を要求します。 ロックボックスは、割り当てられたタスクを完了するために必要な最小限の特権、リソース、時間への昇格したアクセス権を制限します。 承認済みのレビュー担当者が JIT アクセス要求を承認した場合、エンジニアには、割り当てられた作業を完了するために必要な特権のみを持つ一時アカウントが付与されます。 この一時アカウントは多要素認証を必要とし、承認された期間が過ぎると自動的に削除されます。

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>Microsoft 365 は、運用システムへのリモートアクセスをどのように処理しますか?

Microsoft 365 システム コンポーネントは、運用チームから地理的に分離されたデータ センターに格納されます。 データセンター担当者は、Microsoft 365 システムへの論理的なアクセス権を持ちません。 そのため、Microsoft 365 サービスチームの担当者はリモートアクセスによって環境を管理します。 Microsoft 365 をサポートするためのリモート アクセスを必要とするサービスチームの担当者は、承認されたマネージャーからの承認後にのみリモート アクセスを許可されます。 すべてのリモート アクセスは、安全なリモート接続のために FIPS 140-2 互換 TLS を使用します。

Microsoft 365 では、サービスチームのリモートアクセスに Secure Administration Workstation (SAWs) を使用して、Microsoft 365 環境が侵害されないように保護しています。 これらのワークステーションは、USB ポートをロックダウンし、その環境をサポートするために必要なものについて、使用可能なソフトウェアを制限するなど、運用データの意図的または意図しない損失を防ぐために特に設計されています。 SAWs は、Microsoft のエンジニアがお客様のデータを故意または不注意に侵害することを検出して監視するために、綿密な追跡と監視を行います。

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>顧客のロックボックスを使用して顧客コンテンツの保護を追加する方法

お客様は、カスタマーロックボックスを有効にすることによって、そのコンテンツに対してさらにレベルのアクセス制御を追加できます。 ロックボックス昇格要求にお客様のコンテンツへのアクセスが含まれる場合、お客様のロックボックスには、承認ワークフローの最後の手順としてお客様からの承認が必要です。 これにより、組織はこれらの要求を承認または拒否し、顧客への直接アクセスを制御することができます。 顧客が顧客のロックボックス要求を拒否した場合、要求されたコンテンツへのアクセスは拒否されます。 お客様が一定の期間内に要求を却下または承認しない場合、その要求は、Microsoft がお客様のコンテンツへのアクセス権を取得しない限り、自動的に期限切れになります。 お客様が要求を承認した場合、お客様のコンテンツに対する Microsoft の一時アクセスは、トラブルシューティング操作の完了に割り当てられた時間が経過した後に自動的にログに記録され、監査および取り消しが行われます。

## <a name="related-external-regulations--certifications"></a>関連する外部規制 & 証明書

Microsoft のオンラインサービスは、社外の規制と証明書に準拠するために定期的に監査されます。 Id とアクセス制御に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: アカウント管理 <br> AC-3: アクセスの適用 <br> AC: 職務の分離 <br> AC-6: 最低限の特権 <br> AC-17: リモートアクセス | 2020年9月24日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 9.1: アクセス制御のビジネス要件 <br> 9.2: ユーザーアクセス管理 <br> 「9.3: ユーザーの責任」 <br> 9.4: システムおよびアプリケーションのアクセス制御 <br> 「15.1: サプライヤーとの関係における情報セキュリティ」 | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 9.2: ユーザーアクセス管理 <br> 9.4: システムおよびアプリケーションのアクセス制御 <br> 「15.1: サプライヤーとの関係における情報セキュリティ」 | 2020 月 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-33: アカウントの変更 <br> CA-34: ユーザー認証 <br> CA-35: 特権アクセス <br> CA-36: リモートアクセス <br> CA-57: カスタマーロックボックス Microsoft 管理者の承認 <br> CA-58: カスタマーロックボックスサービス要求 <br> CA-59: 顧客ロックボックスの通知 <br> CA-61: JIT のレビューと承認 | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-32: 共有アカウントポリシー <br> CA-33: アカウントの変更 <br> CA-34: ユーザー認証 <br> CA-35: 特権アクセス <br> CA-36: リモートアクセス <br> CA-53: サードパーティ製の監視 <br> CA-56: 顧客のロックボックスお客様の承認 <br> CA-57: カスタマーロックボックス Microsoft 管理者の承認 <br> CA-58: カスタマーロックボックスサービス要求 <br> CA-59: 顧客ロックボックスの通知 <br> CA-61: JIT のレビューと承認 | 2019 年 9 月 30 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-15: 顧客のロックボックス要求 | 2019 年 9 月 30 日 |