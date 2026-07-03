---
title: 'FBI Seizes NetNut Proxy Platform, Popa Botnet'
date: 2026-07-03
permalink: /posts/2026/07/03/fbi-seizes-netnut-proxy-platform-popa-botnet/
tags:
- veille-cyber
- krebs
---
### Démantèlement du service de proxy NetNut et du botnet Popa

Le FBI, en collaboration avec Google, Lumen et d'autres partenaires, a saisi des centaines de domaines liés à la plateforme de proxy résidentiel **NetNut** (opérée par Alarum Technologies). Cette infrastructure était le pilier du botnet **Popa**, un réseau composé d'au moins deux millions d'appareils domestiques (smart TV, boîtiers de streaming) transformés à l'insu de leurs propriétaires en nœuds de sortie pour relayer du trafic malveillant.

**Points clés :**
* **Fonctionnement :** Les appareils infectés par des SDK malveillants servent de relais pour des activités cybercriminelles (fraude publicitaire, scraping, attaques par force brute, vol de comptes).
* **Impact :** Les cybercriminels utilisaient ces nœuds pour masquer leurs adresses IP d'origine et accéder à des réseaux privés domestiques, exposant les autres appareils connectés au foyer.
* **Écosystème :** NetNut était largement utilisé par des revendeurs tiers, rendant le réseau particulièrement résilient. Bien que ce démantèlement fragilise l'écosystème, les opérateurs de proxy tendent à se transformer en revendeurs de services concurrents pour survivre.

**Vulnérabilités :**
* L'utilisation de **boîtiers de streaming "noname"** utilisant des systèmes Android non officiels, contournant les protections standard (Play Protect).
* Présence de **SDK de proxy intrusifs** dans de nombreuses applications disponibles sur les systèmes d'exploitation **LG webOS** et **Samsung Tizen**.
* Aucune CVE spécifique n'est mentionnée, la menace reposant sur l'installation volontaire ou forcée de logiciels malveillants par les utilisateurs.

**Recommandations :**
* **Privilégier le matériel de marque :** Utiliser uniquement des appareils certifiés par les constructeurs officiels pour garantir la sécurité du système d'exploitation.
* **Vérification de certification :** S'assurer que les appareils Android TV possèdent la certification officielle "Play Protect".
* **Prudence applicative :** Être extrêmement sélectif lors de l'installation d'applications sur les téléviseurs intelligents.
* **Surveillance réseau :** Limiter l'installation d'applications tierces ou douteuses qui demandent des permissions réseau étendues, particulièrement sur les Smart TV.

---
[Source](https://krebsonsecurity.com/2026/07/fbi-seizes-netnut-proxy-platform-popa-botnet/){:target="_blank"}
