---
title: 'Survey of 100+ Energy Systems Reveals Critical OT Cybersecurity Gaps'
date: 2026-01-29
permalink: /posts/2026/01/29/survey-of-100-energy-systems-reveals-critical-ot-cybersecurity-gaps/
tags:
- veille-cyber
- hackernews
---
### Défis de Cybersécurité dans les Systèmes Énergétiques : Une Étude Révèle des Lacunes Critiques

Une analyse approfondie menée sur plus de 100 installations de réseaux électriques, incluant des sous-stations, des centrales et des centres de contrôle, a mis en lumière des vulnérabilités majeures dans la cybersécurité de la technologie opérationnelle (OT). Ces défaillances, qu'elles soient techniques, organisationnelles ou fonctionnelles, exposent l'infrastructure énergétique à des cyberattaques. L'étude, basée sur l'utilisation d'un système de détection d'intrusions (IDS) comme StationGuard d'OMICRON, a révélé que la plupart des problèmes critiques étaient identifiés en moins de 30 minutes après la connexion de l'outil.

#### Points Clés :

*   **Généralisation des failles :** Les systèmes OT dans le secteur de l'énergie présentent des lacunes généralisées en matière de cybersécurité.
*   **Rapidité de détection :** Les problèmes de sécurité et opérationnels critiques sont souvent repérés très rapidement lors de l'évaluation.
*   **Complexité croissante :** La convergence entre les réseaux IT et OT accroît la surface d'attaque, tandis que la sécurisation des infrastructures vieillissantes reste un défi.
*   **Nécessité de détection réseau :** Compte tenu de l'impossibilité d'installer des logiciels de détection sur de nombreux dispositifs OT, la détection au niveau du réseau est essentielle.
*   **Automatisation de l'inventaire :** La création et la maintenance manuelles d'inventaires d'actifs sont complexes ; des méthodes passives et actives sont nécessaires pour une découverte complète.

#### Vulnérabilités Identifiées :

*   **Appareils PAC obsolètes :**
    *   Firmware non mis à jour contenant des vulnérabilités connues.
    *   Exemple : **CVE-2015-5374** (attaque par déni de service sur des relais de protection via un paquet UDP).
    *   Vulnérabilités dans les implémentations GOOSE et les piles de protocoles MMS.
*   **Connexions externes à risque :**
    *   Présence de connexions TCP/IP externes non documentées.
*   **Services non essentiels et non sécurisés :**
    *   Services de partage de fichiers Windows (NetBIOS) inutilisés.
    *   Services IPv6.
    *   Services de gestion de licences avec privilèges élevés.
    *   Fonctions de débogage PLC non sécurisées.
*   **Segmentation réseau faible :**
    *   Réseaux "plats" permettant une communication non restreinte entre de nombreux appareils.
    *   Accessibilité des réseaux IT des bureaux depuis des sous-stations distantes.
*   **Appareils inattendus :**
    *   Caméras IP, imprimantes, dispositifs d'automatisation non répertoriés dans les inventaires.
*   **Problèmes organisationnels :**
    *   Frontières floues entre les équipes IT et OT.
    *   Manque de personnel dédié à la sécurité OT.
    *   Contraintes de ressources.
*   **Problèmes fonctionnels/opérationnels :**
    *   Problèmes de VLAN (marquage incohérent des messages GOOSE).
    *   Incompatibilités RTU et SCD entraînant des ruptures de communication.
    *   Erreurs de synchronisation horaire.
    *   Problèmes de redondance réseau (boucles RSTP, configurations de commutateurs défectueuses).

#### Recommandations :

*   **Mettre en place des solutions de sécurité dédiées aux environnements OT.**
*   **Utiliser des systèmes de détection d'intrusions (IDS) au niveau du réseau** pour surveiller passivement les communications.
*   **Établir des inventaires d'actifs précis et complets** en combinant des méthodes passives (fichiers SCD) et actives (requêtes MMS).
*   **Actualiser régulièrement les firmwares des appareils** pour corriger les vulnérabilités connues.
*   **Auditer et sécuriser les connexions externes** et désactiver les services inutiles et non sécurisés.
*   **Renforcer la segmentation réseau** pour limiter la propagation des incidents.
*   **Clarifier les responsabilités en matière de sécurité OT** et allouer des ressources adéquates.
*   **Corriger les problèmes opérationnels** tels que les configurations VLAN, la synchronisation horaire et la redondance réseau.

---
[Source](https://thehackernews.com/2026/01/survey-of-100-energy-systems-reveals.html){:target="_blank"}
