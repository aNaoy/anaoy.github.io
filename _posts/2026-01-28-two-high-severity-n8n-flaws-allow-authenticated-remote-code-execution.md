---
title: 'Two High-Severity n8n Flaws Allow Authenticated Remote Code Execution'
date: 2026-01-28
permalink: /posts/2026/01/28/two-high-severity-n8n-flaws-allow-authenticated-remote-code-execution/
tags:
- veille-cyber
- hackernews
---
**Exploitation de failles critiques dans n8n : Exécution de code à distance**

Deux vulnérabilités importantes ont été découvertes dans la plateforme d'automatisation de flux de travail n8n, permettant à des utilisateurs authentifiés d'exécuter du code à distance.

**Points clés :**

*   Ces failles permettent à un attaquant de prendre le contrôle total d'une instance n8n, y compris en mode "interne", qui est déconseillé en production.
*   n8n étant souvent connecté à des outils sensibles (API LLM, données de vente, systèmes IAM), l'exploitation de ces failles équivaut à obtenir une "clé maîtresse" pour accéder à l'ensemble d'une organisation.
*   Les chercheurs soulignent la difficulté de sécuriser les environnements d'exécution pour des langages dynamiques comme JavaScript et Python, même avec plusieurs couches de sécurité.

**Vulnérabilités identifiées :**

*   **CVE-2026-1470** (CVSS 9.9) : Une vulnérabilité d'injection d'évaluation (`eval injection`) qui permet à un utilisateur authentifié de contourner le mécanisme de bac à sable des expressions (`Expression sandbox`) pour exécuter du code JavaScript arbitraire sur le nœud principal de n8n.
*   **CVE-2026-0863** (CVSS 8.5) : Une vulnérabilité d'injection d'évaluation (`eval injection`) qui permet à un utilisateur authentifié de contourner les restrictions du bac à sable de l'exécuteur de tâches Python (`python-task-executor sandbox`) pour exécuter du code Python arbitraire sur le système d'exploitation sous-jacent.

**Recommandations :**

Pour corriger ces failles, il est recommandé de mettre à jour n8n vers les versions suivantes :

*   Pour CVE-2026-1470 : versions 1.123.17, 2.4.5, ou 2.4.1.
*   Pour CVE-2026-0863 : versions 1.123.14, 2.3.5, ou 2.4.2.

---
[Source](https://thehackernews.com/2026/01/two-high-severity-n8n-flaws-allow.html){:target="_blank"}
