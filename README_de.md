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

MATLAB Utilities sammelt editorbezogene MATLAB-Skripte und den MBeautifier-Code-Formatter, um tägliche Workflows zu beschleunigen.

## Inhalt

### MWidgets-Skripte

- **AutoCdPath** (`MWidgets/AutoCdPath.m`): Wechselt das aktuelle Arbeitsverzeichnis in den Ordner der aktiven Editor-Datei. Gibt einen Fehler aus, wenn keine Datei geöffnet ist.
- **OneMlx2M** (`MWidgets/OneMlx2M.m`): Konvertiert das aktuell geöffnete `.mlx` Live Script in eine `.m`-Datei.
- **MultiMlx2M** (`MWidgets/MultiMlx2M.m`): Konvertiert alle `.mlx`-Dateien im aktuellen Ordner in `.m`-Dateien (ruft zuvor `AutoCdPath` auf).
- **Beautifier** (`MWidgets/Beautifier.m`): Formatiert die aktive `.m`-Datei, indem `MBeautify.formatCurrentEditorPage()` aufgerufen wird.
- **LiveScriptCustomize** (`MWidgets/LiveScriptCustomize.m`): Setzt Live-Editor-Schriften (Code: JetBrains Mono, normal: Segoe UI, Größe 14px).
- **Setup** (`MWidgets/Setup.m`): Fügt MATLAB-Favoriten (Kategorie `WIDGETS`) für AutoCdPath, OneMlx2M, MultiMlx2M und Beautifier hinzu und verwendet Symbole aus `icons/`.

### MBeautifier-Formatter

- **Einrichtung**: Führen Sie `MBeautify.setup()` einmal aus, um `MBeautifier/resources/settings/MBeautyConfigurationRules.m` aus den XML-Regeln zu erzeugen.
- **Formatierbefehle**:
  - `MBeautify.formatCurrentEditorPage()` (mit `true` speichern)
  - `MBeautify.formatEditorSelection()` (mit `true` speichern)
  - `MBeautify.formatFile(file, outFile)`
  - `MBeautify.formatFiles(directory, fileFilter)`
- **Konfiguration**: Bearbeiten Sie `MBeautifier/resources/settings/MBeautyConfigurationRules.xml` und führen Sie `MBeautify.setup()` erneut aus.
- Basiert auf dem Projekt [MBeautifier](https://github.com/davidvarga/MBeautifier).

## Installation

### Voraussetzungen

- MATLAB-Desktop-Editor-APIs (`matlab.desktop.editor`).
- MATLAB-Live-Editor-APIs (`matlab.internal.liveeditor`) für die `.mlx`-Konvertierung.

### Download von GitHub

1. Öffnen Sie die [GitHub-Releases-Seite](https://github.com/ruiyangzhou01/MATLAB-Utilities/releases).
2. Unter **Assets** laden Sie die gewünschten `.m`-Skripte oder das `.zip`-Archiv herunter.

### Zum MATLAB-Suchpfad hinzufügen

Fügen Sie das Repository-Root (oder die Ordner `MWidgets` und `MBeautifier`) zum MATLAB-Suchpfad hinzu.

## Verwendung

### Befehlsfenster

```matlab
AutoCdPath
OneMlx2M
MultiMlx2M
Beautifier
MBeautify.formatCurrentEditorPage()
```

### Favoriten und Shortcuts

- Führen Sie `Setup` im Ordner `MWidgets` aus, um Favoriten mit Symbolen zur Werkzeugleiste hinzuzufügen.
- MBeautifier kann außerdem Shortcuts für Formatieraktionen erstellen:

```matlab
MBeautify.createShortcut('editorpage')
MBeautify.createShortcut('editorselection')
MBeautify.createShortcut('file')
```

#### Manuelle Favoriten (optional)

<img src="media/image-20210921110048305.png" alt="Zu Favoriten hinzufügen" style="zoom: 50%;" />

<img src="media/image-20210921110103753.png" alt="Favoriten bearbeiten" style="zoom: 50%;" />

<img src="media/image-20210921110115227.png" alt="Favoritenbefehl bearbeiten" style="zoom: 50%;" />

<img src="media/image-20210921110140550.png" alt="Favoriten Ergebnis" />

### Live-Editor-Schriftarten

Führen Sie `LiveScriptCustomize` aus, um die Standard-Schriftarteinstellungen aus dem Skript anzuwenden.

## Lizenz

[GPL-3.0 License](https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/LICENSE) © ruiyangzhou01
