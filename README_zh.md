<p align="center">
	<img width="480px" alt="logo" src="media/logo.png" align="center" />
	<h1 align="center">MATLAB Utilities</h1>
</p>
<p align="center">
	<img src="https://img.shields.io/github/v/release/ruiyangzhou01/MATLAB-Utilities?&color=blue&logo=hack-the-box"/>
	<img alt="MATLAB" src="https://img.shields.io/badge/-MATLAB-00ADD8?style=flat&logo=matrix&logoColor=white"/>
</p>
<p align="center">
	<a href="https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/README.md">English Readme</a>  | 
	<a href="https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/README_zh.md">中文自述文件</a>
</p>

这是一组MATLAB实用程序，旨在优化MATLAB开发流程。

## 工具箱内容

### `AutoCdPath`

- 文件名：`AutoCdPath.m`

- 功能：自动设置当前目录

- 调用命令：`AutoCdPath`

### `OneMlx2M`

- 文件名：`OneMlx2M.m`

- 功能：自动转换当前.mlx文件为.m文件

- 调用命令：`OneMlx2M`

### `MultiMlx2M`

- 文件名：`MultiMlx2M.m`

- 功能：自动转换目录下所有.mlx文件为.m文件

- 调用命令：`MultiMlx2M`

### `MBeautifier`

- 文件夹名称：`MBeautifier`

- 功能：格式化.m文件

- 调用命令：`MBeautify.formatCurrentEditorPage()`

- 注：基于[MBeautifier](https://github.com/davidvarga/MBeautifier)项目。

## 安装

### 要求

MATLAB 版本不低于R2013b.

#### 通过GitHub下载脚本

导航到[GitHub releases page](https://github.com/ruiyangzhou01/MATLAB-Utilities/releases)，点击底部的**Assets**来显示发布版本中可用的文件，然后点击你想要下载的.m 脚本或.zip压缩包。

#### 别忘记将脚本所在文件夹添加到MATLAB搜索路径

## 用法

这里提供了多种方法来使用这些实用程序。

### 1.通过命令行调用

在命令窗口中直接输入命令。

例如，您可以在命令窗口中输入命令将该目录转移到打开文件的目录下:

```matlab
AutoCdPath
```

然后您可以在命令窗口中直接找到类似这样的运行结果:

```matlab
AutoCdPath to "C:\Users\username\Documents\Scripts".
```

### 2.设置为收藏夹命令，即点即用

#### 添加到收藏命令

<img src="media/image-20210921110048305.png" alt="image-20210921110048305" style="zoom：50%;" />

#### 编辑收藏命令

<img src="media/image-20210921110103753.png" alt="image-20210921110103753" style="zoom:50%;" />

<img src="media/image-20210921110115227.png" alt="image-20210921110115227" style="zoom:50%;" />

#### 效果图

<img src="media/image-20210921110140550.png" alt="image-20210921110140550"  /> 

### 3.直接在项目中包含所需要的代码

## 开源许可证

[GPL-3.0 License](https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/LICENSE) © ruiyangzhou01
