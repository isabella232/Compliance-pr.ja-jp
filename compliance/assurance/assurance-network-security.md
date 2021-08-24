---
title: ネットワーク セキュリティ
description: ネットワーク セキュリティの詳細については、Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 92da9e7bb2716f61088e02c244cb9905af142ead
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481839"
---
# <a name="network-security-overview"></a>ネットワーク セキュリティの概要

## <a name="how-do-microsoft-online-services-secure-the-network-boundary"></a>Microsoft オンライン サービスは、ネットワーク境界をセキュリティで保護する方法を説明します。

Microsoft オンライン サービスでは、ネットワークベースの攻撃の自動検出と防止、特殊なファイアウォール デバイス、スパム対策およびマルウェア対策保護のための Exchange Online Protection (EOP) など、ネットワーク境界を保護するための複数の戦略を採用しています。 さらに、Microsoft オンライン サービスは、実稼働環境を論理的に分離されたネットワーク セグメントに分割し、セグメント間で必要な通信のみを許可します。 ネットワーク トラフィックは、境界ポイントで追加のネットワーク ファイアウォールを使用してセキュリティ保護され、ネットワーク攻撃の検出、防止、軽減に役立ちます。

## <a name="how-do-microsoft-online-services-defend-against-ddos-attacks"></a>Microsoft オンライン サービスは、DDoS 攻撃からどのように防御しますか?

Microsoft の大規模なインターネットプレゼンスは、多くの分散型サービス拒否 (DDoS) 攻撃による悪影響からそれを絶縁します。 各 Microsoft オンライン サービスの分散インスタンスと各サービスへの複数のルートは、システムに対する DDoS 攻撃の影響を制限します。 この冗長性により、Microsoft オンライン サービスが DDoS 攻撃を吸収する能力が向上し、サービスの可用性に影響を与える前に、DDoS 攻撃を検出および軽減するために利用可能な時間が増加します。

Microsoft の冗長システム アーキテクチャに加えて、Microsoft は高度な検出および軽減ツールを使用して DDoS 攻撃に対応します。 特殊目的のファイアウォールは、ネットワークに境界を越える前に不要なトラフィックを監視およびドロップし、ネットワーク境界内にあるシステムのストレスを軽減します。 Microsoft は、クラウド サービスをさらに保護するために、クラウド サービスの一部として展開された DDoS 防御Microsoft Azure。 Azure DDoS 防御システムは、外部および他の Azure テナントからの攻撃に耐えるように設計されています。

## <a name="how-does-microsoft-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Microsoft は、オンライン サービスを介してアップロードまたは送信されるスパムやマルウェアからユーザーを保護する方法を説明します。

Microsoft オンライン サービスは、マルウェア対策保護を、悪意のあるコードのベクトルである可能性があるサービス (たとえば、Exchange OnlineおよびオンラインSharePointします。 Exchange Online Protection (EOP) は、システムに入ってシステムを終了すると、すべての電子メールと電子メールの添付ファイルをスキャンしてマルウェアを検出し、感染したメッセージと添付ファイルが配信されるのを防ぐ。 高度なスパム フィルターは、顧客組織がスパムを受信および送信するのを防ぐために、受信メッセージと送信メッセージに自動的に適用されます。 この保護層は、フィッシング攻撃など、迷惑メールや承認されていないメールを利用する攻撃から保護します。 SharePointオンラインでは、同じウイルス検出エンジンを使用して、アップロードされたファイルを選択的にスキャンしてマルウェアを検出します。 ファイルが感染したとマークされている場合、ユーザーはクライアント エンドポイントを保護するためにファイルをダウンロードまたは同期できません。 同様に、Azure は、アップロードされたファイルに関連するハッシュを、既知Azure Storageのハッシュと比較します。 一致が見つかると、Azure セキュリティ センターでアラートが発生し、アラートの正当性と対処方法に関する決定が行されます。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 ネットワーク セキュリティに関連するコントロールの検証については、次の表を参照してください。

### <a name="azure-and-dynamics-365"></a>Azure と Dynamics 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | VM-1: セキュリティ イベント ログ <br> VM-3: 侵入の検出と監視 <br> VM-4: 悪意のあるイベントの調査 <br> VM-6: 脆弱性スキャン <br> VM-7: ネットワーク デバイスの構成 <br> VM-8: 侵入テスト <br> VM-9: ネットワーク デバイスのセキュリティ イベント ログ <br> VM-13: ネットワーク デバイスの脆弱性の軽減 | 3 月 31 日。 2021 |

### <a name="office-365"></a>Office 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SC-5: サービス拒否の保護 <br> SC-7: 境界保護 <br> SI-2: 欠陥修復 <br> SI-3: 悪意のあるコード保護 <br> SI-8: スパム保護 | 2020 年 9 月 24 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: 脆弱性スキャン | 2020 年 12 月 24 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: 脆弱性スキャン <br> CA-45: マルウェア対策 | 2020 年 12 月 24 日 |