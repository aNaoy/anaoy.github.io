---
title: 'Amazon Q Developer Flaw Could Let Malicious Repos Run Code via MCP Configs'
date: 2026-06-26
permalink: /posts/2026/06/26/amazon-q-developer-flaw-could-let-malicious-repos-run-code-via-mcp-configs/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans Amazon Q Developer : Risque d'exécution de code via les fichiers MCP

Une faille de sécurité majeure dans l'assistant de codage Amazon Q permettait à des attaquants d'exécuter des commandes arbitraires et de dérober les identifiants cloud d'un développeur simplement en lui faisant ouvrir un dépôt Git malveillant.

**Points clés :**
*   **Mécanisme d'attaque :** Amazon Q lisait automatiquement un fichier de configuration (`.amazonq/mcp.json`) présent dans le répertoire de travail. Ce fichier permettait de lancer des serveurs MCP (Model Context Protocol), qui s'exécutaient avec les privilèges du développeur (clés AWS, jetons CLI, secrets API).
*   **Impact :** Un attaquant pouvait capturer une session cloud active pour accéder aux services internes, créer des portes dérobées ou compromettre l'infrastructure de production sans aucune interaction supplémentaire.
*   **Contexte :** Cette vulnérabilité met en lumière les risques liés à l'exécution automatique de configurations basées sur des projets, un vecteur d'attaque déjà observé sur d'autres outils comme Claude Code, Cursor et Windsurf.

**Vulnérabilités identifiées :**
*   **CVE-2026-12957 (CVSS 8.5) :** Absence de contrôle de consentement explicite lors du lancement de serveurs MCP, permettant l'exécution de code à distance.
*   **CVE-2026-12958 :** Absence de vérification des liens symboliques, permettant potentiellement l'écriture de fichiers arbitraires en dehors du périmètre de confiance du projet.

**Recommandations :**
*   **Mise à jour immédiate :** Installez la version 1.69.0 du composant "Language Servers for AWS".
*   **Versions minimales requises :**
    *   **VS Code :** 2.20 ou supérieur.
    *   **JetBrains :** 4.3 ou supérieur.
    *   **Eclipse :** 2.7.4 ou supérieur.
    *   **Visual Studio :** 1.94.0.0 ou supérieur.
*   **Prudence :** Redémarrez vos IDE pour forcer la mise à jour et restez vigilant face aux fichiers de configuration contenus dans les dépôts de code provenant de sources non fiables.

---
[Source](https://thehackernews.com/2026/06/amazon-q-developer-flaw-could-let.html){:target="_blank"}
