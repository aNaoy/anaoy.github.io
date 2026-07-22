---
title: 'LG to Ban Residential Proxies from Smart TV Apps'
date: 2026-07-22
permalink: /posts/2026/07/22/lg-to-ban-residential-proxies-from-smart-tv-apps/
tags:
- veille-cyber
- krebs
---
### Sécurisation des Smart TV : LG bannit les proxys résidentiels

LG Electronics a annoncé le bannissement prochain des applications utilisant des kits de développement logiciel (SDK) de proxy résidentiel sur sa plateforme webOS. Cette décision fait suite à une étude révélant que plus de 42 % des applications disponibles sur son store transformaient les téléviseurs en nœuds de sortie pour des tiers, permettant à ces derniers de faire transiter leur trafic Internet via le réseau domestique de l'utilisateur.

**Points clés**
*   **Risque de détournement :** De nombreuses applications (jeux, économiseurs d'écran) intègrent des SDK monétisant la bande passante de l'utilisateur en le transformant en relais réseau.
*   **Implication des constructeurs :** Le problème touche également les téléviseurs Samsung (système Tizen), où plus d'un quart des applications contiennent des composants similaires.
*   **Limites du consentement :** Bien que les fournisseurs de proxys comme Bright Data affirment obtenir un consentement utilisateur, les experts soulignent que ces autorisations sont souvent opaques, mal comprises par les membres du foyer (mineurs) et inadaptées à des appareils qui ne sont pas perçus comme des ordinateurs classiques.
*   **Vulnérabilités :** Bien qu'aucune CVE spécifique ne soit associée à cette pratique, l'utilisation de proxys résidentiels expose le réseau local de l'utilisateur à des abus potentiels, permettant à des tiers d'utiliser l'adresse IP domestique pour des activités de scraping ou de cybercriminalité.

**Recommandations**
*   **Surveillance des autorisations :** Soyez vigilant lors de l'installation d'applications sur les téléviseurs connectés, notamment celles demandant des accès inhabituels à la connectivité réseau ou proposant des modèles économiques basés sur le partage de bande passante.
*   **Audit des applications :** LG procède actuellement à un retrait forcé des applications non conformes. Il est conseillé de désinstaller toute application suspecte ou inutile sur votre Smart TV.
*   **Segmentation réseau :** Pour une sécurité accrue, isolez les objets connectés (IoT) sur un réseau Wi-Fi « invité » distinct de votre réseau principal afin de limiter l'impact d'une compromission éventuelle sur vos appareils critiques (PC, serveurs NAS, etc.).

---
[Source](https://krebsonsecurity.com/2026/07/lg-to-ban-residential-proxies-from-smart-tv-apps/){:target="_blank"}
