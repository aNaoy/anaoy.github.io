---
title: 'Coordinated Cyberattack Targets 30+ Minnesota Water Systems as One Plant Goes Offline'
date: 2026-07-29
permalink: /posts/2026/07/29/coordinated-cyberattack-targets-30-minnesota-water-systems-as-one-plant-goes-offline/
tags:
- veille-cyber
- hackernews
---
### Attaque coordonnée contre les infrastructures hydrauliques du Minnesota

Une campagne cybercriminelle coordonnée a ciblé, les 26 et 27 juillet, les systèmes de contrôle opérationnel de plus de 30 installations hydrauliques au Minnesota. Bien que l'attribution officielle soit toujours en cours, les modes opératoires observés présentent des similitudes marquées avec les tactiques du groupe « CyberAv3ngers » (affilié au Corps des gardiens de la révolution islamique iranien), connu pour viser les systèmes de contrôle industriel (ICS).

**Points clés :**
*   **Impact opérationnel :** Les perturbations ont varié selon les sites, incluant des pannes complètes d'usines, des coupures de communication cellulaire et des défaillances des contrôles automatisés.
*   **Réponse :** Une coordination immédiate entre les services de l'État (MNIT), la CISA, le FBI et l'EPA a permis de contenir les incidents.
*   **Cible :** Les infrastructures critiques, spécifiquement les automates programmables industriels (API/PLC) et les interfaces homme-machine (IHM).

**Vulnérabilités :**
*   Aucune CVE spécifique n'a été nommée publiquement à ce stade.
*   Les attaques exploitent généralement des accès exposés sur Internet vers des équipements industriels (PLC/SCADA) de constructeurs tels que Rockwell Automation, Schneider Electric et Siemens.

**Recommandations de sécurité (CISA) :**
*   **Sécurisation des accès :** Restreindre strictement l'accès aux contrôleurs industriels aux seuls systèmes autorisés.
*   **Monitoring :** Auditer et journaliser systématiquement toutes les connexions via modems cellulaires.
*   **Intégrité des systèmes :** Inspecter régulièrement les fichiers de projets pour détecter toute modification non autorisée et valider les sauvegardes avant toute restauration.
*   **Contrôle physique :** Sur les équipements dotés d'un commutateur de mode physique, s'assurer que le mode « run » n'est activé qu'après une vérification complète des configurations.

---
[Source](https://thehackernews.com/2026/07/coordinated-cyberattack-targets-30.html){:target="_blank"}
