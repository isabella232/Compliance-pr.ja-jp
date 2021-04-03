---
title: ネットワーク セキュリティ
description: Microsoft 365 のネットワーク セキュリティの詳細
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
hideEdit: true
ms.openlocfilehash: a2b153b2f2f57a011c28ee65cbe03019cbaa27a1
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496922"
---
# <a name="network-security-overview"></a>ネットワーク セキュリティの概要

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>Microsoft 365 はネットワーク境界をセキュリティで保護する方法を説明します。

Microsoft 365 では、ネットワークベースの攻撃の自動検出と防止、特殊なファイアウォール デバイス、スパム対策およびマルウェア対策保護のための Exchange Online Protection (EOP) など、ネットワーク境界を保護するための複数の戦略を採用しています。 さらに、Microsoft 365 は、その実稼働環境を論理的に分離されたネットワーク セグメントに分離し、セグメント間で必要な通信のみを許可します。 ネットワーク トラフィックは、境界ポイントで追加のネットワーク ファイアウォールを使用してセキュリティ保護され、ネットワーク攻撃の検出、防止、軽減に役立ちます。

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>Microsoft 365 は DDoS 攻撃からどのように防御しますか?

Microsoft の大規模なインターネットプレゼンスは、多くの分散型サービス拒否 (DDoS) 攻撃による悪影響からそれを絶縁します。 各 Microsoft 365 サービスの分散インスタンスと各サービスへの複数のルートは、システムに対する DDoS 攻撃の影響を制限します。 この冗長性により、Microsoft 365 は DDoS 攻撃を吸収する能力が向上し、サービスの可用性に影響を与える前に、DDoS 攻撃を検出および軽減するために使用できる時間が増えます。

Microsoft の冗長システム アーキテクチャに加えて、Microsoft は高度な検出および軽減ツールを使用して DDoS 攻撃に対応します。 特殊目的のファイアウォールは、ネットワークに境界を越える前に不要なトラフィックを監視およびドロップし、ネットワーク境界内にあるシステムのストレスを軽減します。 Microsoft は、クラウド サービスをさらに保護するために、Microsoft Azure の一部として展開された DDoS 防御システムを利用しています。 Azure DDoS 防御システムは、外部からの攻撃や他の Azure テナントからの攻撃に耐えるように設計されています。

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Microsoft 365 は、オンライン サービスを介してアップロードまたは送信されるスパムやマルウェアからユーザーを保護する方法を説明します。

Microsoft 365 は、Exchange Online や SharePoint Online などの悪意のあるコードのベクトルになる可能性のあるサービスにマルウェア対策保護を構築します。 Exchange Online Protection (EOP) は、システムに入ってシステムを終了すると、すべての電子メールと電子メールの添付ファイルをスキャンしてマルウェアを検出し、感染したメッセージと添付ファイルが配信されるのを防きます。 高度なスパム フィルターは、顧客組織がスパムを受信および送信するのを防ぐために、受信メッセージと送信メッセージに自動的に適用されます。 この保護層は、フィッシング攻撃など、迷惑メールや承認されていないメールを利用する攻撃から保護します。 SharePoint Online は、同じウイルス検出エンジンを使用して、アップロードされたファイルを選択的にスキャンしてマルウェアを検出します。 ファイルが感染したとマークされている場合、ユーザーはクライアント エンドポイントを保護するためにファイルをダウンロードまたは同期できません。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 ネットワーク セキュリティに関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5: サービス拒否の保護 <br> SC-7: 境界保護 <br> SI-2: 欠陥修復 <br> SI-3: 悪意のあるコード保護 <br> SI-8: スパム保護 | 2020 年 9 月 24 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: 脆弱性スキャン | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: 脆弱性スキャン <br> CA-45: マルウェア対策 | 2020 年 12 月 24 日 |