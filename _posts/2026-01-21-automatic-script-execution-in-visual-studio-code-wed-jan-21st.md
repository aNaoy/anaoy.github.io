---
title: 'Automatic Script Execution In Visual Studio Code, (Wed, Jan 21st)'
date: 2026-01-21
permalink: /posts/2026/01/21/automatic-script-execution-in-visual-studio-code-wed-jan-21st/
tags:
- veille-cyber
- sans-isc
---
### Exécution Automatique de Scripts dans Visual Studio Code

Visual Studio Code, un éditeur de code populaire et une plateforme de développement complète, peut être ciblé par des acteurs malveillants via ses extensions. Une méthode exploitée consiste à utiliser la fonctionnalité d'exécution automatique de tâches définie dans un fichier `tasks.json` situé dans le répertoire `.vscode` d'un projet.

Le paramètre `"runOn": "folderOpen"` dans ce fichier permet de déclencher automatiquement un script (ici, une commande PowerShell encodée en Base64) dès l'ouverture du dossier du projet dans VSCode. Bien que l'exemple présenté affiche une simple boîte de message, cette technique peut être utilisée pour exécuter des commandes malveillantes sans intervention de l'utilisateur. Des acteurs malveillants ont déjà exploité des méthodes similaires.

**Points Clés :**

*   Visual Studio Code est une cible pour les acteurs malveillants en raison de sa popularité et de son extensibilité.
*   Le fichier `.vscode/tasks.json` permet de configurer des tâches automatiques.
*   L'option `"runOn": "folderOpen"` déclenche des scripts à l'ouverture du projet.
*   L'utilisation de scripts encodés (comme le Base64) peut servir à masquer des actions malveillantes.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (CVE) n'est explicitement mentionnée dans cet article, mais la fonctionnalité d'exécution automatique de scripts via `.vscode/tasks.json` est décrite comme une méthode d'exploitation potentielle.

**Recommandations :**

*   Soyez vigilant face aux répertoires `.vscode` inattendus dans vos projets.
*   Examinez attentivement le contenu des fichiers de configuration de tâches, en particulier ceux qui déclenchent des scripts lors de l'ouverture de dossiers.

---
[Source](https://isc.sans.edu/diary/rss/32644){:target="_blank"}
