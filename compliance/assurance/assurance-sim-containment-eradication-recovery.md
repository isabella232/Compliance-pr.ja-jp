---
title: 'Microsoft 365 セキュリティ インシデント管理: 格納、根絶、および回復'
description: この記事では、Microsoft 365 のセキュリティ インシデント管理の格納、根絶、および回復プロセスの概要について説明します。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 7fff9c1909f0acd076945e3d569b143fe2324c0f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496720"
---
# <a name="microsoft-365-security-incident-management-containment-eradication-and-recovery"></a>Microsoft 365 セキュリティ インシデント管理: 格納、根絶、および回復

Microsoft 365 Security Response チーム、サービス チーム、その他によって実行される分析に基づいて、セキュリティ インシデントの影響を最小限に抑えるための適切な格納および回復計画が開発されています。 適切なサービス チームは、Microsoft 365 セキュリティ対応チームのサポートを受けて、その計画を実稼働環境で適用します。

## <a name="containment"></a>コンテインメント

セキュリティ インシデントを検出した後、敵対者がリソースにアクセスしたり、より多くの損害を与える前に侵入を含めすることが重要です。 セキュリティ インシデント対応手順の主な目的は、顧客またはデータ、または Microsoft システム、サービス、およびアプリケーションへの影響を制限することです。

## <a name="eradication"></a>根絶

根絶は、高い信頼性を有するセキュリティ インシデントの根本原因を解消するプロセスです。 目標は 2 倍です。

- 環境から敵対者を完全に追い出す
- を有効にするか、または攻撃者が環境を再入力できる可能性がある脆弱性 (既知の場合) を軽減します。

インシデントの性質、セキュリティ インシデントの範囲、侵入の深さ、および可能性のある反響に応じて、Microsoft 365 セキュリティ対応チームは、サービス チームが根絶技術を採用することを推奨します。 これらの根絶手順によって引き起こされる可能性のあるビジネス上の影響を考慮すると、これらの決定は、サービス チームと Microsoft 365 セキュリティ対応チームが、エグゼクティブ インシデント マネージャー (必要に応じて) から詳細な分析と承認を受けた後に行います。

## <a name="recovery"></a>回復

応答チームが、敵対者が環境から追い出され、既知のすべての脆弱なパスが排除されたという妥当なレベルの信頼を得たので、個々のサービス チームは、サービスを既知の良好な構成に戻す復元手順を開始します。 これらの復元手順は、Microsoft 365 セキュリティ対応チームと協議します。 このアクティビティには、サービスの最後の既知の良好な状態の特定、バックアップからこの状態への復元、復元された状態での脆弱な攻撃パスの検査などが含まれます。Microsoft 365 セキュリティ対応チームは、サービス チームと協議して、環境に最適な回復計画を決定します。

回復の重要な側面は、回復計画が正常に実行され、環境に侵害の兆候が存在しないか検証するために、警戒と制御を強化する必要があります。

## <a name="customer-notification-of-security-incident"></a>セキュリティ インシデントの顧客通知

Microsoft がセキュリティ インシデントが発生したと判断した場合、弊社は、契約要件およびコンプライアンス要件の範囲内で、遅延が発生した場合に通知します。 影響を受けるすべてのテナントを特定した後、Microsoft 365 Customer Experience (CxP) Communications チームは、影響を受けるテナントに適用される可能性のある関連する規制を特定します。 Microsoft 365 CxP Communications チームは、該当する規制で定義されている適切な通信チャネルを使用して、適切なテナント連絡先に通知します。

通知には、インシデントの説明、顧客データへの影響、Microsoft が実行したアクション、および/または問題の解決と再発防止のためにお客様が実行する推奨されるアクションなど、インシデントに関する詳細情報が含まれます。 通知は、Microsoft 365 テナントの指定された管理者に配信されます。 通知を確実に受信するには、管理者がテナント プロファイルに正確な連絡先情報を提供し、維持する必要があります。 さらに、インシデントの性質に応じて、Microsoft 365 サービス正常性ダッシュボードを介して顧客に通知することもできます[。](http://status.yammer.com/)

## <a name="related-articles"></a>関連記事

- [Microsoft 365 のセキュリティ インシデント管理](assurance-security-incident-management.md)
- [Microsoft 365 セキュリティ インシデント管理の準備](assurance-sim-preparation.md)
- [Microsoft 365 セキュリティ インシデント管理の検出と分析](assurance-sim-detection-analysis.md)
- [Microsoft 365 セキュリティ インシデント管理インシデント後のアクティビティ](assurance-sim-post-incident-activity.md)
