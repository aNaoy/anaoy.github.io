---
title: 'OpenClaw AI Agent Flaws Could Enable Prompt Injection and Data Exfiltration'
date: 2026-03-14
permalink: /posts/2026/03/14/openclaw-ai-agent-flaws-could-enable-prompt-injection-and-data-exfiltration/
tags:
- veille-cyber
- hackernews
---
### Risques de sécurité critiques liés à l'agent IA OpenClaw

L'agent d'IA autonome OpenClaw fait l'objet d'une alerte de sécurité majeure du CNCERT chinois en raison de vulnérabilités critiques facilitant l'exfiltration de données, le contrôle d'endpoints et l'exécution de code arbitraire.

**Points clés :**
*   **Injection de prompts indirecte (IDPI/XPIA) :** L'agent peut être manipulé pour extraire des informations sensibles via l'analyse de contenus web malveillants ou via des aperçus de liens dans des messageries (Telegram, Discord).
*   **Risques opérationnels :** Risque de suppression irréversible de données par mauvaise interprétation des instructions et déploiement de malwares via des "compétences" (skills) malveillantes téléchargées sur des dépôts tiers (ClawHub).
*   **Campagnes malveillantes :** Des attaquants usurpent OpenClaw sur GitHub pour distribuer des info-stealers (Atomic, Vidar) et des proxys (GhostSocks).
*   **Impact :** Des secteurs critiques (finance, énergie) sont menacés, poussant les autorités chinoises à restreindre son usage.

**Vulnérabilités :**
*   **Injection de prompts indirecte :** Manipulation de l'agent via des contenus tiers ou des aperçus de liens (CVE non mentionnée, risques inhérents à l'architecture).
*   **Clawjacked / Failles d'exécution :** Vulnérabilités permettant le compromis total du système et l'exfiltration de données.

**Recommandations :**
*   **Isolement :** Isoler le service dans un conteneur et ne pas exposer le port de gestion par défaut sur Internet.
*   **Sécurisation des accès :** Éviter le stockage des identifiants en clair et renforcer les contrôles réseau.
*   **Gestion des extensions :** Télécharger des "skills" uniquement via des canaux vérifiés et désactiver les mises à jour automatiques pour éviter l'exécution de code arbitraire.
*   **Maintenance :** Maintenir l'agent strictement à jour et privilégier les sources officielles pour l'installation.

---
[Source](https://thehackernews.com/2026/03/openclaw-ai-agent-flaws-could-enable.html){:target="_blank"}
