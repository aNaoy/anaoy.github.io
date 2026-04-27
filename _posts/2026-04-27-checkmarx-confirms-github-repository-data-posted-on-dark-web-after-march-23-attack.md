---
title: 'Checkmarx Confirms GitHub Repository Data Posted on Dark Web After March 23 Attack'
date: 2026-04-27
permalink: /posts/2026/04/27/checkmarx-confirms-github-repository-data-posted-on-dark-web-after-march-23-attack/
tags:
- veille-cyber
- hackernews
---
### Compromission des données de Checkmarx via une attaque de la chaîne d'approvisionnement

Checkmarx a confirmé que des données provenant de ses dépôts GitHub ont été exposées sur le dark web, suite à une attaque initiale sur sa chaîne d'approvisionnement survenue le 23 mars 2026. L'incident fait suite à l'exploitation de flux de travail GitHub Actions et d'extensions VS Code, permettant l'injection de logiciels malveillants capables de dérober des identifiants.

**Points clés :**
*   **Origine de la fuite :** Accès non autorisé à un dépôt GitHub suite à une attaque par chaîne d'approvisionnement (impliquant le groupe TeamPCP).
*   **Données compromises :** Le groupe LAPSUS$ revendique la possession de code source, bases de données employés, clés API et identifiants de bases de données (MongoDB/MySQL).
*   **Impact étendu :** L'incident a entraîné des compromissions en cascade, notamment sur les images Docker KICS et le package npm `bitwarden-cli`.
*   **Périmètre :** Checkmarx précise que le dépôt GitHub est isolé de l'environnement de production des clients, affirmant qu'aucune donnée client n'y était stockée.

**Vulnérabilités :**
*   L'attaque a exploité la confiance accordée à des dépendances tierces (attaques de type *supply chain*). Bien qu'aucune CVE spécifique ne soit citée pour l'intrusion, le mode opératoire repose sur l'injection de code malveillant dans des workflows automatisés (GitHub Actions) et des extensions de développement (VS Code).

**Recommandations :**
*   **Verrouillage des accès :** Checkmarx a immédiatement restreint l'accès aux dépôts GitHub concernés.
*   **Audit et forensique :** Une enquête approfondie est en cours pour déterminer la portée exacte de l'exfiltration et identifier si des informations sensibles ont été touchées.
*   **Communication :** La société s'est engagée à notifier proactivement ses clients et les parties prenantes si des preuves d'exposition de données clients sont découvertes.
*   **Sécurisation CI/CD :** Renforcer la surveillance des flux de déploiement et valider systématiquement l'intégrité des outils tiers intégrés aux pipelines de développement pour prévenir les compromissions par rebond.

---
[Source](https://thehackernews.com/2026/04/checkmarx-confirms-github-repository.html){:target="_blank"}
