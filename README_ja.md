<p align="center">
<img width="480px" alt="logo" src="media/logo.png" align="center" />
<h1 align="center">MATLAB Utilities</h1>
</p>
<p align="center">
<img src="https://img.shields.io/github/v/release/ruiyangzhou01/MATLAB-Utilities?&color=blue&logo=hack-the-box"/>
<img alt="MATLAB" src="https://img.shields.io/badge/-MATLAB-00ADD8?style=flat&logo=matrix&logoColor=white"/>
</p>
<p align="center">
<a href="https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/README.md">English</a>  |
<a href="https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/README_zh.md">简体中文</a>  |
<a href="https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/README_de.md">Deutsch</a>  |
<a href="https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/README_es.md">Español</a>  |
<a href="https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/README_fr.md">Français</a>  |
<a href="https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/README_ja.md">日本語</a>
</p>

MATLAB Utilities は、エディタ向けの MATLAB スクリプトと MBeautifier コードフォーマッタをまとめたもので、日常の作業を効率化します。

## 含まれる内容

### MWidgets スクリプト

- **AutoCdPath**（`MWidgets/AutoCdPath.m`）：アクティブなエディタファイルのフォルダに作業ディレクトリを変更します。ファイルが開かれていない場合はエラーになります。
- **OneMlx2M**（`MWidgets/OneMlx2M.m`）：アクティブな `.mlx` Live Script を `.m` ファイルに変換します。
- **MultiMlx2M**（`MWidgets/MultiMlx2M.m`）：現在のフォルダ内の `.mlx` をすべて `.m` に変換します（先に `AutoCdPath` を呼び出します）。
- **Beautifier**（`MWidgets/Beautifier.m`）：`MBeautify.formatCurrentEditorPage()` を呼び出してアクティブな `.m` ファイルを整形します。
- **LiveScriptCustomize**（`MWidgets/LiveScriptCustomize.m`）：Live Editor のフォント設定（コード：Jetbrains Mono、通常：Segoe UI、サイズ 14px）を適用します。
- **Setup**（`MWidgets/Setup.m`）：`icons/` のアイコンを使って AutoCdPath、OneMlx2M、MultiMlx2M、Beautifier の MATLAB お気に入り（カテゴリ `WIDGETS`）を追加します。

### MBeautifier フォーマッタ

- **セットアップ**：`MBeautify.setup()` を一度実行して XML ルールから `MBeautifier/resources/settings/MBeautyConfigurationRules.m` を生成します。
- **整形コマンド**：
  - `MBeautify.formatCurrentEditorPage()`（保存する場合は `true`）
  - `MBeautify.formatEditorSelection()`（保存する場合は `true`）
  - `MBeautify.formatFile(file)`（整形して保存せずに開いたままにします）
  - `MBeautify.formatFile(file, outFile)`（整形して出力ファイルに書き込みます）
  - `MBeautify.formatFiles(directory, fileFilter)`
- **設定**：`MBeautifier/resources/settings/MBeautyConfigurationRules.xml` を編集し、`MBeautify.setup()` を再実行します。
- [MBeautifier](https://github.com/davidvarga/MBeautifier) プロジェクトに基づいています。

## インストール

### 要件

- MATLAB Desktop Editor API（`matlab.desktop.editor`）。
- `.mlx` 変換には MATLAB Live Editor API（`matlab.internal.liveeditor`）が必要です。

### GitHub からダウンロード

1. [GitHub releases page](https://github.com/ruiyangzhou01/MATLAB-Utilities/releases) を開きます。
2. **Assets** から必要な `.m` スクリプトまたは `.zip` アーカイブをダウンロードします。

### MATLAB パスへの追加

リポジトリのルート（または `MWidgets` と `MBeautifier` フォルダ）を MATLAB の検索パスに追加します。

## 使い方

### コマンドウィンドウ

```matlab
AutoCdPath
OneMlx2M
MultiMlx2M
Beautifier
MBeautify.formatCurrentEditorPage()
```

### お気に入りとショートカット

- MATLAB エディタで `MWidgets/Setup.m` を開き、アクティブな状態で `Setup` を実行すると、アイコン付きのお気に入りがツールバーに追加されます。
- MBeautifier では整形アクションのショートカットも作成できます。

```matlab
MBeautify.createShortcut('editorpage')
MBeautify.createShortcut('editorselection')
MBeautify.createShortcut('file')
```

#### 手動のお気に入り追加（任意）

<img src="media/image-20210921110048305.png" alt="お気に入りに追加" style="zoom: 50%;" />

<img src="media/image-20210921110103753.png" alt="お気に入りを編集" style="zoom: 50%;" />

<img src="media/image-20210921110115227.png" alt="お気に入りコマンドを編集" style="zoom: 50%;" />

<img src="media/image-20210921110140550.png" alt="お気に入りの結果" />

### Live Editor のフォント設定

`LiveScriptCustomize` を実行して、スクリプトに定義された既定のフォント設定を適用します。

## ライセンス

[GPL-3.0 License](https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/LICENSE) © ruiyangzhou01
