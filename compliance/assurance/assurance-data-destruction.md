---
title: データの破棄Microsoft 365
description: データ センター のディスク ドライブとサーバーのリサイクル、廃棄、またはMicrosoft 365に関する Microsoft ポリシーの概要。
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
ms.openlocfilehash: bf7769852a41e8f78724c64e9a189ba7652c8f95a4cb71db1d5a7c3d286892e5
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "54288705"
---
# <a name="data-destruction-in-microsoft-365"></a>データの破棄Microsoft 365

## <a name="physical-data-destruction"></a>物理データの破棄

Microsoft には、ディスク ドライブのリサイクルと廃棄、サーバーの障害または廃止に対応するデータ処理標準ポリシーがあります。 Microsoft 365 ディスク ドライブを再利用する前に、Microsoft は国立標準技術研究所の特別文書 800-88[(NIST SP 800-88](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)メディア サニティ化ガイドライン) と一致する物理的なサニティ化プロセスを実行します。 Microsoft 365 のすべてのディスク ドライブは BitLocker ボリューム レベルの暗号化を使用して暗号化されます。NIST SP 800-88 準拠の消去は技術的に必要ありません。 それにもかかわらず、Microsoft は、このプロセスを実行します。

データセンター内で使用Microsoft 365失敗したディスクは、ISO プロセスを通じて物理的に破棄および監査されます。 アセットの種類は、適切な廃棄手段を決定します。 ワイプできないハード ドライブの場合、Microsoft は破棄プロセスを使用してメディアを破棄し、情報の回復を不可能にしています。 たとえば、ディスクは物理的に破壊、粉砕、または焼却されます。 Microsoft は破壊のすべてのレコードを保持し、サーバー内で再利用されたサーバーで同様のサニMicrosoft 365。 これらのガイドラインには、電子的なサニティゼーションと物理サニティゼーションの両方が含されます。

各データセンターは、オンサイトの物理的破壊プロセスを使用してディスクを破棄します。 ディスク廃棄用に指定されたストレージ メディア用のセキュリティで保護されたビンは、データセンターの各領域にあります。 セキュリティで保護された各ビン ステーションには、ビデオ監視監視があります。 廃棄ビンの容量が約 50% に達すると、Site Services チームは物理セキュリティ チームに連絡して削除を調整します。 Site Services 担当者とセキュリティ 管理者Office、セキュリティで保護された廃棄箱を削除し、指定されたセキュリティで保護された記憶域に配置します。 廃棄時のデータ ベアリング デバイスの処理を管理するポリシーと手順は、破棄が承認された機械の状態を確認する手順など、日常的にテストされます。

データ破壊プロセスでは、ディスクは NIST 800-88 (可能な場合) に準拠した方法で消去され、産業シュレッダーに配置され、物理的に取り壊されます。 Microsoft は、NIST SP 800-88 の一貫したクレンジング/削除、資産の破壊、暗号化、正確なインベントリ、追跡、およびトランスポート中の保管チェーンの保護を使用してデータセンターを離れる資産に対する説明責任を維持します。 このプロセスは、閉回路テレビを介して監視され、完了時に破棄証明書が発行されます。

Microsoft では、Extreme Protocol Solutions (EPS) の [データ消去ユニット](https://www.enterprisedataerasure.com/) を使用しています。 EPS ソフトウェアは、クレンジングおよび削除/安全な消去に関する NIST SP 800-88 の要件をサポートしています。 クレンジングまたは破棄の前に、Microsoft アセット マネージャーによってインベントリが作成されます。 ベンダーが破壊に使用される場合、ベンダーは破棄された各資産に対して破棄証明書を提供します。これは資産マネージャーによって検証されます。

## <a name="virtual-data-destruction"></a>仮想データの破棄

Microsoft には、サービス テナント間でデータが不適切に共有される可能性や、サービスでハード削除された後にアクセスできる可能性から保護するために、データの効果的な仮想破壊に対処するデータ処理ポリシーと手順があります。 1 つのテナントのサービスから削除されたデータは、基になる物理記憶域が再割り当てされた場合でも、別のサービス テナントからアクセスできません。 これは、仮想環境の拡張に使用される複数の仮想化および断片化テクノロジの複合効果、各サービス テナント内のアプリケーションのアクティブな削除動作 (ページのゼロ化[](/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)など)、および必要なメディアおよびアプリケーション コンテンツ暗号化プロセスの結果です。