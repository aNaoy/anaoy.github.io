---
title: 'Max severity Cisco Secure Workload flaw gives Site Admin privileges'
date: 2026-05-21
permalink: /posts/2026/05/21/max-severity-cisco-secure-workload-flaw-gives-site-admin-privileges/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique dans Cisco Secure Workload

Cisco a corrigé une faille de sécurité critique au sein de sa plateforme **Secure Workload** (anciennement Tetration), permettant à un attaquant non authentifié d'obtenir des privilèges d'administrateur de site.

**Points clés :**
*   **Origine du problème :** Une validation et une authentification insuffisantes au niveau des API REST internes de la solution.
*   **Impact :** Un attaquant peut exploiter cette faille en envoyant une requête API malveillante pour consulter des données sensibles et modifier des configurations, y compris entre les différents clients (tenants).
*   **Statut actuel :** Aucune preuve d'exploitation active n'a été constatée à ce jour par Cisco. Les versions SaaS sont déjà corrigées.

**Vulnérabilité :**
*   **CVE-2026-20223 :** Vulnérabilité de sévérité maximale liée à une erreur d'authentification dans l'API REST.

**Recommandations :**
*   Il n'existe aucun contournement possible ; la mise à jour logicielle est impérative.
*   Pour les clients sur site, les correctifs doivent être appliqués selon les versions suivantes :
    *   **Version 3.10 :** Passer à la version **3.10.8.3** ou ultérieure.
    *   **Version 4.0 :** Passer à la version **4.0.3.17** ou ultérieure.
    *   **Versions 3.9 et antérieures :** Migrer vers une version corrigée.

---
[Source](https://www.bleepingcomputer.com/news/security/cisco-max-severity-secure-workload-flaw-gives-hackers-site-admin-privileges/){:target="_blank"}
