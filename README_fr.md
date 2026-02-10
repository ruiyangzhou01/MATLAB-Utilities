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

MATLAB Utilities rassemble des scripts MATLAB orientés éditeur et le formateur de code MBeautifier pour accélérer les workflows quotidiens.

## Contenu

### Scripts MWidgets

- **AutoCdPath** (`MWidgets/AutoCdPath.m`) : Change le dossier courant vers le répertoire du fichier actif dans l'éditeur. Génère une erreur si aucun fichier n'est ouvert.
- **OneMlx2M** (`MWidgets/OneMlx2M.m`) : Convertit le Live Script `.mlx` actif en fichier `.m`.
- **MultiMlx2M** (`MWidgets/MultiMlx2M.m`) : Convertit tous les `.mlx` du dossier courant en `.m` (appelle d'abord `AutoCdPath`).
- **Beautifier** (`MWidgets/Beautifier.m`) : Formate le fichier `.m` actif via `MBeautify.formatCurrentEditorPage()`.
- **LiveScriptCustomize** (`MWidgets/LiveScriptCustomize.m`) : Configure les polices du Live Editor (code : JetBrains Mono, normal : Segoe UI, taille 14px).
- **Setup** (`MWidgets/Setup.m`) : Ajoute des Favoris MATLAB (catégorie `WIDGETS`) pour AutoCdPath, OneMlx2M, MultiMlx2M et Beautifier en utilisant les icônes de `icons/`.

### Formateur MBeautifier

- **Initialisation** : Exécutez `MBeautify.setup()` pour générer `MBeautifier/resources/settings/MBeautyConfigurationRules.m` à partir des règles XML.
- **Commandes de formatage** :
  - `MBeautify.formatCurrentEditorPage()` (utilisez `true` pour enregistrer)
  - `MBeautify.formatEditorSelection()` (utilisez `true` pour enregistrer)
  - `MBeautify.formatFile(file, outFile)`
  - `MBeautify.formatFiles(directory, fileFilter)`
- **Configuration** : Modifiez `MBeautifier/resources/settings/MBeautyConfigurationRules.xml`, puis relancez `MBeautify.setup()`.
- Basé sur le projet [MBeautifier](https://github.com/davidvarga/MBeautifier).

## Installation

### Prérequis

- APIs de l'éditeur MATLAB (`matlab.desktop.editor`).
- APIs du Live Editor MATLAB (`matlab.internal.liveeditor`) pour la conversion `.mlx`.

### Télécharger depuis GitHub

1. Rendez-vous sur la [page des releases GitHub](https://github.com/ruiyangzhou01/MATLAB-Utilities/releases).
2. Dans **Assets**, téléchargez les scripts `.m` ou l'archive `.zip` souhaités.

### Ajouter au chemin de recherche MATLAB

Ajoutez la racine du dépôt (ou les dossiers `MWidgets` et `MBeautifier`) au chemin de recherche MATLAB.

## Utilisation

### Fenêtre de commandes

```matlab
AutoCdPath
OneMlx2M
MultiMlx2M
Beautifier
MBeautify.formatCurrentEditorPage()
```

### Favoris et raccourcis

- Exécutez `Setup` dans le dossier `MWidgets` pour ajouter des favoris avec des icônes à la barre d'outils.
- MBeautifier peut aussi créer des raccourcis pour les actions de formatage :

```matlab
MBeautify.createShortcut('editorpage')
MBeautify.createShortcut('editorselection')
MBeautify.createShortcut('file')
```

#### Favoris manuels (optionnel)

<img src="media/image-20210921110048305.png" alt="Ajouter aux favoris" style="zoom: 50%;" />

<img src="media/image-20210921110103753.png" alt="Modifier les favoris" style="zoom: 50%;" />

<img src="media/image-20210921110115227.png" alt="Modifier la commande des favoris" style="zoom: 50%;" />

<img src="media/image-20210921110140550.png" alt="Résultat des favoris" />

### Polices du Live Editor

Exécutez `LiveScriptCustomize` pour appliquer les paramètres de police par défaut définis dans le script.

## Licence

[GPL-3.0 License](https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/LICENSE) © ruiyangzhou01
