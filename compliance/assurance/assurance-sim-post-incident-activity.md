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
ms.openlocfilehash: 66c25503ac574de512f5201981112a0e54714968
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040350"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a>Microsoft 365 セキュリティ インシデント管理: インシデント後のアクティビティ

## <a name="postmortem"></a>Postmortem

セキュリティ インシデントの中には、特にお客様が影響を与えるインシデントやデータ侵害を引き起しているインシデントの中には、インシデントの完全な事後分析の対象となるものがあります。 Microsoft 365 セキュリティ対応チームは、セキュリティ インシデント対応に関わるすべての関係者と詳細な事後分析を行い、次の処理を行います。

- インシデントを発生した一連のイベントを文書化する
- 違反に関与するアクターを含む証拠によってサポートされているインシデントの技術的な概要を作成します (既知の場合)。 この概要には、応答の実行方法と他の重要な項目が含まれます。
- 技術的な経過、手順の失敗、手動エラー、プロセスの欠陥、通信障害、セキュリティ インシデント対応中に特定された未知の攻撃ベクトルを特定します。

事後分析は、Microsoft 365 エンジニアリング開発サイクルで新しい優先順位を設定することで、Microsoft 365 サービスの改善、運用プロセス、およびドキュメントに直接影響します。

## <a name="documentation"></a>ドキュメント

事後分析プロセスにおける主要な技術的な調査結果はすべて、バグや開発変更要求の形でレポートとサービスへの投資または修正に取り込まれています。 これらの結果は、適切なエンジニアリング チームとフォローアップされます。 プロセスの失敗と組織間の問題については、Microsoft 365 セキュリティ対応チームのデータベースに問題を文書化し、対応する適切なグループをフォローアップします。

## <a name="process-improvement"></a>プロセスの改善

Microsoft 365 のセキュリティ インシデントへの対応には、Microsoft 内の異なる組織に分散している複数のグループとの連携や、法執行機関などの適切な外部組織との連携が含まれる場合があります。 十分性と完全性の両方について、セキュリティ インシデントが発生した後の対応を評価する必要があります。 特定された改善や変更に関して、Microsoft 365 セキュリティ対応チームは提案を適切なチームや関係者と相談して評価し、適切な場合は標準業務手順に組み込めます。 セキュリティ インシデント対応または事後活動中に特定された必要な変更、バグ、またはサービスの改善はすべて、内部の Microsoft 365 エンジニアリング データベースに記録および追跡されます。 潜在的なバグや機能はすべて、適切な所有者に割り当てられます。 Microsoft 365 セキュリティ対応チームは、問題が解決されるまですべてのエントリを確認します。

## <a name="related-articles"></a>関連記事

- [Microsoft 365 セキュリティ インシデント管理](assurance-security-incident-management.md)
- [Microsoft 365 セキュリティ インシデント管理の準備](assurance-sim-preparation.md)
- [Microsoft 365 セキュリティ インシデント管理の検出と分析](assurance-sim-detection-analysis.md)
- [Microsoft 365 セキュリティ インシデント管理の格納、強化、および復旧](assurance-sim-containment-eradication-recovery.md)
