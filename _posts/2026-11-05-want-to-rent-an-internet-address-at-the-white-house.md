---
title: 'Want to Rent an Internet Address at the White House?'
date: 2026-11-05
permalink: /posts/2026/11/05/want-to-rent-an-internet-address-at-the-white-house/
tags:
- veille-cyber
- krebs
---
### Vulnérabilité critique au cœur du réseau de la Maison-Blanche : le risque des proxies résidentiels

Des experts en cybersécurité ont détecté une activité persistante de "proxies résidentiels" au sein du réseau informatique officiel de la Maison-Blanche (AS2650). Ce phénomène permet à des tiers extérieurs de louer et d'utiliser les adresses IP du réseau présidentiel pour masquer leur trafic ou usurper leur localisation.

**Points clés :**
*   **Fuite d'accès :** Au moins 28 services de proxy différents ont été identifiés comme capables d'utiliser le réseau de la Maison-Blanche comme point de sortie.
*   **Acteurs à risque :** L'une des solutions identifiées est *Infatica*, dirigée par Vladimir Fomenko, fondateur de *King Servers*, une société historiquement liée à des cyberattaques contre les systèmes électoraux américains en 2016.
*   **Mécanisme :** L'activité provient souvent d'appareils (ordinateurs ou mobiles) appartenant au personnel, sur lesquels des logiciels ou extensions « gratuits » intègrent des kits de développement (SDK) qui monétisent la bande passante de l'utilisateur à son insu.
*   **Envergure :** Le problème dépasse la Maison-Blanche, affectant des centaines de réseaux gouvernementaux, financiers et de santé à travers le monde.

**Vulnérabilités et risques associés :**
*   **Abus de réseau local :** Des vulnérabilités exploitables dans ces services de proxy permettent à des attaquants distants de sonder et d'infecter les réseaux locaux (LAN) auxquels les appareils compromis sont connectés.
*   **Absence de contrôle :** L'écosystème de revente de proxies fonctionne souvent sans procédure « Know Your Customer » (KYC), facilitant l'accès aux réseaux sécurisés pour quelques centimes.

**Recommandations :**
*   **Gestion des terminaux :** Appliquer des politiques strictes de sécurité interdisant l'installation d'applications non approuvées ou d'extensions de navigateur tierces sur les postes de travail professionnels.
*   **Filtrage réseau :** Bloquer les domaines et les flux de trafic associés aux services de proxy résidentiels connus au niveau des passerelles de sécurité (firewalls).
*   **Surveillance active :** Mettre en place une détection continue des sorties de trafic vers les réseaux de proxys résidentiels pour identifier les appareils infectés au sein du parc informatique.
*   **Sensibilisation :** Informer les utilisateurs sur les dangers des logiciels « gratuits » qui cachent des fonctionnalités de partage de connexion (botnets).

---
[Source](https://krebsonsecurity.com/2026/11/want-to-rent-an-internet-address-at-the-white-house/){:target="_blank"}
