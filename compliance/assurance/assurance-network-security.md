---
title: ネットワーク セキュリティ
description: Microsoft 365 でのネットワークセキュリティについて説明します。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: c063460fdfba44265b3a1504a049a4772b484dff
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507759"
---
# <a name="network-security-overview"></a>ネットワークセキュリティの概要

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>Microsoft 365 はネットワーク境界をセキュリティで保護していますか?

Microsoft 365 では、ネットワーク境界をセキュリティで保護するための複数の戦略が採用されています。これには、ネットワークベースの攻撃、特別なファイアウォールデバイス、および Exchange Online Protection (EOP) がスパム対策とマルウェア対策保護のための自動検出と防止を含みます。 さらに、Microsoft 365 は、セグメント間で必要な通信のみを許可することで、運用環境を論理的に分離されたネットワークセグメントに分離します。 ネットワークトラフィックをセキュリティで保護するには、境界ポイントに追加のネットワークファイアウォールを使用します。

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>Microsoft 365 は、DDoS 攻撃に対してどのように防御されるのですか?

Microsoft の大規模なインターネットプレゼンスは、多くの分散型サービス不能 (DDoS) 攻撃の悪影響から分離されています。 各 Microsoft 365 サービスに対する分散インスタンス、および各サービスへの複数のルートは、システムに対する DDoS 攻撃の影響を制限します。 この冗長性により、Microsoft 365 が DDoS 攻撃を吸収する能力が向上し、DDoS 攻撃を検出して軽減する時間が増加して、サービスの可用性に影響を与えることができます。

Microsoft の冗長なシステムアーキテクチャに加えて、Microsoft では、高度な検出および軽減ツールを使用して、DDoS 攻撃に対応しています。 特殊なファイアウォールは、境界をネットワークに通過する前に不要なトラフィックを監視および削除し、ネットワーク境界内に配置されたシステムの負荷を軽減します。 クラウドサービスをさらに保護するために、Microsoft は、Microsoft Azure の一部として展開された DDoS 防御システムを利用しています。 Azure の DDoS 防御システムは、外部からの攻撃や他の Azure テナントからの攻撃に耐えられるように設計されています。

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Microsoft 365 は、オンラインサービス経由でアップロードまたは送信されるスパムやマルウェアからユーザーを保護しますか?

Microsoft 365 は、Exchange Online や SharePoint Online など、悪意のあるコードのようなサービスに対して、マルウェア対策保護を構築します。 Exchange Online Protection (EOP) は、システムを入力して終了し、感染したメッセージや添付ファイルが配信されないように、すべてのメールおよび電子メール添付ファイルをスキャンしてマルウェアをスキャンします。 高度なスパムフィルターは、お客様の組織がスパムを受信および送信できないようにするために、受信メッセージと送信メッセージに自動的に適用されます。 この保護層は、フィッシング攻撃など、要請されていないまたは許可されていない電子メールを悪用する攻撃に対してガードします。 SharePoint Online は、マルウェア用にアップロードされたファイルを選択的にスキャンするのに、同じウイルス検出エンジンを使用します。 ファイルが感染とマークされている場合、ユーザーはファイルをダウンロードまたは同期して、クライアントエンドポイントを保護することはできません。

## <a name="related-external-regulations--certifications"></a>関連する外部規制 & 証明書

Microsoft のオンラインサービスは、社外の規制と証明書に準拠するために定期的に監査されます。 ネットワークセキュリティに関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5: サービス拒否防止 <br> SC-7: 境界保護 <br> SI-2: 問題の修復 <br> SI-3: 悪意のあるコード保護 <br> SI-8: スパム対策 | 2020年9月24日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27: 脆弱性スキャン | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27: 脆弱性スキャン <br> CA-45: マルウェア対策 | 2019 年 9 月 30 日 |