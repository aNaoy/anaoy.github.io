---
title: 'FIRESTARTER Backdoor Hit Federal Cisco Firepower Device, Survives Security Patches'
date: 2026-04-24
permalink: /posts/2026/04/24/firestarter-backdoor-hit-federal-cisco-firepower-device-survives-security-patches/
tags:
- veille-cyber
- hackernews
---
### Persistance persistante du backdoor FIRESTARTER sur les équipements Cisco

Des agences gouvernementales ont identifié une campagne menée par des acteurs étatiques (associés au groupe UAT4356) visant les appareils Cisco Firepower et Adaptive Security Appliance (ASA). Cette intrusion repose sur le déploiement du backdoor **FIRESTARTER**, capable de survivre aux mises à jour de firmware et aux redémarrages système standard, garantissant un accès pérenne aux attaquants.

**Points clés :**
*   **Mode opératoire :** L'attaquant exploite des vulnérabilités pour déployer le toolkit **LINE VIPER**, permettant l'exécution de commandes système, le contournement de l'authentification VPN et l'interception du trafic.
*   **Persistance :** FIRESTARTER s'installe dans la séquence de démarrage du système en manipulant les listes de montage. Le malware intercepte les requêtes WebVPN via des "paquets magiques" pour exécuter du code arbitraire.
*   **Inefficacité des mises à jour :** Les correctifs de sécurité appliqués par les administrateurs ne suppriment pas le malware s'il est déjà présent sur l'appareil.

**Vulnérabilités exploitées :**
*   **CVE-2025-20333 (Score CVSS 9.9) :** Validation incorrecte des entrées utilisateur permettant l'exécution de code à distance (RCE) avec des privilèges root via des requêtes HTTP contrefaites.
*   **CVE-2025-20362 (Score CVSS 6.5) :** Accès non autorisé à des endpoints restreints via une validation insuffisante des entrées.

**Recommandations :**
*   **Élimination immédiate :** Un simple redémarrage logiciel (reboot) est inefficace. Il est impératif d'effectuer une coupure électrique physique (« cold restart ») pour neutraliser temporairement le processus.
*   **Assainissement total :** Cisco recommande formellement de **réimager complètement** les équipements compromis et de les mettre à jour. Toute configuration existante doit être considérée comme compromise et non fiable.
*   **Vigilance accrue :** Surveiller les réseaux de périphériques IoT/SOHO, souvent utilisés comme nœuds de rebond pour masquer l'origine des attaques persistantes.

---
[Source](https://thehackernews.com/2026/04/firestarter-backdoor-hit-federal-cisco.html){:target="_blank"}
