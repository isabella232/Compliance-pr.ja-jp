---
title: オンプレミス ファイル共有の GDPR
description: オンプレミスの Windows Server ファイルで共有一般データ保護規則 (GDPR) の要件に対応する方法について説明します。
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: high
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
hideEdit: true
ms.openlocfilehash: 9c281b6096512f65f20286948addc32127278b98
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160180"
---
# <a name="gdpr-for-on-premises-windows-server-file-shares"></a>オンプレミスの Windows Server ファイル共有の GDPR

ファイル共有のための推奨される基本的なアプローチは、次のとおりです。

-   Azure Information Protection を使用して、機密データにラベルを付けます。

-   Azure Information Protection スキャナーを使用して、データを検索します。

ファイル共有のための推奨されるアプローチには、次の手順が含まれます。

1.  **Azure Information Protection スキャナーをインストールし、構成します。**

    -   使用する機密データの種類を決定します。

    -   使用するローカル フォルダーとネットワーク共有を指定します。

2.  **検出サイクルを完了します。**

    -   検出モードでスキャナーを実行し、検出結果を検証します。

    -   必要に応じて、条件と機密情報の種類を最適化します。

    -   自動的に適用されるラベルの予期される影響を評価します。

3.  **Azure Information Protection スキャナーを実行して、対象となるドキュメントにラベルを適用します**。

4.  **保護のために、**

    -   目的としたラベルのドキュメントを保護するための Exchange データ損失防止ルールを構成します。

    -   アクセス許可を使用して、ファイルにアクセスできるユーザーを制限するようにしてください。

5.  **監視のため、Windows Server のログを SIEM ツールに統合します。**

    -   データ主体要求の個人データを検索するため、Azure Information Protection スキャナーを使用します。また、ファイル共有をクロールするよう、SharePoint Server 検索を構成することもできます。

Azure Information Protection スキャナーを使用して個人データを検索したりラベル付けすることに関する詳細については、「[Deploy AIP Scanner (AIP スキャナーの展開)](/azure/information-protection/deploy-aip-scanner)」 を参照してください。

さまざまな条件でスキャナーを構成すること、また Office 365 データ損失防止 (DLP) のさまざまな機密情報タイプを使用することに関する情報については、「[Azure Information Protection 用の自動および推奨分類の条件を構成する方法](/information-protection/deploy-use/configure-policy-classification)」を参照してください。新しいタイプの Office 365 機密情報はスキャナーですぐに利用できるようになるわけではなく、カスタム機密情報タイプはスキャナーで使用できないことに注意ください。
