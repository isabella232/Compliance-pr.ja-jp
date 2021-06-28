---
title: GDPR
description: Microsoft 技術的なガイダンス - 削除要求を送信するための FastTrack 移行ツールセット
keywords: FastTrack 移行、Microsoft 365 Education、Microsoft 365 ドキュメント、GDPR
localization_priority: Priority
Robots: NOFOLLOW,NOINDEX
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: mohitku
author: MohitKumar
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: d3429d3fb35317146e32fddc71bae2f12c40269d
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089510"
---
# <a name="fasttrack-migration-toolset-for-submitting-delete-request"></a><span data-ttu-id="3fe7f-104">削除要求を送信するための FastTrack 移行ツールセット</span><span class="sxs-lookup"><span data-stu-id="3fe7f-104">FastTrack Migration Toolset for Submitting Delete Request</span></span>

## <a name="toolset-purpose"></a><span data-ttu-id="3fe7f-105">ツールセットの目的</span><span class="sxs-lookup"><span data-stu-id="3fe7f-105">Toolset purpose</span></span>

<span data-ttu-id="3fe7f-p101">FastTrack 移行に関与しているお客様の場合は、ユーザー アカウントを削除しても、Microsoft FastTrack チームが保持しているデータ コピーは削除されません。このデータ コピーは移行を完了する目的でのみ保持されています。移行時に Microsoft FastTrack チームにデータ コピーの削除も依頼する場合は、このツールセットを介してリクエストを送信してください。通常の業務において、移行が完了した時点で、Microsoft FastTrack がすべてのデータ コピーを削除します。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-p101">In the event that you are a customer currently engaged in FastTrack migrations, deleting the user account will not delete the data copy held by the Microsoft FastTrack team, which is held for the sole purpose of completing the migration. If during the migration you would like the Microsoft FastTrack team to also delete the data copy, submit a request via this tool set. In the ordinary course of business, Microsoft FastTrack will delete all data copies once the migration is complete.</span></span>

### <a name="supported-platforms"></a><span data-ttu-id="3fe7f-109">サポートされるプラットフォーム</span><span class="sxs-lookup"><span data-stu-id="3fe7f-109">Supported platforms</span></span>

<span data-ttu-id="3fe7f-p102">Microsoft は、Windows プラットフォームと PowerShell コンソールでこのツールセットの初期リリースをサポートしています。以下の既知のプラットフォームがこのツールセットでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-p102">Microsoft supports the initial release of this  toolset in the Windows platform and PowerShell console. The following known platforms are supported by this toolset:</span></span>

<span data-ttu-id="3fe7f-112">\***表 1 - このツールセットでサポートされているプラットフォーム** _</span><span class="sxs-lookup"><span data-stu-id="3fe7f-112">\***Table 1 — Platforms supported by this toolset** _</span></span>

<span data-ttu-id="3fe7f-113">_\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3fe7f-113">_\*\*\*</span></span>

|<span data-ttu-id="3fe7f-114">PowerShell バージョン</span><span class="sxs-lookup"><span data-stu-id="3fe7f-114">PowerShell version</span></span>|<span data-ttu-id="3fe7f-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3fe7f-115">Windows 7</span></span>|<span data-ttu-id="3fe7f-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3fe7f-116">Windows 8</span></span>|<span data-ttu-id="3fe7f-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="3fe7f-117">Windows 10</span></span>|<span data-ttu-id="3fe7f-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3fe7f-118">Windows Server 2012</span></span>|<span data-ttu-id="3fe7f-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3fe7f-119">Windows Server 2016</span></span>|
|:---:|:---:|:---:|:---:|:---:|:---:|
|<span data-ttu-id="3fe7f-120">5.0</span><span class="sxs-lookup"><span data-stu-id="3fe7f-120">5.0</span></span>|<span data-ttu-id="3fe7f-121">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="3fe7f-121">Not Supported</span></span>|<span data-ttu-id="3fe7f-122">サポートされている</span><span class="sxs-lookup"><span data-stu-id="3fe7f-122">Supported</span></span>|<span data-ttu-id="3fe7f-123">サポート</span><span class="sxs-lookup"><span data-stu-id="3fe7f-123">Supported</span></span>|<span data-ttu-id="3fe7f-124">サポート</span><span class="sxs-lookup"><span data-stu-id="3fe7f-124">Supported</span></span>|<span data-ttu-id="3fe7f-125">サポート</span><span class="sxs-lookup"><span data-stu-id="3fe7f-125">Supported</span></span>|
|<span data-ttu-id="3fe7f-126">5.1</span><span class="sxs-lookup"><span data-stu-id="3fe7f-126">5.1</span></span>|<span data-ttu-id="3fe7f-127">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="3fe7f-127">Not Supported</span></span>|<span data-ttu-id="3fe7f-128">サポートされている</span><span class="sxs-lookup"><span data-stu-id="3fe7f-128">Supported</span></span>|<span data-ttu-id="3fe7f-129">サポート</span><span class="sxs-lookup"><span data-stu-id="3fe7f-129">Supported</span></span>|<span data-ttu-id="3fe7f-130">サポート</span><span class="sxs-lookup"><span data-stu-id="3fe7f-130">Supported</span></span>|<span data-ttu-id="3fe7f-131">サポート済み</span><span class="sxs-lookup"><span data-stu-id="3fe7f-131">Supported</span></span>|
|

