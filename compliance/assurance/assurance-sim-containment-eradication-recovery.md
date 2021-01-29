---
title: 'Microsoft 365 セキュリティ インシデント管理: 格納、復旧、回復'
description: この記事では、Microsoft 365 のセキュリティ インシデント管理の格納、復旧、および回復プロセスの概要について説明します。
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
ms.openlocfilehash: 702735ed2ba35a4f3b0a02123f0c58b5fb4d397e
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037605"
---
# <a name="microsoft-365-security-incident-management-containment-eradication-and-recovery"></a>Microsoft 365 セキュリティ インシデント管理: 格納、復旧、回復

Microsoft 365 セキュリティ対応チーム、サービス チーム、その他によって実行された分析に基づいて、セキュリティ インシデントの影響を最小限に抑えるための適切な格納および復旧計画を作成します。 適切なサービス チームは、Microsoft 365 セキュリティ対応チームのサポートを受けて、そのプランを実稼働環境で適用します。

## <a name="containment"></a>コンテインメント

セキュリティ インシデントを検出した後、攻撃者が多くのリソースにアクセスしたり、より多くの損害を与える前に侵入を含めすることが重要です。 セキュリティ インシデント対応手順の主な目的は、お客様やデータ、または Microsoft のシステム、サービス、アプリケーションへの影響を制限することです。

## <a name="eradication"></a>根絶

根絶は、高い信頼性を有するセキュリティ インシデントの根本原因を解消するプロセスです。 目標は次の 2 つあります。

- 環境から敵対者を完全に削除する
- を使用して、攻撃者が環境に再入できる可能性がある脆弱性 (既知の場合) を軽減します。

インシデントの性質、セキュリティ インシデントの範囲、侵入の深さ、および可能な反言に応じて、Microsoft 365 セキュリティ対応チームは、サービス チームが採用する方法を推奨します。 これらの取り組み手順によってビジネスに及ぼす可能性のある影響を考慮し、これらの決定は、エグゼクティブ インシデント マネージャーからの詳細な分析と承認の後 (必要に応じて) サービス チームと Microsoft 365 セキュリティ対応チームによって行います。

## <a name="recovery"></a>回復

対応チームが、敵対者が環境から排除され、既知の脆弱なパスはすべて排除されたという妥当なレベルの信頼を得たので、個々のサービス チームは、サービスを既知の良好な構成に戻す復元手順を開始します。 これらの復元手順は、Microsoft 365 セキュリティ対応チームと相談する必要があります。 このアクティビティには、サービスの最新の既知の良好な状態の特定、バックアップからこの状態への復元、復元された状態での脆弱な攻撃パスの検査などが含まれます。Microsoft 365 セキュリティ対応チームは、サービス チームと相談して、環境に最適な回復計画を決定します。

回復の重要な側面は、回復計画が正常に実行され、環境に違反の兆候が存在しないか検証するために強化された監視と制御を行う必要があります。

## <a name="customer-notification-of-security-incident"></a>セキュリティ インシデントに関する顧客通知

Microsoft がセキュリティ インシデントが発生したと判断した場合は、期限が近づいて、契約要件およびコンプライアンス要件内で Microsoft が合意した範囲内でお客様に通知します。 影響を受けるすべてのテナントを特定した後、Microsoft 365 カスタマー エクスペリエンス (CxP) コミュニケーション チームは影響を受けるテナントに適用される可能性のある関連規制を特定します。 Microsoft 365 CxP コミュニケーション チームは、該当する規制で定義されている適切な通信チャネルを使用して、適切なテナントの連絡先に通知します。

通知には、インシデントの説明、顧客データへの影響 (お持ちである場合)、Microsoft が実行したアクション、問題を解決して繰り返し発生を防止するためにお客様が実行する推奨アクションなど、インシデントに関する詳細情報が含まれます。 通知は、Microsoft 365 テナントの指定された管理者に配信されます。 通知を確実に受信するには、管理者がテナント プロファイルに正確な連絡先情報を提供し、維持する必要があります。 また、インシデントの性質に応じて、Microsoft 365 サービス正常性ダッシュボードを使用して通知することもできます[。](http://status.yammer.com/)

## <a name="related-articles"></a>関連記事

- [Microsoft 365 セキュリティ インシデント管理](assurance-security-incident-management.md)
- [Microsoft 365 セキュリティ インシデント管理の準備](assurance-sim-preparation.md)
- [Microsoft 365 セキュリティ インシデント管理の検出と分析](assurance-sim-detection-analysis.md)
- [Microsoft 365 セキュリティ インシデント管理インシデント後のアクティビティ](assurance-sim-post-incident-activity.md)
