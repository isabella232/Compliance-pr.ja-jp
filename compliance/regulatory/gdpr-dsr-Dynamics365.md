---
title: GDPR および CCPA のための Dynamics 365 データ対象要求
description: このガイドは、個人データを検索して操作する方法、および Dynamics 365 のお客様による DSR および CCPA 要求への対応方法について説明します。
keywords: Microsoft 365、Microsoft 365 Education、Microsoft 365 ドキュメント、GDPR、CCPA
ms.localizationpriority: high
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
hideEdit: true
ms.custom:
- seo-marvel-mar2020
titleSuffix: Microsoft GDPR
ms.openlocfilehash: 7b6919cbdf2ece468eeec8931b652972a74b07dc
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947840"
---
# <a name="dynamics-365-data-subject-requests-for-the-gdpr-and-ccpa"></a>GDPR および CCPA のための Dynamics 365 データ対象要求

EU [一般データ保護規則 (GDPR)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) では、ユーザー (規則では *データ主体* と呼ばれる) に対して、雇用主やその他の会社または組織 (*データ管理者* または単に *管理者* と呼ばれる) が収集した個人データを管理する権利を与えます。GDPR では、個人データとは、識別された、または識別可能な自然人と関連するあらゆるデータとして広範に定義されています。GDPR は個人データに対する固有の権利をデータ主体に与えます。この権利には、個人データのコピーの取得、変更の要求、処理の制限、削除、または、別の管理者に移動できるようにするための電子形式での受信が含まれます。データ主体から管理者に個人データへの操作実行を求める正式な要求は、*データ主体の権利要求* または DSR と呼ばれます。

同様に、カリフォルニア州消費者プライバシー法 (CCPA) では、個人情報の削除、アクセスおよび受信 (移植性) など、GDPR のデータ主体の権利に類似している権利を含む、カリフォルニア州の消費者のプライバシーの権利および義務を規定します。  また、CCPA では、特定の開示、権利の行使を選択する際の差別に対する保護、"売上" として分類された特定のデータ転送の "オプトアウト/オプトイン" 要件を規定します。 「販売」は広く定義されており、有価約因に関するデータの共有を含みます。 CCPA の詳細については、「[カリフォルニア州消費者プライバシー法](offering-ccpa.md)」と「[カリフォルニア州消費者プライバシー法に関する FAQ](ccpa-faq.yml)」を参照してください。

このガイドでは、コントローラーが DSR 要求に応じて個人データを検索して操作できるように Microsoft 製品、サービス、管理ツールを使用する方法について説明します。特に、Microsoft クラウドにある個人データまたは個人情報の検索、アクセス、処理に関する方法を扱います。このガイドで説明するプロセスの概要は次のとおりです。

- **検出:** 検索/検出ツールを使用することで、DSR の対象となる可能性がある顧客データをより簡単に見つけられます。対応の対象となる可能性のあるドキュメントが収集されたら、以下のステップの DSR アクションを 1 つまたは複数実行して要求に対応できます。あるいは、DSR 対応に関する組織のガイドラインを要求が満たしていないと判断することも可能です。
- **アクセス:** Microsoft クラウドにある個人データを取り出し、要求がある場合は、データ主体が利用できるコピーを作成します。
- **修正:** 必要に応じて、個人データを変更したり、要求された他の操作を個人データに対して実行したりします。
- **制限:** さまざまなオンライン サービスに対するライセンスを削除するか、または可能な場合は目的のサービスをオフにすることで、個人データの処理を制限します。
- **削除:** Microsoft のクラウドに格納されていた個人データを完全に削除します。
- **エクスポート/受信 (移植性):** 個人データまたは個人情報の電子コピー (コンピューターで読み取り可能な形式) をデータ主体に提供します。 CCPA における個人情報とは、識別された人、または識別可能な人に関するあらゆる情報のことです。 個人の私的、公的、または職業上の役割による区別はありません。 "個人情報" と定義された用語は、GDPR における "個人データ" とほぼ同義語です。 ただし、CCPA では家族データおよび世帯データも含まれます。 CCPA の詳細については、「[カリフォルニア州消費者プライバシー法](offering-ccpa.md)」と「[カリフォルニア州消費者プライバシー法に関する FAQ](ccpa-faq.yml)」を参照してください。

