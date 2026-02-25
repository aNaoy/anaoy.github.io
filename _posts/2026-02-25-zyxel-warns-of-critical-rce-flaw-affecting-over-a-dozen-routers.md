---
title: 'Zyxel warns of critical RCE flaw affecting over a dozen routers'
date: 2026-02-25
permalink: /posts/2026/02/25/zyxel-warns-of-critical-rce-flaw-affecting-over-a-dozen-routers/
tags:
- veille-cyber
- bleepingcomp
---
**Faille critique sur les routeurs Zyxel : Exécution de commandes à distance possible**

Des mises à jour de sécurité ont été publiées par Zyxel pour corriger une vulnérabilité critique affectant plus d'une douzaine de modèles de routeurs. Cette faille, identifiée sous le nom de CVE-2025-13942, concerne la fonction UPnP et permet à des attaquants non authentifiés d'exécuter des commandes à distance sur des appareils non patchés.

Les attaquants peuvent exploiter cette vulnérabilité en envoyant des requêtes UPnP SOAP spécialement conçues. Cependant, le risque est limité car une exploitation réussie nécessite que la fonction UPnP et l'accès WAN soient activés, l'accès WAN étant désactivé par défaut.

Zyxel a également corrigé deux vulnérabilités post-authentification de gravité élevée (CVE-2025-13943 et CVE-2026-1459) qui permettent l'exécution de commandes système via des identifiants compromis.

Environ 120 000 appareils Zyxel, dont plus de 76 000 routeurs, sont exposés sur Internet. Ces appareils sont fréquemment ciblés car ils sont souvent fournis par les fournisseurs d'accès à Internet comme équipement par défaut.

**Points clés :**

*   **Nature de la faille :** Injection de commandes via UPnP (CVE-2025-13942), permettant l'exécution de commandes système à distance.
*   **Attaques post-authentification :** Deux autres failles (CVE-2025-13943, CVE-2026-1459) permettent l'exécution de commandes avec des identifiants compromis.
*   **Impact :** Près de 120 000 appareils Zyxel exposés sur Internet, y compris plus de 76 000 routeurs.
*   **Contexte :** Les appareils Zyxel sont une cible fréquente pour les attaquants.

**Vulnérabilités :**

*   **CVE-2025-13942 :** Injection de commandes via UPnP dans la fonction UPnP des routeurs Zyxel 4G LTE/5G NR CPE, DSL/Ethernet CPE, Fiber ONTs et extensions sans fil. Permet l'exécution de commandes OS par des attaquants distants non authentifiés.
*   **CVE-2025-13943 :** Injection de commandes post-authentification.
*   **CVE-2026-1459 :** Injection de commandes post-authentification.

**Recommandations :**

*   **Installer les correctifs de sécurité :** Zyxel recommande fortement aux utilisateurs d'installer les mises à jour pour maintenir une protection optimale.
*   **Vérifier les paramètres :** Les utilisateurs devraient s'assurer que l'accès WAN n'est pas activé s'il n'est pas nécessaire et que la fonction UPnP n'est utilisée qu'en cas de besoin.
*   **Remplacer les appareils obsolètes :** Pour les produits qui ont atteint leur fin de vie (EOL) et qui ne recevront plus de correctifs (comme certains modèles VMG et SBG), il est vivement conseillé de les remplacer par des produits plus récents.

---
[Source](https://www.bleepingcomputer.com/news/security/zyxel-warns-of-critical-rce-flaw-affecting-over-a-dozen-routers/){:target="_blank"}
