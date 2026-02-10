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

MATLAB Utilities est un ensemble de scripts d'aide qui simplifient les tâches de développement courantes et les workflows de l'éditeur MATLAB.

## Utilitaires inclus

### `AutoCdPath`

- Fichier : `AutoCdPath.m`
- Objectif : Change automatiquement le répertoire courant vers le dossier du fichier actif.
- Commande : `AutoCdPath`

### `OneMlx2M`

- Fichier : `OneMlx2M.m`
- Objectif : Convertit le Live Script `.mlx` actuel en un fichier `.m`.
- Commande : `OneMlx2M`

### `MultiMlx2M`

- Fichier : `MultiMlx2M.m`
- Objectif : Convertit tous les fichiers `.mlx` du dossier courant en fichiers `.m`.
- Commande : `MultiMlx2M`

### `MBeautifier`

- Dossier : `MBeautifier`
- Objectif : Un formatteur/embellisseur de code source MATLAB, intégré à l'éditeur et configurable.
- Commande : `MBeautify.formatCurrentEditorPage()`
- Note : Basé sur le projet [MBeautifier](https://github.com/davidvarga/MBeautifier).

## Installation

### Prérequis

MATLAB R2013b ou version ultérieure.

### Télécharger depuis GitHub

1. Rendez-vous sur la [page des releases GitHub](https://github.com/ruiyangzhou01/MATLAB-Utilities/releases).
2. Dans **Assets**, téléchargez les scripts `.m` ou l'archive `.zip` souhaités.

### Ajouter au chemin de recherche MATLAB

Ajoutez le dossier contenant les scripts au chemin de recherche MATLAB.

## Utilisation

Il existe plusieurs façons d'utiliser ces utilitaires.

### 1. Fenêtre de commandes

Saisissez les commandes directement dans la fenêtre de commandes.

Par exemple, pour passer au répertoire du fichier actif, exécutez :

```matlab
AutoCdPath
```

Vous verrez un message similaire à :

```matlab
AutoCdPath to "C:\Users\username\Documents\Scripts".
```

### 2. Ajouter aux favoris pour un accès en un clic

#### Ajouter aux favoris

<img src="media/image-20210921110048305.png" alt="Ajouter aux favoris" style="zoom: 50%;" />

#### Modifier les favoris

<img src="media/image-20210921110103753.png" alt="Modifier les favoris" style="zoom: 50%;" />

<img src="media/image-20210921110115227.png" alt="Modifier la commande des favoris" style="zoom: 50%;" />

#### Résultat

<img src="media/image-20210921110140550.png" alt="Résultat des favoris" />

### 3. Inclure les utilitaires dans votre projet

Copiez les scripts nécessaires dans votre projet ou appelez-les depuis vos propres scripts.

## Licence

[GPL-3.0 License](https://github.com/ruiyangzhou01/MATLAB-Utilities/blob/main/LICENSE) © ruiyangzhou01
