---
title: 'China-Made ZBT Routers Ship With Two Implants Giving Unauthenticated Attackers Root Access'
date: 2026-08-28
permalink: /posts/2026/08/28/china-made-zbt-routers-ship-with-two-implants-giving-unauthenticated-attackers-root-access/
tags:
- veille-cyber
- hackernews
---
### Implants de surveillance dans les routeurs ZBT : Accès root non authentifié

Des chercheurs de VulnCheck ont découvert deux implants malveillants intégrés au firmware des routeurs fabriqués par Shenzhen Zhibotong Electronics (ZBT), permettant à des attaquants distants d'exécuter des commandes avec les privilèges **root** sans aucune authentification.

#### Points clés
*   **SPEAKINGSTONE (CVE-2026-74232) :** Un implant communiquant via le port UDP 10000 avec un serveur de commande et de contrôle (C2). Il permet l'exécution de commandes, l'exfiltration d'identifiants PPPoE, le détournement DNS et l'ouverture de tunnels SSH inverses.
*   **DARKLANTERN (CVE-2026-74233) :** Un service écoutant sur le port UDP 9992, accessible depuis Internet. Son authentification est inefficace, reposant sur un sel codé en dur et un mécanisme de contournement basé sur une adresse MAC factice.
*   **Impact :** Ces vulnérabilités présentent un score CVSS de 9.3 à 9.8. Des centaines de dispositifs ont été identifiés comme actifs et vulnérables à travers le monde.
*   **Origine :** Les implants sont présents au niveau de l'usine dans le firmware d'origine de ZBT. Les appareils rebadgés par d'autres marques utilisant ce même matériel sont également concernés.

#### Vulnérabilités identifiées
*   **CVE-2026-74232 :** Impliant C2 (service `yunmgrd`).
*   **CVE-2026-74233 :** Injection de commande (service `infosrvd`).

#### Recommandations de sécurité
*   **Filtrage réseau :** Bloquer les connexions entrantes vers le port UDP 9992 au niveau de la passerelle réseau.
*   **Surveillance :** Surveiller le trafic sortant sur le port UDP 10000, caractéristique des balises (beacons) de l'implant SPEAKINGSTONE.
*   **Isolement :** Considérer le réseau local (LAN) derrière ces routeurs comme non fiable.
*   **Identification :** Utiliser le préfixe MAC du constructeur (`78:A3:51` ou `F8:5E:3C`) pour identifier les appareils ZBT potentiellement compromis.
*   **Mise à jour :** Vérifier les versions de firmware. Bien qu'aucune correction officielle ne soit listée, il est recommandé de mettre à jour le firmware si une version plus récente est disponible ou d'opter pour des firmwares tiers (ex: MOFI Network) lorsqu'ils sont compatibles et exempts de ces composants.

---
[Source](https://thehackernews.com/2026/08/china-made-zbt-routers-ship-with-two.html){:target="_blank"}
