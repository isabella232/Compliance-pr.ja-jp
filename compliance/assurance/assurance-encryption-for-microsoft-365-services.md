---
title: データ、Skype、OneDrive、SharePoint、およびExchange
description: '概要: Skype、OneDrive、SharePoint、Microsoft Teams、およびExchange Online。'
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- SPO_Content
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 480e7e03564075707c90e25ad5777631c1e68ed8
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482029"
---
# <a name="encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-microsoft-teams-and-exchange-online"></a>オンライン、Skype for Business、OneDrive for Business、SharePoint、およびMicrosoft Teamsの暗号化Exchange Online

Microsoft 365は、物理データ センター のセキュリティ、ネットワーク セキュリティ、アクセス セキュリティ、アプリケーション セキュリティ、データ セキュリティなど、複数の層で広範な保護を提供する高度にセキュリティの高い環境です。

## <a name="skype-for-business"></a>Skype for Business

Skype for Businessデータは、会議参加者によってアップロードされたファイルまたはプレゼンテーションの形式で保存される場合があります。 Web 会議サーバーは、256 ビット キーを使用して AES を使用して顧客データを暗号化します。 暗号化された顧客データはファイル共有に保存されます。 顧客データの各部分は、異なるランダムに生成された 256 ビット キーを使用して暗号化されます。 電話会議で顧客データの一部を共有すると、Web 会議サーバーは、HTTPS を介して暗号化された顧客データをダウンロードするように会議クライアントに指示します。 顧客データを復号化できるよう、対応するキーをクライアントに送信します。 また、Web 会議サーバーは、クライアントが電話会議の顧客データにアクセスできる前に、会議クライアントを認証します。 Web 会議に参加すると、各会議クライアントは、最初に TLS を使用してフロントエンド サーバー内で実行される会議フォーカス コンポーネントを使用して SIP ダイアログを確立します。 会議フォーカスは、Web 会議サーバーによって生成された認証 Cookie を会議クライアントに渡します。 その後、会議クライアントは、サーバーによって認証される認証 Cookie を提示する Web 会議サーバーに接続します。

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online と OneDrive for Business

SharePoint Online のすべての顧客ファイルは、常に 1 つのテナントに排他的な一意のファイルごとのキーによって保護されます。 キーは、SharePoint Online サービスによって作成および管理される場合、または顧客がカスタマー キーを使用、作成、管理するときに行います。 ファイルがアップロードされると、Azure ストレージに送信される前に、SharePoint Online によってアップロード要求のコンテキスト内で暗号化が実行されます。 ファイルがダウンロードされると、SharePoint Online は一意のドキュメント識別子に基づいて Azure ストレージから暗号化された顧客データを取得し、ユーザーに送信する前に顧客データを復号化します。 Azure ストレージには、顧客データを解読したり、識別したり理解したりする機能はありません。 すべての暗号化と暗号化解除は、テナントの分離を強制する同じシステムで行Azure Active DirectoryオンラインSharePointです。

Microsoft 365 では、SharePoint Online のすべてのファイルを格納する Microsoft Teams、SharePoint Online をストレージに使用する OneDrive for Business など、SharePoint Online にデータを格納する複数のワークロード。 SharePoint Online に保存されている顧客データはすべて暗号化され (1 つ以上の AES 256 ビット キーを使用)、次のようにデータセンター全体に分散されます。 (この暗号化プロセスのすべての手順は、FIPS 140-2 レベル 2 検証済みです。 FIPS 140-2 コンプライアンスの詳細については [、「FIPS 140-2 コンプライアンス」を参照](/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105))してください。