このガイドの各セクションでは、Microsoft のクラウドにある個人データについて DSR 要求がなされた場合に、その対応としてデータ コントローラー組織が実行できる技術的な手順の概要を示します。

## <a name="gdpr-terminology"></a>GDPR 用語

このガイドに関連する用語を以下の表に定義します。

- **管理者:** 単独または他者と共同で、個人データの処理に関する目的と手段を決定する自然人や法人、公的機関、団体、その他の組織。そのような処理の目的と手段が EU 法もしくは加盟国の法律によって決定される場合、コントローラーまたはその指名に関する具体的な基準が EU 法または加盟国の法律によって提供される場合があります。
- **個人データおよびデータ主体:** 特定されたまたは特定可能な自然人 ('データ主体') に関するあらゆる情報。特定可能な自然人とは、その者の名前、ID 番号、位置データ、オンライン ID、または当該自然人に固有の 1 つ以上の特に身体的、生理学的、遺伝的、心理的、経済的、文化的、社会的な識別情報などの要素を参照することにより、直接または間接的に特定することができる者のことです。
- **処理者:** 管理者に代わって個人データを処理する自然人または法人、公的機関、団体、その他の組織。
- **顧客データ**: お客様または代理者がエンタープライズ サービスの使用を通じて Microsoft に提供する、すべてのテキスト、サウンド、ビデオ、イメージ ファイルを含むすべてのデータを意味します。顧客データには次の両方が含まれます: (1) エンド ユーザーを特定可能な個人情報 (たとえば Azure Active Directory でのユーザー名と連絡先情報)、特定のサービスでお客様がアップロードまたは作成したカスタマー コンテンツ (たとえば Azure Storage アカウント内のカスタマー コンテンツ、Azure SQL Database のカスタマー コンテンツ、Azure Virtual Machines でのお客様の仮想マシン イメージ)。
- **システム生成ログ:** Microsoft がエンタープライズ サービスをユーザーに提供するうえで役立つ、Microsoft により生成されるログおよび関連データ。システム生成ログには主に固有 ID などの仮名化データが含まれています。固有 ID とは通常、それ自体は特定の個人を識別しないものの、エンタープライズ サービスをユーザーに提供するために使われるシステム生成番号のことです。また、ユーザー名などのエンド ユーザーの個人を特定できる情報がシステム生成ログに含まれることもあります。

## <a name="how-this-guide-can-help-you-meet-your-controller-responsibilities"></a>管理者としての責任を果たすためのこのガイドの活用方法

このガイドは、2 つの部分に分かれており、GDPR で定められた権利を行使するデータ主体による要求に応じて、ユーザーが Microsoft クラウドのデータを検索して操作できるように Dynamics 365 製品、サービス、管理ツールを使用する方法について説明します。パート 1 では、顧客データに含まれる個人データを取り上げます。その後、パート 2 で、システム生成ログによってキャプチャされるその他の仮名化された個人データについて取り上げます。

- **パート 1: 顧客データに含まれる個人データに関するデータ主体の権利 (DSR) 要求に対応する:** このガイドのパート 1 では、Dynamics 365 アプリケーション (サービスとしてのソフトウェア) から、ユーザーがオンライン サービスに提供した顧客データの一部として処理される個人情報にアクセス、修正、制限、削除、エクスポートの処理を実行する方法を説明します。
- **パート 2: 仮名化データに関するデータ対象の権利要求に対応する。** Dynamics 365 エンタープライズ サービスを使用すると、サービスを提供する目的で Microsoft によりある種の情報が生成されます (このドキュメントでは *システム生成ログ* と呼びます)。これは、システム内でのアクションを特定する目的でエンド ユーザーによって残された利用履歴に限られます。この種のデータは、そのほかの情報を使用しない限り、特定のデータ対象に関連付けることはできませんが、GDPR では個人情報として定められている場合があります。このガイドのパート 2 では、Dynamics 365 によって生成されるシステム生成ログのアクセス、削除、エクスポート方法について説明します。

## <a name="preparing-for-data-subject-rights-investigations"></a>データ主体権限の調査の準備

データ主体が当人の権限を行使して要求を行う場合は、次の点を考慮してください。

