---
title: 'Kimwolf Android botnet abuses residential proxies to infect internal devices'
date: 2026-01-07
permalink: /posts/2026/01/07/kimwolf-android-botnet-abuses-residential-proxies-to-infect-internal-devices/
tags:
- veille-cyber
- bleepingcomp
---
## Kimwolf : Le botnet Android qui exploite les réseaux de proxies résidentiels

Le botnet Kimwolf, une variante Android du malware Aisuru, a infecté plus de deux millions d'appareils en exploitant des vulnérabilités dans les réseaux de proxies résidentiels. Son principal mode opératoire consiste à scanner les réseaux à la recherche d'appareils Android avec des services ADB (Android Debug Bridge) exposés et non authentifiés, particulièrement sur les boîtiers TV et appareils de streaming.

Ces appareils compromis sont ensuite utilisés pour des attaques par déni de service distribué (DDoS), la revente de leurs capacités de proxy, et la monétisation par l'installation d'applications via des SDK tiers. Kimwolf est responsable de l'une des plus grandes attaques DDoS jamais enregistrées.

Les infections proviennent souvent de SDK pré-installés sur les appareils vendus, comme ceux de fournisseurs de proxy résidentiels. Des fournisseurs comme IPIDEA ont été identifiés comme des cibles majeures.

**Points Clés :**

*   **Croissance rapide :** Plus de 2 millions d'hôtes infectés.
*   **Méthode d'infection :** Exploitation des services ADB exposés sur les réseaux internes via des proxies résidentiels.
*   **Cibles principales :** Appareils TV Android et boîtiers de streaming avec ADB non authentifié.
*   **Utilisations du botnet :** Attaques DDoS, revente de proxy, monétisation via SDK.
*   **Origine des infections :** Souvent des appareils vendus pré-infectés avec des SDK malveillants.

**Vulnérabilités :**

*   **Exposition des services ADB non authentifiés :** Les ports 5555, 5858, 12108 et 3222 sont ciblés. L'ADB permet une connexion distante non autorisée pour modifier ou prendre le contrôle des appareils Android lorsqu'il est exposé sur un réseau. (Pas de CVE spécifique mentionné dans l'article).

**Recommandations :**

*   **Vérification :** Utiliser l'outil scanner en ligne de Synthient pour vérifier si des appareils sur le réseau sont infectés.
*   **Action en cas d'infection :** Les boîtiers TV infectés doivent être "effacés ou détruits" pour éliminer la persistance du botnet.
*   **Prévention :** Éviter les boîtiers TV Android génériques et peu coûteux. Privilégier les appareils certifiés "Google Play Protect" provenant de fabricants réputés (ex: Google Chromecast, NVIDIA Shield TV, Xiaomi Mi TV Box).

---
[Source](https://www.bleepingcomputer.com/news/security/kimwolf-android-botnet-abuses-residential-proxies-to-infect-internal-devices/){:target="_blank"}
