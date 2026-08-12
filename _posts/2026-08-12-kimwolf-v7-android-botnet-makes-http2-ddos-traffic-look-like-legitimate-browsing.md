---
title: 'Kimwolf v7 Android Botnet Makes HTTP/2 DDoS Traffic Look Like Legitimate Browsing'
date: 2026-08-12
permalink: /posts/2026/08/12/kimwolf-v7-android-botnet-makes-http2-ddos-traffic-look-like-legitimate-browsing/
tags:
- veille-cyber
- hackernews
---
### Kimwolf v7 : Une nouvelle génération de botnet Android furtif

La version 7 du botnet Kimwolf (alias AISURU) a été identifiée comme une évolution majeure ciblant les boîtiers Android TV et les objets connectés (IoT). Ce malware se distingue par sa capacité à saturer les infrastructures cibles tout en mimant le comportement d'un utilisateur légitime.

**Points clés :**
* **Furtivité accrue :** Le botnet génère des attaques DDoS via le protocole HTTP/2, en reproduisant fidèlement les empreintes numériques et les en-têtes des navigateurs classiques.
* **Infrastructure résiliente :** Utilisation de l'Ethereum Name Service (ENS) pour résoudre ses adresses de commande et contrôle (C2), couplée à un service caché Tor (.onion) en secours.
* **Architecture modulaire :** Séparation des fonctions de propagation (réalisées par des chargeurs externes) et des fonctions de nuisance (DDoS et proxy), permettant une plus grande discrétion.
* **Dissimulation :** Le malware se masque en tant que processus système (ex: `netd_service`).
* **Propagation :** Le botnet exploite les interfaces Android Debug Bridge (ADB) laissées ouvertes sur le port 5555.

**Vulnérabilités :**
* Bien que non listée sous une CVE spécifique dans le rapport, l'article mentionne l'utilisation historique d'exploits de type **Dirty COW** (CVE-2016-5195) pour l'élévation de privilèges sur les systèmes Linux/Android. La menace principale repose toutefois sur l'exposition de l'interface **ADB (port 5555)**.

**Recommandations :**
* **Segmentation réseau :** Isoler les boîtiers Android TV et les appareils IoT des réseaux d'entreprise critiques.
* **Sécurisation ADB :** Désactiver l'interface Android Debug Bridge (ADB) sur tous les appareils qui ne l'utilisent pas activement. Si nécessaire, restreindre son accès exclusivement à une connexion physique via USB.
* **Surveillance réseau :** Surveiller les flux HTTP/2 anormaux et les requêtes répétées vers des services RPC Ethereum, qui peuvent indiquer une tentative de résolution d'adresse C2.

---
[Source](https://thehackernews.com/2026/08/kimwolf-v7-android-botnet-makes-http2.html){:target="_blank"}
