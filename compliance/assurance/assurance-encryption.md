---
title: 暗号化とキー管理の概要
description: 暗号化とキー管理の詳細については、Microsoft 365
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
ms.openlocfilehash: 5e46fdb5ddc3b1b80df0bcadf9054b9353a0dc8e
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088646"
---
# <a name="encryption-and-key-management-overview"></a>暗号化とキー管理の概要

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>顧客コンテンツの保護において暗号化が果たす役割は何ですか?

ほとんどの Microsoft ビジネス クラウド サービスはマルチテナントです。つまり、顧客コンテンツは他の顧客と同じ物理ハードウェアに保存される可能性があります。 顧客コンテンツの機密性を保護するために、Microsoft 365は、利用可能な最も強力で最も安全な暗号化プロトコルの一部を使用して、保存中および転送中のすべてのデータを暗号化します。

暗号化は、強力なアクセス制御に代わるものではありません。 Microsoft 365のアクセス制御ポリシーであるゼロ スタンディング アクセス (ZSA) は、Microsoft の従業員による承認されていないアクセスから顧客コンテンツを保護します。 暗号化は、保存されている場所で顧客コンテンツの機密性を保護し、Microsoft 365 システム間または Microsoft 365 と顧客間の転送中にコンテンツが読み取らされるのを防ぐことによって、アクセス制御を補完します。

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>保存時Microsoft 365データを暗号化する方法

1 つ以上の形式Microsoft 365暗号化によって、すべての顧客コンテンツが保護されます。 Microsoft サーバーは、BitLocker を使用して、ボリューム レベルで顧客コンテンツを含むディスク ドライブを暗号化します。 BitLocker によって提供される暗号化は、顧客コンテンツを含むディスクへの物理的な不正なアクセスにつながる可能性がある他のプロセスまたはコントロール (たとえば、ハードウェアのアクセス制御やリサイクル) で経過した場合に、顧客のコンテンツを保護します。

Exchange Online、Microsoft Teams、SharePoint、および OneDrive for Businessアプリケーション層でサービス暗号化を使用して顧客コンテンツを暗号化します。 サービス暗号化は、強力な暗号化保護の上に権限保護と管理機能を提供します。 また、これらのオペレーティング システムによって保存Windows処理される顧客データと、これらのオペレーティング システム間で分離することができます。

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>転送中Microsoft 365暗号化する方法

Microsoft 365サービスは、TLS などの強力なトランスポート プロトコルを使用して、承認されていないユーザーがネットワーク上を移動している間に顧客データを盗聴するのを防ぐ。 転送中のデータの例には、配信中のメール メッセージ、オンライン会議で行う会話、データセンター間でレプリケートされるファイルがあります。

このMicrosoft 365、ユーザーのデバイスが Microsoft サーバーと通信している場合や、Microsoft サーバーが別のサーバーと通信している場合、データは "転送中" と見なされます。 Exchange Online、SharePoint、Microsoft Teams、Office オンラインでは、すべて TLS を使用して、転送中にデータが機密に保持されます。

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>暗号化にMicrosoft 365キーを管理する方法

強力な暗号化は、データの暗号化に使用されるキーと同じだけ安全です。 Microsoft は、独自のセキュリティ証明書を使用して、転送中のデータの TLS 接続を暗号化します。 保存データの場合、BitLocker で保護されたボリュームは、ボリューム マスター キーで暗号化されるフル ボリューム暗号化キーで暗号化され、サーバー内のトラステッド プラットフォーム モジュール (TPM) にバインドされます。 BitLocker は、FIPS 準拠のアルゴリズムを使用して、暗号化キーがクリアでワイヤーを使用して保存または送信されるのを確実にします。

サービス暗号化は、Exchange Online、Microsoft Teams、SharePoint Online、および OneDrive for Business の顧客データ保存時の暗号化の追加レイヤーを提供します。 サービス暗号化を使用すると、暗号化キー管理の 2 つのオプション (Microsoft 管理キーまたは顧客キー) が提供されます。 Microsoft 管理キーを使用する場合、Microsoft 365サービスは自動的に生成し、サービス暗号化に使用されるルート キーを安全に保存します。

独自のルート暗号化キーを制御する要件をお持ちのお客様は、顧客キーを使用してサービス暗号化を利用できます。 顧客キーを使用すると、オンプレミスのハードウェア サービス モジュール (HSM) または Azure Key Vault (AKV) のいずれかを使用して、独自の暗号化キーを生成できます。 顧客のルート キーは AKV に格納され、顧客のメールボックス データまたはファイルを暗号化するキーチェーンのルートとして使用できます。 顧客のルート キーには、データ暗号化Microsoft 365サービス コードによってのみ間接的にアクセスできるだけでなく、Microsoft の従業員が直接アクセスすることはできません。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 暗号化とキー管理に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: 伝送の機密性と整合性 <br> SC-13: 暗号化の使用 <br> SC-28: 残りの情報の保護 <br>  | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: 暗号化コントロール <br> A.18.1.5: 暗号化コントロール | 2021 年 4 月 20 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: 暗号化コントロール <br> A.18.1.5: 暗号化コントロール | 2021 年 4 月 20 日 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: パブリック データ伝送ネットワーク経由で送信される PII の暗号化 | 2021 年 4 月 20 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: 転送中のデータ暗号化 <br> CA-54: 保存時のデータ暗号化 <br> CA-62: 顧客キーメールボックスの暗号化 <br> CA-63: 顧客キー データの削除 <br> CA-64: 顧客キー | 2020 年 12 月 24 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: 顧客の暗号化キー <br> CUEC-17: 顧客キー コンテナー <br>  CUEC-18: 顧客キーのローテーション| 2020 年 12 月 24 日 |