### <a name="obtaining-the-toolset"></a><span data-ttu-id="3fe7f-132">ツールセットの取得</span><span class="sxs-lookup"><span data-stu-id="3fe7f-132">Obtaining the toolset</span></span>

<span data-ttu-id="3fe7f-p103">このツールセットは、PowerShell コンソール アプリケーション上の PowerShell ギャラリーで入手できます。このコマンドレット モジュールを検索して読み込むには、まず、PowerShell を管理者モードで開いて、モジュールをインストールするための適切なアクセス許可が付与されるようにします。過去に PowerShell を使用したことがない場合は、Windows のタスク バーに移動して、検索ボックスに「PowerShell」と入力します。右クリックを使用してコンソール アプリケーションを選択し、**[管理者として実行]** を選択してから、**[はい]** をクリックして Windows PowerShell を実行します。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-p103">This toolset is available in the PowerShell Gallery on the PowerShell console application.  To locate and load this cmdlet module, first open PowerShell in administrator mode so it has the appropriate permissions to install the module. If you have not used PowerShell previously go to your Windows Task Bar and in the search box type 'PowerShell”. Select the console app using right-click and choose **Run as administrator**, then click **Yes** to run Windows PowerShell.</span></span>

![PowerShell - 管理者として実行](../media/fasttrack-powershell_image.png)

![PowerShell - アプリケーションに変更を許可する](../media/fasttrack-run-powershell_image.png)

<span data-ttu-id="3fe7f-p104">これでコンソールが開くので、スクリプト実行のアクセス許可を設定する必要があります。次のコマンドを入力して、スクリプトの実行を許可します。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-p104">Now that the console is open, you need to set permissions for script execution. Type the following command to allow the scripts to run:</span></span>

```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process
```

<span data-ttu-id="3fe7f-141">この操作の確認が要求されます。これは、管理者が自分の判断で範囲を変更できるためです。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-141">You will be prompted to confirm this action, as the administrator can change the scope at their discretion.</span></span>

<span data-ttu-id="3fe7f-142">\**_実行ポリシーの設定_* _</span><span class="sxs-lookup"><span data-stu-id="3fe7f-142">\**_Set Execution Policy_* _</span></span>

![PowerShell での実行ポリシー変更の設定](../media/powershell-set-execution-policy_image.png)

<span data-ttu-id="3fe7f-144">これで、スクリプトを許可するようにコンソールが設定されたので、次のコマンドを実行してモジュールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-144">Now that the console is set to allow the script, run this next command to install the module:</span></span>

```powershell
Install-Module -Name Microsoft.FastTrack -Repository PSGallery -WarningAction SilentlyContinue -Force
```

### <a name="prerequisites-for-module"></a><span data-ttu-id="3fe7f-145">モジュールの前提条件</span><span class="sxs-lookup"><span data-stu-id="3fe7f-145">Prerequisites for module</span></span>

<span data-ttu-id="3fe7f-p105">このモジュールが正常に動作するためには、まだインストールされていない依存モジュールをインストールする必要があります。PowerShell を再起動しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-p105">To successfully execute this module, you may need to install dependent modules for use if they are not already installed. You may need to restart PowerShell.</span></span>

<span data-ttu-id="3fe7f-p106">DSR を送信するには、まず、Office 365 認証情報を使用してログインする必要があります。適切な認証情報を入力すると、全体管理者の状態が検証され、テナント情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-p106">In order to submit a DSR, you must first log in using your Office 365 credentials. Entering the proper credentials will validate your global administrator status and collect tenant information.</span></span>

```powershell
Login-FastTrackAccount -ApiKey <API Key provided by FastTrack MVM>
```

