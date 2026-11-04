---
title: 'Radio With No Radar: Why Agent Runtime Security Fails Without the Layers Beneath It'
date: 2026-11-04
permalink: /posts/2026/11/04/radio-with-no-radar-why-agent-runtime-security-fails-without-the-layers-beneath-it/
tags:
- veille-cyber
- hackernews
---
### Sécuriser les agents IA : Au-delà de la passerelle unique

La sécurité des agents IA ne peut se limiter à une approche par "passerelle" (gateway), car la majorité des agents opèrent au sein de plateformes tierces (Salesforce, Slack, M365) où le trafic est invisible pour les outils de filtrage réseau classiques. L'absence de visibilité sur ces couches sous-jacentes rend toute tentative de contrôle inefficace.

**Points clés**
*   **Le périmètre de l'agent :** La sécurité doit être intégrée là où l'agent s'exécute (hooks natifs, API, endpoint) plutôt qu'en un point de contrôle unique.
*   **L'importance du contexte :** Une décision de sécurité pertinente nécessite une connaissance globale : identité, permissions, historique des délégations et sensibilité des données.
*   **Risque lié aux outils de contrôle :** La centralisation du filtrage via des passerelles crée un point de défaillance unique (ex: vulnérabilité de LiteLLM).
*   **Approche recommandée :** Construire une cartographie en temps réel (Identity, Permissions, Connectivity, Activity - IPCA) pour évaluer les risques avant de tenter de bloquer les actions.

**Vulnérabilités et risques identifiés**
*   **AST09 (OWASP Agentic Skills Top 10) :** "No Governance" – déploiement d'agents dans des plateformes tierces échappant au contrôle de sécurité externe.
*   **Chaînes de délégation malveillantes :** Les agents peuvent être instrumentés par des chaînes d'appels non approuvées, rendant les permissions d'origine trompeuses.
*   **Incident LiteLLM (Mars 2026) :** Compromission d'un composant de routage open-source utilisé pour inspecter le trafic IA, exposant plus de 2 500 organisations.

**Recommandations stratégiques**
1.  **Prioriser la découverte :** Identifier tous les agents actifs, leurs propriétaires, leurs accès et leurs configurations sur l'ensemble de l'écosystème avant d'appliquer des blocages.
2.  **Adopter une réponse graduée :** Ne pas se limiter au blocage. Privilégier des mesures adaptées (avertissement utilisateur, rédaction de données, interruption d'un agent compromis) selon la criticité du risque.
3.  **Audit de la chaîne de confiance :** Pour chaque agent, être capable de reconstruire le chemin causal (qui a sollicité l'agent, quels sauts ont eu lieu, quelle est la destination finale).
4.  **Déploiement progressif :**
    *   *Semaines 1-2 :* Découverte totale via les API existantes.
    *   *Semaines 3-6 :* Attribution d'un propriétaire humain à chaque agent et tri des configurations.
    *   *Semaines 7-12 :* Mise en place d'une hiérarchisation des risques basée sur le contexte pour les actions critiques.

---
[Source](https://thehackernews.com/2026/11/radio-with-no-radar-why-agent-runtime.html){:target="_blank"}
