---
title: 'FCC Blocks New Foreign-Produced Robots and Power Inverters Over Cyber Risks'
date: 2026-07-30
permalink: /posts/2026/07/30/fcc-blocks-new-foreign-produced-robots-and-power-inverters-over-cyber-risks/
tags:
- veille-cyber
- hackernews
---
### Restrictions sur les robots et onduleurs étrangers : Nouvelle directive de la FCC

La Commission fédérale des communications (FCC) américaine a étendu sa liste d'équipements sous surveillance ("Covered List") aux robots mobiles et aux onduleurs de puissance connectés de fabrication étrangère. Cette mesure interdit, à compter du 28 juillet, l'autorisation de mise sur le marché de nouveaux modèles présentant des risques de sécurité nationale, bien que les équipements déjà en service ou déjà autorisés ne soient pas concernés.

**Points clés :**
* **Champ d'application :** La restriction cible tout équipement ne répondant pas aux normes de fabrication domestique ("Buy American").
* **Robots visés :** Appareils mobiles autonomes (plus de 4,4 lbs) dotés de capacités de navigation, de capteurs environnementaux et de connectivité (≥ 200 kbps), incluant les logiciels de contrôle et les modèles d'IA.
* **Onduleurs visés :** Systèmes de conversion d'énergie (CC/CA) équipés de fonctionnalités de contrôle ou de communication à distance.
* **Dérogations :** Un moratoire permet la maintenance logicielle (correctifs de sécurité) jusqu'au 1er janvier 2029. Une approbation conditionnelle via le ministère de la Guerre ou le DHS reste possible jusqu'au 1er janvier 2028.

**Vulnérabilités identifiées :**
* **CVE-2025-35027 :** Faille liée au Bluetooth Low Energy (BLE) permettant l'exécution de code arbitraire (root) sur les robots Unitree (modèles Go2, B2, G1, H1).
* **CVE-2025-2894 :** Vulnérabilité permettant une prise de contrôle totale à distance via le service CloudSail sur les robots Unitree Go1.
* **Risques globaux :** Accès non autorisé aux flux vidéo, aux cartes de navigation et exfiltration de données sensibles. Pour les onduleurs, les recherches (ex: étude SUN:DOWN) pointent 46 failles critiques pouvant mener à une déstabilisation du réseau électrique.

**Recommandations :**
* Les fabricants doivent se conformer aux normes de souveraineté technologique pour toute nouvelle importation.
* Prioriser l'application des correctifs de sécurité autorisés par la FCC pour maintenir la compatibilité des systèmes existants.
* Évaluer les risques de supply-chain liés aux accès distants, identifiés comme vecteurs principaux de sabotage des infrastructures critiques.

---
[Source](https://thehackernews.com/2026/07/fcc-blocks-new-foreign-produced-robots.html){:target="_blank"}
