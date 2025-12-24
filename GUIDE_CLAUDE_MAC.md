# Guide d'installation de Claude Code sur Mac

Ce guide vous montre comment installer et utiliser Claude Code avec VS Code sur votre Mac.

## 🤖 Qu'est-ce que Claude Code ?

Claude Code est un assistant IA développé par Anthropic qui s'intègre directement dans votre terminal et VS Code pour vous aider à :
- Écrire du code
- Déboguer des problèmes
- Comprendre votre codebase
- Automatiser des tâches de développement

---

## 📋 Prérequis

- ✅ macOS (vous l'avez déjà !)
- ✅ VS Code installé (vous l'avez déjà !)
- ✅ Un compte Anthropic (gratuit ou Pro)
- ✅ Terminal

---

## 🔧 Installation de Claude Code

### Étape 1 : Installer Claude Code CLI

Ouvrez votre Terminal sur Mac et exécutez :

```bash
# Installer avec npm (recommandé)
npm install -g @anthropic-ai/claude-code

# OU installer avec Homebrew
brew install anthropic-ai/tap/claude-code
```

### Étape 2 : Vérifier l'installation

```bash
claude --version
```

Vous devriez voir le numéro de version s'afficher.

### Étape 3 : Authentification

```bash
# Lancer la configuration
claude auth login
```

Cela ouvrira votre navigateur pour vous connecter avec votre compte Anthropic.

---

## 🔌 Intégration avec VS Code

### Option 1 : Extension Claude Code (Recommandée)

1. **Ouvrez VS Code**
2. **Allez dans Extensions** : `Cmd+Shift+X`
3. **Recherchez** : `Claude Code`
4. **Installez** l'extension officielle d'Anthropic
5. **Connectez-vous** avec votre compte Anthropic

### Option 2 : Terminal intégré de VS Code

1. **Ouvrez VS Code**
2. **Ouvrez le terminal intégré** : `Ctrl+` ` (ou `Cmd+` `)
3. **Lancez Claude Code** :

```bash
# Ouvrir Claude Code dans le dossier actuel
claude code

# Ou avec un prompt spécifique
claude code "aide-moi à créer un programme C++"
```

---

## 🚀 Utilisation de Claude Code

### Démarrer une session

Depuis votre terminal VS Code :

```bash
# Dans votre dossier de projet
cd ~/chemin/vers/votre/projet

# Lancer Claude Code
claude code
```

### Commandes utiles

```bash
# Démarrer une conversation
claude code "explique-moi ce fichier main.cpp"

# Générer du code
claude code "crée un programme C++ pour trier un tableau"

# Déboguer
claude code "pourquoi mon programme ne compile pas ?"

# Mode interactif
claude code
# Puis tapez vos questions directement
```

### Exemples d'utilisation pour C++

```bash
# Aide sur la compilation
claude code "comment compiler mon projet C++ ?"

# Debugging
claude code "trouve l'erreur dans mon code C++"

# Optimisation
claude code "optimise cette fonction de tri"

# Apprentissage
claude code "explique-moi les pointeurs en C++"
```

---

## ⚙️ Configuration avancée

### Créer un alias pour Claude Code

Ajoutez à votre `~/.zshrc` ou `~/.bash_profile` :

```bash
# Alias pour Claude Code
alias cc='claude code'
alias cchelp='claude code --help'
```

Puis rechargez :

```bash
source ~/.zshrc  # pour zsh
# ou
source ~/.bash_profile  # pour bash
```

Maintenant vous pouvez utiliser :
```bash
cc "aide-moi avec mon code"
```

### Configuration du projet

Créez un fichier `.claude/config.json` dans votre projet :

```json
{
  "project": "Mon projet C++",
  "language": "cpp",
  "preferences": {
    "style": "detailed",
    "language": "fr"
  }
}
```

---

## 💡 Astuces pour VS Code + Claude Code

### 1. Terminal divisé

- **Divisez le terminal** : Cliquez sur l'icône de division dans le terminal
- **Un terminal** pour Claude Code
- **Un autre** pour vos commandes habituelles (git, compilation, etc.)

### 2. Raccourcis personnalisés

Dans VS Code, créez un raccourci pour lancer Claude Code :

1. `Cmd+K Cmd+S` pour ouvrir les raccourcis clavier
2. Recherchez "Terminal: Run Selected Text"
3. Assignez un raccourci (ex: `Cmd+Shift+C`)

### 3. Intégration avec Git

Claude Code peut vous aider avec Git :

```bash
claude code "explique-moi ces changements git"
claude code "écris un bon message de commit"
claude code "résous ce conflit de merge"
```

---

## 🎯 Exemples pratiques pour votre apprentissage C++

### Créer un nouveau projet

```bash
# Demandez à Claude de créer la structure
claude code "crée un projet C++ avec Makefile pour un programme de gestion d'étudiants"
```

### Comprendre du code existant

```bash
# Analysez du code
claude code "explique-moi ce que fait ce code C++"
```

### Déboguer

```bash
# Trouvez les erreurs
claude code "pourquoi j'ai une erreur de segmentation ?"
```

### Apprendre

```bash
# Posez des questions
claude code "quelle est la différence entre new et malloc en C++ ?"
```

---

## 🔑 Commandes Claude Code essentielles

| Commande | Description |
|----------|-------------|
| `claude code` | Démarrer une session interactive |
| `claude auth login` | Se connecter à votre compte |
| `claude auth logout` | Se déconnecter |
| `claude --help` | Voir toutes les commandes |
| `claude --version` | Voir la version |

---

## 🆘 Dépannage

### Claude Code ne se lance pas

```bash
# Vérifier l'installation
which claude

# Réinstaller si nécessaire
npm uninstall -g @anthropic-ai/claude-code
npm install -g @anthropic-ai/claude-code
```

### Problèmes d'authentification

```bash
# Se déconnecter et reconnecter
claude auth logout
claude auth login
```

### Permissions refusées

```bash
# Sur Mac, vous pourriez avoir besoin de sudo
sudo npm install -g @anthropic-ai/claude-code
```

---

## 📚 Ressources supplémentaires

- **Documentation officielle** : [docs.anthropic.com](https://docs.anthropic.com)
- **VS Code + Claude** : [code.visualstudio.com/docs](https://code.visualstudio.com/docs)
- **Votre email** : boubasid2000@yahoo.fr

---

## 🎓 Workflow recommandé pour apprendre C++

1. **Ouvrez VS Code** dans votre dossier de projet
2. **Lancez le terminal** : `Cmd+` `
3. **Démarrez Claude Code** : `claude code`
4. **Posez vos questions** sur C++ au fur et à mesure
5. **Testez le code** suggéré par Claude
6. **Itérez et apprenez** !

---

## ✨ Exemple de session complète

```bash
# 1. Ouvrir VS Code dans votre projet
cd ~/Documents/MesProjetsC++
code .

# 2. Dans le terminal VS Code
claude code

# 3. Conversation avec Claude
> Aide-moi à créer un programme C++ qui lit des nombres et calcule leur moyenne

# 4. Claude génère le code, vous le testez
g++ moyenne.cpp -o moyenne
./moyenne

# 5. Si problème, demandez à Claude
> J'ai une erreur "undefined reference to...", que faire ?

# 6. Claude vous aide à corriger
# Et ainsi de suite !
```

---

## 🎉 Vous êtes prêt !

Maintenant vous pouvez :
- ✅ Utiliser Claude Code depuis VS Code
- ✅ Poser des questions en français
- ✅ Apprendre C++ avec un assistant IA
- ✅ Déboguer et améliorer votre code

**Bon codage avec Claude ! 🚀**

---

## 📞 Besoin d'aide ?

- **Email** : boubasid2000@yahoo.fr
- **Documentation** : [docs.anthropic.com](https://docs.anthropic.com)
- **Support Claude** : support@anthropic.com
