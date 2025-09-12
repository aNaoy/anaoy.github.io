---
title: 'Cursor AI Code Editor Flaw Enables Silent Code Execution via Malicious Repositories'
date: 2025-09-12
permalink: /posts/2025/09/12/cursor-ai-code-editor-flaw-enables-silent-code-execution-via-malicious-repositories/
tags:
- veille-cyber
- hackernews
---
**Vulnérabilité dans Cursor AI et Risques Liés aux Outils IA de Développement**

Une faille de sécurité découverte dans l'éditeur de code IA Cursor permet l'exécution silencieuse de code malveillant. Cette vulnérabilité survient lorsqu'un dépôt spécialement conçu est ouvert dans Cursor, profitant de la désactivation par défaut de la fonctionnalité "Workspace Trust". Un fichier `.vscode/tasks.json` malveillant peut déclencher l'exécution de code arbitraire avec les privilèges de l'utilisateur, exposant potentiellement des identifiants sensibles et permettant des compromissions système.

Plusieurs autres outils et plateformes de développement assistés par IA font face à des menaces similaires, notamment des injections de prompts et des contournements de sécurité. Des vulnérabilités traditionnelles ont également été identifiées dans des extensions d'IDE comme Claude Code (CVE-2025-52882, CVSS 8.8), des serveurs MCP (injection SQL), et des plateformes comme Base44 (XSS, fuite de données). Ollama Desktop est également vulnérable à des attaques par drive-by.

**Points Clés :**

*   **Exécution de Code Silencieuse dans Cursor :** La désactivation par défaut de "Workspace Trust" permet à des dépôts malveillants d'exécuter du code sans alerte.
*   **Risques de Chaîne d'Approvisionnement :** Les vulnérabilités exploitent la confiance accordée aux dépôts de code, typique des attaques sur la chaîne d'approvisionnement logicielle.
*   **Menaces Généralisées sur les Outils IA :** Les injections de prompts, les fuites de données et les vulnérabilités classiques affectent divers outils d'IA de développement.

**Vulnérabilités (avec CVE si possible) :**

*   Exécution de code arbitraire via `.vscode/tasks.json` dans Cursor (pas de CVE spécifique mentionné pour Cursor lui-même).
*   **CVE-2025-52882 (Claude Code IDE extensions) :** Contournement d'authentification WebSocket permettant l'exécution de commandes à distance (CVSS 8.8).
*   Injection SQL dans le serveur Postgres MCP.
*   Traversée de répertoire dans Microsoft NLWeb.
*   **CVE-2025-48757 (Lovable) :** Vulnérabilité d'autorisation incorrecte permettant la lecture/écriture sur des tables de base de données arbitraires (CVSS 9.3).
*   Vulnérabilités (Open redirect, XSS, fuite de données sensibles) dans Base44.
*   Vulnérabilité dans Ollama Desktop (contrôles cross-origin incomplets) permettant des attaques par drive-by.

**Recommandations :**

*   **Activer "Workspace Trust" dans Cursor.**
*   Ouvrir les dépôts non fiables dans un éditeur de code différent ou les auditer avant de les ouvrir dans Cursor.
*   **Surveiller l'utilisation des fonctionnalités d'IA** et arrêter les actions inattendues.
*   Appliquer les correctifs de sécurité dès qu'ils sont disponibles.
*   Traiter la sécurité comme un élément fondamental, et non comme une réflexion après coup, dans l'écosystème des plateformes de développement.

---
[Source](https://thehackernews.com/2025/09/cursor-ai-code-editor-flaw-enables.html){:target="_blank"}
