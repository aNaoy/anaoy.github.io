---
title: 'Snowflake Hacker Pleads Guilty Over Breaches Affecting at Least 100 Million People'
date: 2026-08-06
permalink: /posts/2026/08/06/snowflake-hacker-pleads-guilty-over-breaches-affecting-at-least-100-million-people/
tags:
- veille-cyber
- hackernews
---
### Condamnation liée à la campagne de piratage massive des comptes Snowflake

Connor Riley Moucka a plaidé coupable de fraude informatique et d'extorsion dans le cadre des cyberattaques de 2024 ayant ciblé les instances cloud de Snowflake. Ces intrusions, orchestrées par le groupe UNC5537, ont compromis au moins 165 organisations et exposé les données personnelles de plus de 100 millions d'individus, générant plus de 9,5 millions de dollars de pertes directes.

**Points clés :**
*   **Méthodologie simple :** L'attaque n'a exploité aucune vulnérabilité technique (faille zéro-day ou bug) de la plateforme Snowflake.
*   **Vecteur d'attaque :** Utilisation d'identifiants (noms d'utilisateurs et mots de passe) volés par des malwares de type *infostealer* et jamais renouvelés depuis plusieurs années.
*   **Facteur aggravant :** L'absence d'authentification multifacteur (MFA) sur les comptes ciblés et l'absence de listes d'autorisation réseau (*allow lists*).
*   **Impact :** Vol massif de données sensibles, incluant des historiques d'appels (notamment chez AT&T), des numéros de sécurité sociale, des informations de paie et des documents officiels.

**Vulnérabilités :**
*   **Aucune CVE n'est associée :** Il s'agit d'une attaque par compromission de comptes légitimes via des identifiants exfiltrés (credential stuffing). Le succès de l'attaque repose sur la négligence de la gestion des identités.

**Recommandations :**
*   **Imposer l'authentification multifacteur (MFA) :** Rendre le MFA obligatoire pour tous les accès, sans exception pour les comptes de service ou les comptes de test.
*   **Rotation régulière des mots de passe :** Appliquer une politique de changement de mot de passe, particulièrement pour les comptes à privilèges, afin de neutraliser l'utilité des identifiants compromis par des *infostealers*.
*   **Segmentation réseau :** Mettre en place des listes d'autorisation réseau (IP allow lists) pour restreindre l'accès aux instances cloud uniquement aux adresses IP professionnelles approuvées.
*   **Surveillance des fuites :** Surveiller activement l'exposition des identifiants sur le Dark Web pour identifier rapidement les comptes dont les informations ont été dérobées.

---
[Source](https://thehackernews.com/2026/08/snowflake-hacker-pleads-guilty-over.html){:target="_blank"}