- 要求の一部としてデータ対象から提供された情報を基に、その人物と役割 (従業員、顧客、仕入先など) を正確に特定します。この種の情報には、名前、従業員 ID、顧客番号、その他の ID などが考えられます。
- 要求のデータと日時を記録します (要求の完了期限は 30 日です)。
- その要求が、データ対象からの要求が承諾または拒否に関する組織の要件を満たしているかどうかを確認します。たとえば、その要求を実行することにより、組織のその他の法律上、財務上、規制上の義務に抵触しないか、および、他者の権利や自由を侵害しないかを確認する必要があります。
- 要求に関連する情報があることを確認します。

## <a name="part-1-responding-to-data-subject-rights-requests-for-personal-data-included-in-customer-data"></a>第 1 部: 顧客データに含まれる個人データに関するデータ主体権限要求に対する対応

次の記事では、Dynamics 365 で処理される顧客データに含まれる個人データに関する DSR 要求に備えて対応するのに役立つ情報を紹介します。重要な点として、個人データは、オンライン サービス サブスクリプションの一連のサービスに際して Microsoft によって処理される別のカテゴリのデータ (管理者データや 「Microsoft プライバシー ステートメント」 で定義されているサポート データなど) に含まれている場合があります。このドキュメントでは、ユーザーが Dynamics 365 に提供した顧客データ内に存在する個人データに影響を与える DSR 要求の検出と管理処理に絞って説明します。

Dynamics 365 は、サービスとしてのソフトウェア (SaaS) として複数のデータ処理機能を提供するオンライン サービスです。このため、Dynamics 365 には、性質や目的などの特性が異なる、売上データ、トランザクション、財務、人事情報などの多様なデータの処理を目的としたさまざまな機能が用意されています。これらの多様性を考慮して、Dynamics 365 では、顧客データを処理するのに必要となる複数のフォーム、フィールド、スキーマ、エンド ポイント、ロジックを提供しています。各アプリケーションで DSR 要求を処理できる複数の方法にも、この多様性が反映されています。Dynamics 365 アプリケーションで、特定の DSR 要求を処理する方法が複数用意されている場合、各アプリケーションによって提供されている技術的な説明の参照先がこのガイドに記載されています。

### <a name="dynamics-365"></a>Dynamics 365

#### <a name="finding-customer-data"></a>顧客データの検索

データ主体の権利要求に対する対応の最初の段階として、要求の対象となっている顧客データを検索して特定します。

顧客データの適切な分類は、Dynamics 365 Customer Engagement ビジネス アプリケーションの個人データを処理する際の基盤になります。Dynamics 365 for Customer Engagement では、データ分類を基にしたアプリケーションの拡張機能を柔軟に構築できます。適切な情報分類により、情報を個人データとして特定でき、データ主体の要求に対応する際にその情報を検索して取得することが可能になります。適切な情報分類は、個人データの収集と管理に関する法律や規制の要件を遵守する上でも役立ちます。

Microsoft は、データ主体の権利要求への対応とそれに伴う顧客データへのアクセスに関して、ユーザーを支援する機能を提供します。ただし、個人データが適切に保存および分類されるようにするのは、お客様の責任です。

***Dynamics 365 for Customer Engagement*** には、高度な検索、レコード検索など、レコード内の個人データをユーザーが検索するための機能が複数用意されています。いずれの機能でも、個人データを特定または検索できます。

- [[高度な検索]](/dynamics365/customer-engagement/basics/save-advanced-find-search)
- [[レコード検索]](/dynamics365/customer-engagement/basics/search-records) は、複数のレコードの種類に対して検索を実行できます。

Dynamics 365 for Marketing には、次の追加機能が用意されています。

1. [[Power BI レポートの作成]](/power-bi/service-connect-to-microsoft-dynamics-crm) は、顧客データをフィルター処理し特定する機能です。
2. 顧客データを含む可能性のあるその他のデータ ポイントを特定するには、マーケティング実行の取引先担当者や対象についてインサイト ビューを使用します。

***Dynamics 365 Customer Service Insights*** では、[顧客データを検索する](/dynamics365/ai/customer-service-insights/gdpr-discovery)ために役立つリソースの一覧を提供しており、お客様が顧客からの GDPR 要求に対応するのに役立てていただけます。

***Dynamics 365 for Finance and Operations*** には、顧客データを検索するための方法が複数用意されています。顧客データを検索するには、テナント管理者として次の操作を実行します。

