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

MATLAB Utilities ist eine Sammlung von Hilfsskripten, die gängige Entwicklungsaufgaben und Editor-Workflows in MATLAB vereinfachen.

## Enthaltene Werkzeuge

### `AutoCdPath`

- Datei: `AutoCdPath.m`
- Zweck: Ändert das aktuelle Verzeichnis automatisch auf den Ordner der aktiven Datei.
- Befehl: `AutoCdPath`

### `OneMlx2M`

- Datei: `OneMlx2M.m`
- Zweck: Konvertiert das aktuelle `.mlx` Live Script in eine `.m`-Datei.
- Befehl: `OneMlx2M`

### `MultiMlx2M`

- Datei: `MultiMlx2M.m`
- Zweck: Konvertiert alle `.mlx`-Dateien im aktuellen Ordner in `.m`-Dateien.
- Befehl: `MultiMlx2M`

### `MBeautifier`

- Ordner: `MBeautifier`
- Zweck: Ein MATLAB-Quellcode-Formatter/Beautifier, der in den MATLAB-Editor integriert und konfigurierbar ist.
- Befehl: `MBeautify.formatCurrentEditorPage()`
- Hinweis: Basiert auf dem [MBeautifier](https://github.com/davidvarga/MBeautifier) Projekt.

## Installation

### Voraussetzungen

MATLAB R2013b oder neuer.

### Download von GitHub

1. Öffnen Sie die [GitHub-Releases-Seite](https://github.com/ruiyangzhou01/MATLAB-Utilities/releases).
2. Unter **Assets** laden Sie die gewünschten `.m`-Skripte oder das `.zip`-Archiv herunter.

### Zum MATLAB-Suchpfad hinzufügen

Fügen Sie den Ordner mit den Skripten zum MATLAB-Suchpfad hinzu.

## Verwendung

Es gibt mehrere Möglichkeiten, diese Werkzeuge zu verwenden.

### 1. Befehlsfenster

Geben Sie die Befehle direkt im Command Window ein.

Zum Beispiel können Sie mit folgendem Befehl in das Verzeichnis der aktiven Datei wechseln:

```matlab
AutoCdPath
```

Sie sehen eine Meldung wie:

```matlab
AutoCdPath to "C:\Users\username\Documents\Scripts".
```

### 2. Zu Favoriten hinzufügen (Klick-und-los)

#### Zu Favoriten hinzufügen

<img src="media/image-20210921110048305.png" alt="Zu Favoriten hinzufügen" style="zoom: 50%;" />

#### Favoriten bearbeiten

<img src="media/image-20210921110103753.png" alt="Favoriten bearbeiten" style="zoom: 50%;" />

<img src="media/image-20210921110115227.png" alt="Favoritenbefehl bearbeiten" style="zoom: 50%;" />

#### Ergebnis

<img src="media/image-20210921110140550.png" alt="Favoriten Ergebnis" />

### 3. In das Projekt einbinden

Fügen Sie die benötigten Skripte in Ihr Projekt ein oder rufen Sie sie aus eigenen Skripten auf.

## Lizenz

[GPL-3.0 License](https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/LICENSE) © ruiyangzhou01
