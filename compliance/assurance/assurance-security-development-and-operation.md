---
title: セキュリティの開発と運用の概要
description: Microsoft 365 のセキュリティ開発と運用について説明します。
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
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 7c6752b84470eebbdb6ad78c212361156dea957b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508096"
---
# <a name="security-development-and-operations-overview"></a>セキュリティの開発と運用の概要

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Microsoft は、安全な開発方法をどのように実装していますか?

Microsoft のセキュリティ開発ライフサイクル (SDL) は、セキュリティで保護されたソフトウェアを開発および運用することに重点を置いたセキュリティ保証プロセスです。 SDL には、Microsoft の開発者やエンジニアにとって、より多くの測定可能なセキュリティ要件が用意されています。 Microsoft は、お客様の製品とサービスの脆弱性の数と重大度を削減します。 すべての Microsoft ソフトウェア開発チームは SDL の要件に従う必要があります。また、コンプライアンスのための脅威を変化させ、業界のベストプラクティスや規制基準を反映して SDL を継続的に更新しています。

## <a name="how-does-microsofts-sdl-improve-application-security"></a>マイクロソフトの SDL はアプリケーションセキュリティをどのように改善しますか?

Microsoft の SDL プロセスは、要件、設計、実装、検証、リリースという5つの開発段階において考えることができます。 まず、セキュリティを念頭に置いてソフトウェア要件を定義します。 これを行うには、アプリケーションが実行する必要があるセキュリティ関連の質問を確認します。 アプリケーションで機密データを収集する必要がありますか? アプリケーションは機密情報や重要なタスクを実行しますか? アプリケーションは、信頼できない発行元からの入力を受け入れる必要がありますか?

関連するセキュリティ要件が特定されると、これらの要件を満たすセキュリティ機能が組み込まれるようにソフトウェアを設計します。 開発者は SDL と設計要件をコードに実装し、手動のコード レビュー、自動化されたセキュリティ ツール、および侵入テストで検証します。 最後に、コードをリリースする前に、最終的なセキュリティとプライバシーに関するレビューを行って、すべての要件を満たしていることを確認してください。

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>一般的な脆弱性に関する Microsoft テストのソースコード

コード開発やリリース後のセキュリティ要件を実装する開発者をサポートするために、Microsoft では、セキュリティの欠陥や脆弱性についてソース コードを自動的にチェックする、セキュリティで保護された一連の開発ツールを提供しています。 Microsoft は、Microsoft build パイプライン内で自動的に実行される組み込みのセキュリティチェックとともに、使用する開発者向けの承認済みツール (コンパイラ、開発環境など) のリストを定義して公開します。 弊社の開発者は、新しいセキュリティ機能を活用するために、承認されたツールの最新バージョンを使用しています。

コードをリリースブランチにチェックインする前に、SDL では別のレビュー担当者が手動でコードレビューを行う必要があります。 コード レビュー担当者は、コーディング エラーを確認し、コード変更が SDL および設計要件を満たしているか、機能およびセキュリティのテストに合格したか、確実に動作するかを確認します。 また、コードの変更が適切に文書化され、意図しない副作用が発生しないことを確認するために、関連するドキュメント、構成、および依存関係を確認します。 レビュー担当者は、コード レビュー中に問題を発見した場合、提出者に、提案された変更と追加のテストを含めたコードを再提出するよう依頼できます。 また、コード担当者は、要件を満たしていないコードのチェックインを全面的にブロックすることもできます。 レビュー担当者がコードを満足していると判断されると、レビュー担当者は承認を提供します。これは、コードが次の展開フェーズに進む前に必要になります。

セキュリティで保護された開発ツールと手動のコードレビューに加えて、Microsoft は自動セキュリティツールを使用して SDL の要件を適用します。 これらのツールの多くは、コミットパイプラインに組み込まれており、セキュリティ上の問題がチェックインされ、新しいビルドがコンパイルされたときに、そのコードを自動的に分析します。 例としては、一般的なセキュリティの欠陥と、埋め込まれた機密情報のコードを分析する資格情報スキャナーの静的コード分析があります。 新しいビルドがセキュリティレビューを通過してリリースを承認されるようにするには、自動セキュリティツールによって検出された問題を修正する必要があります。

## <a name="how-does-microsoft-manage-open-source-software"></a>Microsoft はオープンソースソフトウェアをどのように管理していますか?

Microsoft では、オープンソースセキュリティを管理するための大まかな戦略を採用しており、次の目的に設計されたツールとワークフローを活用しています。

- 当社の製品およびサービスで使用されているオープン ソース コンポーネントを理解します。
- これらのコンポーネントがどこでどのように使用されているかを追跡します。
- それらのコンポーネントに脆弱性があるかどうかを確認します。
- これらのコンポーネントに影響を与える脆弱性が発見された場合は、適切に対応します。

Microsoft のエンジニアリング チームは、製品またはサービスに含まれるすべてのオープン ソース ソフトウェアのセキュリティに対する責任を維持します。 これを大規模に実現するために、Microsoft は、オープン ソースの検出、法的要件のワークフロー、および脆弱なコンポーネントのアラートを自動化する CG を通じて、エンジニアリング システムに不可欠な機能を組み込みました。 自動 CG ツールは、オープンソースのコンポーネントと関連するセキュリティの脆弱性または法的責任を得るために、Microsoft でビルドをスキャンします。 検出されたコンポーネントは登録され、ビジネスおよびセキュリティ レビューのために適切なチームに送信されます。 これらのレビューは、オープン ソース コンポーネントに関連する法的義務またはセキュリティの脆弱性を評価し、コンポーネントの展開を承認する前にそれらを解決するように設計されています。

## <a name="related-external-regulations--certifications"></a>関連する外部規制 & 証明書

Microsoft のオンラインサービスは、社外の規制と証明書に準拠するために定期的に監査されます。 セキュリティの開発と操作に関連する制御の検証については、次の表を参照してください。

| **外部監査** | **Section** | **最新のレポート日付** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3: システム開発ライフサイクル | 2020年9月24日 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.1.2: 変更管理コントロール <br> 14.2: 開発およびサポートプロセスのセキュリティ | 2020 月 2 月 22 日 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [適用性に関するステートメント](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [認定](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.1.2: 変更管理コントロール <br> 14.2: 開発およびサポートプロセスのセキュリティ | 2020 月 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03: リスク管理 <br> CA-18: 変更管理 <br> CA-19: 変更監視 <br> CA-21: 変更テスト <br> CA-38: ベースライン構成 <br> CA-46: セキュリティレビュー | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03: リスク管理 <br> CA-18: 変更管理 <br> CA-19: 変更監視 <br> CA-21: 変更テスト <br> CA-38: ベースライン構成 <br> CA-46: セキュリティレビュー | 2019 年 9 月 30 日 |

## <a name="resources"></a>リソース

- [Microsoft のセキュリティ開発ライフサイクル](https://www.microsoft.com/securityengineering/sdl)
