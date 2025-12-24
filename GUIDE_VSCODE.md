# Guide de Connexion VS Code

Ce guide vous montre comment configurer et utiliser Visual Studio Code pour le développement.

## 📋 Table des matières

1. [Installation de VS Code](#installation-de-vs-code)
2. [Cloner votre dépôt GitHub](#cloner-votre-dépôt-github)
3. [Connexion à distance (Remote SSH)](#connexion-à-distance-remote-ssh)
4. [Extensions recommandées](#extensions-recommandées)

---

## 🔧 Installation de VS Code

### Windows
1. Téléchargez VS Code depuis [code.visualstudio.com](https://code.visualstudio.com/)
2. Exécutez l'installateur
3. Suivez les instructions d'installation

### macOS
1. Téléchargez VS Code depuis [code.visualstudio.com](https://code.visualstudio.com/)
2. Ouvrez le fichier `.dmg`
3. Glissez VS Code dans Applications

### Linux
```bash
# Ubuntu/Debian
sudo apt update
sudo apt install code

# Ou téléchargez depuis le site officiel
wget -O vscode.deb 'https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64'
sudo dpkg -i vscode.deb
```

---

## 📦 Cloner votre dépôt GitHub

### Méthode 1 : Depuis VS Code (Recommandée)

1. **Ouvrez VS Code**
2. **Ouvrez la palette de commandes** : `Ctrl+Shift+P` (Windows/Linux) ou `Cmd+Shift+P` (macOS)
3. **Tapez** : `Git: Clone`
4. **Entrez l'URL** de votre dépôt :
   ```
   https://github.com/KouroumaAs/KouroumaAs.git
   ```
5. **Sélectionnez** le dossier de destination
6. **Ouvrez** le dépôt cloné

### Méthode 2 : Ligne de commande

```bash
# Cloner le dépôt
git clone https://github.com/KouroumaAs/KouroumaAs.git

# Ouvrir dans VS Code
cd KouroumaAs
code .
```

---

## 🌐 Connexion à distance (Remote SSH)

VS Code permet de se connecter à des serveurs distants via SSH.

### Prérequis
- Un serveur distant avec SSH activé
- Vos identifiants SSH

### Installation de l'extension Remote SSH

1. **Ouvrez VS Code**
2. **Allez dans Extensions** : `Ctrl+Shift+X`
3. **Recherchez** : `Remote - SSH`
4. **Installez** l'extension de Microsoft

### Configuration de la connexion SSH

1. **Ouvrez la palette de commandes** : `Ctrl+Shift+P`
2. **Tapez** : `Remote-SSH: Connect to Host`
3. **Sélectionnez** : `Configure SSH Hosts...`
4. **Choisissez** votre fichier de configuration SSH (généralement `~/.ssh/config`)

### Ajouter votre serveur

Ajoutez cette configuration dans votre fichier `~/.ssh/config` :

```ssh
Host mon-serveur
    HostName adresse.du.serveur.com
    User votre-nom-utilisateur
    Port 22
    IdentityFile ~/.ssh/id_rsa
```

### Se connecter

1. **Palette de commandes** : `Ctrl+Shift+P`
2. **Tapez** : `Remote-SSH: Connect to Host`
3. **Sélectionnez** votre serveur
4. **Entrez** votre mot de passe si demandé

---

## 🔌 Extensions recommandées

### Pour le développement C++

```
C/C++ (Microsoft)
C/C++ Extension Pack
CMake Tools
```

### Pour Git

```
GitLens
Git History
Git Graph
```

### Installation rapide

1. **Ouvrez Extensions** : `Ctrl+Shift+X`
2. **Recherchez** le nom de l'extension
3. **Cliquez** sur Install

Ou utilisez la ligne de commande :

```bash
# C++
code --install-extension ms-vscode.cpptools
code --install-extension ms-vscode.cpptools-extension-pack

# Git
code --install-extension eamodio.gitlens
code --install-extension donjayamanne.githistory
```

---

## 💡 Astuces utiles

### Raccourcis clavier essentiels

- **Palette de commandes** : `Ctrl+Shift+P`
- **Terminal intégré** : `Ctrl+` `
- **Explorateur de fichiers** : `Ctrl+Shift+E`
- **Recherche** : `Ctrl+Shift+F`
- **Contrôle de source (Git)** : `Ctrl+Shift+G`

### Utiliser le terminal intégré

1. **Ouvrez le terminal** : `Ctrl+` `
2. **Exécutez vos commandes** git, compilations, etc.

```bash
# Exemple pour C++
g++ main.cpp -o programme
./programme
```

### Synchroniser vos paramètres

1. **Connectez-vous** avec votre compte GitHub/Microsoft
2. **Palette de commandes** : `Settings Sync: Turn On`
3. Vos paramètres seront synchronisés entre appareils

---

## 📞 Besoin d'aide ?

- **Email** : boubasid2000@yahoo.fr
- **Documentation VS Code** : [code.visualstudio.com/docs](https://code.visualstudio.com/docs)
- **Remote SSH** : [code.visualstudio.com/docs/remote/ssh](https://code.visualstudio.com/docs/remote/ssh)

---

## 🚀 Prochaines étapes

1. ✅ Installer VS Code
2. ✅ Cloner votre dépôt
3. ✅ Installer les extensions C++
4. ✅ Commencer à coder !

Bon développement ! 🎉
