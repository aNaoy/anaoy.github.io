---
title: 'Running Tesla Model 3’s Computer on My Desk Using Parts From Crashed Cars'
date: 2026-03-23
permalink: /posts/2026/03/23/running-tesla-model-3s-computer-on-my-desk-using-parts-from-crashed-cars/
tags:
- veille-cyber
- zerodaysfans
---
### Rétro-ingénierie et mise en service de l'unité centrale Tesla Model 3

Ce projet documente la méthode pour isoler et faire fonctionner en laboratoire (sur un bureau) l'unité centrale (MCU) et l'ordinateur de conduite autonome d'une Tesla Model 3, en utilisant des composants issus de véhicules accidentés.

**Points clés :**
*   **Approvisionnement :** Les composants essentiels (MCU, écran, câblage) sont disponibles sur le marché de l'occasion via des entreprises de démantèlement automobile.
*   **Documentation technique :** Tesla met à disposition publiquement son manuel de référence électrique, permettant d'identifier les schémas de câblage et l'assignation des broches (pinouts).
*   **Connectivité :** Le système expose un réseau Ethernet interne (sans DHCP, sous-réseau `192.168.90.X/24`) permettant d'accéder à divers services, dont un serveur SSH (protégé par certificat) et une interface de diagnostic REST (ODIN) sur le port 8080.
*   **Complexité physique :** Les câbles de liaison spécifiques (type Rosenberger) ne sont pas vendus individuellement ; ils font partie intégrante de faisceaux de câblage complets ("looms"), rendant les tentatives de bricolage risquées pour le matériel.

**Vulnérabilités et vecteurs d'attaque :**
*   **Services exposés :** L'interface de diagnostic ODIN et le serveur SSH constituent les surfaces d'attaque principales pour l'analyse du système.
*   **Absence de CVE spécifique :** L'article ne mentionne pas de CVE, mais souligne que l'accès root au système est une étape critique que Tesla encourage via son programme *Bug Bounty* ("Root access program"), récompensant les chercheurs par des certificats SSH valides.

**Recommandations et bonnes pratiques :**
*   **Sécurisation du diagnostic :** Les interfaces de diagnostic (ODIN) doivent faire l'objet de restrictions d'accès strictes pour éviter l'exécution de commandes non autorisées sur le bus interne du véhicule.
*   **Intégrité du matériel :** L'usage de composants de seconde main souligne l'importance pour les constructeurs de gérer la révocation des accès ou des clés de chiffrement liées au matériel lors du déclassement d'un véhicule.
*   **Précautions techniques :** Pour les chercheurs, l'utilisation de faisceaux officiels (plutôt que des connexions artisanales) est indispensable pour éviter les courts-circuits, ces systèmes de contrôle de puissance étant extrêmement sensibles et difficiles à réparer.

---
[Source](https://bugs.xdavidhu.me/tesla/2026/03/23/running-tesla-model-3s-computer-on-my-desk-using-parts-from-crashed-cars/){:target="_blank"}