- 個人データをすばやく検出する目的にかなう方法で顧客データを整理します。この目的に関しては、「[データ インベントリの分類方法](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#detailed-inventory)」をご覧ください。
- 個人データを検索および収集するには、[[個人検索レポート]](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#the-person-search-report) を使用します。
- [[個人検索レポートの拡張]](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-extend-person-search-report) では、エンティティを新規に作成するか既存のエンティティを拡張することにより、個人検索レポートを拡張します。
- 検索機能とフィルター処理機能を使用して、特定の個人データを検索し、Microsoft Office エクスポート機能を使用してそのデータをエクスポートしたり、ブラウザーの拡張機能を使用して .pdf ファイルにその情報を書き込んだりできます。
- 個人データを検索してエクスポートするユーザー設定のフォームを作成します。
- 認証済み顧客が当人の個人データを確認できる外部ポータルまたは Web サイトを作成します。

***Dynamics 365 Business Central*** は、顧客データを検索するためのいくつかの方法を提供します。詳細については、「[データの検索、フィルター処理、および並べ替え](/dynamics365/business-central/ui-enter-criteria-filters)」を参照してください。

***Dynamics 365 for Talent*** には、特定の個人データを検索するための高度な検索機能とフィルター処理機能に加えて、ブラウザーの拡張機能を使用して .pdf ファイルにその情報をエクスポートまたは書き込むための Microsoft Office エクスポート機能が用意されています。

- 顧客データを検索および収集するには、[[個人検索レポート]](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#the-person-search-report) を使用します。
- 新しいエンティティを作成するか、既存のエンティティを拡張することにより、[個人検索レポートを拡張します](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-extend-person-search-report)。

### <a name="providing-a-copy-of-customer-data"></a>顧客データのコピーの提供

***Dynamics 365 for Customer Engagement*** の顧客データは、包括的なエンティティ エクスポート機能を使用してエクスポートできます。顧客データを静的な Excel ファイルにエクスポートして、データの移植性要求を容易にできます。また、Excel を使用すると、個人データが移植性要求に含まれるように編集することができ、.csv や .xml などの、コンピューターで読み取り可能な一般的に使用されるファイル形式で保存できます。Dynamics 365 for Customer Engagement レコードは、[Common Data Service Web API](/powerapps/developer/common-data-service/webapi/overview) を介してエクスポートすることもできます。

さらに、Dynamics 365 for Marketing には[専用 API](/dynamics365/customer-engagement/marketing/developer/retrieve-interactions-contact) が用意されており、キャプチャされた顧客とのやり取りに関するその他のレコード (個人データを含む可能性がある) を取得する拡張機能を顧客が構築できます。この API は、関連するすべての情報をバックエンド システムから読み込み、その情報を単一のポータブル ドキュメントに組み立てます。

***Dynamics 365 Customer Service Insights*** では、データ エクスポートを使用して、[顧客データのコピーを提供](/dynamics365/ai/customer-service-insights/gdpr-export)することができます。

***Dynamics 365 for Finance and Operations** _ 内の顧客データは、包括的なエンティティ エクスポート機能を使用してエクスポートできます。テナントの管理者は、[_データ管理と統合エンティティ*](/dynamics365/unified-operations/dev-itpro/data-entities/data-management-integration-data-entity)を使用し、個人データを Excel や他の多くの一般的な形式に [*データ インポート/エクスポート ジョブ*](/dynamics365/unified-operations/dev-itpro/data-entities/data-import-export-job)を使用して繰り返しエクスポートするため、提供されているエンティティを使用するか、新しいエンティティを作成したり、既存のエンティティを拡張したりできます。または、多くのリストを静的な Excel ファイルにエクスポートして、データの移植性要求を容易にできます。顧客データを Excel にエクスポートすると、個人データが移植性要求に含まれるように編集することができ、.csv や .xml などの、コンピューターで読み取り可能な一般的に使用されるファイル形式でそのファイルを保存できます。*個人検索レポート* を使用して、個人データとして分類したデータをデータ対象に提供することも検討できます。

***Dynamics 365 Business Central*** では、次の 2 つの機能を使用して、データ主体に顧客データのコピーを提供できます。

顧客データを Excel ファイルにエクスポートできます。その後に、Excel で顧客データ移植性の要求に含まれるように編集し、.csv や .xml などの、コンピューターで読み取り可能な一般的に使用されるファイル形式でそのファイルを保存できます。詳細については、「[ビジネス データを Excel にエクスポートする](/dynamics365/business-central/about-export-data)」をご覧ください。

***Dynamics 365 for Talent*** では、[[個人検索レポートの拡張]](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-extend-person-search-report) を使用して、データ対象の個人データのコピーに関する要求をサポートするのに必要な情報を収集できます。

### <a name="rectifying-customer-data"></a>顧客データの修正

***Dynamics 365 for Customer Engagement*** は、不正確または不完全な顧客データを修正したり、顧客データを消去したりするための次の方法を提供します。

- 「顧客データの検索」で説明した機能を使用して顧客データを検索し、Customer Engagement フォーム内で直接データを編集します。1 行ごとの編集もできますが、複数の行を直接変更することもできます。
- 複数の Customer Engagement レコードを一括編集する場合、Microsoft Office アドインを使用して、データを Microsoft Excel にエクスポートし、変更を加え、変更されたデータを Excel から Dynamics 365 for Customer Engagement にインポートできます。

さらに、Dynamics 365 for Marketing では次の機能も実行できます。

- 1 行または複数の行を直接編集することにより、マイ データのランディング ページを更新します。
- 含めることが可能な、できるだけ多くの編集可能な連絡先フィールドが設定された[サブスクリプション センター](/dynamics365/customer-engagement/marketing/set-up-subscription-center) ページを準備します。これにより、エンドユーザーは、自分の情報を最大限に更新できます。

***Dynamics 365 Customer Service Insights*** では、組織が [顧客データを修正または変更する](/dynamics365/ai/customer-service-insights/gdpr-summary)機能も用意されています。

***Dynamics 365 for Finance and Operations** _ では、[_カスタマイズ ツール*](/dynamics365/unified-operations/dev-itpro/dev-tools/developer-home-page) も使用できますが、決定と実装はお客様の責任です。

***Dynamics 365 Business Central*** では、不正確または不完全な顧客データを修正する方法が 2 つ用意されています。

Business Central の複数のレコードをすばやく一括編集する場合、[Business Central Excel アドイン](/dynamics365/business-central/finance-analyze-excel#the--excel-add-in)を使用して Excel にリストをエクスポートし、複数のレコードを修正してから、修正したデータを Excel から Business Central に発行することができます。詳細については、「[ビジネス データを Excel にエクスポートする](/dynamics365/business-central/about-export-data)」をご覧ください。

対象となる個人データを含むデータ要素を手動で編集することにより、顧客カードにある顧客情報など、任意のフィールドに格納された顧客データを変更できます。詳細については、「[データの入力](/dynamics365/business-central/ui-enter-data)」をご覧ください。

#### <a name="brief-note-about-modifying-entries-in-business-transactions"></a>ビジネス トランザクションでのエントリの変更について

全般エントリ、顧客エントリ、税元帳エントリなどのトランザクション レコードは、エンタープライズ リソース プランニング システムの整合性に不可欠です。財務その他のトランザクションの一部をなす個人データは、財務法の遵守 (税法など)、不正行為防止 (セキュリティ監査証跡)、業界の認定資格の遵守を目的として、その状態のままで保持されます。このため、Dynamics 365 for Finance and Operations および Dynamics 365 Business Central では、このようなレコードのデータ変更を制限しています。

ビジネス トランザクション レコードに個人データを保存している場合、データ対象の要求を承諾して個人データの修正、削除、処理の制限などを実行するには、Dynamics 365 Business Central の[カスタマイズ機能](/dynamics365/business-central/dev-itpro/index)を使用する以外に方法はありません。[修正データ対象の要求を承諾するかどうかの決定](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#reasons-why-certain-personal-data-may-not-be-modified-or-deleted)とその実装については、お客様の責任において行われるものとします。

### <a name="restricting-the-processing-of-customer-data"></a>顧客データの処理の制限

データ主体から、顧客データの処理を制限する要求を受けた場合、影響を受ける顧客データをオンライン サービスから簡単に抽出し、クラウド アプリケーションによって提供される処理機能から完全に分離されている別個のコンテナー (オンプレミスのストレージ、またはデータ分離機能を備えた独立した Web サービス) に保存できます。

データ処理のブロックなど、代替メカニズムが ***Dynamics 365 Business Central*** によって提供されており、ユーザーはデータ主体の特定のレコードをブロックできます。詳細については、「[データ主体のデータ処理を制限する](/dynamics365/business-central/admin-responding-to-requests-about-personal-data#restrict-data-processing-for-a-data-subject)」をご覧ください。レコードがブロック済みとしてマークされている場合、Dynamics 365 Business Central はそのデータ主体の顧客データの処理を中断します。ブロックされたレコードを使用するトランザクションを新たに作成することはできません。たとえば、顧客か店員がブロックされている場合、その顧客に新しい請求書を作成することはできません。

### <a name="deleting-customer-data"></a>顧客データの削除

データ主体から当人の顧客データを削除するように要求された場合は、次のような方法で対処できます。

- 複数の Dynamics 365 レコードを一括編集する場合、Microsoft Office アドインを使用して、データを Microsoft Excel にエクスポートし、変更を加え、変更されたデータを Excel からそのオンライン サービスにインポートし直すことができます。
- 削除するデータを特定し、対象の顧客データを含むデータ要素を手動で削除することにより、任意のフィールドに格納されている顧客データを削除できます。たとえば、データ主体を表す連絡先レコードや個人データを含む他のレコードを物理的に削除できます。

また、Dynamics 365 Marketing の場合、連絡先を削除すると、個人情報を含むアウトバウンド マーケティングの対話データも同様に削除されます。 カスタム フィールドやエンティティについては、ユーザーがシステムをカスタマイズして、関連するレコードからすべての顧客データが削除され、連絡先レコードとのリンクが解除されて、個人情報がすべて削除されるようにする必要があります。 リアルタイム マーケティング モジュールを使用しているお客様は、リアルタイムの対話データがすべて削除されるように、削除を求めるサポート チケットも提出する必要があります。 詳細については、「[開発者ガイド (マーケティング)](/dynamics365/customer-engagement/marketing/developer/marketing-developer-guide)」を参照してください。

***Dynamics 365 Customer Service Insights*** では、組織に対して [顧客データを削除する](/dynamics365/ai/customer-service-insights/gdpr-delete)機能も提供しています。

***Dynamics 365 for Finance and Operations** _ では、[_カスタマイズ ツール*](/dynamics365/unified-operations/dev-itpro/dev-tools/developer-home-page) を使用して顧客データを削除または変更できます。

***Dynamics 365 Business Central*** では、データ主体から顧客データに含まれている当人の個人データを削除するように要求された場合、この要求に対応するには、次のようないくつかの方法があります。

- Business Central の複数のレコードをすばやく一括編集する場合、[Business Central Excel アドイン](/dynamics365/business-central/finance-analyze-excel#the--excel-add-in)を使用して Excel にデータをエクスポートし、複数のレコードを削除してから、その変更を Excel から Business Central に発行し直すことができます。詳細については、「[ビジネス データを Excel にエクスポートする](/dynamics365/business-central/about-export-data)」をご覧ください。
- 対象の顧客データを含むデータ要素を手動で削除することにより、任意のフィールドに保存されている顧客データを削除できます。詳細については、「[データの入力](/dynamics365/business-central/ui-enter-data)」をご覧ください。
- 連絡先を削除し、Delete Canceled Interaction Log Entries バッチ ジョブを実行して、その連絡先に関するやり取りを削除するなどの方法で、顧客データを直接削除できます。
- メモ、転記済売上、仕入請求書などの顧客データを含む[ドキュメントを削除](/dynamics365/business-central/admin-manage-documents)できます。

個別レコードの一括削除または個別削除のほかに、***Dynamics 365 for Talent*** から完全に削除できるのは契約関係が終了した従業員のみであることにご注意ください。[契約関係が終了した従業員の削除についてはこの手順に従います](/dynamics365/unified-operations/dev-itpro/gdpr/respond-dsr-request-talent#additional-notes-that-apply-to-requests-for-personal-data)。

### <a name="exporting-customer-data"></a>顧客データのエクスポート

データ移植性の要求に対応するため、***Dynamics 365 for Customer Engagement*** の顧客データは、包括的なエンティティ エクスポート機能を使用してエクスポートできます。顧客データを静的な Excel ファイルにエクスポートできるのでデータ移植性の要求に簡単に対応できます。また、Excel を使用すると、個人データが移植性要求に含まれるように編集することができ、.csv や .xml などの、コンピューターで読み取り可能な一般的に使用されるファイル形式で保存できます。

さらに、Dynamics 365 for Marketing には[専用 API](/dynamics365/customer-engagement/marketing/developer/retrieve-interactions-contact) が用意されており、キャプチャされた顧客とのやり取りに関するその他のレコード (個人データを含む可能性がある) を取得する拡張機能を顧客が構築できます。この API は、関連するすべての情報をバックエンド システムから読み込み、その情報を単一のポータブル ドキュメントに組み立てます。

***Dynamics 365 Customer Service Insights*** では、Azure の管理ポータルを使用して [顧客データをエクスポート](/dynamics365/ai/customer-service-insights/gdpr-export)します。

***Dynamics 365 for Finance and Operations*** には、［データ管理と統合エンティティが用意されています。これは、提供されているエンティティ、新しく作成されたエンティティ、拡張されたエンティティで、個人データを Excel や他の多くの一般的な形式に [データ インポート/エクスポート ジョブ](/dynamics365/unified-operations/dev-itpro/data-entities/data-import-export-job)を使用して繰り返しエクスポートできるようにするものです。または、多くのリストを静的な Excel ファイルにエクスポートして、データの移植性要求を容易にできます。このようにして顧客データを Excel にエクスポートすると、個人データが移植性要求に含まれるように編集することができ、.csv や .xml などの、コンピューターで読み取り可能な一般的に使用されるファイル形式でそのファイルを保存できます。

Dynamics 365 for Finance and Operations と ***Dynamics 365 for Talent*** のどちらでも、ユーザーが個人データとして分類したデータをデータ対象に提供する個人検索レポートが用意されています。

***Dynamics 365 Business Central*** には、次の機能が用意されています。

- 顧客データを Excel ファイルにエクスポートできます。その後に、Excel で顧客データが移植性要求に含まれるように編集し、.csv や .xml などの、コンピューターで読み取り可能な一般的に使用されるファイル形式でそのファイルを保存できます。詳細については、「[ビジネス データを Excel にエクスポートする](/dynamics365/business-central/about-export-data)」をご覧ください。
- 顧客データを Excel ファイルにエクスポートできます。その後に、Excel で顧客データが移植性要求に含まれるように編集し、.csv や .xml などの、コンピューターで読み取り可能な一般的に使用されるファイル形式でそのファイルを保存できます。詳細については、「[ビジネス データを Excel にエクスポートする](/dynamics365/business-central/about-export-data)」をご覧ください。


## <a name="part-2-responding-to-dsrs-for-system-generated-logs"></a>第 2 部: システム生成ログに関する DSR に対する対応

Microsoft は、GDPR における「個人データ」の広範な定義の下で個人のものと見なされるシステム生成ログに対して、アクセス、エクスポート、および削除するための機能も提供しています。次に、GDPR の下で個人のものと見なされるシステム生成のログの例を示します。

- 製品およびサービスの利用状況データ (ユーザー アクティビティ ログなど)
- ユーザー検索要求およびクエリ データ
- ユーザーまたはその他のシステムによるシステム機能および相互作用の結果として製品およびサービスによって生成されたデータ

システム生成ログのデータを制限または修正する機能はサポートされていません。システム生成ログのデータは、Microsoft のクラウド内で実行された実際のアクションと診断データであると見なされ、そのようなデータの変更はアクションの履歴記録が損なわれ詐欺やセキュリティのリスクが高まります。

### <a name="accessing-and-exporting-system-generated-logs"></a>システム生成ログのアクセスとエクスポート

管理者は、特定のユーザーの Dynamics 365 サービスおよびアプリケーションの使用に関連付けられたシステム生成ログにアクセスできます。システム生成ログにアクセスしてエクスポートするには、次の操作を実行します。

1. [Microsoft Service Trust Portal](https://servicetrust.microsoft.com/) に移動し、Dynamics 365 全体管理者の資格情報を使用してサインインします。
2. ページ上部にある **[プライバシー]** ドロップダウン リストから、**[データ対象要求]** をクリックします。
3. [**データ主体要求**] ページの [**システム生成ログ**] から、[**データ ログのエクスポート**] をクリックします。
    > [!NOTE]
    > **[データ ログのエクスポート]** が表示されます。所属する組織によって送信されたエクスポート データ要求の一覧が表示されます。
4. あるユーザーに関して新しい要求を作成するには、**[エクスポート データ要求を作成する]** をクリックします。

新しい要求を作成すると、その要求は現在の状態を追跡できる **[データ ログのエクスポート]** ページの一覧に表示されます。要求が完了すると、リンクをクリックしてシステム生成ログにアクセスできるようになります。このログは、要求の作成から 30 日以内に、組織で指定した Azure Storage の場所にエクスポートされます。データは、JSON や XML などの、コンピューターで読み取り可能な一般的なファイル形式で保存されます。Azure アカウントや Azure Storage の場所がない場合、Data Log Export ツールでシステム生成ログをエクスポートできるように、組織の Azure アカウントや Azure Storage の場所を作成する必要があります。

Azure では、ユーザーの組織がネイティブ JSON 形式のデータを指定の Azure Storage コンテナーにエクスポートできるようにすることで、この要求をサポートしています。詳細については、「[Microsoft Azure Storage コンテナーの概要 – BLOB ストレージ](/azure/storage/common/storage-introduction#blob-storage)」の記事をご覧ください。 取得されるデータにはサービスのセキュリティおよび安定性を損なう可能性があるデータは含まれません。

> [!IMPORTANT]
> ユーザー データをテナントからエクスポートするには、テナント管理者である必要があります。

次の表に、システム生成ログのアクセスとエクスポートについての概要を示します。

| **質問** | **回答** |
|:----|:---|
|**Microsoft データ ログのエクスポート ツールが要求の処理を完了するのにはどのくらいの時間がかかりますか?**| これは、いくつかの要因によって異なる場合があります。ほとんどの場合、1 ～ 2 日で完了しますが、最長で 30 日間かかる場合があります。 |
|**出力はどんな形式ですか?**| 出力は、XML、CSV、または JSON など、コンピューターで読み取り可能な構造化されたファイルになります。 |
|**データ ログのエクスポート ツールはどのようなデータを返しますか?**| データ ログのエクスポート ツールは、Microsoft が保存しているシステム生成ログを返します。エクスポートされたデータは、各種の Microsoft サービス (Office 365、Azure、Dynamics など) 全体にわたります。 |
|***データ ログのエクスポート ツールには、誰がアクセスしてシステム生成ログに対するアクセス要求を送信できますか?**| Dynamics 365 の全体管理者は、GDPR ログ マネージャー ユーティリティにアクセスできます。 |
|**データは、どのようにしてユーザーに返されますか?**| データは、ユーザー組織 &#39;s の Azure ストレージの場所にエクスポートされます。このデータをユーザーに示す方法または返す方法を決定するのは、ユーザー組織の管理者の役割です。 |
|**システム生成ログ内のデータはどのように表示されますか?**| JSON 形式のシステム生成ログ レコードの例を次に示します。 <br><br> "DateTime": "2017-04-28T12:09:29-07:00"、 <br> "AppName": "SharePoint"、 <br> "Action": "OpenFile"、 <br> "IP": "154.192.13.131"、 <br> "DevicePlatform": "Windows 1.0.1607" |

### <a name="deleting-system-generated-logs"></a>システム生成ログの削除

アクセス要求を通して取得されたシステム生成ログを削除するには、そのユーザーをサービスから削除して、Azure Active Directory アカウントを完全に削除する必要があります。 ユーザーを完全に削除する方法については、Azure データ主体の要求のトピックの「[手順 5: 削除](gdpr-dsr-azure.md#step-5-delete)」セクションを参照してください。 ユーザー アカウントを完全に削除すると、元に戻すことはできませんのでご注意ください。 ユーザーのアカウントを完全に削除すると、ユーザーのデータは、ほぼすべての Dynamics 365 サービスのシステム生成ログから 30 日以内に削除されます。ただし、サービスのセキュリティや安定性を損なう可能性のあるデータは削除されません。

## <a name="learn-more"></a>詳細情報

- [Microsoft Trust Center](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
