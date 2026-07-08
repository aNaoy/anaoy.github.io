---
title: 'Hidden backdoor in Tenda router firmware grants admin access'
date: 2026-07-08
permalink: /posts/2026/07/08/hidden-backdoor-in-tenda-router-firmware-grants-admin-access/
tags:
- veille-cyber
- bleepingcomp
---
### Backdoor critique sur les routeurs Tenda : Accès administrateur non autorisé

Une vulnérabilité critique a été identifiée dans le firmware de plusieurs routeurs Tenda, permettant à un attaquant d'obtenir un accès administrateur complet via une porte dérobée (backdoor) non documentée. Le mécanisme d'authentification du serveur web (`/bin/httpd`) comporte une fonction de repli qui compare le mot de passe fourni par l'utilisateur avec une valeur de configuration système (`sys.rzadmin.password`). Si les valeurs correspondent, l'appareil accorde un accès avec privilèges élevés, quel que soit le nom d'utilisateur saisi.

**Points clés :**
*   **Vulnérabilité :** Mécanisme d'authentification de secours non documenté.
*   **Conséquences :** Prise de contrôle totale de l'interface de gestion, reconfiguration réseau et désactivation des fonctionnalités de sécurité.
*   **Statut :** Aucun correctif disponible auprès du fabricant, injoignable par le CERT/CC.

**Identifiant :**
*   **CVE-2026-11405**

**Appareils affectés :**
*   Tenda FH1201, W15E, AC10, AC5, et AC6 (version V2).

**Recommandations :**
*   Désactiver impérativement l'interface de gestion web distante pour bloquer tout accès depuis Internet.
*   Restreindre l'exposition sur le réseau local en modifiant l'adresse IP par défaut du LAN afin de limiter la découverte par des scanners automatisés.

---
[Source](https://www.bleepingcomputer.com/news/security/hidden-backdoor-in-tenda-router-firmware-grants-admin-access/){:target="_blank"}
