---
title: Microsoft 365 でのデータの破棄
description: Microsoft 365 データ センター ディスク ドライブとサーバーのリサイクル、破棄、または破棄に関する Microsoft ポリシーの概要。
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
ms.openlocfilehash: d97c5f1be6bf09a772244aac14086171643af89e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120676"
---
# <a name="data-destruction-in-microsoft-365"></a>Microsoft 365 でのデータの破棄

## <a name="physical-data-destruction"></a>物理データの破棄

Microsoft は、ディスク ドライブのリサイクルと廃棄、およびサーバーの障害または廃棄に対応するデータ処理標準ポリシーを持っています。 Microsoft 365 ディスク ドライブを再利用する前に、Microsoft は National Institute of Standards and Technology Special Publication 800-88[(NIST SP 800-88 Guidelines for Media Sanitization)](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)と一致する物理的なサニティ化プロセスを実行します。 Microsoft 365 のすべてのディスク ドライブは BitLocker ボリューム レベルの暗号化を使用して暗号化されます。NIST SP 800-88 準拠の消去は技術的には必要ありません。 ただし、Microsoft は、このプロセスを実行します。

Microsoft 365 データセンター内で使用される障害が発生したディスクは、物理的に破棄され、ISO プロセスによって監査されます。 アセットの種類によって、適切な廃棄方法が決まれます。 ワイプできないハード ドライブの場合、Microsoft は破棄プロセスを使用してメディアを破棄し、情報の回復を不可能にレンダリングします。 たとえば、ディスクは物理的に破壊、取り付け、または破壊されます。 Microsoft は破棄のすべてのレコードを保持し、Microsoft 365 内で再利用されたサーバーで同様のサニティ化プロセスを実行します。 これらのガイドラインには、電子サニティゼーションと物理サニティゼーションの両方が含されます。

各データセンターは、オンサイトの物理的な破棄プロセスを使用してディスクを破棄します。 ディスクの廃棄用に指定された記憶域メディア用のセキュリティで保護された bin は、データセンターの各領域にあります。 各セキュリティで保護されたビン ステーションには、ビデオ監視監視機能があります。 ごみ箱の容量が約 50% に達すると、サイト サービス チームは物理セキュリティ チームに連絡して削除を調整します。 サイト サービス担当者とセキュリティ 管理者Office、安全な廃棄ビンを削除し、指定されたセキュリティで保護された記憶域に配置します。 破棄中のデータ受け入れデバイスの処理を管理するポリシーと手順は、破棄が承認された機械の状態を確認する手順を含め、日常的にテストされます。

データ破棄プロセスでは、ディスクは NIST 800-88 (可能な場合) に準拠した方法で消去され、その後、生産的な細断機に配置され、物理的に降格されます。 Microsoft は、NIST SP 800-88 の一貫性のあるパージ/削除、資産の破壊、暗号化、正確なインベントリ作成、追跡、および転送中の保管チェーンの保護を使用して、データセンターを離れる資産に対する責任を維持しています。 このプロセスは閉回線テレビを介して監視され、完了時に破棄証明書が発行されます。

Microsoft では、Extreme Protocol Solutions (EP) のデータ [消去ユニットを](https://www.enterprisedataerasure.com/) 使用しています。 EP ソフトウェアは、NIST SP 800-88 の消去と消去/安全な消去の要件をサポートしています。 クレンジングまたは破壊を行う前に、インベントリは Microsoft アセット マネージャーによって作成されます。 ベンダーが破棄に使用されている場合、ベンダーは破棄された各資産の破棄証明書を提供します。この証明書はアセット マネージャーによって検証されます。

## <a name="virtual-data-destruction"></a>仮想データの破棄

Microsoft は、データがサービス テナント間で不適切に共有される可能性や、サービスのハード削除後にアクセス可能になる可能性から保護するために、データの効果的な仮想破壊に対処するデータ処理ポリシーと手順を用意しています。 あるテナントのサービスから削除されたデータは、基礎となる物理ストレージが再割り当てされた場合でも、別のサービス テナントからアクセスできません。 これは、仮想環境のスケーリングに使用される複数の仮想化および断片化テクノロジ、各サービス テナント内のアプリケーションのアクティブな削除動作 (ページの削除など)、および[](/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)必要なメディアおよびアプリケーション コンテンツの暗号化プロセスによる複合的な影響の結果です。