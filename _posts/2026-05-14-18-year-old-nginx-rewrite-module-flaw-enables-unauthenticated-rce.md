---
title: '18-Year-Old NGINX Rewrite Module Flaw Enables Unauthenticated RCE'
date: 2026-05-14
permalink: /posts/2026/05/14/18-year-old-nginx-rewrite-module-flaw-enables-unauthenticated-rce/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique "NGINX Rift" : Exécution de code à distance

Une vulnérabilité majeure a été découverte dans le module `ngx_http_rewrite_module` de NGINX, présente depuis 18 ans. Identifiée sous le nom de **NGINX Rift**, cette faille permet à un attaquant non authentifié de corrompre le tas (heap) du processus de travail NGINX via une requête HTTP spécialement conçue.

**Points clés :**
*   **Impact :** Exécution de code à distance (RCE) ou déni de service (DoS). L'exécution de code est particulièrement réalisable sur les systèmes sans protection ASLR.
*   **Accessibilité :** Aucune authentification requise ; une simple requête HTTP suffit pour déclencher le débordement de mémoire.
*   **Autres vulnérabilités découvertes :** Trois failles supplémentaires liées à la gestion de la mémoire et à la cryptographie ont été corrigées simultanément.

**Vulnérabilités identifiées :**
*   **CVE-2026-42945 (Score 9.2) :** Débordement de tampon dans `ngx_http_rewrite_module`.
*   **CVE-2026-42946 (Score 8.3) :** Allocation excessive de mémoire dans `ngx_http_scgi_module` et `ngx_http_uwsgi_module`.
*   **CVE-2026-40701 (Score 6.3) :** *Use-after-free* dans `ngx_http_ssl_module`.
*   **CVE-2026-42934 (Score 6.3) :** Lecture hors limites dans `ngx_http_charset_module`.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs fournis par F5 pour NGINX Open Source (versions 1.30.1 / 1.31.0+) et NGINX Plus (versions R32 P6 / R36 P4+).
*   **Atténuation temporaire (CVE-2026-42945) :** Si la mise à jour n'est pas immédiatement possible, remplacer toutes les captures d'expressions régulières non nommées par des **captures nommées** au sein des directives de réécriture.
*   **Inventaire :** Vérifier les versions des modules complémentaires (Ingress Controller, App Protect, etc.) qui nécessitent également des mises à jour spécifiques.

---
[Source](https://thehackernews.com/2026/05/18-year-old-nginx-rewrite-module-flaw.html){:target="_blank"}
