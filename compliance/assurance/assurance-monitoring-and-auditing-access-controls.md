---
title: Microsoft 365アクセス制御の監視と監査
description: '概要: サーバー内で使用できる各種の監視および監査アクセス制御の概要Microsoft 365。'
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e374b22212bce461329e14764a3b35eaa76d5f27fd340e64b9b64fb26ecf35f6
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290581"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>ネットワーク内のアクセス制御の監視と監査Microsoft 365

Microsoft は、すべての委任、特権、および操作の広範な監視と監査を実行します。Microsoft 365。 Microsoft 365アクセス制御は、最小特権とデータ アクセス制御と監査の組み込みの原則に基いて構築された自動化されたプロセスです。

- 許可されたアクセスはすべて、一意のユーザーに対して追跡可能です。 管理者は、顧客コンテンツの処理に対して責任を持つ。
- アクセス制御要求、承認、および管理操作ログは、セキュリティおよび悪意のあるイベントの分析のためにキャプチャされます。
- アクセス レベルは、ビジネス上の正当性を承認し、適格性要件を満たすユーザーのみがシステムにアクセスできるセキュリティ グループ メンバーシップに基づいて、ほぼリアルタイムで確認されます。
- Microsoft 365、アクセス制御、および Azure Active Directory および物理データセンターを含む[](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)サポート サービスは[、ISO/IEC 27001、ISO/IEC 27018、SOC、FedRAMP](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [(Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)などの標準[](https://www.microsoft.com/TrustCenter/Compliance/SOC)に準拠するための独立したサード パーティによって定期的に監査されます。 [](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018)
- Microsoft 365エンジニアは、毎年セキュリティ トレーニングを受け、アクセスの最高の手順を確認し、サービスの権利を維持するために Microsoft のセキュリティとプライバシー ポリシーを確認する必要があります。

警告の自動トリガーは、不審なアクティビティが検出されるとトリガーされます (短時間で複数のログインが失敗した場合など)。 セキュリティMicrosoft 365チームは、機械学習とビッグ データ分析を使用して、アクティビティを確認および分析し、不規則なアクセス パターンを探し、異常で違法なアクティビティに積極的に対応します。 また、Microsoft はペネトレーション テスターの専用チームを採用し、サービスのセキュリティとアクセス制御の問題を見つけるために定期的に Red Team と Blue Team の演習に取り組む。 お客様は、監査レポートと、ユーザーが提供する管理アクティビティ API を使用して、アクセス制御システムの有効性をMicrosoft 365。

詳細については、「管理アクティビティ[API Office 365」](/office/office-365-management-api/office-365-management-activity-api-reference)および「監査とレポート」を[参照Microsoft 365。](assurance-auditing-and-reporting-overview.md)
