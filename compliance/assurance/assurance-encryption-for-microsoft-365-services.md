---
title: Skype、OneDrive、SharePoint、Exchange の暗号化
description: '概要: Skype、OneDrive、SharePoint、Microsoft Teams、Exchange Online の暗号化の説明。'
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- SPO_Content
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 9317b112d1fa759b1f90e072203e7b8093a432fd
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120546"
---
# <a name="encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-microsoft-teams-and-exchange-online"></a>Skype for Business、OneDrive for Business、SharePoint Online、Microsoft Teams、Exchange Online の暗号化

Microsoft 365 は、物理データ センターのセキュリティ、ネットワーク セキュリティ、アクセス セキュリティ、アプリケーション セキュリティ、データ セキュリティなど、複数のレイヤーで広範な保護を提供する高度なセキュリティ環境です。

## <a name="skype-for-business"></a>Skype for Business

Skype for Business の顧客データは、会議の参加者によってアップロードされたファイルまたはプレゼンテーションの形式で保存される場合があります。 Web 会議サーバーは、AES を使用して 256 ビット キーを使用して顧客データを暗号化します。 暗号化された顧客データはファイル共有に保存されます。 顧客データの各部分は、異なるランダムに生成された 256 ビット キーを使用して暗号化されます。 電話会議で顧客データの一部が共有されている場合、Web 会議サーバーは、HTTPS を介して暗号化された顧客データをダウンロードするように会議クライアントに指示します。 顧客データを復号化できるよう、対応するキーをクライアントに送信します。 また、Web 会議サーバーは、クライアントが会議顧客データにアクセスする前に会議クライアントを認証します。 Web 会議に参加する場合、各会議クライアントは、最初に TLS を使用してフロントエンド サーバー内で実行される会議フォーカス コンポーネントを使用して SIP ダイアログを確立します。 会議フォーカスは、Web 会議サーバーによって生成された認証 Cookie を会議クライアントに渡します。 次に、会議クライアントは、サーバーによって認証される認証 Cookie を表示する Web 会議サーバーに接続します。

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online と OneDrive for Business

SharePoint Online のすべての顧客ファイルは、常に 1 つのテナントに排他的な一意のファイルごとのキーによって保護されます。 キーは、SharePoint Online サービスによって作成および管理されます。または、顧客が顧客キーを使用、作成、および管理する場合です。 ファイルがアップロードされると、Azure Storage に送信される前に、アップロード要求のコンテキスト内で SharePoint Online によって暗号化が実行されます。 ファイルがダウンロードされると、SharePoint Online は一意のドキュメント識別子に基づいて暗号化された顧客データを Azure Storage から取得し、ユーザーに送信する前に顧客データを復号化します。 Azure Storage には、顧客データを解読したり、識別または理解したりする機能はありません。 すべての暗号化と復号化は、テナントの分離を強制する同じシステム (Azure Active Directory と SharePoint Online) で行います。

Microsoft 365 のいくつかのワークロードでは、データを SharePoint Online に保存します。たとえば、すべてのファイルを SharePoint Online に格納する Microsoft Teams や、そのストレージに SharePoint Online を使用する OneDrive for Business があります。 SharePoint Online に保存されている顧客データはすべて暗号化され (1 つ以上の AES 256 ビット キーを使用)、データセンター全体に次のように分散されます。 (この暗号化プロセスのすべての手順は、FIPS 140-2 レベル 2 検証済みです。 FIPS 140-2 コンプライアンスの詳細については [、「FIPS 140-2 Compliance](/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105))」を参照してください)。

