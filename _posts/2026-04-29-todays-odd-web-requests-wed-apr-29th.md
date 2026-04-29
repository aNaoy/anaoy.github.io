---
title: 'Todays Odd Web Requests, (Wed, Apr 29th)'
date: 2026-04-29
permalink: /posts/2026/04/29/todays-odd-web-requests-wed-apr-29th/
tags:
- veille-cyber
- sans-isc
---
### Nouvelles activités de reconnaissance sur le Web

Les honeypots du SANS Internet Storm Center ont détecté deux nouvelles requêtes de reconnaissance ciblant des infrastructures spécifiques, bien qu'aucune vulnérabilité précise n'ait été exploitée pour le moment.

**Points clés :**
*   **Broadcom API Gateway :** Une requête `/bam/restart/if/required` a été identifiée. Bien qu'inoffensive en l'état, elle sert à identifier la présence de cette passerelle, ce qui pourrait faciliter des attaques ultérieures.
*   **Appareils ESP32 :** Une requête vers le chemin `/esps/` cible les systèmes sur puce ESP32, largement utilisés dans l'IoT et la domotique. Ce point d'entrée pourrait être lié à des fonctionnalités de mise à jour du firmware.

**Vulnérabilités :**
*   Aucune CVE associée à ce stade. Il s'agit d'une phase de reconnaissance visant à cartographier la surface d'attaque.

**Recommandations :**
*   **Surveillance :** Inspectez les journaux de vos serveurs pour détecter ces requêtes spécifiques.
*   **Réduction de la surface d'attaque :** Limitez l'accès aux interfaces de gestion et d'administration (comme celles des API Gateways ou des interfaces IoT) en les rendant inaccessibles depuis Internet ou en restreignant l'accès via des listes blanches d'adresses IP.
*   **Mise à jour :** Assurez-vous que les firmwares des appareils IoT et les correctifs des API Gateways sont à jour pour limiter les risques en cas d'exploitation ultérieure.

---
[Source](https://isc.sans.edu/diary/rss/32934){:target="_blank"}
