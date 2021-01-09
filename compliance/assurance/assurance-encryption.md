---
title: 暗号化とキー管理の概要
description: Microsoft 365 での暗号化とキー管理について
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
ms.openlocfilehash: ca13c5dfb229acd46ef0dd027b537afc2ac20b5a
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787346"
---
# <a name="encryption-and-key-management-overview"></a>暗号化とキー管理の概要

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>顧客のコンテンツを保護する上で暗号化はどのような役割を果たしますか?

ほとんどの Microsoft ビジネス クラウド サービスはマルチテナントです。つまり、顧客のコンテンツは、他のお客様と同じ物理ハードウェアに保存される可能性があります。 お客様のコンテンツの機密性を保護するために、Microsoft 365 は、利用可能な最も強力で最も安全な暗号化プロトコルを使用して、保存中および転送中のすべてのデータを暗号化します。

暗号化は、強力なアクセス制御の代わりに使用されるのではありません。 Microsoft 365 のアクセス制御ポリシーである Zero Standing Access (ZSA) は、Microsoft の従業員による不正なアクセスから顧客コンテンツを保護します。 暗号化は、保存されている場所で顧客のコンテンツの機密性を保護し、Microsoft 365 システム間または Microsoft 365 と顧客との間で転送中にコンテンツが読み取らなされるのを防ぐことで、アクセス制御を補完します。

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>Microsoft 365 は、保存データを暗号化する方法を説明します。

Microsoft 365 のすべての顧客コンテンツは、1 つ以上の形式の暗号化によって保護されます。 Microsoft サーバーは、BitLocker を使用して、顧客のコンテンツを含むディスク ドライブをボリューム レベルで暗号化します。 BitLocker によって提供される暗号化は、顧客のコンテンツを含むディスクへの不正な物理的アクセスにつながる可能性がある他のプロセスまたは制御 (アクセス制御やハードウェアのリサイクルなど) が失効した場合に、お客様のコンテンツを保護します。

Exchange Online、Microsoft Teams、SharePoint Online、OneDrive for Business は、アプリケーションレイヤーで Service Encryption を使用して顧客コンテンツを暗号化します。 Service Encryption は、強力な暗号化保護の上に権利保護と管理機能を提供します。 また、Windows オペレーティング システムと、それらのオペレーティング システムによって保存または処理される顧客データを分離できます。

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>Microsoft 365 は、転送中のデータを暗号化する方法を説明します。

Microsoft 365 製品とサービスは、TLS などの強力なトランスポート プロトコルを使用して、未承認の関係者がネットワークを越える移動中に顧客データを盗聴するのを防ぐ。 送信中のデータの例としては、配信中のメール メッセージ、オンライン会議で行う会話、データセンター間でレプリケートされるファイルがあります。

Microsoft 365 では、ユーザーのデバイスが Microsoft サーバーと通信している場合や、Microsoft サーバーが別のサーバーと通信している場合、データは "送信中" と見なされます。 Exchange Online、SharePoint Online、Microsoft Teams、および Office Online は、すべて TLS を使用して、転送中もデータを機密に維持します。

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>Microsoft 365 では、暗号化に使用されるキーを管理する方法について説明します。

強力な暗号化は、データの暗号化に使用されるキーと同じだけ安全です。 Microsoft は、独自のセキュリティ証明書を使用して、転送中のデータの TLS 接続を暗号化します。 保存データの場合、BitLocker で保護されたボリュームはボリューム全体の暗号化キーで暗号化されます。この暗号化キーはボリューム マスター キーで暗号化され、ボリューム マスター キーはサーバーのトラステッド プラットフォーム モジュール (TPM) にバインドされます。 BitLocker は FIPS 準拠のアルゴリズムを使用して、暗号化キーがクリアでネットワークに保存または送信されるのを確実にします。

Service Encryption は、Exchange Online、Microsoft Teams、SharePoint Online、OneDrive for Business で保存中の顧客データの暗号化の追加レイヤーを提供します。 サービスの暗号化を使用すると、Microsoft で管理されるキーと顧客キーの 2 つの暗号化キー管理のオプションが提供されます。 Microsoft が管理するキーを使用する場合、Microsoft 365 サービスはサービスの暗号化に使用されるルート キーを自動的に生成し、安全に保存します。

独自のルート暗号化キーを制御する要件を持つお客様は、顧客キーを使用してサービスの暗号化を利用できます。 顧客キーを使用すると、顧客はオンプレミスのハードウェア サービス モジュール (VAULT) または Azure Key Vault (A VAULT) を使用して、独自の暗号化キーを生成できます。 顧客のルート キーは ARK に格納され、顧客のメールボックス のデータまたはファイルを暗号化するキーチェーンのルートとして使用できます。 顧客のルート キーは、データ暗号化のために Microsoft 365 サービス コードによって間接的にのみアクセスできます。また、Microsoft の従業員が直接アクセスすることはできません。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 暗号化とキー管理に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: 伝送の機密性と整合性 <br> SC-13: 暗号化の使用 <br> SC-28: 残りの情報の保護 <br>  | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: 暗号化コントロール <br> A.18.1.5: 暗号化コントロール | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: 暗号化コントロール <br> A.18.1.5: 暗号化コントロール | 2020 月 2 月 22 日 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: パブリック データ送信ネットワーク経由で送信される PII の暗号化 | 2020 月 2 月 22 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: 転送中データの暗号化 <br> CA-54: 保存データの暗号化 <br> CA-62: 顧客キーメールボックスの暗号化 <br> CA-63: 顧客キー データの削除 <br> CA-64: 顧客キー | 2020 年 12 月 24 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: 顧客の暗号化キー <br> CUEC-17: 顧客キー コンテナー <br>  CUEC-18: 顧客キーの回転| 2020 年 12 月 24 日 |
