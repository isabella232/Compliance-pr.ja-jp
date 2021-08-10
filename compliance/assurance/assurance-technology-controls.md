---
title: Microsoft 365
description: この記事では、Microsoft がテクノロジ制御に使用するツールとテクノロジの概要を説明Microsoft 365。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: b82dfdbe3de63f8b5ded42c037d0d574da051047462c6900d368a70efd625fcf
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54291725"
---
# <a name="technology-controls-in-microsoft-365"></a>Microsoft 365 

Microsoft では、いくつかのツールとテクノロジを使用して、オンライン サービス内の顧客データへのアクセスを制御、管理、監査します。 これらは、Exchange Online、SharePoint、ロックボックス、顧客ロックボックス、多要素認証などに適用されます。 Yammerアクセスコントロールで説明されている同様の[コントロールYammer Enterprise使用します](assurance-yammer-enterprise-access-controls.md)。

Microsoft 365エンジニアは、顧客データに対する永続的Microsoft 365アクセス権を持つ必要があります。 エンジニアは、サービス操作のために顧客データにアクセスする前に、Microsoft の承認プロセスを実行する必要があります。 顧客が顧客ロックボックス機能のライセンスをオンラインおよびオンラインExchange OnlineするSharePoint顧客データへのアクセスには、顧客の承認が必要です。 承認された後、サービス固有の管理アカウントは、サービス要求で必要なタスクに対する Just-in-time アクセスをプロビジョニングされます。

## <a name="lockbox-and-customer-lockbox"></a>ロックボックスと顧客ロックボックス

まれですが、お客様は Microsoft のエンジニアに顧客コンテンツを公開するサポートを Microsoft に要求できます。 ユーザーへのアクセスを制御Exchange Online、Microsoft は Lockbox と呼ばれるアクセス制御システムを使用します。 Microsoft のエンジニアがオンライン システムまたはオンライン Exchange OnlineまたはSharePointにアクセスする前に、Lockbox を使用してアクセス要求を送信する必要があります。 オンラインおよびオンラインのExchange OnlineサービスSharePointは、ロックボックス システムによって処理されます。 Lockbox と Customer Lockbox の両方を使用すると、承認されたアクセスはすべて一意のユーザーに対して追跡可能であり、エンジニアは顧客データの処理に対して責任を持つ必要があります。

> [!NOTE]
> Exchange Onlineメールボックスに格納Skype for Businessデータが含まれます。 Skype for Businessには、ユーザー Skypeにアップロードされた会議ブロードキャストの録画やコンテンツは含まれます。 SharePointオンラインには、OneDrive for Businessが含まれます。

Lockbox は、サービス内で運用機能および管理機能を実行する機能をエンジニアに付与するアクセス許可の要求を処理します。 エンジニアは Lockbox を介して要求を送信し、エンジニアが顧客データにアクセスするには、Microsoft マネージャーが要求を承認する必要があります。 管理者の承認後、エンジニアは顧客データへの時間制限と範囲限定のアクセス権を持ち、顧客の問題に取り組む。

顧客ロックボックスはMicrosoft 365データ アクセスの承認のための手順が必要な場合に、コンプライアンスの義務を満たすのに役立ちます。 これは、FedRAMP や HIPAA などの一部のコンプライアンス基準に対する要件です。 Customer Lockbox は、ロックボックス承認プロセスにユーザーを挿入し、サービス操作用の Exchange Online または SharePoint Online コンテンツへの Microsoft アクセスの承認を制御する機能を提供します。

まれに、Microsoft サービス エンジニアがデータにアクセスする必要がある場合は、問題の解決に必要なデータにのみアクセス権を付与し、一部の時間だけアクセスできます。 アクセス要求を拒否した場合、Microsoft エンジニアはコンテンツにアクセスする権限を持たれなく、サービス操作を完了できない。 要求を承認した場合、Microsoft のエンジニアは監視された制限付きの管理インターフェイスを介して、コンテンツへのジャストインタイム アクセスを使用できるようになります。

