---
title: 'CISA warns of cyberattacks disrupting U.S. water utilities'
date: 2026-07-31
permalink: /posts/2026/07/31/cisa-warns-of-cyberattacks-disrupting-us-water-utilities/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaques contre les infrastructures hydrauliques : Alerte sur les automates exposés

La CISA a émis une alerte urgente suite à une vague d'attaques coordonnées visant les systèmes de traitement des eaux aux États-Unis, notamment dans le Minnesota. Ces cyberattaques exploitent des automates programmables industriels (API/PLC) directement exposés sur Internet pour perturber les opérations, modifier les adresses IP et verrouiller l'accès aux opérateurs.

**Points clés :**
*   **Cible :** Systèmes de contrôle industriel (OT) et API/PLC au sein des infrastructures hydrauliques.
*   **Impact :** Plus de 30 systèmes affectés, entraînant des pannes d'équipement et le passage forcé en mode manuel.
*   **Vecteur principal :** Exposition directe des API sur Internet, incluant des modems cellulaires non répertoriés (souvent oubliés ou mal documentés).
*   **Volume de risque :** Des milliers d'appareils (Rockwell Automation, Siemens, Schneider Electric) restent accessibles publiquement.

**Vulnérabilités :**
*   **Exposition publique :** API connectés directement à Internet sans protection périmétrique.
*   **Gestion des identifiants :** Utilisation de mots de passe par défaut.
*   **Logiciels obsolètes :** Présence de firmwares en fin de vie (End-of-Sale), notamment sur les Rockwell Automation MicroLogix 1400.
*   **Absence de visibilité :** Modems cellulaires intégrés par des tiers non inventoriés par les équipes IT.

**Recommandations :**
*   **Suppression de l'exposition :** Retirer immédiatement tout dispositif OT de l'accès public Internet.
*   **Sécurisation des accès :** Utiliser exclusivement des VPN ou des passerelles sécurisées pour accéder aux systèmes distants.
*   **Durcissement :** Changer systématiquement les mots de passe par défaut et restreindre l'accès réseau via une liste blanche d'adresses IP (allow-list).
*   **Audit :** Inventorier l'ensemble des modems cellulaires et équipements OT, y compris ceux installés par des intégrateurs tiers.
*   **Récupération :** Consulter les guides constructeurs (notamment pour Rockwell Automation) pour restaurer l'accès aux dispositifs compromis.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-warns-of-cyberattacks-disrupting-us-water-utilities/){:target="_blank"}
