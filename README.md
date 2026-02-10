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
<a href="https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/README_fr.md">Français</a>
</p>

MATLAB Utilities is a collection of helper scripts that streamline common development tasks and editor workflows.

## Included utilities

### `AutoCdPath`

- File: `AutoCdPath.m`
- Purpose: Automatically change the current directory to the folder of the active file.
- Command: `AutoCdPath`

### `OneMlx2M`

- File: `OneMlx2M.m`
- Purpose: Convert the current `.mlx` live script to a `.m` file.
- Command: `OneMlx2M`

### `MultiMlx2M`

- File: `MultiMlx2M.m`
- Purpose: Convert all `.mlx` files in the current folder to `.m` files.
- Command: `MultiMlx2M`

### `MBeautifier`

- Folder: `MBeautifier`
- Purpose: A MATLAB source code formatter/beautifier that integrates with the MATLAB Editor and is configurable.
- Command: `MBeautify.formatCurrentEditorPage()`
- Note: Based on the [MBeautifier](https://github.com/davidvarga/MBeautifier) project.

## Installation

### Requirements

MATLAB R2013b or later.

### Download from GitHub

1. Go to the [GitHub releases page](https://github.com/ruiyangzhou01/MATLAB-Utilities/releases).
2. Under **Assets**, download the `.m` scripts or the `.zip` archive you want.

### Add to the MATLAB search path

Add the folder that contains the scripts to your MATLAB search path.

## Usage

There are several ways to use these utilities.

### 1. Command Window

Enter commands directly in the Command Window.

For example, to change to the directory of the active file, run:

```matlab
AutoCdPath
```

You will see a message similar to:

```matlab
AutoCdPath to "C:\Users\username\Documents\Scripts".
```

### 2. Add to Favorites for point-and-click use

#### Add to Favorites

<img src="media/image-20210921110048305.png" alt="Add to favorites" style="zoom: 50%;" />

#### Edit Favorites

<img src="media/image-20210921110103753.png" alt="Edit favorites" style="zoom: 50%;" />

<img src="media/image-20210921110115227.png" alt="Edit favorites command" style="zoom: 50%;" />

#### Result

<img src="media/image-20210921110140550.png" alt="Favorites result" />

### 3. Include the utilities in your project

Copy the required scripts into your project or call them from your own scripts.

## License

[GPL-3.0 License](https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/LICENSE) © ruiyangzhou01
