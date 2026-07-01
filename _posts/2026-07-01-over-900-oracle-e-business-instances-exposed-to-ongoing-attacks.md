---
title: 'Over 900 Oracle E-Business instances exposed to ongoing attacks'
date: 2026-07-01
permalink: /posts/2026/07/01/over-900-oracle-e-business-instances-exposed-to-ongoing-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne d'attaques actives contre les instances Oracle E-Business Suite

Plus de 900 instances Oracle E-Business Suite (EBS) sont actuellement exposées en ligne et font l'objet d'une campagne d'exploitation active. Des chercheurs en sécurité ont confirmé que des attaquants exploitent une faille critique pour prendre le contrôle total des systèmes vulnérables sans nécessiter d'authentification.

**Points clés :**
*   **Vulnérabilité exploitée :** Une faille située dans le composant *File Transmission* d'Oracle Payments est activement utilisée par des attaquants pour des prises de contrôle à distance.
*   **Visibilité :** Le service Shadowserver a recensé environ 950 instances exposées sur Internet.
*   **Contexte :** Cette attaque s'inscrit dans une tendance plus large où les produits Oracle (WebLogic, PeopleSoft, EBS) sont régulièrement ciblés par des groupes cybercriminels, notamment pour des vols de données massifs.

**Vulnérabilité identifiée :**
*   **CVE-2026-46817 :** Score CVSS de 9.8. Cette vulnérabilité permet à un attaquant non authentifié disposant d'un accès HTTP d'exécuter une prise de contrôle complète du système via une attaque de faible complexité.

**Recommandations :**
*   **Application des correctifs :** Il est impératif d'appliquer immédiatement les mises à jour contenues dans le *Critical Security Patch Update* de mai 2026 publié par Oracle.
*   **Réduction de la surface d'exposition :** Vérifier l'exposition des instances EBS sur le réseau public et restreindre l'accès aux seules plages IP nécessaires via un pare-feu ou un VPN.

---
[Source](https://www.bleepingcomputer.com/news/security/over-900-oracle-e-business-instances-exposed-to-ongoing-attacks/){:target="_blank"}
