---
title: 'With the Rise of AI Agents, SOC 2 Should Adapt or Risk Irrelevance'
date: 2026-09-25
permalink: /posts/2026/09/25/with-the-rise-of-ai-agents-soc-2-should-adapt-or-risk-irrelevance/
tags:
- veille-cyber
- bleepingcomp
---
### L'obsolescence des contrôles SOC 2 face à l'essor des agents IA

La montée en puissance des agents IA fragilise la pertinence de la certification SOC 2. Bien que le référentiel soit neutre vis-à-vis des technologies, ses critères reposent sur des hypothèses obsolètes concernant l'identité, l'approbation et la responsabilité des accès, permettant ainsi aux agents IA de fonctionner sans contrôle réel tout en validant les audits.

**Points clés :**
*   **Identité floue :** Les agents IA utilisent souvent les identifiants d'utilisateurs humains (clés API, sessions actives), rendant les journaux d'audit et les revues d'accès trompeurs.
*   **Absence de cycle de vie :** Contrairement aux employés, les agents n'ont pas de processus d'onboarding ou d'offboarding formel. Lorsqu'un employé quitte l'entreprise, ses agents associés restent souvent actifs.
*   **Risque lié aux tiers (MCP) :** L'intégration d'outils comme les serveurs MCP (Model Context Protocol) via des fichiers de configuration échappe aux revues de sécurité des fournisseurs classiques.
*   **Faille de ségrégation des tâches :** La revue et l'approbation de changements par deux instances d'agents IA constituent une séparation des tâches purement formelle et non réelle.

**Vulnérabilités identifiées (non liées à des CVE spécifiques) :**
*   **Fuite de privilèges :** Les agents héritent de droits humains étendus ("Least privilege" inefficace face à l'autonomie de l'agent).
*   **Angle mort d'audit (CC6.1–CC6.3, CC8.1, CC9.2) :** Les contrôles actuels échouent à détecter l'exécution, l'autorisation et la propriété des processus automatisés par IA.

**Recommandations :**
*   **Traitement en tant qu'utilisateurs :** Classer explicitement les agents IA comme une catégorie d'identité distincte dans les systèmes d'information et les rapports d'audit.
*   **Sécurité basée sur l'intention :** Ne pas se contenter de vérifier les permissions (ce qu'un agent *peut* faire), mais définir ce qu'il est *censé* faire.
*   **Inventaire et gestion :** Mettre en place des outils permettant d'identifier chaque agent, d'attribuer une propriété humaine claire et de révoquer immédiatement leurs accès lors de départs ou de changements de rôle.
*   **Approfondissement des audits :** Aller au-delà de la simple conformité aux cases à cocher du SOC 2 en intégrant une visibilité réelle sur l'activité des agents dans le périmètre audité.

---
[Source](https://www.bleepingcomputer.com/news/security/with-the-rise-of-ai-agents-soc-2-should-adapt-or-risk-irrelevance/){:target="_blank"}
