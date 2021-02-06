---
title: Microsoft 365 レポート機能
description: Azure Active Directory や Exchange Online など、Microsoft 365 内のさまざまなレポート機能について説明します。
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
- M365-analytics
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: a745c470dc30703f438258985169431c1053e65d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120786"
---
# <a name="microsoft-365-reporting-features"></a>Microsoft 365 レポート機能

Microsoft 365 のレポート機能は、Azure Active Directory (Azure AD)、Exchange Online、デバイス管理、監督レビュー、およびデータ損失防止 (DLP) のさまざまな監査レポートを提供します。 これらのレポートは、Microsoft 365 アクティビティ レポートとは異なります。

## <a name="microsoft-365-reports-dashboard"></a>Microsoft 365 レポート ダッシュボード

Microsoft 365 管理センター プレビューのレポート ダッシュボードには、Microsoft 365 全体の使用状況アクティビティが表示されます。 Microsoft 365 全体管理者、または Exchange Online、SharePoint Online、または Skype for Business 管理者は、そのサービスの使用状況に関する詳細な情報を取得できます。 たとえば、特定の Microsoft 365 サービスのユーザー数、Microsoft 365 Apps for enterprise (以前の名前は Office 365 ProPlus) をアクティブ化したユーザーの数、および組織を通過するメールの量。 レポートは、過去 7 日間、30 日間、90 日間、および 180 日間利用できます。

次の利用状況レポートを使用できます。

