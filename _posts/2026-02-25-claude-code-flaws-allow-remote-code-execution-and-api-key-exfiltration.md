---
title: 'Claude Code Flaws Allow Remote Code Execution and API Key Exfiltration'
date: 2026-02-25
permalink: /posts/2026/02/25/claude-code-flaws-allow-remote-code-execution-and-api-key-exfiltration/
tags:
- veille-cyber
- hackernews
---
### Failles Critiques dans Claude Code Permettant l'Exécution de Code à Distance et le Vol d'Identifiants API

Des chercheurs en cybersécurité ont identifié plusieurs vulnérabilités dans Claude Code, l'assistant de codage d'Anthropic. Ces failles, exploitant des configurations telles que les Hooks, les serveurs MCP et les variables d'environnement, peuvent permettre à des attaquants d'exécuter des commandes arbitraires et de dérober des clés API Anthropic.

**Points Clés :**

*   L'ouverture de dépôts de code non fiables peut conduire à l'exécution de code à distance sans consentement de l'utilisateur ou via un contournement de celui-ci.
*   Des informations sensibles, notamment des clés API Anthropic, peuvent être exfiltrées par des dépôts malveillants.
*   Ces vulnérabilités transforment le modèle de menace : le simple fait d'ouvrir un projet non fiable devient un risque.

**Vulnérabilités Identifiées :**

*   **Sans CVE** (Score CVSS : 8.7) : Une vulnérabilité d'injection de code permettant l'exécution de code arbitraire sans confirmation supplémentaire via les hooks de projet définis dans `.claude/settings.json`. Contourne le consentement de l'utilisateur.
*   **CVE-2025-59536** (Score CVSS : 8.7) : Permet l'exécution de commandes shell arbitraires automatiquement lors de l'initialisation de l'outil dans un répertoire non fiable.
*   **CVE-2026-21852** (Score CVSS : 5.3) : Une vulnérabilité de divulgation d'informations qui permet à un dépôt malveillant d'exfiltrer des données, y compris les clés API Anthropic, lors du chargement d'un projet. L'exfiltration peut se produire avant l'affichage de l'invite de confiance, notamment si la variable `ANTHROPIC_BASE_URL` est configurée de manière malveillante.

**Recommandations :**

*   Les utilisateurs devraient faire preuve d'une extrême prudence lors de l'ouverture de dépôts de code provenant de sources non fiables.
*   La mise à jour de Claude Code vers les dernières versions corrigeant ces vulnérabilités est essentielle (versions 1.0.87, 1.0.111 et 2.0.65 mentionnées comme étant corrigées).
*   Une vigilance accrue est nécessaire concernant les fichiers de configuration qui, avec les capacités d'exécution autonome des outils IA, font désormais partie de la couche d'exécution et influencent directement le comportement du système.

---
[Source](https://thehackernews.com/2026/02/claude-code-flaws-allow-remote-code.html){:target="_blank"}
