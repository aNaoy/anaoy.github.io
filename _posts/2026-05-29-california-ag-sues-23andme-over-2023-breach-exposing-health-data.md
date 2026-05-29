---
title: 'California AG sues 23andMe over 2023 breach exposing health data'
date: 2026-05-29
permalink: /posts/2026/05/29/california-ag-sues-23andme-over-2023-breach-exposing-health-data/
tags:
- veille-cyber
- bleepingcomp
---
### Poursuites judiciaires contre 23andMe : une gestion défaillante des données génétiques

Le procureur général de Californie a engagé des poursuites contre 23andMe suite à une violation de données massive survenue en 2023, exposant les informations sensibles de 6,9 millions de clients. L'entreprise, désormais en faillite, est accusée de négligence sécuritaire et de déclarations trompeuses concernant la protection de ses utilisateurs.

**Points clés :**
*   **Vol de données :** Les pirates ont exfiltré des profils génétiques, des rapports de santé, des informations sur les ancêtres et des données sur les proches biologiques.
*   **Responsabilité engagée :** L'État de Californie reproche à l'entreprise un manque de mesures de protection adéquates, une détection tardive de l'intrusion et des erreurs de code dans la fonctionnalité « DNA Relatives ».
*   **Communication fallacieuse :** 23andMe a minimisé la gravité de la faille en rejetant la faute sur les utilisateurs (réutilisation de mots de passe) tout en prétendant initialement que ses systèmes n'avaient pas été directement compromis.

**Vulnérabilités :**
*   **Credential Stuffing :** L'attaque a été rendue possible par l'utilisation de mots de passe compromis ailleurs, exploités par les attaquants contre des comptes protégés par des identifiants faibles.
*   **Erreur de logique applicative :** Une faille dans la fonctionnalité « DNA Relatives » a permis aux pirates d'extraire des données bien au-delà des comptes initialement ciblés.
*   *Note : Aucune CVE spécifique n'est associée à cet incident, car il s'agit d'une vulnérabilité liée à l'architecture et à la gestion des identifiants.*

**Recommandations :**
*   **Authentification forte :** Implémentation systématique de l'authentification multifacteur (MFA) pour contrer le *credential stuffing*.
*   **Audit de sécurité :** Réalisation de tests de pénétration réguliers pour identifier les erreurs de logique métier et les failles de conception dans les fonctionnalités sensibles.
*   **Transparence :** Adoption de politiques de divulgation honnêtes et rapides en cas de violation de données pour se conformer aux réglementations (CCPA) et maintenir la confiance des utilisateurs.
*   **Hygiène des mots de passe :** Encourager l'utilisation de gestionnaires de mots de passe et interdire le recyclage des identifiants.

---
[Source](https://www.bleepingcomputer.com/news/security/california-ag-sues-23andme-over-2023-breach-exposing-health-data/){:target="_blank"}
