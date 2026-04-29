---
title: 'cPanel, WHM emergency update fixes critical auth bypass bug'
date: 2026-04-29
permalink: /posts/2026/04/29/cpanel-whm-emergency-update-fixes-critical-auth-bypass-bug/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique de contournement d'authentification dans cPanel et WHM

Une faille de sécurité critique a été identifiée dans les panneaux de contrôle cPanel et WebHost Manager (WHM), permettant à un attaquant non authentifié d'obtenir un accès complet aux serveurs et aux sites web hébergés. La compromission d'un compte WHM peut entraîner une prise de contrôle totale du serveur, tandis qu'un accès cPanel permet la manipulation de sites, l'exfiltration de données, l'injection de backdoors ou l'envoi de spams.

**Points clés :**
*   **Gravité :** Élevée, car elle permet un accès sans authentification préalable.
*   **Impact :** Contrôle total des comptes d'hébergement, des bases de données et, pour WHM, de l'intégralité du serveur.
*   **Statut :** Aucun identifiant CVE n'a été attribué à ce jour.

**Versions corrigées :**
La mise à jour est disponible pour les versions supportées : 11.110.0.97, 11.118.0.63, 11.126.0.54, 11.132.0.29, 11.136.0.5 et 11.134.0.20.

**Recommandations :**
*   **Mise à jour immédiate :** Les administrateurs doivent exécuter manuellement la commande suivante pour forcer la mise à jour, même si le système indique être à jour : `/scripts/upcp --force`
*   **Systèmes non supportés :** Les serveurs utilisant des versions obsolètes de cPanel ne recevront pas de correctif ; une migration vers une version supportée est impérative pour sécuriser l'infrastructure.

---
[Source](https://www.bleepingcomputer.com/news/security/cpanel-whm-emergency-update-fixes-critical-auth-bypass-bug/){:target="_blank"}
