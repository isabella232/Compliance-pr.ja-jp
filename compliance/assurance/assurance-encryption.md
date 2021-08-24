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
ms.openlocfilehash: dc53f42c6aa7ce16e1291538bfad6d63c5a1689d
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482009"
---
# <a name="encryption-and-key-management-overview"></a>暗号化とキー管理の概要

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>顧客コンテンツの保護において暗号化が果たす役割は何ですか?

ほとんどの Microsoft ビジネス クラウド サービスはマルチテナントです。つまり、顧客コンテンツは他の顧客と同じ物理ハードウェアに保存される可能性があります。 お客様のコンテンツの機密性を保護するために、Microsoft オンライン サービスは、利用可能な最も強力で最も安全な暗号化プロトコルの一部を使用して、保存中および転送中のすべてのデータを暗号化します。

暗号化は、強力なアクセス制御に代わるものではありません。 ゼロ スタンディング アクセス (ZSA) の Microsoft のアクセス制御ポリシーは、Microsoft 従業員による未承認アクセスから顧客コンテンツを保護します。 暗号化は、保存されている場所で顧客コンテンツの機密性を保護し、Microsoft オンライン サービス システム間、または Microsoft オンライン サービスと顧客間の転送中にコンテンツが読み取らされるのを防ぐことによって、アクセス制御を補完します。

## <a name="how-do-microsoft-online-services-encrypt-data-at-rest"></a>Microsoft オンライン サービスは、保存時のデータを暗号化する方法を説明します。

Microsoft オンライン サービスのすべての顧客コンテンツは、1 つ以上の形式の暗号化によって保護されます。 Microsoft サーバーは、BitLocker を使用して、ボリューム レベルで顧客コンテンツを含むディスク ドライブを暗号化します。 BitLocker によって提供される暗号化は、他のプロセスやコントロール (ハードウェアのアクセス制御やリサイクルなど) に失効が生じ、顧客コンテンツを含むディスクへの物理的な不正アクセスにつながる可能性がある場合に、顧客のコンテンツを保護します。

Microsoft オンライン サービスは、ボリューム レベルの暗号化に加えて、アプリケーション層でサービス暗号化を使用して顧客コンテンツを暗号化します。 サービス暗号化は、強力な暗号化保護の上に権限保護と管理機能を提供します。 また、これらのオペレーティング システムによって保存Windows処理される顧客データと、これらのオペレーティング システム間で分離することができます。

## <a name="how-do-microsoft-online-services-encrypt-data-in-transit"></a>Microsoft オンライン サービスは、転送中のデータを暗号化する方法を説明します。

Microsoft オンライン サービスは、TLS などの強力なトランスポート プロトコルを使用して、承認されていないユーザーがネットワーク上を移動している間に顧客データを盗聴するのを防ぐ。 転送中のデータの例には、配信中のメール メッセージ、オンライン会議で行う会話、データセンター間でレプリケートされるファイルがあります。

Microsoft オンライン サービスの場合、ユーザーのデバイスが Microsoft サーバーと通信している場合や、Microsoft サーバーが別のサーバーと通信している場合、データは 「転送中」 と見なされます。

## <a name="how-do-microsoft-online-services-manage-the-keys-used-for-encryption"></a>暗号化に使用するキーを Microsoft オンライン サービスで管理する方法

強力な暗号化は、データの暗号化に使用されるキーと同じだけ安全です。 Microsoft は、独自のセキュリティ証明書を使用して、転送中のデータの TLS 接続を暗号化します。 保存データの場合、BitLocker で保護されたボリュームは、ボリューム マスター キーで暗号化されるフル ボリューム暗号化キーで暗号化され、サーバー内のトラステッド プラットフォーム モジュール (TPM) にバインドされます。 BitLocker は、FIPS 準拠のアルゴリズムを使用して、暗号化キーがクリアでワイヤーを使用して保存または送信されるのを確実にします。

サービス暗号化は、顧客のデータ保存時に別の暗号化層を提供し、顧客に暗号化キー管理の 2 つのオプション (Microsoft 管理キーまたは顧客キー) を提供します。 Microsoft が管理するキーを使用する場合、Microsoft オンライン サービスはサービス暗号化に使用されるルート キーを自動的に生成し、安全に保存します。

独自のルート暗号化キーを制御する要件をお持ちのお客様は、顧客キーを使用してサービス暗号化を使用できます。 顧客キーを使用すると、オンプレミスのハードウェア サービス モジュール (HSM) または Azure Key Vault (AKV) のいずれかを使用して、独自の暗号化キーを生成できます。 顧客のルート キーは AKV に格納され、顧客のメールボックス データまたはファイルを暗号化するキーチェーンのルートとして使用できます。 顧客のルート キーにアクセスできるのは、データ暗号化用の Microsoft オンライン サービス コードによってのみ間接的に行え、Microsoft の従業員が直接アクセスすることはできません。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 暗号化とキー管理に関連するコントロールの検証については、次の表を参照してください。

### <a name="azure-and-dynamics-365"></a>Azure と Dynamics 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: 暗号化コントロール <br> A.18.1.5: 暗号化コントロール | 2020 年 12 月 2 日 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: 暗号化コントロール <br> A.18.1.5: 暗号化コントロール | 2020 年 12 月 2 日 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: パブリック データ伝送ネットワーク経由で送信される PII の暗号化 | 2020 年 12 月 2 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | DS-1: 暗号化証明書とキーのセキュリティで保護されたストレージ <br> DS-2: 顧客データが転送中に暗号化される <br> DS-3: 転送中に暗号化された Azure コンポーネントの内部通信 <br> DS-4: 暗号化の制御と手順 | 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SC-8: 伝送の機密性と整合性 <br> SC-13: 暗号化の使用 <br> SC-28: 残りの情報の保護 <br>  | 2020 年 9 月 24 日 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: 暗号化コントロール <br> A.18.1.5: 暗号化コントロール | 2021 年 4 月 20 日 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: パブリック データ伝送ネットワーク経由で送信される PII の暗号化 | 2021 年 4 月 20 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: 転送中のデータ暗号化 <br> CA-54: 保存時のデータ暗号化 <br> CA-62: 顧客キーメールボックスの暗号化 <br> CA-63: 顧客キー データの削除 <br> CA-64: 顧客キー | 2020 年 12 月 24 日 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: 顧客の暗号化キー <br> CUEC-17: 顧客キー コンテナー <br>  CUEC-18: 顧客キーのローテーション| 2020 年 12 月 24 日 |
