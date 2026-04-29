---
title: 'What to Look for in an Exposure Management Platform (And What Most of Them Get Wrong)'
date: 2026-04-29
permalink: /posts/2026/04/29/what-to-look-for-in-an-exposure-management-platform-and-what-most-of-them-get-wrong/
tags:
- veille-cyber
- hackernews
---
### Évaluer les plateformes de gestion des expositions : Au-delà du simple comptage de vulnérabilités

La gestion des expositions ne doit pas se limiter au suivi du nombre de CVE ou aux scores CVSS, car ces métriques ne reflètent pas le risque réel pour l'entreprise. Une stratégie efficace nécessite une vision contextuelle capable de relier les vulnérabilités aux chemins d'attaque potentiels.

#### Typologie des plateformes
1.  **Portefeuilles "cousus" (Stitched) :** Regroupement de solutions acquises sans réelle intégration des données.
2.  **Agrégateurs de données :** Normalisent les alertes d'outils tiers mais échouent à corréler les expositions entre elles.
3.  **Spécialistes par domaine :** Efficaces sur un segment spécifique (ex: Cloud), mais aveugles aux mouvements latéraux inter-domaines.
4.  **Plateformes intégrées :** Conçues nativement pour modéliser l'environnement et cartographier les chemins d'attaque de bout en bout.

#### Points clés pour l'évaluation
*   **Couverture étendue :** Ne pas se limiter aux CVE (qui représentent environ 25 % des expositions), mais inclure les erreurs de configuration, les identités, les permissions excessives et les charges de travail émergentes.
*   **Cartographie des chemins d'attaque :** La plateforme doit modéliser la progression latérale d'un attaquant à travers les frontières (on-prem, cloud, hybride).
*   **Validation de l'exploitabilité :** Vérifier si une vulnérabilité est réellement exploitable dans le contexte spécifique de l'entreprise (ex: service actif, port ouvert).
*   **Intégration des contrôles de sécurité :** Prendre en compte les protections existantes (pare-feu, MFA, EDR) pour valider si un chemin d'attaque est réellement ouvert.
*   **Priorisation basée sur les actifs critiques :** Se concentrer sur les correctifs qui éliminent les « points d'étranglement » (choke points) menaçant les actifs métiers, réduisant ainsi la charge de travail de 98 %.

#### Recommandations stratégiques
*   **Privilégier les architectures intégrées :** Opter pour des solutions capables de créer un "jumeau numérique" de l'environnement pour visualiser les menaces en temps réel.
*   **Prioriser le risque métier :** Ne plus corriger aveuglément les vulnérabilités à haut score CVSS, mais celles qui font partie intégrante d'un chemin d'attaque validé vers un actif critique.
*   **Automatisation dynamique :** Utiliser des plateformes qui mettent à jour automatiquement le graphe des menaces après chaque remédiation pour garantir une vision toujours pertinente du niveau de sécurité réel.

---
[Source](https://thehackernews.com/2026/04/what-to-look-for-in-exposure-management.html){:target="_blank"}
