---
title: 'Hackers Weaponize Balochistan Police Portal in Multi-Group Espionage Campaigns'
date: 2026-07-11
permalink: /posts/2026/07/11/hackers-weaponize-balochistan-police-portal-in-multi-group-espionage-campaigns/
tags:
- veille-cyber
- hackernews
---
### Espionnage cybernétique : convergence d'attaquants étatiques contre la police pakistanaise

Entre février 2024 et avril 2026, plusieurs entités des forces de l'ordre pakistanaises, notamment la police du Baloutchistan, ont été la cible de campagnes d'espionnage coordonnées menées par des groupes liés à la Chine et à l'Inde. L'objectif était de dérober des données sensibles, incluant des dossiers criminels, des registres biométriques et des informations sur le personnel.

**Points clés :**
*   **Double menace :** L'utilisation simultanée d'outils sophistiqués par des groupes aux intérêts géopolitiques divergents souligne la valeur stratégique des données policières.
*   **Détournement d'outils publics :** Le portail « Complaint Management System » (CMS) a été compromis pour distribuer des logiciels malveillants, infectant potentiellement à la fois les citoyens et les policiers.
*   **Infrastructure visée :** Les attaquants ont compromis des serveurs d'applications web, des équipements réseau et une passerelle de messagerie Fortinet FortiMail.

**Vulnérabilités et vecteurs d'attaque :**
*   **Malwares utilisés :** PlugX, ShadowPad (groupes chinois) ; Cobalt Strike (groupe lié à la Chine) ; Remcos RAT (groupe lié à l'Inde, possiblement *Mysterious Elephant*).
*   **Implants identifiés :** 
    *   Un stager en Rust déguisé en mise à jour du portail CMS.
    *   Un exécutable .NET imitant le logiciel de sécurité légitime `360Safe.exe` pour charger un client AsyncRAT.

**Recommandations :**
*   **Sécurisation des passerelles :** Mettre à jour et auditer rigoureusement les équipements réseau (notamment Fortinet) et les serveurs d'applications accessibles sur le web.
*   **Surveillance des logs :** Détecter les communications sortantes inhabituelles vers des serveurs de commande et contrôle (C2) connus ou suspects (ex: `142.171.183[.]8` et `193.42.25[.]65`).
*   **Intégrité des logiciels :** Mettre en place des mécanismes d'intégrité pour les mises à jour des portails web afin d'empêcher l'injection de binaires malveillants (type `cms_plugin.exe`).
*   **Protection des endpoints :** Renforcer la détection comportementale pour identifier les processus légitimes détournés (comme le masquage sous `360Safe.exe`).

---
[Source](https://thehackernews.com/2026/07/hackers-weaponize-balochistan-police.html){:target="_blank"}
