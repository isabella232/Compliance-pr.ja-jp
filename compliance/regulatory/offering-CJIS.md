---
title: 刑事司法情報サービス (CJIS) セキュリティ ポリシー
description: Microsoft Government クラウド サービスは、米国刑事司法情報サービスセキュリティ ポリシーに準拠しています。
keywords: Microsoft 365、コンプライアンス、サービス
ms.localizationpriority: medium
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 313905ec68c7d730cd2372ebd4679943ff124993
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482732"
---
# <a name="criminal-justice-information-services-cjis-security-policy"></a>刑事司法情報サービス (CJIS) セキュリティ ポリシー

## <a name="cjis-overview"></a>CJIS の概要

米国連邦捜査局 (FBI) の刑事司法情報サービス (CJIS) 部門は、州、地方、および連邦の法執行機関および刑事司法機関に対して、指紋記録や犯罪歴など、刑事司法情報 (CJI) にアクセスできます。 米国の法執行機関および他の政府機関は、CJI の送信、ストレージ、または処理にクラウド サービスを使用する場合、CJI のセキュリティに関する最低限の要件と管理を確立する [CJIS](https://aka.ms/cjis-security-policy)セキュリティ ポリシーに準拠していることを確認する必要があります。

CJIS セキュリティ ポリシーは、国家標準技術研究所 (NIST) のガイダンスと共に、大統領および FBI 指令、連邦法、刑事司法コミュニティのアドバイザリー ポリシー ボードの決定を統合します。 ポリシーは、進化するセキュリティ要件を反映するように定期的に更新されます。

CJIS セキュリティ ポリシーは、クラウド サービス プロバイダーなどの民間請負業者が、クラウド サービスの使用が CJIS 要件と一致できるかどうかを判断するために評価する必要がある 13 の領域を定義します。 これらの領域は NIST 800-53 と密接に対応しています。これは、Microsoft が政府機関向けクラウド製品の認定を受けた連邦リスクおよび承認管理プログラム [(FedRAMP)](offering-FedRAMP.md)の基礎にもなっています。

さらに、CJI を処理するすべての民間請負業者は、セキュリティ ポリシーで必要な CJI のセキュリティと機密性の確保に役立つ米国司法長官によって承認された統一契約である CJIS Security Addendum に署名する必要があります。 また、請負業者は、連邦および州の法律、規制、および標準に準拠したセキュリティ プログラムを維持し、CJI の使用を政府機関が提供した目的に限定します。

## <a name="microsoft-and-cjis-security-policy"></a>Microsoft および CJIS セキュリティ ポリシー

Microsoft は、CJIS 情報契約を使用して州の CJIS セキュリティ アドオンに署名します。 これらは、CJIS セキュリティ ポリシーの遵守を担当する州の法執行機関に、Microsoft のクラウド セキュリティ制御がデータの完全なライフサイクルを保護し、CJI にアクセスできる運用担当者の適切なバックグラウンド スクリーニングを保証する方法を示します。 Microsoft は引き続き州政府と取り組み、CJIS 情報契約を締結しています。

Microsoft は、Microsoft Azure Government、Microsoft Office 365 米国政府機関、および Microsoft Dynamics 365 米国政府機関の運用ポリシーと手順を評価し、スコープ内サービスの使用に関する FBI 要件を満たす適切なサービス契約における能力を証明します。

Microsoft Cloud での CJIS セキュリティ ポリシーの利点について説明します。 Genetec が犯罪捜査をクリアした方法 [を読む](https://customers.microsoft.com/story/genetec)

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- Azure Government
- Dynamics 365 米国政府機関
- Office 365米国政府
- Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに組み込まれているサービス)

## <a name="azure-dynamics-365-and-cjis"></a>Azure、Dynamics 365、および CJIS

Azure、Dynamics 365、その他のオンライン サービスのコンプライアンスの詳細については [、「Azure CJIS](/azure/compliance/offerings/offering-cjis)の提供」を参照してください。

## <a name="office-365-and-cjis"></a>Office 365 CJIS

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **GCC** | Azure Active Directory、コンプライアンス マネージャー、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 Advanced Compliance アドオン、Office 365 セキュリティ/コンプライアンス センター、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365 監査、レポート、証明書

FBI は、CJIS 要件に準拠した Microsoft の認定を提供していない。 代わりに、Microsoft の構成証明は、Microsoft と州の CJIS 機関との間、および Microsoft とその顧客間の契約に含まれています。

[Microsoft CJIS クラウド要件](https://aka.ms/MicrosoftCJISCloudRequirements)

### <a name="cjis-status-in-the-united-states-current-as-of-1152020"></a>米国の CJIS ステータス (2020 年 11 月 5 日現在)

45 の州とコロンビア特別区と管理契約が締結され、緑色のマップで強調表示されます。

アラバマ州、アラスカ州、アリゾナ州、アーカンソー州、カリフォルニア州、コロラド州、コネチカット州、フロリダ州、ジョージア州、ハワイ州、アイダホ州、イリノイ州、インディアナ州、アイオワ州、 カンザス州、ケンタッキー州、メイン州、マサチューセッツ州、ミシガン州、ミネソタ州、ミネソタ州、ミシシッピ州、ミズーリ州、モンタナ州、ネブラスカ州、ネバダ州、ニューハンプシャー州、ニューハンプシャー州、ニューメキシコ州、ニューヨーク州、ノースカロライナ州、ノースダコタ州、オクラホマ州、オレゴン州、ペンシルベニア州、ロードアイランド州、サウスカロライナ州、テネシー州、テキサス州、ユタ州、バージニア州、ワシントン州、ウェストバージニア州、ウィスコンシン州、コロンビア州

適用される CJIS 規制規制を遵守する Microsoft の取り組みにより、刑事司法組織はクラウドベースのソリューションを実装し、CJIS セキュリティ ポリシー V5.9 に準拠することができます。

### <a name="frequently-asked-questions"></a>よく寄せられる質問

**コンプライアンス情報はどこで要求できますか?**

関心のある管轄区域に関する情報については、Microsoft アカウント担当者にお問い合わせください。 現在 <cjis@microsoft.com> 利用可能なサービスの状態に関する情報については、お問い合わせください。

**Microsoft は、クラウド サービスが自分の状態の要件に準拠していることをどのように実証しますか?**

Microsoft は、州 CJIS Systems Agency (CSA) と情報契約を締結します。州の CSA からコピーを要求できます。 さらに、Microsoft は、お客様に詳細なセキュリティ、プライバシー、コンプライアンス情報を提供します。 また、独立監査人が作成したセキュリティおよびコンプライアンス レポートを確認して、Microsoft が関連する監査範囲に適したセキュリティ制御 (ISO 27001 など) を実装したと検証することもできます。

**代理店のコンプライアンスの取り組みからどこから始めるのですか?**

[CJIS セキュリティ ポリシーでは、CJI](https://aka.ms/cjis-security-policy) を保護するために代理店が取る必要がある予防措置について説明します。 さらに、Microsoft アカウント担当者は、お客様の管轄地域の要件に精通しているユーザーと連絡を取り合う場合があります。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

### <a name="resources"></a>リソース

- [刑事司法情報サービス](https://aka.ms/cjis)
- [CJIS セキュリティ ポリシー](https://aka.ms/cjis-security-policy)
- [Microsoft Common Controls Hub コンプライアンス フレームワーク](https://www.microsoft.com/trustcenter/common-controls-hub)
- [Microsoft Government クラウド](https://go.microsoft.com/fwlink/?linkid=2087246)
- [Microsoft Trust Center のコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
