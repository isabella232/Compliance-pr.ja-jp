---
title: Microsoft 365エンジニアのアクセス制御
description: サービス エンジニアのアクセスMicrosoft 365アーキテクチャの概要。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2700c95feb5c32765e2dc3420c67800b154b1e9d
ms.sourcegitcommit: 85b36ce8c79fb111980cc6462f2addb44a924065
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2021
ms.locfileid: "60678474"
---
# <a name="microsoft-365-service-engineer-access-control"></a>Microsoft 365エンジニアのアクセス制御

ゼロスタンディング アクセス (ZSA) は、Microsoft サービス チームの担当者が、ユーザーの実稼働環境または顧客データに対する永続的な特権アクセスMicrosoft 365持たなことを意味します。 Microsoft サービス チーム のメンバーが何らかの理由でサービスを更新したり、顧客データにアクセスしたりする場合は、その必要性を理由として要求を提出し、承認されたマネージャーから承認を受ける必要があります。 大規模では、Microsoft 365 サービスを維持するために必要に応じて手動でアクセスを提供および削除することはできません。そのため、Microsoft は必要に応じて特権アクセスを管理するための自動ソリューションを開発しました。

## <a name="lockbox"></a>ロックボックス

Microsoft 365 システムおよび顧客データへのすべてのアクセスは、Just-In-Time (JIT) および Just-Enough-Access (JEA) モデルを使用してサービス エンジニアに、指定された Microsoft 365 サービスとデータへの一時的な特権アクセスを提供するアクセス制御システムである Lockbox によって仲介されます。 さらに、すべての要求とアクションは監査目的でログに記録され[、Office 365 管理](/office/office-365-management-api/get-started-with-office-365-management-apis)アクティビティ API とセキュリティとコンプライアンス センターを使用して[アクセスできます](https://protection.office.com/)。

Microsoft サービス エンジニアが任意のシステムに接続したり、Microsoft 365データにアクセスしたりするには、ロックボックスを使用してアクセス要求を送信する必要があります。 この要求は、特定の条件が満たされている場合にのみ承認できます。

- サービス エンジニアは、サービス チーム [アカウントの適格性要件を満たしています](assurance-microsoft-365-account-management.md)。
- これらは、要求内の作業に関連付けられた Lockbox ロールに属します。
- 要求されたアクセス時間は、許可される最大時間を超え
- 正当なビジネス上の正当な理由があります。
- アクセスする要求されたリソースは、作業スコープ内に含
- 管理者の承認を受ける

すべての条件が Lockbox によって満たされ、確認された後、要求された特定のアクションを実行するための一時的なアクセスが許可されます。 要求の時間が経過すると、アクセスが取り消されます。

![ロックボックス アクセス プロセス。](../media/assurance-lockbox-process.png)

さらに、顧客が顧客ロックボックス機能をライセンス[](/microsoft-365/compliance/customer-lockbox-requests)して有効にした場合、Microsoft サービス エンジニアが顧客データにアクセスしようとする試みは、顧客テナントの管理者によってさらに承認される必要があります。 顧客データにアクセスする必要性は、顧客と Microsoft の両方から発生する可能性があります。 たとえば、お客様が発生したインシデントでは、問題を解決するためにデータへのアクセスが必要な場合や、Microsoft が特定の更新プログラムを適用するためにデータ アクセスを必要とする場合があります。

![カスタマー ロックボックス アクセス プロセス。](../media/assurance-customer-lockbox-process.png)

お客様には、Customer Lockbox 要求を開始するためのツールが用意されていない。顧客ロックボックス要求を発生する必要があるチケットを Microsoft に提出する必要があります。 Microsoft サービス エンジニアによって発生した Customer Lockbox 要求は、Microsoft Manager および顧客テナントの承認された管理者によって承認される必要があります。

### <a name="lockbox-roles"></a>ロックボックスの役割

職務の分離と最小特権の原則を強制するには、サービス エンジニアは、チームでの役割に対応する Lockbox ロールに属している必要があります。 ロックボックスの役割は、Identity Management ツール内で管理され、サービス チーム メンバーがロックボックス要求プロセスを通じて承認できる特権とアクションを定義します。 サービス チームの担当者は、Lockbox ロールのメンバーを要求し、管理者の承認を受ける必要があります。 承認された場合、従業員のサービス チーム アカウントは、Active Directory (AD) および Azure Active Directory (AAD) によって適用されるセキュリティ グループに配置されます。

## <a name="constrained-management-interfaces"></a>制約付き管理インターフェイス

サービス エンジニアは、2 つの管理インターフェイスを使用して管理タスクを実行します。セキュリティで保護されたターミナル サービス ゲートウェイ (TSG) とリモート PowerShell を介した Secure Access ワークステーション (SAW) からのリモート デスクトップ。 これらの管理インターフェイス内では、承認されたロックボックス要求とソフトウェア ポリシーに基づくアクセス制御によって、どのアプリケーションが実行され、どのコマンドとコマンドレットを使用できるのかという大きな制限が適用されます。

## <a name="remote-desktop"></a>リモート デスクトップ

リモート デスクトップを使用してサービスを管理するサービス チーム メンバーは、特にこの使用例のために Microsoft が管理する特別に設計および製造されたノート PC を SAW から接続する必要があります。 Microsoft はサプライヤーと協力して SAW を構築し、短く安全なサプライチェーンを構築します。 SAW は、定義済みの管理タスクに必要な機能を除くすべての機能を制限するように構成された強化されたオペレーティング システムを使用します。 これらの制限には、すべての USB ポートの無効化、厳密なアプリケーション アクセス リスト、メール アクセスの削除、インターネット閲覧の制限、非アクティブスクリーンセーバーロックアウトの適用が含まれます。 Microsoft のアクセス制御システムは、SAW マシンを定期的に調べて、最新のセキュリティ制御に準拠しているか確認し、非準拠と判断された場合は自動的にコンピューターを無効にします。

サービス エンジニアは一度に 1 つの TSG にのみ接続できます。複数のセッションは許可されません。 ただし、TSG を使用すると、Microsoft 365チームの管理者は、それぞれ 1 つの同時セッションのみを持つ複数のサーバーに接続できます。そのため、管理者は効果的に職務を遂行できます。 サービス チームの管理者は、TSG 自体に対するアクセス許可を持つ必要があります。 TSG は、多要素認証 (MFA) と暗号化の要件を適用する場合にのみ使用されます。 サービス チーム管理者が TSG を介して特定のサーバーに接続すると、特定のサーバーは管理者ごとに 1 つのセッション制限を適用します。

従業員の使用制限、接続、および構成要件Microsoft 365 Active Directory グループ ポリシーによって確立されます。 これらのポリシーには、次の TSG 特性が含まれます。

- [FIPS 140-2](/compliance/regulatory/offering-FIPS-140-2)検証済みの暗号化のみを使用する
- 15 分の非アクティブ状態の後にセッションが切断される
- セッションは 24 時間後に自動的にログオフする

TSG への接続には、個別の物理スマート カードを使用する MFA も必要です。 サービス エンジニアは、さまざまなプラットフォームに対して異なるスマート カードを発行し、シークレット管理プラットフォームは資格情報の安全なストレージを確保します。 TSG は Active Directory グループ ポリシーを使用して、リモート サーバーにログインできるユーザー、許可されたセッション数、アイドル タイムアウト設定を制御します。

## <a name="remote-powershell"></a>リモート PowerShell

特別に構成された TSG を使用したリモート アクセスに加えて、Service Engineer Operations Lockbox の役割を持つサービス チームの担当者は、リモート PowerShell を使用して運用サーバー上の特定の管理機能にアクセスできます。 このアクセスを使用するには、ユーザーが読み取り専用 (デバッグ) アクセスを許可されている必要があります。Microsoft 365です。 特権エスカレーションは、ロックボックス プロセスを使用して TSG で有効になっているのと同じ方法で有効になります。

リモート アクセスの場合、各データセンターには、1 つのアクセス ポイントとして機能する負荷分散された仮想 IP があります。 使用可能なリモート PowerShell コマンドレットは、認証時に取得したアクセス要求で識別される特権レベルに基づいて行います。 これらのコマンドレットは、このメソッドを使用して接続するユーザーがアクセスできる唯一の管理機能を提供します。 リモート PowerShell は、エンジニアが使用できるコマンドの範囲を制限し、ロックボックス プロセスによって付与されるアクセスのレベルに基づいて行います。 たとえば、Exchange OnlineコマンドレットGet-Mailbox使用できますが、Set-Mailboxコマンドレットは使用できません。

## <a name="resources"></a>リソース

- [分離のMicrosoft 365](assurance-isolation-in-microsoft-365.md)
- [Microsoft の雇用前スクリーニング](assurance-pre-employment-screening.md)[Microsoft クラウドのバックグラウンド チェック](assurance-cloud-background-check.md)
