---
title: ネットワーク セキュリティ
description: Microsoft 365 のネットワーク セキュリティについて
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
ms.openlocfilehash: e246cc3c84a17fe697baea29eda285599832b0fa
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787432"
---
# <a name="network-security-overview"></a>ネットワーク セキュリティの概要

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>Microsoft 365 はネットワーク境界をセキュリティで保護する方法を説明します。

Microsoft 365 では、ネットワークベースの攻撃の自動検出と防止、特殊なファイアウォール デバイス、スパム対策およびマルウェア対策保護のための Exchange Online Protection (EOP) など、ネットワーク境界を保護するための複数の戦略を採用しています。 さらに、Microsoft 365 は、実稼働環境を論理的に分離されたネットワーク セグメントに分け、セグメント間の通信が必要な場合にのみ許可されます。 ネットワーク トラフィックは、境界ポイントで追加のネットワーク ファイアウォールを使用してセキュリティ保護され、ネットワーク攻撃の検出、防止、軽減に役立ちます。

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>Microsoft 365 は DDoS 攻撃からどのように防御しますか?

Microsoft の大規模なインターネット プレゼンスは、多くの分散型サービス拒否 (DDoS) 攻撃による悪影響を受け取らない。 各 Microsoft 365 サービスの分散インスタンスと各サービスへの複数のルートによって、システムに対する DDoS 攻撃の影響が制限されます。 この冗長性により、Microsoft 365 の DDoS 攻撃を吸収する能力が向上し、サービスの可用性に影響を与える前に DDoS 攻撃を検出して軽減するために使用可能な時間が増加します。

Microsoft の冗長システム アーキテクチャに加えて、Microsoft は高度な検出および軽減ツールを使用して DDoS 攻撃に対応します。 特殊な用途のファイアウォールは、ネットワークに境界を越える前に不要なトラフィックを監視およびドロップし、ネットワーク境界の内側にあるシステムに対する負荷を軽減します。 Microsoft では、クラウド サービスをさらに保護するために、Microsoft Azure の一部として展開された DDoS 防御システムを利用しています。 Azure DDoS 防御システムは、外部および他の Azure テナントからの攻撃に対応するように設計されています。

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Microsoft 365 は、オンライン サービスを介してアップロードまたは送信されるスパムやマルウェアからユーザーを保護する方法を説明します。

Microsoft 365 はマルウェア対策保護を、Exchange Online や SharePoint Online などの悪意のあるコードのベクトルになる可能性があるサービスに組み込む。 Exchange Online Protection (EOP) は、システムに入ってシステムを終了するマルウェアについて、すべてのメールと電子メールの添付ファイルをスキャンして、感染したメッセージと添付ファイルが配信されるのを防ぐ。 高度なスパム フィルターは、受信メッセージと送信メッセージに自動的に適用され、顧客組織がスパムを受信および送信するのを防ぐのに役立ちます。 この保護層は、フィッシング攻撃など、未承諾または未承認の電子メールを利用する攻撃から保護します。 SharePoint Online は、同じウイルス検出エンジンを使用して、アップロードされたファイルを選択的にスキャンしてマルウェアを検出します。 ファイルがウイルスに感染したとマークされている場合、ユーザーはファイルをダウンロードまたは同期してクライアント エンドポイントを保護できません。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 ネットワーク セキュリティに関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5: サービス拒否の保護 <br> SC-7: 境界保護 <br> SI-2: 欠陥の修復 <br> SI-3: 悪意のあるコード保護 <br> SI-8: スパム保護 | 2020 年 9 月 24 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: 脆弱性スキャン | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: 脆弱性スキャン <br> CA-45: マルウェア対策 | 2020 年 12 月 24 日 |