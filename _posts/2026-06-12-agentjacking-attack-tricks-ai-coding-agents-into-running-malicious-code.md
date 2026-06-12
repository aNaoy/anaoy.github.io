---
title: 'Agentjacking Attack Tricks AI Coding Agents Into Running Malicious Code'
date: 2026-06-12
permalink: /posts/2026/06/12/agentjacking-attack-tricks-ai-coding-agents-into-running-malicious-code/
tags:
- veille-cyber
- hackernews
---
### Agentjacking : L'exploitation des agents de codage IA via Sentry

L'« Agentjacking » est une nouvelle classe d'attaque qui manipule les agents de codage IA (tels que Claude Code ou Cursor) pour leur faire exécuter du code arbitraire sur la machine du développeur. Cette attaque exploite la confiance implicite accordée par ces agents aux données transmises via le protocole MCP (Model Context Protocol).

**Points clés :**
* **Mécanisme :** L'attaquant envoie une erreur factice à Sentry via une clé DSN (*Data Source Name*) publique.
* **Ingénierie sociale technique :** Le message d'erreur contient des instructions malveillantes formatées en Markdown, mimant les modèles de diagnostic légitimes de Sentry.
* **Exécution :** Lorsqu'un développeur demande à son IA de corriger les problèmes Sentry, l'agent interprète les données malveillantes comme des instructions de résolution valides et exécute le code malveillant avec les privilèges complets de l'utilisateur.
* **Impact :** Vol de variables d'environnement, identifiants Git, accès à des dépôts privés et usurpation d'identité, sans nécessiter de compromission préalable du serveur ou de phishing classique.
* **Contournement :** L'attaque passe inaperçue face aux solutions de sécurité traditionnelles (EDR, WAF, pare-feu) car toutes les actions sont réalisées par un agent de confiance utilisant des canaux autorisés.

**Vulnérabilités :**
* Il n'existe pas de CVE spécifique pour cette faille, car elle repose sur une **faille architecturale** liée au manque de validation des entrées et à l'excès de confiance dans les données tierces traitées par les agents IA via le protocole MCP.

**Recommandations :**
* **Limiter l'exposition des DSN :** Vérifier que les clés Sentry ne sont pas inutilement exposées publiquement dans le code client.
* **Vigilance humaine :** Ne jamais laisser un agent IA exécuter des commandes ou des correctifs sans une revue humaine approfondie, en particulier lorsque ces instructions proviennent de sources externes comme des outils de monitoring.
* **Privilèges restreints :** Exécuter les agents de codage dans des environnements isolés (conteneurs, machines virtuelles) avec des permissions minimales pour limiter les dégâts en cas d'exécution malveillante.
* **Surveillance des sorties :** Bien que difficile, tenter de filtrer les réponses provenant des serveurs MCP avant qu'elles ne soient interprétées par l'agent IA.

---
[Source](https://thehackernews.com/2026/06/agentjacking-attack-tricks-ai-coding.html){:target="_blank"}
