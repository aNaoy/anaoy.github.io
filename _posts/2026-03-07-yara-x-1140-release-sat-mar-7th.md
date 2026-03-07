---
title: 'YARA-X 1.14.0 Release, (Sat, Mar 7th)'
date: 2026-03-07
permalink: /posts/2026/03/07/yara-x-1140-release-sat-mar-7th/
tags:
- veille-cyber
- sans-isc
---
### Mise à jour de YARA-X 1.14.0 : Analyse des dépendances

La version 1.14.0 de YARA-X introduit quatre améliorations et deux correctifs. L'ajout majeur est la commande CLI `deps`, conçue pour visualiser la hiérarchie et les interdépendances entre les différentes règles YARA.

**Points clés :**
*   **Nouvelle fonctionnalité `deps` :** Permet d'afficher les relations de dépendance entre les règles.
*   **Visibilité accrue :** Facilite la gestion des règles complexes où certaines dépendent directement ou indirectement d'autres règles.

**Vulnérabilités :**
*   Aucune vulnérabilité (CVE) n'est mentionnée dans cette mise à jour.

**Recommandations :**
*   Mettre à jour vers la version 1.14.0 pour bénéficier des corrections de bogues.
*   Utiliser la commande `deps` pour auditer et documenter l'architecture de vos ensembles de règles afin d'éviter les redondances ou les erreurs de logique.

---
[Source](https://isc.sans.edu/diary/rss/32774){:target="_blank"}
