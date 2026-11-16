---
title: 'Amazon Uncovers AI Agent Campaign Targeting LiteLLM, Dify, and Other Apps for API Keys'
date: 2026-11-16
permalink: /posts/2026/11/16/amazon-uncovers-ai-agent-campaign-targeting-litellm-dify-and-other-apps-for-api-keys/
tags:
- veille-cyber
- hackernews
---
### Campagne de cybercriminalité automatisée via des agents IA : Menaces sur les outils d'IA

Des groupes de pirates, probablement basés en Chine, utilisent des agents d'IA autonomes basés sur l'outil de test d'intrusion open-source **ARTEX** pour cibler des applications d'IA exposées sur Internet. Leur objectif est d'exfiltrer des clés d'API (LiteLLM, Dify, One API, etc.) afin de construire un pool de ressources de calcul pour mener leurs attaques à grande échelle.

#### Points clés
*   **Mode opératoire :** Les agents analysent le web pour identifier des applications d'IA mal sécurisées, exploitent des vulnérabilités ou des mauvaises configurations, et extraient les clés d'API stockées.
*   **Vitesse et persistance :** Contrairement aux attaques classiques, l'IA permet aux attaquants d'automatiser la découverte de cibles et l'exploitation de failles avec une rapidité et une persistance accrues.
*   **Vecteurs d'attaque :** Utilisation de jetons CI/CD non restreints, recherche de secrets dans les dépôts GitHub/conteneurs, et exploitation d'interfaces d'administration sans authentification.
*   **Polyvalence :** En plus de l'exfiltration de données, ces agents ont été observés tentant de contourner des systèmes de vérification d'identité via des *deepfakes*.

#### Vulnérabilités identifiées
*   **Langflow (CVE-2025-3248) :** Défaut d'authentification permettant l'exécution de code à distance (RCE).
*   **RAGFlow (CVE-2026-28797) :** Injection de modèles côté serveur (SSTI) permettant à un utilisateur d'exécuter des commandes système.
*   **One API :** Contournement d'authentification via l'en-tête HTTP `isCliRequest`.

#### Recommandations de sécurité
*   **Gestion des accès :** Appliquer le principe du moindre privilège, supprimer les comptes par défaut (ex: clé maître LiteLLM), et utiliser des jetons d'API restreints (date d'expiration et filtrage IP).
*   **Hygiène des secrets :** Scanner activement les dépôts, fichiers de configuration et variables d'environnement pour détecter des clés exposées. Révoquer et renouveler immédiatement toute clé compromise.
*   **Renforcement applicatif :** Mettre à jour les outils d'IA (ex: Langflow 1.3.0+, RAGFlow 0.25.0+) et isoler les environnements d'exécution des agents.
*   **Surveillance :**
    *   Rechercher la présence de scripts suspects dans les environnements cloud (notamment ceux préfixés par `artex-`).
    *   Surveiller les logs pour détecter des comportements anormaux ou des pics de consommation de ressources.
    *   Utiliser les règles de détection Snort publiées par Cisco Talos pour identifier les activités liées aux frameworks de type ARTEX.

---
[Source](https://thehackernews.com/2026/11/amazon-uncovers-ai-agent-campaign.html){:target="_blank"}
