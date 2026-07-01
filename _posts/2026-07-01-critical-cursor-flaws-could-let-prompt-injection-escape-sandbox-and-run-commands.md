---
title: 'Critical Cursor Flaws Could Let Prompt Injection Escape Sandbox and Run Commands'
date: 2026-07-01
permalink: /posts/2026/07/01/critical-cursor-flaws-could-let-prompt-injection-escape-sandbox-and-run-commands/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques "DuneSlide" dans l'éditeur Cursor

Deux vulnérabilités critiques, baptisées **DuneSlide**, permettent à un attaquant de s'échapper du bac à sable (sandbox) de l'éditeur IA Cursor et d'exécuter des commandes arbitraires sur la machine de l'utilisateur sans aucune interaction de sa part (attaque "zero-click").

**Points clés :**
*   **Vecteur d'attaque :** Injection de prompts via des sources externes (recherches web, services connectés via MCP) lues par l'agent IA.
*   **Impact :** L'attaquant obtient un accès complet au poste du développeur ainsi qu'aux accès liés aux sessions ouvertes dans l'éditeur.
*   **Historique :** Ces failles s'inscrivent dans une série récurrente de vulnérabilités affectant la sécurité des agents de codage IA.

**Vulnérabilités identifiées :**
*   **CVE-2026-50548 (Score CVSS 9.8/10) :** Abus du paramètre `working_directory`. L'agent peut forcer l'écriture dans des répertoires systèmes en manipulant le chemin de travail, permettant d'écraser des fichiers de configuration (ex: `~/.zshrc`) ou l'exécutable du sandbox lui-même.
*   **CVE-2026-50549 (Score CVSS 9.8/10) :** Contournement de la vérification de sécurité des liens symboliques. En provoquant l'échec de la résolution d'un chemin, l'éditeur fait confiance par défaut à un chemin malicieux pointant en dehors de la zone autorisée, permettant l'écrasement de fichiers critiques.

**Recommandations :**
*   **Mise à jour immédiate :** Passer impérativement à **Cursor 3.0** ou une version supérieure. Toutes les versions antérieures à la 3.0 sont vulnérables.
*   **Prudence avec l'IA :** Traiter les données issues de sources externes (web, MCP) comme des vecteurs d'attaque potentiels, même si aucune interaction manuelle n'est requise.

---
[Source](https://thehackernews.com/2026/07/critical-cursor-flaws-could-let-prompt.html){:target="_blank"}
