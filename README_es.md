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

MATLAB Utilities es un conjunto de scripts de ayuda que agilizan tareas comunes de desarrollo y flujos de trabajo del editor en MATLAB.

## Utilidades incluidas

### `AutoCdPath`

- Archivo: `AutoCdPath.m`
- Propósito: Cambia automáticamente el directorio actual a la carpeta del archivo activo.
- Comando: `AutoCdPath`

### `OneMlx2M`

- Archivo: `OneMlx2M.m`
- Propósito: Convierte el Live Script `.mlx` actual en un archivo `.m`.
- Comando: `OneMlx2M`

### `MultiMlx2M`

- Archivo: `MultiMlx2M.m`
- Propósito: Convierte todos los archivos `.mlx` de la carpeta actual en archivos `.m`.
- Comando: `MultiMlx2M`

### `MBeautifier`

- Carpeta: `MBeautifier`
- Propósito: Un formateador/embellecedor de código fuente de MATLAB, integrado en el editor y configurable.
- Comando: `MBeautify.formatCurrentEditorPage()`
- Nota: Basado en el proyecto [MBeautifier](https://github.com/davidvarga/MBeautifier).

## Instalación

### Requisitos

MATLAB R2013b o posterior.

### Descarga desde GitHub

1. Visite la [página de lanzamientos de GitHub](https://github.com/ruiyangzhou01/MATLAB-Utilities/releases).
2. En **Assets**, descargue los scripts `.m` o el archivo `.zip` que necesite.

### Añadir a la ruta de búsqueda de MATLAB

Añada la carpeta que contiene los scripts a la ruta de búsqueda de MATLAB.

## Uso

Hay varias formas de usar estas utilidades.

### 1. Ventana de comandos

Ingrese los comandos directamente en la ventana de comandos.

Por ejemplo, para cambiar al directorio del archivo activo, ejecute:

```matlab
AutoCdPath
```

Verá un mensaje similar a:

```matlab
AutoCdPath to "C:\Users\username\Documents\Scripts".
```

### 2. Agregar a Favoritos para uso con un clic

#### Agregar a Favoritos

<img src="media/image-20210921110048305.png" alt="Agregar a Favoritos" style="zoom: 50%;" />

#### Editar Favoritos

<img src="media/image-20210921110103753.png" alt="Editar Favoritos" style="zoom: 50%;" />

<img src="media/image-20210921110115227.png" alt="Editar comando de favoritos" style="zoom: 50%;" />

#### Resultado

<img src="media/image-20210921110140550.png" alt="Resultado de favoritos" />

### 3. Incluir las utilidades en su proyecto

Copie los scripts necesarios en su proyecto o llámelos desde sus propios scripts.

## Licencia

[GPL-3.0 License](https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/LICENSE) © ruiyangzhou01
