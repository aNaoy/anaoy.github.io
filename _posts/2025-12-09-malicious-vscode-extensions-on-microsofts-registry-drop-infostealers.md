---
title: 'Malicious VSCode extensions on Microsofts registry drop infostealers'
date: 2025-12-09
permalink: /posts/2025/12/09/malicious-vscode-extensions-on-microsofts-registry-drop-infostealers/
tags:
- veille-cyber
- bleepingcomp
---
### Extensions Malveillantes VS Code Volent des Informations

Deux extensions pour Visual Studio Code, "Bitcoin Black" et "Codo AI", ont été découvertes sur le marketplace de Microsoft, déguisées en thèmes de couleurs et en assistants IA respectivement. Ces extensions contenaient des logiciels espions conçus pour voler des informations sensibles sur les machines des développeurs.

**Points Clés :**

*   Les extensions malveillantes distribuaient un exécutable légitime (Lightshot) et un fichier DLL malveillant.
*   Ce DLL détournait la technique du "DLL hijacking" pour exécuter un logiciel espion nommé `runtime.exe`.
*   Le logiciel espion créait un répertoire "Evelyn" dans `%APPDATA%\Local\` pour stocker les données volées.
*   Il pouvait effectuer des captures d'écran, voler des identifiants, des portefeuilles de cryptomonnaies, et intercepter les sessions de navigation web.
*   Les extensions utilisaient des scripts pour télécharger le code malveillant de manière discrète, souvent sans afficher de fenêtre visible.
*   Microsoft a été contacté et a depuis retiré ces extensions du marketplace.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec identifiant CVE n'est mentionnée directement dans l'article pour les extensions elles-mêmes, mais le mécanisme exploité repose sur :

*   **L'ingénierie sociale / tromperie :** Les extensions se faisaient passer pour des outils légitimes.
*   **DLL Hijacking :** Technique exploitant la manière dont Windows charge les DLLs.

**Recommandations :**

*   Installer des extensions uniquement à partir d'éditeurs réputés.
*   Être vigilant face aux comportements inhabituels ou aux fonctionnalités inattendues des extensions (par exemple, l'exécution de scripts PowerShell ou batch par un thème de couleurs).
*   Surveiller la présence de répertoires suspects ou d'activités réseau inhabituelles sur les machines de développement.

---
[Source](https://www.bleepingcomputer.com/news/security/malicious-vscode-extensions-on-microsofts-registry-drop-infostealers/){:target="_blank"}
