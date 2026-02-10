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

MATLAB Utilities 是一组用于简化常见开发任务和编辑器工作流的辅助脚本。

## 工具列表

### `AutoCdPath`

- 文件：`AutoCdPath.m`
- 用途：自动将当前目录切换到当前打开文件所在的文件夹。
- 命令：`AutoCdPath`

### `OneMlx2M`

- 文件：`OneMlx2M.m`
- 用途：将当前 `.mlx` Live Script 转换为 `.m` 文件。
- 命令：`OneMlx2M`

### `MultiMlx2M`

- 文件：`MultiMlx2M.m`
- 用途：将当前文件夹中的所有 `.mlx` 文件转换为 `.m` 文件。
- 命令：`MultiMlx2M`

### `MBeautifier`

- 文件夹：`MBeautifier`
- 用途：MATLAB 源代码格式化/美化工具，可直接在 MATLAB 编辑器中使用并支持配置。
- 命令：`MBeautify.formatCurrentEditorPage()`
- 备注：基于 [MBeautifier](https://github.com/davidvarga/MBeautifier) 项目。

## 安装

### 要求

MATLAB R2013b 或更高版本。

### 从 GitHub 下载

1. 访问 [GitHub releases page](https://github.com/ruiyangzhou01/MATLAB-Utilities/releases)。
2. 在 **Assets** 中下载需要的 `.m` 脚本或 `.zip` 压缩包。

### 添加到 MATLAB 搜索路径

将包含脚本的文件夹添加到 MATLAB 搜索路径。

## 用法

提供多种使用方式。

### 1. 命令窗口

在命令窗口中直接输入命令。

例如，要切换到当前打开文件所在的目录，请运行：

```matlab
AutoCdPath
```

你会看到类似如下的输出：

```matlab
AutoCdPath to "C:\Users\username\Documents\Scripts".
```

### 2. 添加到收藏夹，点击即可使用

#### 添加到收藏夹

<img src="media/image-20210921110048305.png" alt="添加到收藏夹" style="zoom: 50%;" />

#### 编辑收藏夹

<img src="media/image-20210921110103753.png" alt="编辑收藏夹" style="zoom: 50%;" />

<img src="media/image-20210921110115227.png" alt="编辑收藏命令" style="zoom: 50%;" />

#### 效果

<img src="media/image-20210921110140550.png" alt="收藏夹效果" />

### 3. 在项目中直接包含这些工具

将所需脚本复制到项目中，或在自己的脚本中调用它们。

## 开源许可证

[GPL-3.0 License](https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/LICENSE) © ruiyangzhou01
