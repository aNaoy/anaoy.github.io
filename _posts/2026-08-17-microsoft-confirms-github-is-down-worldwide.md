---
title: 'Microsoft confirms GitHub is down worldwide'
date: 2026-08-17
permalink: /posts/2026/08/17/microsoft-confirms-github-is-down-worldwide/
tags:
- veille-cyber
- bleepingcomp
---
### Interruption majeure des services GitHub : État des lieux

Le 17 août 2026, GitHub a subi une panne mondiale affectant gravement ses infrastructures critiques. Malgré le déploiement de mesures d'atténuation, une instabilité persistante impacte les flux de travail des développeurs.

**Points clés :**
* **Services impactés :** L'interface web, l'API, les Webhooks, les Issues, les Pull Requests et GitHub Actions (affectant les CI/CD).
* **Services dégradés :** Copilot connaît une disponibilité réduite.
* **Taux d'erreur :** Environ 20 % d'erreurs sur le trafic web et les API, et jusqu'à 50 % d'échecs pour le téléchargement d'archives et de dépôts bruts.
* **Authentification :** Les services SAML, OIDC, SCIM et Team Sync sont instables, compliquant l'accès aux plateformes.
* **Cause :** L'origine de l'incident n'a pas été divulguée par Microsoft, l'enquête est toujours en cours.

**Vulnérabilités :**
* Aucune vulnérabilité logicielle (CVE) n'a été identifiée ou liée à cet incident technique à ce stade.

**Recommandations :**
* **Surveillance :** Consulter régulièrement la [page de statut officielle de GitHub](https://www.githubstatus.com/) pour suivre l'évolution des services.
* **Continuité d'activité :** En raison de l'instabilité des workflows automatisés (Actions), les équipes de développement doivent suspendre les déploiements critiques en production jusqu'au rétablissement complet.
* **Gestion des accès :** Anticiper des difficultés de connexion pour les services s'appuyant sur l'authentification SSO (SAML/OIDC) et prévoir des accès de secours si nécessaire.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-confirms-github-is-down-worldwide/){:target="_blank"}