- 各ファイルは、ファイル サイズに応じて 1 つ以上のチャンクに分割されます。 各チャンクは、独自の一意の AES 256 ビット キーを使用して暗号化されます。
- ファイルが更新された場合、更新は同じ方法で処理されます。変更は 1 つ以上のチャンクに分割され、各チャンクは個別の一意のキーで暗号化されます。
- これらのチャンク (ファイル、ファイル、更新デルタ) は、複数の Azure ストレージ アカウントにランダムに分散された Blob として Azure ストレージに格納されます。
- これらの顧客データのチャンクの暗号化キーのセットは、それ自体が暗号化されています。

    - BLOB の暗号化に使用されるキーは、オンライン コンテンツ データベースSharePoint格納されます。
    - コンテンツ データベースは、保存時にデータベース アクセス制御と暗号化によって保護されます。 暗号化は、Transparent Data Encryption [](/sql/relational-databases/security/encryption/transparent-data-encryption-tde) (TDE) を使用[Azure SQL Database。](/azure/sql-database/sql-database-technical-overview) (Azure SQL Databaseは、リレーショナル データ、JSON、空間、XML などの構造をサポートする Microsoft Azure の汎用リレーショナル データベース サービスです。これらのシークレットは、テナント レベルではなく、SharePoint Online のサービス レベルです。 これらのシークレット (マスター キーとも呼ばれます) は、キー ストアと呼ばれる別のセキュリティで保護されたリポジトリに格納されます。 TDE は、アクティブ なデータベースとデータベースのバックアップとトランザクション ログの両方にセキュリティを提供します。
    - ユーザーがオプションのキーを指定すると、顧客キーは Azure Key Vault に格納され、サービスはキーを使用してテナント キーを暗号化し、サイト キーを暗号化するために使用され、ファイル レベルのキーを暗号化するために使用されます。 基本的に、顧客がキーを提供するときに新しいキー階層が導入されます。
- ファイルの再アセンブルに使用されるマップは、暗号化されたキーと共にコンテンツ データベースに格納され、暗号化解除に必要なマスター キーとは別に格納されます。
- 各 Azure ストレージ アカウントには、アクセスの種類 (読み取り、書き込み、列挙、削除) ごとに固有の資格情報があります。 各資格情報セットはセキュリティが確保されたキー ストアで保管され、定期的に更新されます。 前述のように、3 つの異なる種類のストアがあります。それぞれに個別の関数があります。
    - 顧客データは、Azure ストレージに暗号化された BLOB として格納されます。 顧客データの各チャンクのキーは暗号化され、コンテンツ データベースに個別に格納されます。 顧客データ自体は、復号化方法に関する手がかりを持っていません。
    - コンテンツ データベースは、SQL Serverデータベースです。 Azure ストレージに保持されている顧客データ BLOB の検索と再構成に必要なマップと、それらの BLOB の暗号化に必要なキーが保持されます。 ただし、キーのセット自体は (上記で説明したように) 暗号化され、別のキー ストアに保持されます。
    - キー ストアは、コンテンツ データベースと Azure ストレージとは物理的に分離されています。 各 Azure ストレージ コンテナーの資格情報と、コンテンツ データベースに保持されている暗号化されたキーのセットにマスター キーが保持されます。

Azure BLOB ストア、コンテンツ データベース、およびキー ストアの 3 つのストレージ コンポーネントは、それぞれ物理的に分離されています。 いずれかのコンポーネントに保管されている情報は、それ自体では使用できません。 3 つすべてのキーにアクセスできない場合は、チャンクのキーを取得したり、キーを解読して使用したり、対応するチャンクにキーを関連付ける、各チャンクを復号化したり、構成チャンクからドキュメントを再構築したりすることは不可能です。

データ センター内のコンピューター上の物理ディスク ボリュームを保護する BitLocker 証明書は、ファーム キーによって保護されるセキュリティで保護されたリポジトリ (SharePoint Online シークレット ストア) に格納されます。

BLOB ごとのキーを保護する TDE キーは、次の 2 つの場所に格納されます。

- BitLocker 証明書を保存し、ファーム キーによって保護されるセキュリティで保護されたリポジトリ。そして
- ユーザーが管理するセキュリティで保護されたリポジトリAzure SQL Database。

Azure ストレージ コンテナーにアクセスするために使用される資格情報は、SharePoint Online シークレット ストアにも保持され、必要に応じて各 SharePoint に委任されます。 これらの資格情報は Azure ストレージ SAS 署名であり、データの読み取りまたは書き込みに使用される別個の資格情報と、ポリシーが適用され、60 日ごとに自動有効期限が切れます。 異なる資格情報は、データの読み取りまたは書き込み (両方ではなく) に使用され、オンライン ファームSharePoint列挙するアクセス許可は付与されません。

> [!NOTE]
> 米国Office 365のお客様の場合、データ BLOB は Azure 米国政府機関にStorage。 さらに、米国SharePointの Office 365 キーへのアクセスは、特にOffice 365されたスタッフに制限されます。 Azure 米国政府機関の運用スタッフは、データ blob の暗号化に使用SharePointオンライン キー ストアにアクセスできません。

SharePoint Online および OneDrive for Business でのデータ暗号化の詳細については、「OneDrive for Business および SharePoint オンライン」を[参照してください](https://technet.microsoft.com/library/dn905447.aspx)。

### <a name="list-items-in-sharepoint-online"></a>オンラインでアイテムをSharePointする

リスト アイテムは、ユーザーが作成したリスト内の行、SharePoint Online ブログ内の個々の投稿、SharePoint Online Wiki ページ内のエントリなど、サイト内で動的に生活できる顧客データの小さなチャンクです。 リスト アイテムはコンテンツ データベース (Azure SQL Database) に格納され、TDE で保護されます。

## <a name="encryption-of-data-in-transit"></a>転送中データの暗号化

オンラインOneDrive for Businessおよび SharePointでは、データがデータセンターに入り、データセンターを終了する 2 つのシナリオがあります。

- **サーバーとのクライアント通信**- オンラインおよびインターネットSharePointサーバー OneDrive for Business通信は TLS 接続を使用します。
- **データセンター間のデータ移動** - データセンター間でデータを移動する主な理由は、障害復旧を有効にするために geo レプリケーションを行う場合です。 たとえば、トランザクション ログSQL Server BLOB ストレージデルタは、このパイプに沿って移動します。 このデータは既にプライベート ネットワークを使用して送信されていますが、クラス最高の暗号化によってさらに保護されます。

## <a name="exchange-online"></a>Exchange Online

Exchange Onlineすべてのメールボックス データに BitLocker を使用し、BitLocker 構成については[、「BitLocker for Encryption」で説明します](/microsoft-365/compliance/office-365-bitlocker-and-distributed-key-manager-for-encryption)。 サービス レベルの暗号化では、メールボックス レベルのすべてのメールボックス データが暗号化されます。 

サービス暗号化に加えて、Microsoft 365暗号化の上に構築された顧客キーもサポートしています。 顧客キーは、Microsoft のロードマップにも含Exchange Onlineサービスの暗号化に関する Microsoft が管理するキー オプションです。 この暗号化方法では、サーバー管理者とデータの暗号化解除に必要な暗号化キーが分離され、暗号化がデータに直接適用される (論理ディスク ボリュームで暗号化が適用される BitLocker とは対照的に) Exchange サーバーからコピーされた顧客データは暗号化されたままなので、BitLocker では保護されません。

サービスの暗号化Exchange Onlineスコープは、ユーザーデータ内に保存されている顧客Exchange Online。 (Skype for Businessは、ユーザーが生成したコンテンツのほぼすべてをユーザーの Exchange Online メールボックス内に格納するため、Exchange Online のサービス暗号化機能を継承します。


## <a name="microsoft-teams"></a>Microsoft Teams

Teams TLS と MTLS を使用してインスタント メッセージを暗号化します。 すべてのサーバー間トラフィックでは、トラフィックが内部ネットワークに限定されているのか、内部ネットワーク境界を越えた場合でも、MTLS が必要です。

次の表は、ユーザーが使用するプロトコルTeams。

|**トラフィックの種類**|**暗号化されたユーザー**|
|:-----|:-----|
|サーバー間|MTLS|
|クライアント間サーバー (例: インスタント メッセージングとプレゼンス)|TLS|
|メディア フロー (例: メディアのオーディオとビデオの共有)|TLS|
|メディアのオーディオとビデオの共有|SRTP/TLS|
|通知|TLS|

#### <a name="media-encryption"></a>メディアの暗号化

メディア トラフィックは、RTP トラフィックに機密性、認証、再生攻撃保護を提供する Real-Time トランスポート プロトコル (RTP) のプロファイルである Secure RTP (SRTP) を使用して暗号化されます。 SRTP は、セキュリティで保護された乱数ジェネレーターを使用して生成されたセッション キーを使用し、シグナリング TLS チャネルを使用して交換されます。 クライアント間のメディア トラフィックは、クライアント間接続シグナリングを介してネゴシエートされますが、クライアントからクライアントに直接送信する場合は SRTP を使用して暗号化されます。

Teamsは、TURN を使用してメディア リレーに安全にアクセスするために資格情報ベースのトークンを使用します。 メディア リレーは、TLS で保護されたチャネルを使用してトークンを交換します。

#### <a name="fips"></a>FIPS

Teamsは、暗号化キー交換に FIPS (連邦情報処理標準) 準拠のアルゴリズムを使用します。 FIPS の実装の詳細については、「Federal [Information Processing Standard (FIPS) Publication 140-2」を参照してください](/microsoft-365/compliance/offering-fips-140-2)。
