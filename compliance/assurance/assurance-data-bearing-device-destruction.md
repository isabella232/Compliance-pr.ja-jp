---
title: データを持つデバイスの破壊
description: この記事では、Microsoft データセンターのデータベアリング デバイス破棄プロセスの概要について説明します。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 6a26334b805be069298302d3ad1e8e5b9e728150
ms.sourcegitcommit: 1fd50ef5f165228109a3f2f0aef4b0c2aa59b2ff
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2021
ms.locfileid: "58862401"
---
# <a name="data-bearing-device-destruction"></a>データを持つデバイスの破壊

## <a name="data-destruction-overview"></a>データ破壊の概要

Microsoft には、Microsoft データセンター内の DBD の処理と管理に関する、データ関連デバイス (DBD) のガイドライン、ポリシー、セキュリティ要件、および手順があります。

DBD は、顧客または Microsoft 独自のデータを格納できる任意のストレージ デバイスです。

- ハード ディスク ドライブ (HDD)
- ソリッド ステート ドライブ (SSD)
- USB ドライブ
- IO アクセラレータ カード
- SD/Compact フラッシュ カード
- HSM カード
- PCIe SSD カード
- NVDIMM (非揮発性デュアル インライン メモリ モジュール)

Microsoft データセンター内で使用される障害が発生した DBD は、データセンター キャンパス内で監査および破棄されます。 サービスから廃止された資産は、そのセキュリティ/プライバシー要件と資産分類に見合った方法で、適用される規則、法律、および規制に従って廃棄が評価されます。

Microsoft では、DBD およびデータを含むアセットに対して、次の 3 つのカテゴリのデータ サニティ化を使用します。

- **Clear**: 単純な非侵襲的なデータ復旧手法に対する保護のために、すべてのユーザーアドレス指定可能な記憶域の場所でデータをサニタイズするのに役立つ論理的な手法に関連します。 これらは、通常、標準の読み取りおよび書き込みコマンドを使用してストレージ デバイスに適用される手法です。新しい値を使用して書き換える方法や、メニュー オプションを使用してデバイスを工場出荷時の状態にリセットする (書き換えはサポートされていません)。
- **Purge**: 最新のラボ技術を使用してターゲット データの回復を実行できない物理的または論理的な手法に関連します。
- **Destroy**: 最先端のラボ技術を使用してターゲット データ復旧を実行できない状態にし、メディアをデータの保存に使用できないという結果になります。

削除と削除のサニティ化は、セキュリティ グループによって承認されたツールとプロセスを使用して実行されます。 レコードは、資産の消去と破棄を保持します。 クリアを完了できなかったデバイスは、正常に消去されます (磁気メディアの場合のみ)。マルチピンパンチ (SSD などのチップベースのボードの場合)、または破棄されます。

## <a name="clear"></a>Clear

廃止された資産が評価され、アクセスできないと判断された場合は、承認済みのデータ根絶ソリューションによって削除されます。 Microsoft データセンターでは、NIST SP-800-88 の明確なガイドラインを使用します。

## <a name="purge"></a>Purge

オンサイトの構成とデバイスの可用性に応じて、一部のデバイスは破棄前に削除されます。 パージ デバイスには、磁気メディア用の NSA 承認済み degaussers と、ソリッドステート メディア用のマルチピン パンチ デバイスが含まれます。 Microsoft データセンターでは、NIST SP-800-88 の削除ガイドラインを使用します。

## <a name="destroy"></a>破棄

廃止された資産が評価され、アクセス可能と判断された場合、NIST SP-800-88 ガイドラインを満たす承認済みの標準運用手順を使用してオンサイトで破棄されます。 これらの DBD は、物理的および論理的に追跡され、最終的な処分を通じて親権のチェーンを維持します。

各 Microsoft データセンターでは、オンサイト プロセスを使用して、障害が発生した DBD と廃止された DBD をサニタイズして破棄します。 このプロセスの間、Microsoft の担当者は、廃棄プロセスを通じて保管のチェーンが維持されます。

## <a name="resources"></a>リソース

- [NIST Special Publication 800-88](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)