<span data-ttu-id="3fe7f-150">ログインに成功すると、資格情報とキーが保存され、現在の PowerShell セッションの残りの部分に対して FastTrack モジュールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-150">Once successfully logged in, the credentials and key will be stored for use with FastTrack modules for the remainder of the current PowerShell session.</span></span>

<span data-ttu-id="3fe7f-151">商用以外のクラウド環境に接続する必要がある場合は、次の有効な環境のいずれかを使用して、_-Environment\* を *Log in* コマンドに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-151">If you need to connect to a cloud environment, other than commercial, _-Environment\* will need to be added to *Log in* command with one of the following valid environments:</span></span>

- <span data-ttu-id="3fe7f-152">AzureCloud</span><span class="sxs-lookup"><span data-stu-id="3fe7f-152">AzureCloud</span></span>
- <span data-ttu-id="3fe7f-153">AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="3fe7f-153">AzureChinaCloud</span></span>
- <span data-ttu-id="3fe7f-154">AzureGermanCloud</span><span class="sxs-lookup"><span data-stu-id="3fe7f-154">AzureGermanCloud</span></span>
- <span data-ttu-id="3fe7f-155">AzureUSGovernmentCloud</span><span class="sxs-lookup"><span data-stu-id="3fe7f-155">AzureUSGovernmentCloud</span></span>

```powershell
Login-FastTrackAccount -ApiKey <API Key provided by FastTrack MVM> -Environment <cloud environment>
```

<span data-ttu-id="3fe7f-156">DSR 要求を送信するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-156">To submit a DSR request, run the following command:</span></span>

```powershell
Submit-FastTrackGdprDsrRequest -DsrRequestUserEmail SubjectUserEmail@mycompany.com
```

<span data-ttu-id="3fe7f-p107">成功すると、コマンドレットがトランザクション ID オブジェクトを返します。このトランザクション ID を保管してください。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-p107">On success, the cmdlet will return a Transaction ID object. Please retain the Transaction ID.</span></span>

#### <a name="checking-the-status-of-a-request-transaction"></a><span data-ttu-id="3fe7f-159">要求トランザクションの状態の確認</span><span class="sxs-lookup"><span data-stu-id="3fe7f-159">Checking the status of a request transaction</span></span>

<span data-ttu-id="3fe7f-160">先ほど取得したトランザクション ID を使用して、次の関数を実行します。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-160">Run the following function using the previously obtained Transaction ID:</span></span>

```powershell
Get-FastTrackGdprDsrRequest -TransactionID "YourTransactionID"
```

#### <a name="transaction-status-codes"></a><span data-ttu-id="3fe7f-161">トランザクション状態コード</span><span class="sxs-lookup"><span data-stu-id="3fe7f-161">Transaction Status Codes</span></span>

|<span data-ttu-id="3fe7f-162">トランザクション</span><span class="sxs-lookup"><span data-stu-id="3fe7f-162">Transaction</span></span>|<span data-ttu-id="3fe7f-163">状態</span><span class="sxs-lookup"><span data-stu-id="3fe7f-163">Status</span></span>|
|---|---|
|<span data-ttu-id="3fe7f-164">**Created**</span><span class="sxs-lookup"><span data-stu-id="3fe7f-164">**Created**</span></span>|<span data-ttu-id="3fe7f-165">要求が作成されました。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-165">Request has been created.</span></span>|
|<span data-ttu-id="3fe7f-166">**Failed**</span><span class="sxs-lookup"><span data-stu-id="3fe7f-166">**Failed**</span></span>|<span data-ttu-id="3fe7f-167">要求を作成できませんでした。再送信するか、サポートにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-167">Request failed to create, please resubmit, or contact support.</span></span>|
|<span data-ttu-id="3fe7f-168">**Completed**</span><span class="sxs-lookup"><span data-stu-id="3fe7f-168">**Completed**</span></span>|<span data-ttu-id="3fe7f-169">要求が完了してサニタイズされました。</span><span class="sxs-lookup"><span data-stu-id="3fe7f-169">Request has been completed and sanitized.</span></span>|
|

<!-- original version: **Created**  Request has been created<br/>**Failed** Request failed to create, please resubmit, or contact support<br/>**Completed** Request has been completed and sanitized -->

## <a name="learn-more"></a><span data-ttu-id="3fe7f-170">詳細情報</span><span class="sxs-lookup"><span data-stu-id="3fe7f-170">Learn more</span></span>

[<span data-ttu-id="3fe7f-171">Microsoft Trust Center</span><span class="sxs-lookup"><span data-stu-id="3fe7f-171">Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