サポート エンジニアが実行したアクションは監査目的でログに記録され[、Office 365 管理](/office/office-365-management-api/get-started-with-office-365-management-apis)アクティビティ API とセキュリティ とコンプライアンス センターを介[してアクセスできます](https://protection.office.com/)。

>[!NOTE]
> 顧客ロックボックスは[、Microsoft 365 E5購入](https://products.office.com/business/office-365-enterprise-e5-business-software)として使用できます。 詳細については、「顧客ロック[ボックス要求Microsoft 365を参照してください](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2)。

## <a name="just-in-time-access"></a>Just-In-Time アクセス

Microsoft では、資格情報の改ざんリスクと横方向の攻撃を軽減するために、Microsoft 365(JIT) アクセス原則を使用します。 JIT は、サービスへの永続的な管理アクセスを削除し、エンタイトルメントをオンデマンドでそれらのロールに昇格する機能に置き換わります。 管理者から永続的なアクセス権を削除すると、資格情報が必要な場合にのみ使用できます。資格情報の盗難リスクを軽減します。

JIT アクセス モデルでは、管理者の職務を実行するために、エンジニアが制限された期間の昇格された特権を要求する必要があります。 さらに、エンジニアは、コンピューターで生成された複雑なパスワードで作成された一時的なアカウントを使用し、必要なタスクを実行できる役割のみを付与します。 たとえば、Lockbox によって付与される管理アクセスは時間にバインドされ、付与される時間アクセスの量は要求された役割によって異なります。 エンジニアは、ロックボックス システムへの要求に必要な時間アクセスの期間を指定します。 要求された時間が昇格の最大許容時間を超えると、ロックボックス システムは要求を拒否します。 有効期限が切れると、管理アクセスが削除され、一時的なアカウントの有効期限が切れます。

アクセスが承認および承認されると、エンジニアは承認システムによって生成された 1 回の使用管理パスワードを受け取る。 昇格されたアクセスの要求が承認されるごとに、新しいパスワードが生成されます。 パスワードはパスワード セーフにコピーされ、Microsoft 企業環境のエンジニアの資格情報とは別であり、承認された管理者特権アクセス セッションにのみ有効です。

## <a name="constrained-management-interfaces"></a>制約付き管理インターフェイス

エンジニアは、2 つの管理インターフェイスを使用して管理タスクを実行します。セキュリティで保護されたターミナル サービス ゲートウェイ (TSG) とリモート PowerShell を介したリモート デスクトップ。 これらの管理インターフェイス内では、ソフトウェア ポリシーとアクセス制御によって、実行されるアプリケーションと使用可能なコマンドとコマンドレットに大きな制限が適用されます。

Microsoft 365サーバーは、同時セッションをサービスごとのチーム管理者 (サーバーごとに) 1 つのセッションに制限します。 TSG は、ユーザーに対して 1 つの同時セッションのみを許可し、複数のセッションを許可しません。 サーバーごとに 1 つのセッションを使用すると、Microsoft 365チームの管理者は複数のサーバーに同時に接続できます。管理者は効果的に職務を遂行できます。 サービス チームの管理者は、TSG 自体に対するアクセス許可を持つ必要があります。 TSG は、多要素認証 (MFA) と暗号化の要件を適用する場合にのみ使用されます。 サービス チーム管理者が TSG を介して特定のサーバーに接続すると、特定のサーバーは管理者ごとに 1 つのセッション制限を適用します。

ユーザーの使用制限と接続および構成要件は、Active Directory Microsoft 365ポリシーによって確立されます。 これらのポリシーには、次の特性が含まれます。

- TSG は [FIPS](https://www.microsoft.com/TrustCenter/Compliance/FIPS) 140-2 検証済みの暗号化のみを使用します。
- TSG セッションは、30 分の非アクティブ状態の後に切断されます。
- TSG セッションは、24 時間後に自動的にログオフします。

TSG への接続には、個別の物理スマート カードと、エンジニアの Microsoft 企業資格情報とは別のアカウントを使用する MFA も必要です。 エンジニアは、さまざまなプラットフォームに対して異なるスマート カードを発行され、シークレット管理プラットフォームは資格情報の安全なストレージを確保します。 TSG は Active Directory グループ ポリシーを使用して、リモート サーバーにログインできるユーザー、許可されたセッション数、アイドル タイムアウト設定を制御します。 追加のポリシーは、許可されたアプリケーションへのアクセスを制限し、インターネット アクセスを制限します。

特別に構成された TSG を使用したリモート アクセスに加えて、Exchange Online を使用すると、サービス エンジニア操作の役割を持つユーザーは、リモート PowerShell を使用して運用サーバー上の特定の管理機能にアクセスできます。 これを行うには、ユーザーに対して、実稼働環境への読み取り専用 (デバッグ) アクセスMicrosoft 365必要があります。 特権エスカレーションは、ロックボックス プロセスを使用して TSG で有効になっているのと同じ方法で有効になります。

リモート アクセスの場合、各データセンターには、1 つのアクセス ポイントとして機能する負荷分散された仮想 IP があります。 使用可能なリモート PowerShell コマンドレットは、認証時に取得したアクセス要求で識別される特権レベルに基づいて行います。 これらのコマンドレットは、このメソッドを使用して接続するユーザーがアクセスできる唯一の管理機能を提供します。 リモート PowerShell は、エンジニアが使用できるコマンドの範囲を制限し、ロックボックス プロセスによって付与されるアクセスのレベルに基づいて行います。 たとえば、このExchange Online、Get-Mailbox使用できますが、Set-Mailbox使用できません。
