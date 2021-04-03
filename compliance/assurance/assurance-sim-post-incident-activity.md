---
title: 'Microsoft 365 セキュリティ インシデント管理: インシデント後のアクティビティ'
description: この記事では、Microsoft 365 のセキュリティ インシデント管理インシデント後のアクティビティ プロセスの概要について説明します。
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
ms.openlocfilehash: 4ebd31c16f8abb3eddd6ed924a045d88597aba40
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496712"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a>Microsoft 365 セキュリティ インシデント管理: インシデント後のアクティビティ

## <a name="postmortem"></a>事後分析

一部のセキュリティ インシデント、特に顧客に影響を与えるインシデント、またはデータ漏洩の可能性があるインシデントは、完全なインシデントの事後分析の対象となります。 Microsoft 365 セキュリティ対応チームは、セキュリティ インシデント対応に関わるすべての関係者と詳細な事後分析を行います。

- インシデントの原因となる一連のイベントを文書化する
- 侵害に関与するアクター (既知の場合) を含む証拠によってサポートされているインシデントの技術的な概要を作成します。 この概要には、応答の実行方法と他の主要なテイクアウトが含まれます。
- 技術的な経過、手続き上の失敗、手動エラー、プロセスの欠陥、通信の不具合、および/またはセキュリティ インシデント対応中に特定された未知の攻撃ベクトルを特定します。

事後分析は、Microsoft 365 エンジニアリング開発サイクルで新しい優先順位を設定することで、Microsoft 365 サービスの改善、運用プロセス、およびドキュメントに直接影響します。

## <a name="documentation"></a>ドキュメント

死後のプロセスにおける主要な技術的な調査結果はすべて、バグや開発変更要求の形でレポートとサービスへの投資または修正に取り込まれています。 これらの結果は、適切なエンジニアリング チームとフォローアップされます。 プロセスの失敗や組織間の問題については、Microsoft 365 セキュリティ対応チームのデータベースに問題が文書化され、それに対処するために適切なグループがフォローアップされます。

## <a name="process-improvement"></a>プロセスの改善

Microsoft 365 のセキュリティ インシデントに対応するには、Microsoft 内の異なる組織、および法執行機関などの適切な外部組織にまたがって複数のグループとの連携が必要です。 十分性と完全性の両方について、セキュリティ インシデントが発生した後の対応を評価する必要があります。 特定された改善や変更に関して、Microsoft 365 セキュリティ対応チームは、適切なチームや関係者と協議して提案を評価し、適切な場合は標準の運用手順に組み込む必要があります。 セキュリティ インシデント対応または死後のアクティビティ中に特定された必要な変更、バグ、またはサービスの改善はすべて、内部の Microsoft 365 エンジニアリング データベースに記録および追跡されます。 潜在的なバグや機能はすべて、適切な所有者に割り当てられます。 Microsoft 365 セキュリティ対応チームは、問題が解決されるまですべてのエントリを確認します。

## <a name="related-articles"></a>関連記事

- [Microsoft 365 のセキュリティ インシデント管理](assurance-security-incident-management.md)
- [Microsoft 365 セキュリティ インシデント管理の準備](assurance-sim-preparation.md)
- [Microsoft 365 セキュリティ インシデント管理の検出と分析](assurance-sim-detection-analysis.md)
- [Microsoft 365 セキュリティ インシデント管理の格納、根絶、および回復](assurance-sim-containment-eradication-recovery.md)
