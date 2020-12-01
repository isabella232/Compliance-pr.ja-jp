---
title: 暗号化とキー管理の概要
description: Microsoft 365 での暗号化とキー管理について説明します。
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
ms.openlocfilehash: 96a3871657dc1e6021949ca9fc2376df382fe15b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508199"
---
# <a name="encryption-and-key-management-overview"></a>暗号化とキー管理の概要

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>お客様のコンテンツを保護する際に、暗号化はどのような役割を果たしますか?

ほとんどの Microsoft business cloud services はマルチテナントです。つまり、お客様のコンテンツは他のお客様と同じ物理ハードウェアに格納されることがあります。 お客様のコンテンツの機密性を保護するために、Microsoft 365 は、すべてのデータを保存中に暗号化し、最も強力で最も安全な暗号化プロトコルを使用して転送中に暗号化します。

暗号化は、強力なアクセス制御に代わるものではありません。 Microsoft 365 のアクセス制御ポリシーゼロによるアクセス (ZSA) は、Microsoft の従業員による権限のないアクセスからお客様のコンテンツを保護します。 暗号化は、保存場所に関係なく顧客のコンテンツの機密性を保護することにより、アクセス制御を補完し、Microsoft 365 システム間、または Microsoft 365 とお客様との間で転送中にコンテンツを閲覧することを防止します。

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>Microsoft 365 は、保存データを暗号化する方法を教えてください。

Microsoft 365 のすべてのお客様のコンテンツは、1つまたは複数の形式の暗号化によって保護されています。 Microsoft サーバーは、BitLocker を使用して、ボリュームレベルで顧客コンテンツを含むディスクドライブを暗号化します。 BitLocker によって提供される暗号化は、ユーザーのコンテンツを含むディスクへの不正な物理的なアクセスにつながる可能性がある他のプロセスやコントロールで lapses が発生した場合にお客様のコンテンツを保護します (たとえば、アクセス制御やハードウェアのリサイクル)

Exchange Online、Microsoft Teams、SharePoint Online、および OneDrive for Business では、アプリケーション層でサービス暗号化を使用して、顧客コンテンツを暗号化します。 サービス暗号化は、強力な暗号化保護の上に権限の保護機能と管理機能を提供します。 また、Windows オペレーティングシステムと、これらのオペレーティングシステムによって保存または処理されるお客様のデータを分離することもできます。

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>Microsoft 365 は、送信データを暗号化する方法を教えてください。

Microsoft 365 製品とサービスでは、TLS などの強力なトランスポートプロトコルを使用して、許可されていない第三者がネットワーク上を移動している間に顧客データを傍受できないようにします。 転送中のデータの例としては、配信処理中のメールメッセージ、オンライン会議で行われた会話、データセンター間でレプリケートされるファイルなどがあります。

Microsoft 365 では、ユーザーのデバイスが Microsoft サーバーと通信している場合、または Microsoft サーバーが別のサーバーと通信している場合は、データは「転送中」と見なされます。 Exchange Online、SharePoint Online、Microsoft Teams、および Office Online はすべて TLS を使用して、転送中のデータを機密に保つことができます。

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>Microsoft 365 は、暗号化に使用されるキーをどのように管理していますか?

強力な暗号化は、データの暗号化に使用されるキーと同じようにセキュリティで保護されています。 Microsoft では、独自のセキュリティ証明書を使用して、送信データの TLS 接続を暗号化しています。 データを保存する場合、BitLocker で保護されたボリュームは、ボリュームマスターキーで暗号化された完全なボリューム暗号化キーを使用して暗号化されます。これは、サーバーのトラステッドプラットフォームモジュール (TPM) にバインドされます。 BitLocker は FIPS に準拠したアルゴリズムを使用して、暗号化キーが暗号化されずに保存または送信されることがないようにします。

サービス暗号化では、Exchange Online、Microsoft Teams、SharePoint Online、OneDrive for business に保存された、お客様のデータに対する暗号化の層が追加されています。 サービスの暗号化では、暗号化キーの管理に関して、Microsoft が管理するキーまたは顧客キーという2つのオプションが提供されます。 Microsoft 管理キーを使用する場合、Microsoft 365 サービスは、サービスの暗号化に使用されるルートキーを自動的に生成し、安全に保存します。

独自のルート暗号化キーを制御する要件を持つお客様は、お客様のキーを使用してサービス暗号化を利用できます。 顧客キーを使用すると、オンプレミスのハードウェアサービスモジュール (HSM) または Azure Key Vault (AKV) を使用して、独自の暗号化キーを生成できます。 顧客のルートキーは、ユーザーのメールボックスのデータまたはファイルを暗号化する keychains の1つのルートとして使用できる AKV に格納されます。 顧客のルートキーには、データ暗号化用の Microsoft 365 サービスコードによる間接的なアクセスのみが可能で、Microsoft の従業員が直接アクセスすることはできません。

## <a name="related-external-regulations--certifications"></a>関連する外部規制 & 証明書

Microsoft のオンラインサービスは、社外の規制と証明書に準拠するために定期的に監査されます。 暗号化とキー管理に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: 伝送の機密性と整合性 <br> SC-13: 暗号化の使用 <br> SC-28: rest での情報の保護 <br>  | 2020年9月24日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | -10.1: 暗号化コントロール <br> 18.1.5: 暗号化コントロール | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | -10.1: 暗号化コントロール <br> 18.1.5: 暗号化コントロール | 2020 月 2 月 22 日 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 11.6: パブリックデータ転送ネットワーク経由で送信される PII の暗号化 | 2020 月 2 月 22 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-44: データ転送暗号化 <br> CA-54: データインレスト暗号化 <br> CA-62: 顧客キーメールボックスの暗号化 <br> CA-63: 顧客キーデータの削除 <br> CA-64: 顧客キー | 2019 年 9 月 30 日 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-16: 顧客の暗号化キー <br> CUEC-17: カスタマーキーヴォールト <br>  CUEC-18: 顧客キーの回転| 2019 年 9 月 30 日 |
