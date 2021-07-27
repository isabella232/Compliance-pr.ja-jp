---
title: セキュリティの開発と運用の概要
description: セキュリティの開発と運用について詳しくは、Microsoft 365
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
ms.openlocfilehash: 7a706cda887c0c2675841648ef8541ffbb872884
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573695"
---
# <a name="security-development-and-operations-overview"></a>セキュリティの開発と運用の概要

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Microsoft はセキュリティで保護された開発プラクティスを実装する方法を説明します。

Microsoft のセキュリティ開発ライフサイクル (SDL) は、セキュリティ保護されたソフトウェアの開発と運用に重点を置くセキュリティ 保証プロセスです。 SDL には、Microsoft の開発者やエンジニアにとって、より多くの測定可能なセキュリティ要件が用意されています。 Microsoft は、お客様の製品とサービスの脆弱性の数と重大度を削減します。 すべての Microsoft ソフトウェア開発チームは、SDL の要件に従う必要があります。また、変化する脅威の状況、業界のベスト プラクティス、コンプライアンスに関する規制基準を反映するように SDL を継続的に更新します。

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Microsoft の SDL は、アプリケーションのセキュリティを向上させる方法を説明します。

Microsoft の SDL プロセスは、要件、設計、実装、検証、およびリリースの 5 つのフェーズで考え得る。 まず、セキュリティを念頭に置いてソフトウェア要件を定義します。 これを行うには、アプリケーションが実行する必要があるセキュリティ関連の質問を確認します。 アプリケーションで機密データを収集する必要がありますか? アプリケーションは機密情報や重要なタスクを実行しますか? アプリケーションは、信頼できない発行元からの入力を受け入れる必要がありますか?

関連するセキュリティ要件が特定されると、これらの要件を満たすセキュリティ機能が組み込まれるようにソフトウェアを設計します。 開発者は SDL と設計要件をコードに実装し、手動のコード レビュー、自動化されたセキュリティ ツール、および侵入テストで検証します。 最後に、コードをリリースする前に、新しい機能と重要な変更は最終的なセキュリティとプライバシーのレビューを受け、すべての要件が満たされます。

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Microsoft は、一般的な脆弱性のソース コードをテストする方法を説明します。

コード開発やリリース後のセキュリティ要件を実装する開発者をサポートするために、Microsoft では、セキュリティの欠陥や脆弱性についてソース コードを自動的にチェックする、セキュリティで保護された一連の開発ツールを提供しています。 Microsoft は、コンパイラや開発環境など、開発者が使用する承認済みツールの一覧と、Microsoft ビルド パイプライン内で自動的に実行される組み込みのセキュリティ チェックを定義して発行します。 弊社の開発者は、新しいセキュリティ機能を活用するために、承認されたツールの最新バージョンを使用しています。

コードをリリース ブランチにチェックインする前に、SDL には別のレビューアーによる手動のコード レビューが必要です。 コード レビュー担当者は、コーディング エラーを確認し、コード変更が SDL および設計要件を満たしているか、機能およびセキュリティのテストに合格したか、確実に動作するかを確認します。 また、コードの変更が適切に文書化され、意図しない副作用が発生しないことを確認するために、関連するドキュメント、構成、および依存関係を確認します。 レビュー担当者は、コード レビュー中に問題を発見した場合、提出者に、提案された変更と追加のテストを含めたコードを再提出するよう依頼できます。 また、コード担当者は、要件を満たしていないコードのチェックインを全面的にブロックすることもできます。 レビュー者によってコードが満足できると判断された後、レビューアーは承認を提供します。これは、コードが次の展開フェーズに進む前に必要です。

Microsoft では、セキュリティ保護された開発ツールと手動コード レビューに加えて、自動セキュリティ ツールを使用して SDL 要件を適用します。 これらのツールの多くは、コミット パイプラインに組み込まれています。 たとえば、一般的なセキュリティ上の欠陥に対する静的なコード分析や、埋め込みシークレットのコードを分析する資格情報スキャナーがあります。 自動セキュリティ ツールによって発見された問題は、新しいビルドがセキュリティ レビューに合格し、リリースが承認される前に修正する必要があります。

## <a name="how-does-microsoft-manage-open-source-software"></a>Microsoft はオープンソース ソフトウェアを管理する方法を説明します。

Microsoft では、次の目的で設計されたツールとワークフローを活用する、オープンソース のセキュリティを管理するための高度な戦略を採用しています。

- 当社の製品およびサービスで使用されているオープン ソース コンポーネントを理解します。
- これらのコンポーネントがどこでどのように使用されているかを追跡します。
- それらのコンポーネントに脆弱性があるかどうかを確認します。
- これらのコンポーネントに影響を与える脆弱性が発見された場合は、適切に対応します。

Microsoft のエンジニアリング チームは、製品またはサービスに含まれるすべてのオープン ソース ソフトウェアのセキュリティに対する責任を維持します。 これを大規模に実現するために、Microsoft は、オープン ソースの検出、法的要件のワークフロー、および脆弱なコンポーネントのアラートを自動化する CG を通じて、エンジニアリング システムに不可欠な機能を組み込みました。 自動化された CG ツールは、Microsoft のビルドをスキャンして、オープンソース コンポーネントと関連するセキュリティの脆弱性や法的義務をスキャンします。 検出されたコンポーネントは登録され、ビジネスおよびセキュリティ レビューのために適切なチームに送信されます。 これらのレビューは、オープン ソース コンポーネントに関連する法的義務またはセキュリティの脆弱性を評価し、コンポーネントの展開を承認する前にそれらを解決するように設計されています。

## <a name="related-external-regulations--certifications"></a>関連する外部規制&認定

Microsoft のオンライン サービスは、定期的に外部の規制と認定に準拠した監査を受けています。 セキュリティの開発と運用に関連するコントロールの検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3: システム開発ライフサイクル | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: 変更管理コントロール <br> A.14.2: 開発およびサポート プロセスのセキュリティ | 2021 年 4 月 20 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性のステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: 変更管理コントロール <br> A.14.2: 開発およびサポート プロセスのセキュリティ | 2021 年 4 月 20 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: リスク管理 <br> CA-18: 変更管理 <br> CA-19: 変更監視 <br> CA-21: 変更テスト <br> CA-38: ベースライン構成 <br> CA-46: セキュリティ レビュー | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: リスク管理 <br> CA-18: 変更管理 <br> CA-19: 変更監視 <br> CA-21: 変更テスト <br> CA-38: ベースライン構成 <br> CA-46: セキュリティ レビュー | 2020 年 12 月 24 日 |

## <a name="resources"></a>リソース

- [Microsoft のセキュリティ開発ライフサイクル](https://www.microsoft.com/securityengineering/sdl)
