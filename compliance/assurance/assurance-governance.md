---
title: ガバナンスの概要
description: Microsoft 365 のガバナンスについて
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
ms.openlocfilehash: fc8fc40badb6898bc5cc6cd4792a8c6e69df2875
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507839"
---
# <a name="governance-overview"></a>ガバナンスの概要

## <a name="how-does-microsoft-provide-effective-security-governance-across-the-enterprise"></a>Microsoft は、どのようにして企業全体で効果的なセキュリティガバナンスを提供していますか?

Microsoft では、Microsoft の情報システムと顧客を保護するために、効果的なセキュリティポリシーを企業全体で一貫して実装する必要があることを認識しています。 セキュリティポリシーは、ビジネス機能と情報システムのバリエーションを考慮して、普遍的に適用できるようにすることも必要です。 これらの要件を満たすために、Microsoft は、Microsoft Policy Framework の一部として包括的なセキュリティガバナンスプログラムを実装しています。 セキュリティガバナンスは、Microsoft セキュリティポリシー (MSP) に含まれます。

MSP は、microsoft のセキュリティポリシー、標準、および要件を構成して、すべての Microsoft のエンジニアリンググループとビジネスユニットに実装できるようにします。 個々のビジネス単位は、Microsoft セキュリティポリシーの特定の実装を担当します。 たとえば、microsoft 365 は、Microsoft 365 Information Security Policy および関連する Microsoft 365 Control フレームワークのセキュリティ実装を文書にします。 これらのセキュリティ実装は、MSP の目標と目的に沿っています。

Microsoft のセキュリティガバナンスプログラムは、によって通知され、さまざまな規制およびコンプライアンスフレームワークと連携しています。 セキュリティ要件は、新しいテクノロジ、規制およびコンプライアンスの要件、およびセキュリティの脅威に対して常に継続的に進化しています。 そのため、Microsoft は、Microsoft のシステムと顧客を保護し、コミットメントを満たし、顧客の信頼を維持するためのセキュリティポリシーとサポートドキュメントを定期的に更新します。

## <a name="how-does-microsoft-365-implement-the-microsoft-security-policy-msp"></a>Microsoft 365 は Microsoft セキュリティポリシー (MSP) をどのように実装していますか?

Microsoft 365 は、Microsoft 365 情報セキュリティ ポリシーでセキュリティの実装を文書化しています。 このポリシーは、Microsoft セキュリティ ポリシーに準拠し、データの収集、処理、保守、使用、共有、配布、および廃棄に関連するすべての Microsoft 365 環境とすべてのリソースを含む Microsoft 365 情報システムを管理します。

Microsoft 365 情報システムには、Microsoft 365 情報セキュリティ ポリシーで管理される次のコンポーネントが含まれています。

- インフラストラクチャ: Microsoft 36 5システムの物理コンポーネントとハードウェアコンポーネント (設備、機器、ネットワーク)
- ソフトウェア: Microsoft 365 システムのプログラムとオペレーティング ソフトウェア (システム、アプリケーション、ユーティリティ)
- ユーザー: Microsoft 365 システムの操作と使用に関与する担当者 (開発者、オペレーター、ユーザー、マネージャー)
- 手順: Microsoft 365 システムの操作に関連するプログラムされた手順と手動の手順
- データ: Microsoft 365 システムによって生成、収集、処理された情報 (トランザクション ストリーム、ファイル、データベース、テーブル)

Microsoft 365 情報セキュリティ ポリシーは、Microsoft 365 コントロール フレームワークによって補足されます。 Microsoft 365 Control Framework は、すべての Microsoft 365 サービスおよび情報システムコンポーネントの最小セキュリティ要件を詳細に説明しています。 また、各コントロールの背後にある法律および企業の要件も参照します。 フレームワークには、サービス チームによる効果的な制御の実装を確実にするための制御アクティビティ名、説明、およびガイダンスが含まれています。 Microsoft 365 は、コントロールフレームワークを使用して、内部および外部のレポート作成のためのコントロールの実装を追跡します。

## <a name="how-does-microsoft-365-limit-and-track-exceptions-to-established-policies"></a>Microsoft 365 では、確立されたポリシーの例外をどのように制限し、追跡していますか?

Microsoft 365 情報セキュリティ ポリシーの例外はすべて、正当なビジネス上の正当性があり、Microsoft 365 内の適切なガバナンス エンティティによって承認される必要があります。 例外には、サービス チーム管理の承認も必要であり、Microsoft 365 リスク管理ツールに文書化されている必要があります。 例外の範囲とそれが表す潜在的なリスクによっては、例外の承認を企業の副社長以上から取得する必要がある場合があります。 例外は、Microsoft 365 リスク管理ツールで追跡され、関連性を維持するためにレビューおよび承認されます。

## <a name="related-external-regulations--certifications"></a>関連する外部規制 & 証明書

Microsoft のオンラインサービスは、社外の規制と証明書に準拠するために定期的に監査されます。 ガバナンスに関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CA-2: セキュリティ評価 <br> PL-2: システムセキュリティ計画 | 2020年9月24日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 18.1: 法律および契約の要件に準拠する | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 18.1: 法律および契約の要件に準拠する | 2020 月 2 月 22 日 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | (2.1: パブリッククラウド PII プロセッサの目的 | 2018年11月10日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-11: ポリシーフレームワークの更新 <br> CA-12: サービスレベル契約 (Sla) <br> CA-17: Microsoft セキュリティポリシー <br> CA-25: framework の更新を制御する | 2019 年 9 月 30 日 |