- [電子メール アクティビティ レポート](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Microsoft Officeライセンス認証レポート](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [SharePoint Online サイトの利用状況レポート](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [OneDrive for Business 使用状況レポート](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Yammer のアクティビティ レポート](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [Skype for Business アクティビティ レポート](/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [Skype for Business ピアツーピア アクティビティ レポート](/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [Skype for Business 電話会議開催者レポート](/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [Skype for Business 電話会議参加者アクティビティ レポート](/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

詳細については [、Microsoft 365 管理センターのアクティビティ レポートを参照してください](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263)。

## <a name="azure-ad-reports"></a>Azure AD レポート

Microsoft 365 では、Azure ADを使用して認証と ID 管理を行います。 Microsoft 365 管理者は、Azure によって生成されたレポートを使用して、異常なアクティビティとデータへの不正アクセスを特定します。 Azure AD のアクセスレポートと使用状況レポートを使用すると、組織のディレクトリの整合性とセキュリティを確認できます。 この情報を使用すると、考えられるセキュリティ リスクを特定して軽減できます。

Azure ADレポートは、Microsoft Excel にエクスポートして、Microsoft 365 の他のデータと関連付けできます。 たとえば、監査ログ検索の結果は、アクセス、認証、およびアプリケーション レベルのアクティビティに関する分析情報を提供できます。 Azure AD Premium では、高度な異常およびリソース使用状況レポートを利用できます。 これらの高度なレポートは、セキュリティの状況を改善し、デバイス アクセスとアプリケーションの使用状況に関する分析を適用することで潜在的な脅威に対応するのに役立ちます。 レポートとレポートへのアクセス方法の詳細については、「[Azure Active Directory レポート](/azure/active-directory/reports-monitoring/overview-reports/)」を参照してください。

## <a name="exchange-online-audit-reports"></a>Exchange Online 監査レポート

Exchange Online 監査レポートには、メールボックス アクセスの詳細と、管理者が Exchange Online テナントに加えた変更が含まれます。 メールボックス監査では、次の表のタスクを使用してレポートを実行し、Exchange Online 監査ログをエクスポートできます。

> [!NOTE]
> 監査イベントをそのメールボックスの監査ログに保存するには、メールボックスごとにメールボックス監査ログを有効にする必要があります。 メールボックスのメールボックス監査ログが有効になっていない場合、そのメールボックスのイベントは監査ログに保存されません。また、メールボックス監査レポートには表示されません。 詳細については、「メールボックス監査を [有効にする」を参照してください](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918)。

| Task | 説明 |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [所有者以外のメールボックス アクセスのレポートを実行する](/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | メールボックスの所有者以外のユーザーがアクセスしたメールボックスの一覧を表示します。 レポートには、メールボックスにアクセスしたユーザー、メールボックスで行った操作、およびアクションが成功したかどうかに関する情報が含されます。 |
| [メールボックス監査ログのエクスポート](/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | メールボックス監査ログには、メールボックス所有者以外のユーザーが実行したメールボックス内のアクセスとアクションに関する情報が含まれます。 管理者は、レポートを生成する日付範囲と共にメールボックスを指定できます。 ログは XML 形式でエクスポートされ、メッセージに添付され、管理者が決定した特定のユーザーに送信されます。 |
| [管理者役割グループのレポートを実行する](/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | 管理者役割グループは、ユーザーに管理者権限を割り当てる。 これらの特権を使用すると、ユーザーはパスワードのリセット、メールボックスの作成または変更、他のユーザーへの管理者特権の割り当てなどの管理タスクを実行できます。 管理者役割グループ レポートには、メンバーの追加や削除など、役割グループに対する変更が表示されます。 |
| [管理者監査ログを表示する](/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | 管理者監査ログ レポートには、Exchange Online の管理者が実行した作成、更新、および削除のすべての機能が一覧表示されます。 ログ エントリは、実行されたコマンドレット、使用されたパラメーター、コマンドレットを実行したユーザー、および影響を受けたオブジェクトに関する情報を提供します。 |
| [メールボックス コンテンツの検索と保持](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | メールボックスの電子情報開示または電子情報開示In-Place保持設定に対するIn-Place詳細を提供します。 |
| [管理者監査ログをエクスポートする](/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | 管理者監査ログには、Exchange Online での作成、更新、削除などの特定の管理操作が記録されます。 ログの結果は XML にエクスポートされ、管理者は一連のユーザーにこのログを送信できます。 |
| [メールボックスごとの訴訟保留レポートを実行する](/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | メールボックスの訴訟ホールド設定に対する変更の詳細を提供します。 |
| [外部管理者監査ログの表示とエクスポート](/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | 外部管理者が実行する操作の詳細が含まれる。 エントリは、実行されたコマンドレット、使用されたパラメーター、および Exchange Online でオブジェクトを作成、変更、または削除する操作に関する情報を提供します。 |

## <a name="device-compliance-reports"></a>デバイス コンプライアンス レポート

Microsoft 365 の Basic Mobility and Security を使用して、サブスクリプションに接続されているモバイル デバイスを管理し、セキュリティで保護します。 仕事用の電子メール、予定表、連絡先、ドキュメントにアクセスするために使用されるモバイル デバイスは、従業員がいつでもどこからでも仕事を行えるのを確認する上で重要な役割を果たします。 組織の情報を保護する必要があります。 Microsoft 365 の Basic Mobility and Security を使用して、デバイスのセキュリティ ポリシーとアクセス ルールを設定します。 紛失したり盗まれたりした場合は、Microsoft 365 の Basic Mobility and Security を使用してモバイル デバイスをワイプすることもできます。

基本的なモビリティとセキュリティのコンプライアンス レポートでは、Microsoft 365 データにアクセスするモバイル デバイスをセキュリティで保護するために組織が設定したポリシーの概要を示します。 このレポートでは、コンプライアンスの状態、報告された違反、ブロックされたデバイス、セキュリティ ポリシーの結果としてワイプされたデバイスの数によってデバイスをフィルター処理できます。 詳細については [、「Microsoft 365 の Basic Mobility and Security の概要」を参照](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)してください。

## <a name="data-loss-prevention"></a>データ損失防止

DLP ポリシーは、組織内の情報のセキュリティとフローを管理するのに役立ちます。 ポリシーを設定して、コンテンツへのアクセスをブロックしたり、データを暗号化したり、アプリケーション内の DLP ポリシー ヒントを使用してポリシーとポリシー違反をユーザーに通知することができます。 DLP レポートは、ポリシーとルールの一致、上書き、誤検知の数に関する分析情報を提供します。

Microsoft 365 管理センターを使用して、DLP ポリシーによって検出されたメッセージの数に関する情報を表示します。 DLP レポートは、送信メールと受信メールのポリシーとルールの一致に関する分析情報を提供します。 また、Exchange 管理センターを使用して、過去 24 時間以内に各ポリシーの一致、上書き、誤検知の数を表示できます。 Excel レポートをダウンロードすると、どのユーザーがメッセージを送信したのか、何日に、どのポリシー一致がトリガーされたのかなど、さらに詳細な情報を表示できます。 詳細については、「DLP ポリシー検出 [に関するレポートの表示」を参照してください](/previous-versions/exchange-server/exchange-150/jj889415(v=exchg.150))。

## <a name="auditing-in-yammer-enterprise"></a>Yammer Enterprise での監査

Yammer Enterprise を使用すると、管理者は Yammer データエクスポート [API](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)を介して Yammer ネットワークからユーザー アクティビティ データをエクスポートしたり、[Yammer ネットワーク管理者] ページを使用して手動でユーザー アクティビティ データをエクスポートすることができます。 ログをエクスポートする機能は、ネットワーク管理者に制限Yammer。 (すべての Microsoft 365 グローバル管理者はYammer管理者です)。

次のデータをエクスポートできます。

| Filename | 説明 |
|----------------------------|-------------------------------------------------------------------------|
| Users.csv | ネットワーク内のすべての新規ユーザー、保留中ユーザー、中断ユーザー |
| Messages.csv | ネットワーク内のすべてのメッセージ |
| Files.csv (メタデータ) | ファイル名、ファイル API URL、アップデータの ID、アップロード先などのメタデータ。 |
| Files.csv (元のファイル) | ユーザーがファイルにアップロードした元のファイルの zip Yammer |
| Topics.csv | ネットワーク上に作成されたトピック |
| Pages.csv | ネットワーク内のユーザーによって作成されたページ (メモ) |
| Admins.csv | ネットワーク上のすべての認証管理者 |
| Networks.csv | すべてのYammer外部ネットワーク |

Yammerエンタープライズ データは、Microsoft 365 アクティビティ レポートでも利用できます。 さらに、Yammerは、Microsoft 365 マネージメント アクティビティ API を介して追加のログを公開し、Power BI を使用してデータを理由付けする機能に積極的に取り組み中です。 これらの機能 [Office詳細については](https://fasttrack.microsoft.com/roadmap?filters=yammer) 、「ロードマップ」を参照してください。
