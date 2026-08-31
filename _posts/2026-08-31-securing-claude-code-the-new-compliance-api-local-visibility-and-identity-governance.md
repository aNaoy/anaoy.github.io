---
title: 'Securing Claude Code: The New Compliance API, Local Visibility, and Identity Governance'
date: 2026-08-31
permalink: /posts/2026/08/31/securing-claude-code-the-new-compliance-api-local-visibility-and-identity-governance/
tags:
- veille-cyber
- hackernews
---
# Gouvernance et sécurisation des agents IA locaux : Le cas Claude Code

L’intégration d’agents IA locaux comme Claude Code, qui héritent des identités et permissions des développeurs, transforme le poste de travail en une surface d’attaque majeure. Contrairement aux services SaaS centralisés, ces agents agissent localement, rendant la visibilité traditionnelle insuffisante.

### Points clés
*   **Architecture décentralisée :** Claude Code fonctionne comme un "harnais" exécutant des commandes bash, accédant au système de fichiers et utilisant des serveurs MCP (Model Context Protocol). L’IA (le "cerveau") est dans le cloud, mais l’exécution (les "mains") est locale.
*   **Risques inhérents :** 35 % des serveurs MCP découverts sont d'origine inconnue ou communautaire. Les agents possèdent un accès persistant aux informations d’identification et aux données sensibles du développeur.
*   **Données sensibles :** Les journaux de sessions (transcripts) et les fichiers de configuration locaux stockés sur les postes de travail peuvent contenir des secrets, du PII (données personnelles) ou des données client.

### Vulnérabilités et limites
Il n'existe pas de CVE spécifique, mais des vecteurs de risques critiques :
*   **Exécution de code arbitraire :** L'agent peut exécuter des commandes bash potentiellement destructrices sous l'identité du développeur.
*   **Persistance malveillante :** Des plugins ou compétences (skills) malveillants peuvent être installés localement sans supervision centralisée.
*   **Angle mort de la télémétrie :** Les actions exécutées via des "hooks" locaux ou des modèles hors-Anthropic (Bedrock, Google Cloud) ne sont pas capturées par l'API de conformité d'Anthropic.

### Recommandations de sécurité
Pour une gouvernance efficace, une approche multicouche est nécessaire :

1.  **Imposer une ligne de base (Managed Settings) :** Utiliser les fichiers de configuration gérés (JSON/Registre) pour forcer des politiques globales (listes blanches MCP, blocage de commandes bash spécifiques).
2.  **Exploiter l'API de conformité :** Surveiller les nouveaux endpoints (`/v1/compliance/apps/sessions/local`) pour analyser les transcripts de session (interactions outil/IA) et construire un inventaire des plugins et serveurs MCP utilisés.
3.  **Collecte au niveau du endpoint :** 
    *   Récupérer les fichiers de configuration (`.md` des skills et plugins) pour audit.
    *   Utiliser l'**OpenTelemetry (OTel)** pour tracer les décisions de permission locales non visibles par l'IA.
4.  **Corrélation d'identité :** Connecter les signaux techniques (ce que fait l'agent) à l'identité du propriétaire (qui possède l'agent) pour distinguer une activité légitime d'une compromission.
5.  **Gestion du cycle de vie :** Définir des politiques de rétention pour les historiques de sessions locaux (par défaut 30 jours) et auditer régulièrement les prompts pour détecter la fuite de secrets en clair.

---
[Source](https://thehackernews.com/2026/08/securing-claude-code-new-compliance-api.html){:target="_blank"}
