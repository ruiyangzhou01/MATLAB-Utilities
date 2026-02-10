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

MATLAB Utilities reúne scripts orientados al editor de MATLAB y el formateador de código MBeautifier para agilizar los flujos de trabajo diarios.

## Contenido

### Scripts de MWidgets

- **AutoCdPath** (`MWidgets/AutoCdPath.m`): Cambia la carpeta actual al directorio del archivo activo en el editor. Muestra un error si no hay un archivo abierto.
- **OneMlx2M** (`MWidgets/OneMlx2M.m`): Convierte el Live Script `.mlx` activo en un archivo `.m`.
- **MultiMlx2M** (`MWidgets/MultiMlx2M.m`): Convierte todos los `.mlx` de la carpeta actual a archivos `.m` (llama primero a `AutoCdPath`).
- **Beautifier** (`MWidgets/Beautifier.m`): Formatea el archivo `.m` activo llamando a `MBeautify.formatCurrentEditorPage()`.
- **LiveScriptCustomize** (`MWidgets/LiveScriptCustomize.m`): Configura las fuentes del Live Editor (código: JetBrains Mono, normal: Segoe UI, tamaño 14px).
- **Setup** (`MWidgets/Setup.m`): Agrega Favoritos de MATLAB (categoría `WIDGETS`) para AutoCdPath, OneMlx2M, MultiMlx2M y Beautifier usando los iconos de `icons/`.

### Formateador MBeautifier

- **Configuración inicial**: Ejecute `MBeautify.setup()` una vez para generar `MBeautifier/resources/settings/MBeautyConfigurationRules.m` desde las reglas XML.
- **Comandos de formato**:
  - `MBeautify.formatCurrentEditorPage()` (use `true` para guardar)
  - `MBeautify.formatEditorSelection()` (use `true` para guardar)
  - `MBeautify.formatFile(file, outFile)`
  - `MBeautify.formatFiles(directory, fileFilter)`
- **Configuración**: Edite `MBeautifier/resources/settings/MBeautyConfigurationRules.xml` y vuelva a ejecutar `MBeautify.setup()`.
- Basado en el proyecto [MBeautifier](https://github.com/davidvarga/MBeautifier).

## Instalación

### Requisitos

- APIs del Desktop Editor de MATLAB (`matlab.desktop.editor`).
- APIs del Live Editor de MATLAB (`matlab.internal.liveeditor`) para la conversión `.mlx`.

### Descarga desde GitHub

1. Visite la [página de lanzamientos de GitHub](https://github.com/ruiyangzhou01/MATLAB-Utilities/releases).
2. En **Assets**, descargue los scripts `.m` o el archivo `.zip` que necesite.

### Añadir a la ruta de búsqueda de MATLAB

Añada la raíz del repositorio (o las carpetas `MWidgets` y `MBeautifier`) a la ruta de búsqueda de MATLAB.

## Uso

### Ventana de comandos

```matlab
AutoCdPath
OneMlx2M
MultiMlx2M
Beautifier
MBeautify.formatCurrentEditorPage()
```

### Favoritos y accesos directos

- Ejecute `Setup` desde la carpeta `MWidgets` para añadir favoritos con iconos a la barra de herramientas.
- MBeautifier también puede crear accesos directos para acciones de formato:

```matlab
MBeautify.createShortcut('editorpage')
MBeautify.createShortcut('editorselection')
MBeautify.createShortcut('file')
```

#### Favoritos manuales (opcional)

<img src="media/image-20210921110048305.png" alt="Agregar a Favoritos" style="zoom: 50%;" />

<img src="media/image-20210921110103753.png" alt="Editar Favoritos" style="zoom: 50%;" />

<img src="media/image-20210921110115227.png" alt="Editar comando de favoritos" style="zoom: 50%;" />

<img src="media/image-20210921110140550.png" alt="Resultado de favoritos" />

### Fuentes del Live Editor

Ejecute `LiveScriptCustomize` para aplicar la configuración de fuentes predeterminada del script.

## Licencia

[GPL-3.0 License](https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/LICENSE) © ruiyangzhou01
