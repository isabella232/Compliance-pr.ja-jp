---
title: クラウド コンピューティング コンプライアンス コントロール カタログ (C5)
description: Azure、Azure Government、Azure Germany によるクラウド コンピューティング コンプライアンス コントロール カタログ (C5) への準拠証明の方法について説明します。
keywords: Microsoft 365、コンプライアンス、サービス
ms.localizationpriority: high
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 0399a959bce2d15bc856bad25aca29f831193efc
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947834"
---
# <a name="cloud-computing-compliance-controls-catalog-c5"></a>クラウド コンピューティング コンプライアンス コントロール カタログ (C5)

## <a name="c5-overview"></a>C5 の概要

2016 年、ドイツ連邦情報セキュリティ庁 (Bundesamt für Sicherheit in der Informationstechnik、BSI) は、クラウド コンピューティング コンプライアンス コントロール カタログ (C5) を策定しました。 C5 とは、ドイツ政府機関とその関連団体がパブリック クラウド ソリューションを導入する際の必要最低限のクラウド セキュリティを定めた監査標準です。 C5 は、民間部門でも導入が進んでいます。

C5 カタログの各要件は、クラウド サービス プロバイダーの認証に必要な一貫性のあるセキュリティ フレームワークを確立し、プロバイダーのお客様に対して安全なデータ管理を保証することが目的です。

C5 は、ISO/IEC 27001:2013、クラウド セキュリティ アライアンス クラウド コントロール マトリックス 3.0.1 などの国際的に認められた IT セキュリティ基準と、BSI 独自の IT-Grundschutz カタログに基づいています。 C5 カタログは、17 分野 (例: 情報セキュリティと物理的セキュリティに携わる組織)、114 の要件で構成されています。すべてのクラウド サービス プロバイダーの根幹となるセキュリティ要件もあれば、機密性の高いデータと高可用性を必要とする状況を処理するための補足要件もあります。

BSI は透明性も重視しています。 監査の際、クラウド プロバイダーは、詳細なシステム記述を示すとともに、管轄区域やデータ処理の場所などの環境パラメーター、サービスのプロビジョニング方法、クラウド サービスに授与された他の認定、クラウド プロバイダーの公的機関への開示義務情報などを開示する必要があります。 これにより、クラウドの潜在的なお客様は、データ保護などの法的要件の順守、会社のポリシー、産業スパイの脅威への対応能力といった必要な要件をクラウド サービスが満たしているかどうかを判断できます。

## <a name="microsoft-and-c5"></a>Microsoft と C5

Microsoft クラウド サービスでは、少なくとも年に 1 回、SOC 2 (AT Section 101) 標準に照らした監査が実施されます。 BSI によると、C5 監査は SOC 2 監査と合わせて行うことができ、重複するコントロールについては、システム記述と監査結果の一部を再利用することができます。 Microsoft Azure、Azure Government、Azure Germany は、独立監査人によって実施された各種監査評価 (C5、SOC 2 Type 2、CSA STAR 証明) に基づく統合レポートを保持しており、このレポートによって C5 への準拠証明を示すことができます。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>対象となる Microsoft のクラウド プラットフォームとサービス

- [Azure、Azure Government、Azure Germany](https://go.microsoft.com/fwlink/p/?linkid=2051569)
- Office 365 Germany

## <a name="audits-reports-and-certificates"></a>監査、レポート、証明書

- [Azure、Azure Government、および Azure Germany SOC 2 タイプ II レポート.pdf](https://go.microsoft.com/fwlink/p/?linkid=2093520)

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**Microsoft の C5 コンプライアンスを私の組織の C5 準拠証明に利用できますか?**

はい。 C5 を必要とするプログラムまたはイニシアチブの基盤として、Microsoft Cloud サービスの準拠証明を使用できます。 ただし、これらのサービス以外、またはその上に構築されるコンポーネントについては、C5 準拠証明をお客様ご自身で取得する必要があります。

**C5 と IT-Grundschutz カタログの違いは何ですか?**

IT-Grundschutz は、IT システムのセキュリティ対策の決定と実装に役立つ具体的な手法を提供するものであり、C5 標準の基盤となる要素の 1 つです。 C5 は、クラウド サービス プロバイダーの一連の監査標準を提供するものですが、実装の詳細はクラウド サービス プロバイダーに任されています。

**Microsoft Cloud Germany とは何ですか?**

Microsoft Cloud Germany は、ドイツに物理的拠点を置き、ドイツのプライバシー法の要件に準拠しています。この法律は、他国への個人データの移転を制限し、国内法に違反する可能性のある他の管轄区域当局によるアクセスからデータを保護します。 Azure Germany は、ドイツをデータ所在地とするドイツのデータセンターから Azure サービスを提供します。ドイツ法に準拠した固有のデータ トラスティ モデルによって、データのアクセスと制御に厳格に対処します。

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft コンプライアンス マネージャーを使用してリスクを評価する

[Microsoft コンプライアンス マネージャー](/microsoft-365/compliance/compliance-manager)は、[ Microsoft 365 コンプライアンス センター](/microsoft-365/compliance/microsoft-365-compliance-center)の機能で、組織のコンプライアンスに対する姿勢を把握し、リスクを軽減するための処置を実行できるようにします。 コンプライアンスマネージャーには、この規制の評価を構築するためのプレミアム テンプレートが用意されています。 コンプライアンスマネージャーの **評価テンプレート** ページでテンプレートを見つけます。 [コンプライアンスマネージャーで評価をする方法](/microsoft-365/compliance/compliance-manager-assessments)について説明します。

## <a name="resources"></a>リソース

- クラウド コンピューティング コンプライアンス コントロール カタログ (C5) ([英語](https://www.bsi.bund.de/EN/Topics/CloudComputing/Compliance_Criteria_Catalogue/Compliance_Criteria_Catalogue_node.html)) ([ドイツ](https://www.bsi.bund.de/DE/Themen/DigitaleGesellschaft/CloudComputing/Kriterienkatalog/Kriterienkatalog_node.html))
- クラウド コンピューティング プロバイダーのセキュリティに関する推奨事項 ([英語](https://www.bsi.bund.de/EN/Topics/CloudComputing/Secure_use_of_cloud_services/Secure_use_cloud_services_node.html)) ([ドイツ語](https://www.bsi.bund.de/DE/Themen/DigitaleGesellschaft/CloudComputing/Sichere_Nutzung_Cloud/Sichere_Nutzung_Cloud_node.html))
- [コンプライアンス レポート: C5- und SOC-Testate Azure Deutschland](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=df100ae1-baf9-4785-8a6d-864c0bc5c308&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_SOC%20%2F%20SSAE%2016%20Reports)
- Microsoft Azure Germany の [IT-Grundschutz コンプライアンス ワークブック](https://gallery.technet.microsoft.com/Azure-Germany-IT-fca4afd7)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)
