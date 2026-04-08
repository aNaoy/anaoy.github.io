---
title: 'Masjesu Botnet Emerges as DDoS-for-Hire Service Targeting Global IoT Devices'
date: 2026-04-08
permalink: /posts/2026/04/08/masjesu-botnet-emerges-as-ddos-for-hire-service-targeting-global-iot-devices/
tags:
- veille-cyber
- hackernews
---
### Masjesu : Un botnet IoT furtif dédié aux attaques DDoS

Le botnet **Masjesu** (également connu sous le nom de **XorBot**) s'est imposé depuis 2023 comme un service de location d'attaques par déni de service distribué (DDoS-as-a-Service). Opérant via Telegram, il cible spécifiquement les appareils IoT (routeurs, caméras, DVR, NVR) à travers le monde pour constituer son infrastructure.

**Points clés :**
*   **Stratégie de survie :** Le botnet privilégie la discrétion et évite délibérément de cibler des infrastructures critiques (comme celles du Département de la Défense américain) afin de limiter l'attention des autorités.
*   **Mécanisme d'infection :** Il utilise des techniques d'injection de commandes et d'exécution de code à distance pour compromettre divers constructeurs (D-Link, Huawei, TP-Link, Realtek, etc.).
*   **Propagation :** Le malware scanne aléatoirement les adresses IP à la recherche de ports ouverts pour s'auto-propager. Une fois installé, il neutralise des outils concurrents (comme `wget` ou `curl`) et communique via le port TCP 55988.
*   **Origine du trafic :** Les attaques proviennent principalement du Vietnam (50 %), suivies de l'Ukraine, de l'Iran, du Brésil, du Kenya et de l'Inde.

**Vulnérabilités exploitées :**
*   **Miniigd (Realtek SDK) :** Le botnet cible activement le port **52869**, associé au démon UPnP (Universal Plug and Play) du SDK Realtek, une méthode classique d'exploitation pour les botnets IoT.
*   Le malware exploite 12 vulnérabilités distinctes d'exécution de code à distance et d'injection de commandes sur divers équipements.

**Recommandations :**
*   **Mise à jour des firmwares :** Appliquer les correctifs de sécurité fournis par les constructeurs des appareils IoT (notamment pour les routeurs et caméras).
*   **Désactivation des services inutiles :** Désactiver le protocole **UPnP** sur les routeurs et les passerelles si celui-ci n'est pas strictement nécessaire.
*   **Durcissement réseau :** Restreindre l'accès à distance aux interfaces d'administration des appareils IoT et fermer les ports inutilisés exposés sur Internet.
*   **Surveillance du trafic :** Surveiller les communications sortantes inhabituelles, notamment celles utilisant le port TCP 55988, signe potentiel d'une compromission.

---
[Source](https://thehackernews.com/2026/04/masjesu-botnet-emerges-as-ddos-for-hire.html){:target="_blank"}
