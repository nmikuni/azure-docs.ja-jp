---
title: Threat Modeling Tool のリリース - Microsoft Threat Modeling Tool - Azure | Microsoft Docs
description: Threat Modeling Tool のリリース ノートです
services: security
documentationcenter: na
author: jegeib
manager: jegeib
editor: jegeib
ms.assetid: na
ms.service: security
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 01/15/2019
ms.author: jegeib
ms.openlocfilehash: bdf8b701567aaa3a0d9006333557bcec4f312723
ms.sourcegitcommit: 41ca82b5f95d2e07b0c7f9025b912daf0ab21909
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/13/2019
ms.locfileid: "60586466"
---
# <a name="threat-modeling-tool-ga-release-71509112---9122018"></a>Threat Modeling Tool GA リリース 7.1.50911.2 - 9/12/2018

Microsoft Threat Modeling Tool がサポートされる一般公開 (GA) リリースとしてダウンロードできるようになったことをお知らせします。 このリリースには、プライバシーとセキュリティに関する重要な更新だけでなく、バグの修正、機能の更新、および安定性の向上が含まれています。 2017 プレビュー バージョンの既存のユーザーに対しては、クライアントを開くときに、ClickOnce テクノロジを使用して最新リリースに更新することを求めるメッセージが表示されます。 ツールの新しいユーザーの場合は、[こちらをクリックしてクライアントをダウンロードする](https://aka.ms/threatmodelingtool)ことができます。

このリリースをもって、2017 プレビューのサポートは終了するので、プレビューのすべてのユーザーに GA リリースに更新することをお勧めします。 2018 年 10 月 15 日以降、Threat Modeling Tool に対しては必要最低限の ClickOnce バージョンが設定され、すべてのプレビュー クライアントでアップグレードが必要になります。

[Microsoft ダウンロード センター](https://www.microsoft.com/en-us/download/details.aspx?id=49168)から入手できる Microsoft Threat Modeling Tool 2016 は、重要なセキュリティ修正プログラムについてのみ、2019 年 10 月 1 日までサポートされます。

## <a name="feature-changes"></a>機能の変更

### <a name="azure-stencil-updates"></a>Azure ステンシルの更新プログラム

追加の Azure ステンシルと、それに関連する脅威および軽減策が、このリリースに付属するステンシル セットに追加されています。 "Azure App Services"、"Azure データベース オファリング"、"Azure Storage" の分野に関して、重要な変更が行われました。

![Azure ステンシルの更新プログラム](./media/azure-security-threat-modeling-tool-releases-71509112/tmt_azure_stencil_update-300x70.png)

### <a name="onedrive-integration-feature-removed"></a>OneDrive 統合機能の削除

プレビューの [OneDrive に保存]、[OneDrive から開く]、[リンクを共有] の各機能は削除されました。 OneDrive のユーザーには、Microsoft の [OneDrive for Windows](https://onedrive.live.com/about/en-us/download/) クライアントを使用し、ファイルを保存したり開いたりする標準のダイアログで OneDrive に格納されているファイルにアクセスすることをお勧めします。

## <a name="notable-fixed-bugs-reported-by-customers"></a>ユーザーから報告された重要なバグの修正

### <a name="in-tmt-preview-the-tool-crashes-when-using-the-standard-template"></a>TMT プレビューで標準テンプレートを使用するとツールがクラッシュする

- 汎用ステンシル (たとえば "汎用データ フロー") を描画サーフェスに追加して脅威を生成すると、ツールがクラッシュすることがあります。 この問題は修正されています。

### <a name="in-tmt-preview-when-i-save-a-report-or-copy-the-threats-the-risk-levels-are-incorrect"></a>TMT プレビューでレポートを保存したり脅威をコピーしたりするときに、リスク レベルが正しくない

- ユーザーが特定の脅威のリスク レベルを変更してから、レポートを保存したり、リスクをコピーしたりすると、リスク レベルが "高" に戻ることがあります。 この問題は修正されています。

## <a name="known-issues-and-faq"></a>既知の問題とよくあるご質問

### <a name="users-of-high-resolution-screens-may-experience-small-text-in-the-threat-properties"></a>高解像度画面を使用すると、脅威のプロパティのテキストが小さくなることがある

#### <a name="issue"></a>問題

Windows が読みやすいように既定で拡大するよう設定されている高解像度画面でツールの分析ビューを表示すると、脅威の [Possible Mitigation(s)]\(可能な軽減策\) セクションが小さいテキストで表示されることがあります。

![高解像度画面に関する既知の問題](./media/azure-security-threat-modeling-tool-releases-71509112/tmt_screen_resolution-300x153.png)

#### <a name="workaround"></a>対処法

ユーザーは、軽減策のテキストをクリックし、Windows の標準ズーム コントロール (Crtl キーを押しながらマウス ホイールを前方に回す) を使用して、そのセクションの表示倍率を上げることができます。

### <a name="files-in-the-recently-opened-models-section-of-the-main-window-may-fail-to-open"></a>メイン ウィンドウの [Recently Opened Models]\(最近開いたモデル\) セクションのファイルを、開けない場合があります

#### <a name="issue"></a>問題

プレビュー リリースの [OneDrive から開く] 機能は削除されました。 OneDrive に保存された "最近開いたモデル" を使用している場合、次のエラーが表示されます。

![削除された OneDrive の機能](./media/azure-security-threat-modeling-tool-releases-71509112/tmt_save_error-300x131.png)

#### <a name="workaround"></a>対処法

OneDrive のユーザーには、Microsoft の [OneDrive for Windows](https://onedrive.live.com/about/en-us/download/) クライアントを使用し、標準の [Open a model]\(モデルを開く\) ダイアログで OneDrive に格納されているファイルにアクセスすることをお勧めします。

![削除された OneDrive の機能](./media/azure-security-threat-modeling-tool-releases-71509112/tmt_save_onedrive-300x149.png)

### <a name="my-organization-uses-the-2016-version-of-the-tool-can-i-use-the-azure-stencil-set"></a>組織で 2016 バージョンのツールを使用していますが、Azure のステンシル セットを使用できますか?

はい、できます。 [Azure のステンシル セットは GitHub で入手する](https://github.com/Microsoft/threat-modeling-templates/)ことができ、2016 バージョンのツールで読み込むことができます。 Azure のステンシル セットを使用して新しいモデルを作成するには、メイン メニュー画面の [Template For New Models]\(新しいモデルのテンプレート\) ダイアログを使用します。 TMT 2016 では [Possible Mitigations]\(可能な軽減策\) フィールドにある Azure ステンシル セットのリンクをレンダリングできないので、リンクが HTML タグとして表示される可能性があります。

![2016 クライアントでの Azure ステンシルの更新プログラム](./media/azure-security-threat-modeling-tool-releases-71509112/tmt_azure_stencils-300x212.png)

## <a name="system-requirements"></a>システム要件

- サポートされているオペレーティング システム
  - Microsoft Windows 10
- 必要な .NET のバージョン
  - .NET 3.5.2
- その他の要件
  - ツールとテンプレートの更新プログラムを受け取るには、インターネット接続が必要です。

## <a name="documentation-and-feedback"></a>ドキュメントとフィードバック

- Threat Modeling Tool のドキュメントは [docs.microsoft.com](https://docs.microsoft.com/azure/security/azure-security-threat-modeling-tool) にあり、[ツールの使用について](https://docs.microsoft.com/azure/security/azure-security-threat-modeling-tool-getting-started)の情報が含まれます。

## <a name="next-steps"></a>次の手順

最新バージョンの [Microsoft Threat Modeling Tool](https://aka.ms/threatmodelingtool) をダウンロードしてください。
