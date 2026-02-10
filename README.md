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

MATLAB Utilities collects editor-focused MATLAB scripts and the MBeautifier code formatter to speed up everyday workflows.

## What's included

### MWidgets scripts

- **AutoCdPath** (`MWidgets/AutoCdPath.m`): Changes the current folder to the active editor file's directory. Errors if no file is open.
- **OneMlx2M** (`MWidgets/OneMlx2M.m`): Converts the active `.mlx` Live Script to a `.m` file.
- **MultiMlx2M** (`MWidgets/MultiMlx2M.m`): Converts every `.mlx` file in the current folder to `.m` files (calls `AutoCdPath` first).
- **Beautifier** (`MWidgets/Beautifier.m`): Formats the active `.m` file by calling `MBeautify.formatCurrentEditorPage()`.
- **LiveScriptCustomize** (`MWidgets/LiveScriptCustomize.m`): Sets Live Editor fonts (code: JetBrains Mono, normal: Segoe UI, size 14px).
- **Setup** (`MWidgets/Setup.m`): Adds MATLAB Favorites (category `WIDGETS`) for AutoCdPath, OneMlx2M, MultiMlx2M, and Beautifier using icons from `icons/`.

### MBeautifier formatter

- **Setup**: Run `MBeautify.setup()` once to generate `MBeautifier/resources/settings/MBeautyConfigurationRules.m` from the XML rules.
- **Formatting commands**:
  - `MBeautify.formatCurrentEditorPage()` (use `true` to save)
  - `MBeautify.formatEditorSelection()` (use `true` to save)
  - `MBeautify.formatFile(file, outFile)`
  - `MBeautify.formatFiles(directory, fileFilter)`
- **Configuration**: Edit `MBeautifier/resources/settings/MBeautyConfigurationRules.xml`, then rerun `MBeautify.setup()`.
- Based on the [MBeautifier](https://github.com/davidvarga/MBeautifier) project.

## Installation

### Requirements

- MATLAB with Desktop Editor APIs (`matlab.desktop.editor`).
- MATLAB Live Editor APIs (`matlab.internal.liveeditor`) for `.mlx` conversion.

### Download from GitHub

1. Go to the [GitHub releases page](https://github.com/ruiyangzhou01/MATLAB-Utilities/releases).
2. Under **Assets**, download the `.m` scripts or the `.zip` archive you want.

### Add to the MATLAB search path

Add the repository root (or the `MWidgets` and `MBeautifier` folders) to your MATLAB search path.

## Usage

### Command Window

```matlab
AutoCdPath
OneMlx2M
MultiMlx2M
Beautifier
MBeautify.formatCurrentEditorPage()
```

### Favorites and shortcuts

- Run `Setup` from the `MWidgets` folder to add toolbar favorites with icons.
- MBeautifier can also create shortcuts for formatting actions:

```matlab
MBeautify.createShortcut('editorpage')
MBeautify.createShortcut('editorselection')
MBeautify.createShortcut('file')
```

#### Manual favorites (optional)

<img src="media/image-20210921110048305.png" alt="Add to favorites" style="zoom: 50%;" />

<img src="media/image-20210921110103753.png" alt="Edit favorites" style="zoom: 50%;" />

<img src="media/image-20210921110115227.png" alt="Edit favorites command" style="zoom: 50%;" />

<img src="media/image-20210921110140550.png" alt="Favorites result" />

### Live Editor font customization

Run `LiveScriptCustomize` to apply the default font settings defined in the script.

## License

[GPL-3.0 License](https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/LICENSE) © ruiyangzhou01
