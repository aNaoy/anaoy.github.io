---
title: 'Why Secrets in JavaScript Bundles are Still Being Missed'
date: 2026-01-20
permalink: /posts/2026/01/20/why-secrets-in-javascript-bundles-are-still-being-missed/
tags:
- veille-cyber
- hackernews
---
### Fuites de Secrets dans les Bundles JavaScript : Une Vulnérabilité Persistante

Des recherches récentes ont mis en évidence la persistance de fuites de secrets, tels que des clés API et des jetons d'authentification, au sein des bundles JavaScript des applications web, en particulier les applications monopages (SPA). Malgré les méthodes de détection existantes, une part importante de ces vulnérabilités échappe encore à la vigilance des outils de sécurité.

Une analyse approfondie de 5 millions d'applications a révélé plus de 42 000 jetons exposés appartenant à 334 types de secrets différents. Ces fuites ont des implications majeures pour la sécurité, allant de l'accès non autorisé à des dépôts de code sensibles à l'exposition de données internes de gestion de projet et d'autres services tiers.

**Points Clés :**

*   Les méthodes traditionnelles de détection de secrets (basées sur des chemins et des expressions régulières) et les outils de Dynamic Application Security Testing (DAST), bien qu'utiles, présentent des limitations pour découvrir les secrets intégrés dans les fichiers JavaScript chargés dynamiquement.
*   Les outils de Static Application Security Testing (SAST), qui analysent le code source avant la production, ne suffisent pas non plus à couvrir toutes les voies par lesquelles les secrets peuvent se retrouver dans le code front-end.
*   Les secrets introduits lors des processus de build et de déploiement peuvent contourner les contrôles de sécurité "shift-left".
*   La recherche a identifié une quantité significative de jetons de dépôts de code (GitHub, GitLab), de clés API de gestion de projet (Linear), et de jetons pour des plateformes de chat, de conversion de PDF, et de marketing.

**Vulnérabilités identifiées :**

Bien que des CVE spécifiques ne soient pas explicitement mentionnées dans l'article pour les secrets individuels, le problème concerne la mauvaise gestion des secrets dans le code client. Les exemples incluent :

*   **Jetons d'accès personnels GitLab :** Permettant un accès complet aux dépôts privés, y compris aux secrets CI/CD pour des services comme AWS et SSH.
*   **Clés API Linear :** Exposant l'intégralité d'une instance de gestion de projet, y compris les tickets internes et les liens vers des projets SaaS.
*   **Webhooks pour plateformes de chat et d'automatisation :** D'où l'exposition de connexions actives à Slack, Microsoft Teams, Discord et Zapier.

**Recommandations :**

*   **Implémenter des contrôles de sécurité "shift-left"** (SAST, scan de dépôts, garde-fous IDE) pour intercepter les problèmes en amont.
*   **Déployer des mécanismes de détection de secrets spécifiques aux applications monopages (SPA)**, capables de parcourir et d'analyser le code JavaScript chargé dynamiquement.
*   **Éviter de "shiper" les secrets** dans le code front-end ; leur introduction doit être gérée en dehors du code exécuté par le client.
*   L'automatisation et l'IA, bien qu'utiles pour le développement, peuvent aggraver ce risque si elles ne sont pas accompagnées de mesures de sécurité appropriées.

---
[Source](https://thehackernews.com/2026/01/why-secrets-in-javascript-bundles-are.html){:target="_blank"}
