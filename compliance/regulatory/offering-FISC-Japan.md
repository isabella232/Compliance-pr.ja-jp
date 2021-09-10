---
title: 金融情報システム センター (FISC)
description: Microsoft は日本の金融情報システム センターによる安全対策基準第 8 版の要件を満たしています。
keywords: Microsoft 365、コンプライアンス、サービス
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
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: f1eba3e819ae351f1bdff2f8fbdd47c7fca7a1a1
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947956"
---
# <a name="center-for-financial-industry-information-systems-fisc"></a>金融情報システム センター (FISC)

## <a name="fisc-overview"></a>FISC の概要

金融情報システム センター (FISC) は非営利組織であり、日本の銀行取引コンピューター システムの安全性の向上を目的として、1984 年に当時の大蔵大臣により設立されました。 日本の約 700 の企業のスタッフで支えられており、その中には主要な金融機関、保険およびクレジット会社、証券会社、コンピューター メーカー、通信企業などが含まれます。

メンバーの機関、日本銀行、および金融庁 (銀行、証券と為替、および保険の監督を担当する政府組織) の協力により、FISC は銀行取引情報システムの安全性に関するガイドラインを策定しました。 これには、コンピューター システム管理の基本的な監査基準、災害発生時の危機管理計画、および 300 を超える管理項目を網羅するセキュリティ ポリシーと標準の開発が含まれます。

クラウド コンピューティング環境でこれらのガイドラインを適用することは規制による必須事項ではありませんが、クラウド サービスを実装している日本の大部分の金融機関は、これらのセキュリティ基準を満たす情報システムを構築しており、これらの標準から外れて正当性を示すことは困難になっています。 (最新のガイドラインである 2015 年発行第 8 版追補改訂では、金融機関によるクラウド サービスの使用に関する 2 件の改訂とサイバー攻撃への対応策が追加されています。)

このフレームワークの順守は規制による必須事項ではなく、監査されたり、FISC により検証されることはありません。

## <a name="microsoft-and-fisc"></a>Microsoft と FISC

Microsoft は、外部評価機関と連携して、Microsoft Azure、Dynamics 365、およびMicrosoft Office 365 が金融機関向けコンピューター システムに関する FISC セキュリティ ガイドラインの改訂版 9 版の要件を満たしていることを検証しました。Microsoft は、次の各分野における準拠の証明を用意しています。

- 建造物、コンピューター ルーム、電源、空調設備、データセンター、および施設監視用のデータセンター ガイドライン
- 組織、トレーニング、アクセス制御、システム開発、および監査用の運用ガイドライン
- ハードウェアとソフトウェアの信頼性を向上するための方策、およびデータ保護、不正使用の防止、脅威検出、障害復旧などを含むセキュリティ リスクへの対応策用のテクニカル ガイドライン

金融機関は、対象となる Azure、Dynamics 365、Office 365、および Microsoft Cloud App Security のインフラおよびプラットフォーム サービスについて、これらの 3 分野のコンプライアンスの評価を利用できます。

[外部評価機関の検証と評価機関のサイトへのリンクの詳細 (日本語のみ)](https://cloudblogs.microsoft.com/industry-blog/ja-jp/financial-services/2018/05/11/fisc_v9/)。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- Azure
- Intune
- Microsoft Cloud App Security
- Office 365
- Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに搭載されているサービス)

## <a name="office-365-and-fisc"></a>Office 365 と FISC

### <a name="office-365-cloud-environments"></a>Office 365 のクラウド環境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 の適用性と範囲内のサービス

以下の表を使用して、Office 365 サービスとサブスクリプションの適用性を決定します。

| **適用性** | **範囲内のサービス** |
|:------------------|:----------------------|
| **商用** | Access Online、Azure Active Directory、Delve、Exchange Online、Exchange Online Protection、Microsoft Teams、Office 365 ProPlus、Office Online、OneDrive for Business、Power BI for Office 365、Project Online、SharePoint Online、Skype for Business |

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**FISC ガイドラインはだれに適用されますか?**

システムの安全性、信頼性、監査への取り組みを検証して、日本で確立されたベスト プラクティスに従い、FISC ガイドラインに準拠する意向がある、日本の銀行およびその他の金融機関。

**FISC の第 8 版要件に関する詳細情報はどこで入手できますか?**

FISC は、有識者検討会より次の 2 つのレポートを発行しています。

- [金融機関におけるクラウド コンピューティングの利用](https://aka.ms/cloud-computing-report-en)
- [金融機関におけるサイバー攻撃対応](https://aka.ms/cyberattack-counter)

**FISC フレームワークへの Microsoft の対応の詳細はどこで入手できますか?**

Microsoft クラウド サービスの FISC 準拠を評価した第三者のセキュリティに関する参考情報については、Microsoft アカウントの担当者にお問い合わせください。

**このフレームワークへの Microsoft の対応を自分の組織の資格認定プロセスで使用できますか?**

はい。ただし、このフレームワークに対する Microsoft の回答は第三者により準拠が確認されていますが、お客様が Azure または Office 365 で実装したソリューションの準拠状況に関しては、お客様自身で検証する必要があります。

## <a name="resources"></a>リソース

- [Microsoft オンライン サービス条件](https://aka.ms/Online-Services-Terms)
- [FISC セキュリティ ガイドライン/安全基準](https://www.fisc.or.jp/english)
- [クラウド コンピューティングの利用に関する FISC レポート](https://aka.ms/cloud-computing-report-en)
- [Microsoft トラスト センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)

## <a name="resources-in-japanese"></a>日本語のリソース

- [FISC](https://www.fisc.or.jp/)
