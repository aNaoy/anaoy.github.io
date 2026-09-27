---
title: 'Cloudflare fixes Containers cross-tenant flaw exposing customer data'
date: 2026-09-27
permalink: /posts/2026/09/27/cloudflare-fixes-containers-cross-tenant-flaw-exposing-customer-data/
tags:
- veille-cyber
- bleepingcomp
---
### Faille de segmentation inter-locataires chez Cloudflare

Une vulnérabilité critique au sein du service « Cloudflare Containers » permettait à un utilisateur d'accéder aux données résiduelles d'autres clients hébergés sur le même serveur physique. Ce défaut de sécurité brisait l'isolation logique entre les locataires (cross-tenant).

**Points clés :**
*   **Cause technique :** Le système de stockage mutualisé ne réinitialisait pas (zeroing) les blocs de 64 KiB lors de leur réattribution. Lorsqu'un nouveau conteneur utilisait une partie de ces blocs, les données non écrasées de l'ancien client restaient lisibles.
*   **Données exposées :** La faille permettait d'accéder à des fichiers sensibles, notamment des bases de données SQLite, des profils Chromium, des fichiers de configuration (`.env`) et des identifiants.
*   **Portée limitée :** L'attaque ne permettait ni de prendre le contrôle de l'hôte, ni d'interférer avec les données actives d'une autre instance ; elle permettait uniquement la récupération de données résiduelles.
*   **Impact :** Aucune preuve d'exploitation malveillante n'a été détectée dans les logs. Aucun client n'a été compromis.

**Vulnérabilités :**
*   Pas de CVE assignée (vulnérabilité corrigée en interne via une modification de la configuration du pool de stockage).

**Recommandations :**
*   **Aucune action requise :** Cloudflare a automatiquement corrigé l'infrastructure, réinitialisé les disques de conteneurs et purgé les snapshots obsolètes. L'incident est clos.

---
[Source](https://www.bleepingcomputer.com/news/security/cloudflare-fixes-containers-cross-tenant-flaw-exposing-customer-data/){:target="_blank"}