- 各ファイルは、ファイル サイズに応じて 1 つ以上のチャンクに分割されます。 各チャンクは、独自の一意の AES 256 ビット キーを使用して暗号化されます。
- ファイルが更新される場合、更新は同じ方法で処理されます。変更は 1 つ以上のチャンクに分割され、各チャンクは個別の一意キーで暗号化されます。
- これらのチャンク (ファイル、ファイルの一部、更新デルタ) は、複数の Azure ストレージ アカウントにランダムに分散された Blob として Azure ストレージに格納されます。
- これらの顧客データのチャンクに対する暗号化キーのセット自体は暗号化されます。

    - BLOB の暗号化に使用されるキーは、SharePoint Online コンテンツ データベースに格納されます。
    - コンテンツ データベースは、データベース アクセス制御と保存中の暗号化によって保護されます。 暗号化は、Azure [SQL](/sql/relational-databases/security/encryption/transparent-data-encryption-tde) Database で透過的なデータ暗号化 (TDE) [を使用して実行されます](/azure/sql-database/sql-database-technical-overview)。 (Azure SQL データベースは、リレーショナル データ、JSON、空間、XML などの構造をサポートする Microsoft Azure の汎用リレーショナル データベース サービスです。これらのシークレットは、テナント レベルではなく SharePoint Online のサービス レベルです。 これらのシークレット (マスター キーとも呼ばれます) は、キー ストアと呼ばれる別のセキュリティで保護されたリポジトリに格納されます。 TDE は、アクティブ データベースとデータベース バックアップとトランザクション ログの両方にセキュリティを提供します。
    - ユーザーがオプションキーを入力すると、顧客キーは Azure Key Vault に格納され、サービスはそのキーを使用してテナント キーを暗号化します。テナント キーはサイト キーの暗号化に使用され、このキーはファイル レベルキーの暗号化に使用されます。 基本的には、顧客がキーを提供するときに新しいキー階層が導入されます。
- ファイルの再アセンブルに使用されるマップは、暗号化されたキーと共に、暗号化されたキーと共に、暗号化解除に必要なマスター キーとは別にコンテンツ データベースに格納されます。
- 各 Azure ストレージ アカウントには、アクセスの種類 (読み取り、書き込み、列挙、削除) ごとに独自の資格情報があります。 各資格情報セットはセキュリティが確保されたキー ストアで保管され、定期的に更新されます。 上で説明したように、ストアには 3 種類のストアがあります。それぞれのストアには、それぞれ異なる機能があります。
    - 顧客データは、Azure ストレージに暗号化された BLOB として格納されます。 顧客データの各チャンクのキーは暗号化され、コンテンツ データベースに個別に格納されます。 顧客データ自体には、復号化方法に関する手がかりはありません。
    - コンテンツ データベースは、SQL Serverデータベースです。 Azure ストレージに保持されている顧客データ BLOB を見つけて再構成するために必要なマップと、それらの BLOB を暗号化するために必要なキーを保持します。 ただし、キーのセット自体は暗号化され (上で説明したように)、別のキー ストアに保持されます。
    - キー ストアは、コンテンツ データベースおよび Azure ストレージとは物理的に分離されています。 各 Azure ストレージ コンテナーの資格情報と、コンテンツ データベースに保持されている暗号化されたキーのセットに対するマスター キーを保持します。

これら 3 つのストレージ コンポーネント (Azure BLOB ストア、コンテンツ データベース、およびキー ストア) は、それぞれ物理的に独立しています。 いずれかのコンポーネントに保管されている情報は、それ自体では使用できません。 3 つのチャンクにアクセスしない場合、チャンクへのキーの取得、キーの暗号化解除によるキーの使用、対応するチャンクへのキーの関連付け、各チャンクの暗号化解除、構成チャンクからのドキュメントの再構築は不可能です。

BitLocker 証明書は、データセンター内のコンピューター上の物理ディスク ボリュームを保護し、ファーム キーで保護されたセキュリティで保護されたリポジトリ (SharePoint Online シークレット ストア) に格納されます。

BLOB ごとのキーを保護する TDE キーは、次の 2 つの場所に格納されます。

- セキュリティで保護されたリポジトリ。BitLocker 証明書が保管され、ファーム キーによって保護されます。そして
- Azure SQL Database によって管理されるセキュリティで保護されたリポジトリ。

Azure ストレージ コンテナーへのアクセスに使用される資格情報も SharePoint Online シークレット ストアに保持され、必要に応じて各 SharePoint Online ファームに委任されます。 これらの資格情報は Azure Storage SAS 署名であり、データの読み取りまたは書き込みに使用される個別の資格情報を使用し、ポリシーが適用され、60 日ごとに自動有効期限が切れます。 データの読み取りまたは書き込みには異なる資格情報が使用され (両方ではなく)、SharePoint Online ファームには列挙する権限が付与されません。

> [!NOTE]
> 米国Office 365 ユーザーの場合、データ BLOB は Azure U.S. Government Storage に格納されます。 さらに、Office 365 U.S. Government の SharePoint Online キーへのアクセスは、特にスクリーンスクリーンされた Office 365 人のスタッフに制限されています。 Azure U.S. Government の運用スタッフは、データ BLOB の暗号化に使用される SharePoint Online キー ストアにアクセスできません。

SharePoint Online と OneDrive for Business でのデータ暗号化の詳細については [、「OneDrive for Business](https://technet.microsoft.com/library/dn905447.aspx)および SharePoint Online でのデータ暗号化」を参照してください。

### <a name="list-items-in-sharepoint-online"></a>SharePoint Online のリスト アイテム

リスト アイテムは、アドホックで作成される、またはユーザーが作成したリスト内の行、SharePoint Online ブログ内の個々の投稿、SharePoint Online Wiki ページ内のエントリなど、サイト内でより動的に使用できる、より小さな顧客データのチャンクです。 リスト アイテムはコンテンツ データベース (Azure SQL Database) に格納され、TDE で保護されます。

## <a name="encryption-of-data-in-transit"></a>転送中データの暗号化

OneDrive for Business と SharePoint Online では、データがデータセンターに入り、データ センターから退出する 2 つのシナリオがあります。

- **サーバーとのクライアント通信** - インターネット上の SharePoint Online および OneDrive for Business への通信は TLS 接続を使用します。
- **データセンター間のデータ** 移動 - データセンター間でデータを移動する主な理由は、障害復旧を可能にするために geo レプリケーションを使用することです。 たとえば、トランザクション SQL Server BLOB ストレージデルタは、このパイプに沿って移動します。 このデータは既にプライベート ネットワークを使用して送信されているのに対し、クラス最高の暗号化によってさらに保護されます。

## <a name="exchange-online"></a>Exchange Online

Exchange Online は、すべてのメールボックス データに BitLocker を使用し、BitLocker 構成については、暗号化のための [BitLocker で説明されています](/microsoft-365/compliance/office-365-bitlocker-and-distributed-key-manager-for-encryption)。 サービス レベルの暗号化は、メールボックス レベルですべてのメールボックス データを暗号化します。 

Microsoft 365 は、サービスの暗号化に加えて、顧客キーをサポートします。顧客キーは、サービスの暗号化の上に構築されています。 顧客キーは、Microsoft のロードマップにも含まれています Exchange Online サービスの暗号化のための Microsoft が管理するキー オプションです。 この暗号化方法では、サーバー管理者とデータの暗号化解除に必要な暗号化キーが分離され、暗号化がデータに直接適用される (論理ディスク ボリュームで暗号化を適用する BitLocker とは対照的に) Exchange サーバーからコピーされた顧客データは暗号化されたままなので、BitLocker では保護が強化されません。

Exchange Online サービスの暗号化のスコープは、Exchange Online 内に保存されている顧客データです。 (Skype for Business は、ユーザーの Exchange Online メールボックス内にユーザーが生成したコンテンツのほぼすべてを保存するため、Exchange Online のサービス暗号化機能を継承します)。


## <a name="microsoft-teams"></a>Microsoft Teams

Teams では、インスタント メッセージの暗号化に TLS と MTLS を使用します。 すべてのサーバー間トラフィックでは、トラフィックが内部ネットワークに限定されているのか、内部ネットワーク境界を越えるのかにかかわらず、MTLS が必要です。

次の表に、Teams で使用されるプロトコルの概要を示します。

|**トラフィックの種類**|**暗号化**|
|:-----|:-----|
|サーバー間|MTLS|
|クライアントからサーバー (例: インスタント メッセージングとプレゼンス)|TLS|
|メディア フロー (例: メディアのオーディオとビデオの共有)|TLS|
|メディアのオーディオとビデオの共有|SRTP/TLS|
|通知|TLS|

#### <a name="media-encryption"></a>メディアの暗号化

メディア トラフィックは、RTP トラフィックに機密性、認証、リプレイ攻撃保護を提供する Real-Time トランスポート プロトコル (RTP) のプロファイルである Secure RTP (SRTP) を使用して暗号化されます。 SRTP は、セキュリティで保護された乱数ジェネレーターを使用して生成されたセッション キーを使用し、信号 TLS チャネルを使用して交換します。 クライアント間のメディア トラフィックは、クライアントとサーバー間の接続信号を介してネゴシエートされますが、クライアントからクライアントに直接送信する場合は SRTP を使用して暗号化されます。

Teams は、TURN を使用したメディア リレーへの安全なアクセスのために資格情報ベースのトークンを使用します。 メディア リレーは、TLS でセキュリティ保護されたチャネルを使用してトークンを交換します。

#### <a name="fips"></a>FIPS

Teams は、暗号化キー交換に FIPS (Federal Information Processing Standard) 準拠アルゴリズムを使用します。 FIPS の実装の詳細については [、Federal Information Processing Standard (FIPS) Publication 140-2 を参照してください](/microsoft-365/compliance/offering-fips-140-2)。
