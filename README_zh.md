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

MATLAB Utilities 汇集了面向编辑器的 MATLAB 脚本和 MBeautifier 代码格式化器，用于加速日常工作流。

## 包含内容

### MWidgets 脚本

- **AutoCdPath**（`MWidgets/AutoCdPath.m`）：将当前工作目录切换到活动编辑器文件所在文件夹。未打开文件时会报错。
- **OneMlx2M**（`MWidgets/OneMlx2M.m`）：将当前打开的 `.mlx` Live Script 转换为 `.m` 文件。
- **MultiMlx2M**（`MWidgets/MultiMlx2M.m`）：将当前文件夹中的所有 `.mlx` 文件转换为 `.m` 文件（会先调用 `AutoCdPath`）。
- **Beautifier**（`MWidgets/Beautifier.m`）：通过 `MBeautify.formatCurrentEditorPage()` 格式化当前 `.m` 文件。
- **LiveScriptCustomize**（`MWidgets/LiveScriptCustomize.m`）：设置 Live Editor 字体（代码：JetBrains Mono，普通：Segoe UI，大小 14px）。
- **Setup**（`MWidgets/Setup.m`）：使用 `icons/` 中的图标，为 AutoCdPath、OneMlx2M、MultiMlx2M、Beautifier 添加 MATLAB 收藏夹（分类 `WIDGETS`）。

### MBeautifier 格式化器

- **初始化**：运行 `MBeautify.setup()`，从 XML 规则生成 `MBeautifier/resources/settings/MBeautyConfigurationRules.m`。
- **格式化命令**：
  - `MBeautify.formatCurrentEditorPage()`（传入 `true` 可保存）
  - `MBeautify.formatEditorSelection()`（传入 `true` 可保存）
  - `MBeautify.formatFile(file, outFile)`
  - `MBeautify.formatFiles(directory, fileFilter)`
- **配置**：编辑 `MBeautifier/resources/settings/MBeautyConfigurationRules.xml`，然后重新运行 `MBeautify.setup()`。
- 基于 [MBeautifier](https://github.com/davidvarga/MBeautifier) 项目。

## 安装

### 要求

- MATLAB 桌面编辑器 API（`matlab.desktop.editor`）。
- `.mlx` 转换需要 MATLAB Live Editor API（`matlab.internal.liveeditor`）。

### 从 GitHub 下载

1. 访问 [GitHub releases page](https://github.com/ruiyangzhou01/MATLAB-Utilities/releases)。
2. 在 **Assets** 中下载需要的 `.m` 脚本或 `.zip` 压缩包。

### 添加到 MATLAB 搜索路径

将仓库根目录（或 `MWidgets`、`MBeautifier` 文件夹）添加到 MATLAB 搜索路径。

## 用法

### 命令窗口

```matlab
AutoCdPath
OneMlx2M
MultiMlx2M
Beautifier
MBeautify.formatCurrentEditorPage()
```

### 收藏夹与快捷方式

- 在 `MWidgets` 文件夹中运行 `Setup`，可添加带图标的工具栏收藏夹。
- MBeautifier 也可以创建格式化快捷方式：

```matlab
MBeautify.createShortcut('editorpage')
MBeautify.createShortcut('editorselection')
MBeautify.createShortcut('file')
```

#### 手动添加收藏夹（可选）

<img src="media/image-20210921110048305.png" alt="添加到收藏夹" style="zoom: 50%;" />

<img src="media/image-20210921110103753.png" alt="编辑收藏夹" style="zoom: 50%;" />

<img src="media/image-20210921110115227.png" alt="编辑收藏命令" style="zoom: 50%;" />

<img src="media/image-20210921110140550.png" alt="收藏夹效果" />

### Live Editor 字体设置

运行 `LiveScriptCustomize` 以应用脚本中定义的默认字体设置。

## 开源许可证

[GPL-3.0 License](https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/LICENSE) © ruiyangzhou01
