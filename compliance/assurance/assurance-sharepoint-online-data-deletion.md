---
title: Microsoft 365 SharePoint Online データの削除
description: SharePoint Online でのデータ削除の仕組み (削除されたコンテンツの保存場所や期間など) について説明します。
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
- SPO_Content
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e89a261e44ef4eb4a1399027b70be88fffb82036
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497411"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a><span data-ttu-id="45ba2-103">Microsoft 365 での SharePoint Online データの削除</span><span class="sxs-lookup"><span data-stu-id="45ba2-103">SharePoint Online data deletion in Microsoft 365</span></span>

<span data-ttu-id="45ba2-104">SharePoint Online は、アプリケーション データベース内に抽象化されたコードとしてオブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="45ba2-104">SharePoint Online stores objects as abstracted code within application databases.</span></span> <span data-ttu-id="45ba2-105">ユーザーがファイルを SharePoint Online にアップロードすると、そのファイルは逆アセンブルされ、アプリケーション コードに変換され、複数のデータベースの複数のテーブルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="45ba2-105">When a user uploads a file to SharePoint Online, that file is disassembled and translated into application code and stored in multiple tables across multiple databases.</span></span> <span data-ttu-id="45ba2-106">SharePoint Online では、顧客がアップロードするコンテンツはすべてチャンクに分割され、暗号化され (複数の AES 256 ビット キーを使用する可能性があります)、データセンター全体に分散されます。</span><span class="sxs-lookup"><span data-stu-id="45ba2-106">In SharePoint Online, all content that a customer uploads is broken into chunks, encrypted (potentially with multiple AES 256-bit keys), and distributed across the datacenter.</span></span> <span data-ttu-id="45ba2-107">チャンク処理と暗号化プロセスの詳細については [、「Microsoft Cloud での暗号化」を参照してください](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)。</span><span class="sxs-lookup"><span data-stu-id="45ba2-107">For specific details about the chunking and encryption process, see [Encryption in the Microsoft Cloud](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview).</span></span> 

<span data-ttu-id="45ba2-108">SharePoint Online では、アイテムを元の場所から削除した後、アイテムは 93 日間保持されます。</span><span class="sxs-lookup"><span data-stu-id="45ba2-108">In SharePoint Online, items are retained for 93 days from the time you delete them from their original location.</span></span> <span data-ttu-id="45ba2-109">ユーザーがサイトのごみ箱から削除したり、ごみ箱を空にしたりしない限り、サイトのごみ箱に残されます。</span><span class="sxs-lookup"><span data-stu-id="45ba2-109">They stay in the site Recycle Bin the entire time, unless someone deletes them from there or empties that Recycle Bin.</span></span> <span data-ttu-id="45ba2-110">その場合、アイテムはサイト コレクションのごみ箱に移動し、残りの 93 日間は保存されます。</span><span class="sxs-lookup"><span data-stu-id="45ba2-110">In that case, the items go to the site collection Recycle Bin, where they stay for the remainder of the 93 days.</span></span> <span data-ttu-id="45ba2-111">削除済みアイテムの復元の詳細については [、「SharePoint](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) サイトのごみ箱のアイテムを復元する」および「サイト コレクションのごみ箱から削除済みアイテムを復元する」 [を参照してください](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b)。</span><span class="sxs-lookup"><span data-stu-id="45ba2-111">For info about restoring deleted items, see [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and [Restore deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b).</span></span> <span data-ttu-id="45ba2-112">ごみ箱の保持時間は SharePoint Online では構成できません。</span><span class="sxs-lookup"><span data-stu-id="45ba2-112">The Recycle Bin retention time is not configurable in SharePoint Online.</span></span>

<span data-ttu-id="45ba2-113">サイト コレクションを削除すると、コレクション内のサイトの階層と、その中のすべてのコンテンツも削除されます。</span><span class="sxs-lookup"><span data-stu-id="45ba2-113">When you delete a site collection, you're also deleting the hierarchy of sites in the collection, and all content within them:</span></span>

- <span data-ttu-id="45ba2-114">ドキュメントおよびドキュメント ライブラリ</span><span class="sxs-lookup"><span data-stu-id="45ba2-114">Documents and document libraries</span></span>
- <span data-ttu-id="45ba2-115">リストとリスト データ</span><span class="sxs-lookup"><span data-stu-id="45ba2-115">Lists and list data</span></span>
- <span data-ttu-id="45ba2-116">サイト構成の設定</span><span class="sxs-lookup"><span data-stu-id="45ba2-116">Site configuration settings</span></span>
- <span data-ttu-id="45ba2-117">サイトまたはサブサイトに関連する役割とセキュリティ情報</span><span class="sxs-lookup"><span data-stu-id="45ba2-117">Role and security information that is related to the site or its subsites</span></span>
- <span data-ttu-id="45ba2-118">トップ レベルの Web サイトのサブサイト、そのコンテンツ、およびユーザー情報</span><span class="sxs-lookup"><span data-stu-id="45ba2-118">Subsites of the top-level website, their contents, and user information</span></span>

<span data-ttu-id="45ba2-119">サイト コレクションを誤って削除した場合は、SharePoint 管理センターを使用してグローバル管理者または SharePoint 管理者がサイト コレクションを復元できます。</span><span class="sxs-lookup"><span data-stu-id="45ba2-119">If you accidentally delete a site collection, it can be restored by a global or SharePoint admin using the SharePoint admin center.</span></span>

<span data-ttu-id="45ba2-120">削除されたサイト コレクションは 93 日間保持されます。</span><span class="sxs-lookup"><span data-stu-id="45ba2-120">Deleted site collections are retained for 93 days.</span></span> <span data-ttu-id="45ba2-121">93 日を過ぎると、リスト、ライブラリ、ページ、サブサイトなど、サイトおよびサイトのすべてのコンテンツと設定が完全に削除されます。</span><span class="sxs-lookup"><span data-stu-id="45ba2-121">After 93 days, sites and all their content and settings are permanently deleted, including lists, libraries, pages, and any subsites.</span></span>

<span data-ttu-id="45ba2-122">ハード削除は、ユーザーがサイト コレクションのごみ箱から削除済みアイテムを削除した場合、保持期間とバックアップ期間が経過した場合、または管理者が [Remove-SPODeletedSite](/powershell/module/sharepoint-online/remove-spodeletedsite)コマンドレットを使用してサイト コレクションを完全に削除した場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="45ba2-122">Hard deletion occurs when a user purges deleted items from the site collection Recycle Bin, when the retention and backup periods expire, or when an administrator permanently deletes a site collection using the [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/remove-spodeletedsite).</span></span> <span data-ttu-id="45ba2-123">ユーザーが SharePoint Online からコンテンツをハード削除 (完全に削除、または削除) すると、削除されたチャンクのすべての暗号化キーも削除されます。</span><span class="sxs-lookup"><span data-stu-id="45ba2-123">When a user hard deletes (permanently deletes, or purges) content from SharePoint Online, all encryption keys for the deleted chunks are also deleted.</span></span> <span data-ttu-id="45ba2-124">以前に削除されたチャンクを格納したディスク上のブロックは、未使用としてマークされ、再使用できます。</span><span class="sxs-lookup"><span data-stu-id="45ba2-124">The blocks on the disks that previously stored the deleted chunks are marked as unused and available for re-use.</span></span>
