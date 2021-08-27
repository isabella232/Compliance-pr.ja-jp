---
title: Microsoft 365 での分離とアクセス制御
description: '概要: アプリケーションのさまざまなアプリケーション内での分離とアクセス制御のMicrosoft 365。'
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
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 82378b72d8dc17441a1ab92fc7ac222d7b9d4036
ms.sourcegitcommit: 9766d656d0e270f478437bd39c0546ad2e4d846f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/27/2021
ms.locfileid: "58678626"
---
# <a name="isolation-and-access-control-in-microsoft-365"></a>分離とアクセス制御 (Microsoft 365

Azure Active Directory (Azure AD) および Microsoft 365 では、数十のサービス、数百のエンティティ、数千のリレーションシップ、数万の属性を含む非常に複雑なデータ モデルを使用します。 Azure ADディレクトリとサービス ディレクトリは、状態ベースのレプリケーション プロトコルを使用して同期されたテナントと受信者のコンテナーです。 Azure AD内に保持されているディレクトリ情報に加えて、各サービス ワークロードには独自のディレクトリ サービス インフラストラクチャがあります。
 
![Microsoft 365データ同期を使用します。](../media/office-365-isolation-tenant-data-sync.png)

このモデル内には、ディレクトリ データのソースは 1 つはありません。 特定のシステムは個々のデータを所有しますが、すべてのデータを保持する単一のシステムはありません。 Microsoft 365サービスは、このデータ モデルAD Azure と連携します。 Azure ADは、共有データの "真実のシステム" であり、通常、すべてのサービスで使用される小規模で静的なデータです。 このフェデレーション モデルは、Microsoft 365 Azure ADデータの共有ビューを提供します。

Microsoft 365ストレージと Azure クラウド ストレージの両方を使用します。 Exchange Online (Exchange Online Protection含む) Skype for Businessデータに独自のストレージを使用します。 SharePointオンラインでは、SQL ServerとAzure Storageの両方を使用するため、ストレージ レベルで顧客データを追加分離する必要があります。

## <a name="exchange-online"></a>Exchange Online

Exchange Online内に顧客データを格納します。 メールボックスは、メールボックス データベースと呼Storage拡張可能エンジン (ESE) データベース内でホストされます。 これには、ユーザー メールボックス、リンクされたメールボックス、共有メールボックス、パブリック フォルダー メールボックスが含まれます。 ユーザー メールボックスには、会話Skype for Businessなど、保存されたコンテンツが含まれます。

ユーザー メールボックスのコンテンツには、次の内容が含まれます。

- メールと電子メールの添付ファイル
- 予定表と空き時間情報
- 連絡先
- タスク
- Notes
- グループ
- 推論データ

サーバー内の各メールボックス データベースExchange Online複数のテナントからのメールボックスが含まれる場合があります。 承認コードは、テナント内を含む各メールボックスをセキュリティで保護します。 既定では、割り当てられたユーザーだけがメールボックスにアクセスできます。 メールボックスをセキュリティで保護するアクセス制御リスト (ACL) には、テナント レベルで Azure AD認証された ID が含まれる。 各テナントのメールボックスは、テナントの認証プロバイダーに対して認証された ID に制限されます。これには、そのテナントからのユーザーだけが含まれます。 テナント A のコンテンツは、テナント A によって明示的に承認されていない限り、テナント B のユーザーは取得できません。

## <a name="skype-for-business"></a>Skype for Business

Skype for Businessさまざまな場所にデータを格納します。

- 接続エンドポイント、テナント ID、ダイヤル プラン、ローミング設定、プレゼンス状態、連絡先リストなどを含むユーザーおよびアカウント情報は、Skype for Business Active Directory サーバー、およびさまざまな Skype for Business データベース サーバーに格納されます。 連絡先リストは、ユーザーが両方の製品に対して有効になっているExchange Online、ユーザーが有効になっていない場合は Skype for Business サーバーに保存されます。 Skype for Businessサーバーはテナントごとにパーティション分割されませんが、複数テナントによるデータの分離は、役割ベースのアクセス制御 (RBAC) によって適用されます。
- 会議のコンテンツとアップロードされたデータは、分散ファイル システム (DFS) 共有に保存されます。 このコンテンツは、有効な場合は、Exchange Onlineアーカイブできます。 DFS 共有はテナントごとにパーティション分割されません。 コンテンツは ACL で保護され、マルチテナントは RBAC を介して適用されます。
- 通話履歴、IM セッション、アプリケーション共有、IM 履歴などのアクティビティ履歴である通話詳細レコードも Exchange Online に格納できますが、ほとんどの通話詳細レコードは通話詳細レコード (CDR) サーバーに一時的に保存されます。 コンテンツはテナントごとにパーティション分割されませんが、マルチテナントは RBAC を介して適用されます。

## <a name="sharepoint-online"></a>SharePoint Online

SharePointOnline には、データ分離を提供する複数の独立したメカニズムがあります。 アプリケーション データベース内に抽象化されたコードとしてオブジェクトを格納します。 たとえば、ユーザーが SharePoint Online にファイルをアップロードすると、ファイルは逆アセンブルされ、アプリケーション コードに変換され、複数のデータベースの複数のテーブルに格納されます。

ユーザーがデータを含むストレージに直接アクセスできる場合、コンテンツは人間やオンライン以外のシステムSharePointできません。 これらのメカニズムには、セキュリティ アクセス制御とプロパティが含まれます。 すべての SharePointリソースは、テナンシー内を含め、承認コードと RBAC ポリシーによって保護されます。 リソースをセキュリティで保護するアクセス制御リスト (ACL) には、テナント レベルで認証された ID が含まれる。 SharePointテナントのオンライン データは、テナントの認証プロバイダーによって認証された ID に制限されます。

