---
title: 'Dozens of Vendors Patch Security Flaws Across Enterprise Software and Network Devices'
date: 2026-03-11
permalink: /posts/2026/03/11/dozens-of-vendors-patch-security-flaws-across-enterprise-software-and-network-devices/
tags:
- veille-cyber
- hackernews
---
### Vague de correctifs critiques pour les logiciels et équipements réseau

Un large éventail de fournisseurs informatiques a récemment publié des correctifs de sécurité pour combler de nombreuses vulnérabilités dans leurs logiciels et équipements réseau.

**Points clés :**
*   **SAP :** Correction de deux failles critiques permettant l'exécution de code arbitraire.
*   **HPE :** Résolution d'une faille critique (CVE-2026-23813) dans les switches Aruba AOS-CX, permettant potentiellement de contourner l'authentification et de prendre le contrôle total du matériel.
*   **Microsoft et Adobe :** Déploiement massif de correctifs pour 84 et 80 vulnérabilités respectivement, incluant des risques d'élévation de privilèges et d'exécution de code à distance.
*   **Écosystème étendu :** De nombreux autres acteurs (dont Google, VMware, Cisco, Atlassian, et plusieurs distributions Linux) ont également mis à jour leurs solutions.

**Vulnérabilités notables :**
*   **CVE-2019-17571 (Score 9.8) :** Injection de code dans SAP FS-QUO due à une version obsolète d'Apache Log4j 1.2.17.
*   **CVE-2026-27685 (Score 9.1) :** Désérialisation non sécurisée dans SAP NetWeaver Enterprise Portal.
*   **CVE-2026-23813 (Score 9.8) :** Contournement de l'authentification dans l'interface de gestion Web des switches Aruba AOS-CX.

**Recommandations :**
*   **Prioriser les mises à jour :** Appliquer immédiatement les correctifs fournis par les éditeurs, en commençant par les systèmes exposés ou critiques (notamment les équipements réseau et portails d'administration).
*   **Audit des dépendances :** Identifier et mettre à jour les composants tiers obsolètes (tels que les anciennes versions de bibliothèques Java) intégrés dans les applications métier.
*   **Vigilance réseau :** Renforcer la surveillance des interfaces de gestion des équipements réseau pour détecter toute tentative d'accès non autorisé.

---
[Source](https://thehackernews.com/2026/03/dozens-of-vendors-patch-security-flaws.html){:target="_blank"}
