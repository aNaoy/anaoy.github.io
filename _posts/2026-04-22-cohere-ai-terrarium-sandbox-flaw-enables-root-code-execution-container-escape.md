---
title: 'Cohere AI Terrarium Sandbox Flaw Enables Root Code Execution, Container Escape'
date: 2026-04-22
permalink: /posts/2026/04/22/cohere-ai-terrarium-sandbox-flaw-enables-root-code-execution-container-escape/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans le bac à sable Terrarium de Cohere AI

Une vulnérabilité critique a été identifiée dans **Terrarium**, un bac à sable open-source basé sur Python conçu pour isoler l'exécution de code non fiable via des conteneurs Docker. En raison de l'absence de maintenance du projet, ce défaut reste sans correctif officiel.

**Points clés :**
*   **Nature du risque :** L'exploitation permet d'échapper à l'isolation du bac à sable pour exécuter des commandes système arbitraires avec les privilèges `root` sur l'hôte.
*   **Mécanisme :** La faille repose sur une manipulation de la chaîne de prototypes JavaScript au sein de l'environnement Pyodide, permettant d'accéder aux objets de l'environnement hôte (Node.js).
*   **Impact :** Accès à des fichiers sensibles (ex: `/etc/passwd`), interaction avec d'autres services réseau et potentiel d'escalade de privilèges.

**Vulnérabilité identifiée :**
*   **CVE-2026-5752 :** Score CVSS de 9.3 (Critique).

**Recommandations :**
*   **Désactivation :** Suspendre les fonctionnalités permettant l'exécution de code utilisateur non fiable.
*   **Segmentation :** Isoler le réseau pour limiter les déplacements latéraux en cas de compromission.
*   **Sécurité des conteneurs :** Utiliser des outils d'orchestration sécurisés, restreindre les accès aux ressources et surveiller activement les comportements suspects au sein des conteneurs.
*   **Filtrage :** Déployer un pare-feu d'application web (WAF) pour détecter les tentatives d'exploitation.

---
[Source](https://thehackernews.com/2026/04/cohere-ai-terrarium-sandbox-flaw.html){:target="_blank"}
