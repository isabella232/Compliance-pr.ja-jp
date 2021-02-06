---
title: カリフォルニア州消費者プライバシー法 (CCPA)
description: Microsoft サービスおよびカリフォルニア州消費者プライバシー法 (CCPA)。
keywords: Microsoft 365、コンプライアンス、サービス
localization_priority: None
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
ms.openlocfilehash: df5b77a9ae9e5f38e695294b1180bba5a4ef8eca
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121146"
---
# <a name="california-consumer-privacy-act-ccpa"></a>カリフォルニア州消費者プライバシー法 (CCPA)

## <a name="ccpa-overview"></a>CCPA の概要

カリフォルニア州消費者プライバシー法 (CCPA) は、米国で最初の包括的なプライバシー法です。 カリフォルニア州の消費者にさまざまなプライバシーの権利を提供します。  CCPA によって規制されている企業には、開示、一般データ保護規則 (GDPR) に似た消費者データ主体の権利 (DSR)、特定のデータ転送の「オプトアウト」、未成年者の「オプトイン」要件など、多くの義務があります。

CCPA は、次の 1 つ以上を満たす、カリフォルニア州で事業を行う企業にのみ適用されます。(1) 年収の合計が 2500 万ドルを超える場合、または (2) カリフォルニア州の消費者の個人情報の販売による年収の 50% 以上を得るか、(3) カリフォルニア州の消費者の個人情報を毎年 50,000 人以上の個人情報を購入、販売、または共有します。

CCPA は 2020 年 1 月 1 日から有効になります。 ただし、カリフォルニア州弁護士 (AG) による執行は、2020 年 7 月 1 日に開始されます。

カリフォルニア州 AG は CCPA を実施し、コンプライアンス以外の罰金を科す権利を持つ。 CCPA は、データ侵害に限定された個人のアクションの権利も提供します。 私的権利の行使では、1 つのインシデントの損害は、消費者 1 人当たり $100 から $750 です。 カリフォルニア AG でも CCPA をそのまま適用し、違反ごとに $2,500 以下の罰則金を科しています。また、意図的な違反には $7,500 以下の罰則金を科しています。

## <a name="microsoft-and-the-ccpa"></a>Microsoft と CCPA

カリフォルニア州でビジネスを行う商用のお客様の場合、Microsoft はオンライン サービスとプロフェッショナル サービスの提供に関して「サービス プロバイダー」として機能します。  オンライン サービスの使用条件 (OST) および Microsoft プロフェッショナル サービス データ保護に関する追加条項 (MSDPA) は、CCPA の下のサービス プロバイダーの要件を既に満たしています。お客様が引き続きオンライン サービスにデータを転送するには、通常十分です。 そのため、お客様が CCPA の下でサービス プロバイダーとして Microsoft を利用するために、追加の契約上の変更は必要ありません。

OST に規定されている通り、Microsoft はオンライン サービスの提供に適用されるすべての法律および規制 (CCPA を含む) に準拠しています。  

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure](https://aka.ms/AzureCompliance)
- Azure Dev Ops
- [Dynamics 365](https://aka.ms/d365-compliance-list)
- Intune
- [Office 365](https://aka.ms/o365-compliance-framework)
- サポートおよびプロフェッショナル サービス
- Visual Studio

## <a name="how-you-can-prepare-for-your-ccpa-compliance-when-using-microsoft-products-and-services"></a>Microsoft 製品とサービスを使用する際に CCPA コンプライアンスを準備する方法

CCPA の準備に取りかかる手順を次に示します。

- CCPA プライバシー プログラムの一環として [、コンプライアンス](/microsoft-365/compliance/compliance-manager) マネージャーで GDPR 評価を活用します。
- データ主体要求ツールを使用して、データ主体アクセス要求 (DSARs) に効率的に対応するプロセスを確立します。
- ラベルとポリシーを設定し、Microsoft Information Protection を使用して機密データを検索、分類、保護します。
- メールの暗号化機能を使用して、機密情報をさらに管理します。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**CCPA によって私の会社はどのような影響を受けますか?**

カリフォルニア州に与える CCPA の権利の多くは、GDPR が提供する権利 (アクセス、削除、移植性など、開示およびデータ主体権利 (DSR) 要求を含む) に似ています。 そのため、お客様は既存の GDPR ソリューションを参照して、CCPA コンプライアンスを支援することができます。

CCPA への取り入りを開始するには、情報の検出、個人情報の共有方法の決定、情報の使用方法、保護方法、正式なデータ侵害対応プログラムの実行に重点を置く必要があります。

**GDPR と CCPA の違いは何ですか?**

さまざまな違いがあります。 次のような類似点に重点を置く方が簡単です。

- 透明性/開示義務、
- データのコピーにアクセス、削除、および受信する消費者の権利
- GDPR が同様の契約上の義務を持つ 「処理者」を定義する方法に似た 「サービス プロバイダー」の定義
- 「管理者」の GDPR 定義を含む 「ビジネス」の定義。

CCPA の最大の違いは、データのサード パーティへの販売からのオプトアウトを可能にするコア要件です (「セール」は、重要な考慮事項のためにデータの共有を含む大まかに定義されています)。

**CCPA で企業が認めなければならない権利は何ですか?**

CCPA では、次の中でも個人情報の収集、転送、販売を行う規制対象企業が必要です。

- 情報を収集する前に、消費者に対して、収集する情報のカテゴリや目的を開示する。
- 収集される個人情報のソース、ビジネス目的、およびカテゴリに関するプライバシー ポリシーで、それらのカテゴリの販売方法や他のエンティティへの転送方法など、より詳細な開示を提供します。
- お客様が収集した特定の個人情報に対するアクセス、削除、および移植性に関する DSR 権限を有効にする。
- 消費者がコンシューマーのデータの販売をオプトアウトすることを許可するコントロールを有効にする。 ただし、サービス プロバイダーなどの適用除外エンティティへの転送は許可されます。
- 16 歳未満の未成年者の場合は、オプトイン プロセスを有効にして、積極的に販売をオプトインすることなく、未成年者の個人情報の販売が行われるのを無効にします。
- CCPA の消費者の権利に基づき、消費者がその権利の行使によって、差別されないことを確認する。

**CCPA は子供にはどのように適用されますか?**

- CCPA は、13 歳未満の子供に対して、児童オンラインプライバシー保護法 (COPPA) と一致する、保護者による同意の義務を導入しています。
- 13 歳から 16 歳の子供の場合、CCPA は子からオプトインの同意を得る新しい義務を課します。

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

## <a name="resources"></a>リソース

- [新しいカリフォルニア州消費者プライバシー法の準備に役立つ 5 つのヒント](https://aka.ms/M365ComplianceBlog_RSA)
- [CCPA ガイドの使用を開始する](https://info.microsoft.com/ww-landing-Five-tips-to-help-you-prepare-for-the-California-Consumer-Privacy-Act.html)
- [データ主体要求と GDPR](gdpr-data-subject-requests.md)
- [カリフォルニア州消費者プライバシー法 (CCPA) の FAQ](ccpa-faq.md)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
