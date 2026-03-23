---
title: 'Trivy Hack Spreads Infostealer via Docker, Triggers Worm and Kubernetes Wiper'
date: 2026-03-23
permalink: /posts/2026/03/23/trivy-hack-spreads-infostealer-via-docker-triggers-worm-and-kubernetes-wiper/
tags:
- veille-cyber
- hackernews
---
### Compromission de la supply chain Trivy : Propagation de malwares et attaques ciblées

L'outil d'analyse de vulnérabilités Trivy (Aqua Security) a été victime d'une attaque par compromission de la supply chain. Des versions malveillantes (0.69.4 à 0.69.6) ont été diffusées via Docker Hub, permettant au groupe de cybercriminels "TeamPCP" de voler des identifiants et d'infecter les environnements de développement.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation d'un jeton d'accès compromis (service account "Argon-DevOps-Mgt") possédant des droits administrateur sur les organisations GitHub d'Aqua Security.
*   **Conséquences :**
    *   Installation du voleur d'informations (*infostealer*) TeamPCP.
    *   Propagation du ver *CanisterWorm* via des paquets npm compromis.
    *   Défiguration de 44 dépôts internes et exposition de code propriétaire.
    *   Déploiement d'un *wiper* (destructeur de données) ciblant spécifiquement les clusters Kubernetes, avec des commandes de suppression radicale (`rm -rf /`) pour les systèmes localisés en Iran.
*   **Vulnérabilités :** L'attaque exploite l'utilisation de jetons d'accès longue durée (PAT) et la pratique consistant à référencer des actions CI/CD par "tag" plutôt que par empreinte (SHA). Aucune CVE spécifique n'est associée, l'incident reposant sur une compromission de compte de service.

**Recommandations :**
*   **Sécurisation CI/CD :** Fixer les dépendances et les actions GitHub en utilisant le hash SHA (et non les tags ou versions) pour garantir l'intégrité du code exécuté.
*   **Gestion des accès :** Auditer et limiter les privilèges des comptes de service ; éviter les jetons "ponts" ayant des accès sur plusieurs organisations.
*   **Nettoyage :** Supprimer les versions compromises de Trivy (0.69.4, 0.69.5, 0.69.6) et considérer comme compromis tout environnement ayant exécuté ces versions.
*   **Surveillance :** Surveiller étroitement les runners CI/CD avec la même rigueur que les serveurs de production.

---
[Source](https://thehackernews.com/2026/03/trivy-hack-spreads-infostealer-via.html){:target="_blank"}
