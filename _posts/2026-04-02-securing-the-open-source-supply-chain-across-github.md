---
title: 'Securing the open source supply chain across GitHub'
date: 2026-04-02
permalink: /posts/2026/04/02/securing-the-open-source-supply-chain-across-github/
tags:
- veille-cyber
- zerodaysfans
---
# Sécurisation de la chaîne d'approvisionnement logicielle : Défis et stratégies GitHub

Les attaques récentes contre la chaîne d'approvisionnement open source ciblent principalement les workflows GitHub Actions afin d'exfiltrer des secrets, permettant aux attaquants de publier des paquets malveillants et de compromettre davantage de projets.

### Points clés
*   **Vecteur d'attaque :** Compromission de workflows GitHub Actions pour accéder à des secrets (clés API, identifiants).
*   **Propagation :** Utilisation de paquets malveillants pour infiltrer de nouveaux systèmes.
*   **Réponse de GitHub :** Déploiement de mesures de détection (analyse de paquets npm) et promotion de mécanismes d'authentification sans secrets.
*   **Vulnérabilités :** L'article ne mentionne pas de CVE spécifiques, mais souligne des failles d'implémentation récurrentes liées aux workflows CI/CD.

### Recommandations de sécurité
*   **Analyse automatisée :** Activer **CodeQL** pour inspecter les workflows GitHub Actions et détecter les mauvaises pratiques.
*   **Gestion des workflows :**
    *   Éviter de déclencher des workflows via `pull_request_target`.
    *   Verrouiller (*pinning*) les actions tierces en utilisant les SHA de commit complets au lieu des tags.
    *   Restreindre l'injection de scripts lors de l'utilisation de contenus fournis par les utilisateurs.
*   **Authentification sans secret :** Adopter le **"Trusted Publishing"** (via OpenID Connect) pour autoriser les déploiements de paquets sans stocker de secrets permanents dans les pipelines.
*   **Surveillance :** Utiliser **Dependabot** et consulter régulièrement la *GitHub Advisory Database* pour identifier rapidement les dépendances vulnérables ou malveillantes.

---
[Source](https://github.blog/security/supply-chain-security/securing-the-open-source-supply-chain-across-github/){:target="_blank"}