ACL に加えて、認証プロバイダー (テナント固有の Azure AD) を指定するテナント レベル のプロパティは 1 回書き込まれるので、一度設定すると変更できません。 テナントに対して認証プロバイダーテナント プロパティを設定すると、テナントに公開されている API を使用して変更することはできません。

テナントごとに *一意の SubscriptionId* が使用されます。 すべての顧客サイトはテナントによって所有され、テナントに固有の *SubscriptionId* が割り当てられます。 サイト *の SubscriptionId* プロパティは一度書き込まれるので、永続的です。 テナントに割り当てられたサイトを別のテナントに移動することはできません。 *SubscriptionId は*、認証プロバイダーのセキュリティ スコープを作成するために使用されるキーであり、テナントに関連付けされます。

SharePointオンラインでは、SQL ServerメタデータAzure Storageを使用します。 コンテンツ ストアのパーティション キーは、コンテンツ ストア *の SiteId* SQL。 クエリを実行SQL、SharePoint Online はテナント レベルの *SubscriptionId* チェックの一部として確認された *SiteId* を使用します。

SharePointオンラインでは、暗号化されたファイル コンテンツが blob にMicrosoft Azureされます。 各 SharePoint ファームには独自の Microsoft Azure アカウントが設定され、Azure に保存されている BLOB はすべて、SQL コンテンツ ストアに格納されたキーで個別に暗号化されます。 認証層によってコードで保護され、エンド ユーザーに直接公開されない暗号化キー。 SharePointオンラインには、HTTP 要求が複数のテナントのデータを読み取りまたは書き込むときに検出するリアルタイム監視があります。 要求 ID *SubscriptionId は* 、アクセスされたリソース *の SubscriptionId* に対して追跡されます。 複数のテナントのリソースにアクセスする要求は、エンド ユーザーが行う必要があります。 マルチテナント環境でのサービス要求だけが例外です。 たとえば、検索クローラーはデータベース全体のコンテンツ変更を一度にプルします。 これは通常、効率上の理由から行われる、1 つのサービス要求で複数のテナントのサイトにクエリを実行する必要があります。

## <a name="teams"></a>Teams

コンテンツ Teamsに応じて、データの格納方法が異なります。 

詳しい説明については、Microsoft Teamsアーキテクチャに関する[Ignite](https://channel9.msdn.com/Events/Ignite/Microsoft-Ignite-Orlando-2017/BRK3071)ブレークアウト セッションを参照してください。

### <a name="core-teams-customer-data"></a>顧客Teamsコア データ

テナントがオーストラリア、カナダ、EU、フランス、ドイツ、インド、日本、南アフリカ、韓国、スイス (リヒテンシュタインを含む)、アラブ首長国連邦、英国、または米国でプロビジョニングされている場合、Microsoft は次の顧客データをその場所でのみ保存します。

- Teams、チームとチャネルの会話、画像、ボイスメール メッセージ、連絡先を管理します。
- SharePoint Online サイトのコンテンツと、そのサイト内に格納されているファイル。
- 仕事または学校OneDriveにアップロードされたファイル。

#### <a name="chat-channel-messages-team-structure"></a>チャット、チャネル メッセージ、チーム構造

すべてのチームは、TeamsグループとそのMicrosoft 365サイトとSharePointメールボックスによってExchangeされます。 プライベート チャット (グループ チャットを含む)、チャネル内の会話の一部として送信されたメッセージ、チームとチャネルの構造は、Azure で実行されているチャット サービスに格納されます。 データは、情報保護機能を有効にするために、ユーザーおよびグループ メールボックス内の非表示のフォルダーにも格納されます。

#### <a name="voicemail-and-contacts"></a>ボイスメールと連絡先

ボイスメールは、ボイスメールにExchange。 連絡先は、Exchangeベースのクラウド データ ストアに格納されます。 ExchangeおよびExchangeベースのクラウド ストアは、既に世界中の各データセンター geo にデータ常駐を提供しています。 すべてのチームについて、ボイスメールと連絡先は、オーストラリア、カナダ、フランス、ドイツ、インド、日本、アラブ首長国連邦、英国、南アフリカ、韓国、スイス (リヒテンシュタインを含む)、および米国の国内に保存されます。 その他のすべての国では、ファイルはテナントアフィニティに基づいて米国、ヨーロッパ、Asia-Pacificに保存されます。

#### <a name="images-and-media"></a>画像とメディア

チャットで使用されるメディア (Giphy GIF は保存されていないが、元の Giphy サービス URL への参照リンクである場合を除き、Giphy は Microsoft 以外のサービス) は、チャット サービスと同じ場所に展開される Azure ベースのメディア サービスに格納されます。

#### <a name="files"></a>ファイル

チャネル内でOneNote共有するファイル (OneNote Wiki を含む) は、チームのサイトにSharePointされます。 会議または通話中にプライベート チャットまたはチャットで共有されたファイルは、ファイルを共有するユーザーのOneDrive にアップロードされ、OneDrive に保存されます。 Exchange、SharePoint、OneDriveは、世界中の各データセンター地域でデータ常駐を既に提供しています。 したがって、既存の顧客の場合、Teams エクスペリエンスの一部であるすべてのファイル、OneNote ノートブック、Teams Wiki コンテンツ、およびメールボックスは、テナントアフィニティに基づいて既に場所に保存されています。 ファイルは、オーストラリア、カナダ、フランス、ドイツ、インド、日本、アラブ首長国連邦、英国、南アフリカ、韓国、スイス (リヒテンシュタインを含む) の国内で保存されます。 他のすべての国では、ファイルはテナントアフィニティに基づいて米国、ヨーロッパ、またはアジア太平洋の場所に保存されます。
