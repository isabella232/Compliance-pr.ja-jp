---
title: Microsoft 365 の分離コントロール
description: 分離コントロールの詳細については、Microsoft 365
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
ms.openlocfilehash: 2278a2475887e93733ce32b82a1d7d0b15cce91a1f1e70dbe72a6469bdd3e0b7
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290604"
---
# <a name="microsoft-365-isolation-controls"></a>Microsoft 365 の分離コントロール

Microsoft は継続的に、Microsoft 365 のマルチテナント アーキテクチャがエンタープライズ レベルのセキュリティ、機密性、プライバシー、整合性、ローカル、国際、可用性の標準をサポートします[。](https://www.microsoft.com/trust-center/compliance/compliance-overview) Microsoft が提供するサービスの規模と範囲により、人間の重要なやり取りを使用してMicrosoft 365を管理することは困難で経済的ではありません。 Microsoft 365サービスは、グローバルに分散されたデータ センターを通じて提供され、それぞれが高度に自動化され、人間のタッチや顧客コンテンツへのアクセスを必要とする操作が少ない。 弊社のスタッフは、自動化されたツールと高度に安全なリモート アクセスを使用して、これらのサービスとデータ センターをサポートしています。

Microsoft 365は、重要なビジネス機能を提供し、ビジネス エクスペリエンス全体に貢献する複数のサービスMicrosoft 365されています。 これらの各サービスは、自己格納型であり、互いに統合するように設計されています。 Microsoft 365は、次の原則に従って設計されています。

- サービス指向のアーキテクチャ: 適切に定義されたビジネス機能を提供する相互運用可能なサービスの形式でソフトウェアを設計および開発します。
- [運用上](https://www.microsoft.com/securityengineering/osa)のセキュリティ保証: [Microsoft](https://www.microsoft.com/sdl/default.aspx)セキュリティ開発ライフサイクル [、Microsoft](https://www.microsoft.com/msrc)セキュリティ対応センター、サイバーセキュリティ脅威の状況に対する深い認識など、Microsoft 固有のさまざまな機能によって得られる知識を組み込んだフレームワーク。

Microsoft 365サービスは相互に運用されますが、相互に独立した自律サービスとして展開および運用できるよう設計および実装されています。 Microsoft は、組織の資産の無許可または意図しない変更または誤用の機会を減らすMicrosoft 365の義務と責任領域を分離します。 Microsoft 365チームは、包括的な役割ベースのアクセス制御メカニズムの一部として役割を定義しています。

## <a name="tenant-isolation"></a>テナントの分離

クラウド コンピューティングの主な利点の 1 つは、多数の顧客間で同時に共有される共通のインフラストラクチャの概念で、規模の経済性につながる点です。 Microsoft は、クラウド サービスのマルチテナント アーキテクチャによって、エンタープライズレベルのセキュリティ、機密性、プライバシー、完全性、可用性の基準をサポートするため、継続的に取り組んでいます。

Microsoft クラウド サービスは、すべてのテナントが他のすべてのテナントに対して敵対的である可能性があるという前提で設計され、あるテナントのアクションが別のテナントのセキュリティまたはサービスに影響を与え、または別のテナントのコンテンツにアクセスするのを防ぐためのセキュリティ対策を実装しました。

マルチテナント環境でテナントの分離を維持する 2 つの主な目標は次のとおりです。

- テナント間の顧客コンテンツの漏洩または不正アクセスの防止。そして
- あるテナントのアクションが別のテナントのサービスに悪影響を及ぼすのを防ぐ

Microsoft 365 では、Microsoft 365 サービスやアプリケーションを侵害したり、他のテナントや Microsoft 365 システム自体の情報に対する不正アクセスを防止したりするために、Microsoft 365 全体で複数の保護が実装されています。

- 各テナント内の顧客コンテンツの論理的な分離は、Microsoft 365アクセス制御とロールベースAzure Active Directoryによって実現されます。
- SharePointOnline は、ストレージ レベルでのデータ分離メカニズムを提供します。
- Microsoft では、厳密な物理的セキュリティ、バックグラウンド スクリーニング、多層暗号化戦略を使用して、顧客コンテンツの機密性と整合性を保護します。 すべてのMicrosoft 365は生体認証アクセス制御を備え、ほとんどの場合、物理的なアクセスを得るために手のひらの印刷が必要です。 さらに、米国に拠点を置く Microsoft のすべての従業員は、採用プロセスの一環として標準のバックグラウンド チェックを正常に完了する必要があります。 管理アクセスに使用されるコントロールの詳細については、「Microsoft 365アクセス制御」を[参照Microsoft 365してください](assurance-administrative-access-controls-overview.md)。
- Microsoft 365は、BitLocker、ファイルごとの暗号化、トランスポート層セキュリティ (TLS)、インターネット プロトコル セキュリティ (IPsec) などの、保存中および転送中の顧客コンテンツを暗号化するサービス側テクノロジを使用します。 暗号化の詳細については、「Microsoft 365 のデータ暗号化テクノロジ」[を参照Microsoft 365。](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)

上記の保護を組み合わせて、物理的な分離によって提供されるのと同等の脅威保護と軽減策を提供する堅牢な論理分離制御を提供します。

## <a name="resources"></a>リソース

- [分離とアクセス制御 (Azure Active Directory](/microsoft-365/enterprise/microsoft-365-isolation-in-azure-active-directory)
- [テナント境界の監視とテスト](assurance-monitoring-and-testing.md)
- [分離とアクセス制御 (Microsoft 365](/microsoft-365/enterprise/microsoft-365-isolation-in-microsoft-365)
