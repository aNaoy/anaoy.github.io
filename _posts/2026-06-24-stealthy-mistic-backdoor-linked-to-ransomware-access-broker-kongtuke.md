---
title: 'Stealthy Mistic backdoor linked to ransomware access broker KongTuke'
date: 2026-06-24
permalink: /posts/2026/06/24/stealthy-mistic-backdoor-linked-to-ransomware-access-broker-kongtuke/
tags:
- veille-cyber
- bleepingcomp
---
### Menace persistante : Le backdoor Mistic au service des courtiers d'accès

Mistic (aussi appelé MTLBackdoor) est un nouveau logiciel malveillant furtif utilisé depuis avril 2024 pour infiltrer durablement les réseaux d'entreprises. Attribué au courtier d'accès KongTuke, ce backdoor sert de tête de pont pour revendre des accès à divers groupes de ransomwares tels que Qilin, Akira ou Black Basta.

**Points clés :**
* **Vecteur d'attaque :** Souvent déployé après le backdoor ModeloRAT via des campagnes d'ingénierie sociale (Microsoft Teams) ou des techniques de type « ClickFix ».
* **Discrétion extrême :** Utilise le chargement latéral de DLL (*DLL sideloading*) en se faisant passer pour des outils de sécurité légitimes (ex: `EndpointDlp.dll` chargé par `MpExtMs.exe`).
* **Fonctionnalités :** Gestion complète des fichiers, exécution de code en mémoire, et déploiement de *Beacon Object Files* (BOF) pour éviter toute trace sur le disque.
* **Vol d'identifiants :** Intègre un module .NET affichant une fausse page de connexion pour dérober les accès des utilisateurs.

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée ; l'attaque repose sur le détournement de processus légitimes et l'exploitation de l'ingénierie sociale pour contourner les protections natives des systèmes d'exploitation.

**Recommandations :**
* **Surveillance EDR/SIEM :** Surveiller les exécutions anormales de DLL par des processus système légitimes, particulièrement ceux se faisant passer pour des outils de sécurité.
* **Sensibilisation :** Former les employés aux tactiques d'ingénierie sociale, notamment les fausses alertes de support ou de sécurité via des plateformes collaboratives comme Microsoft Teams.
* **Contrôle des privilèges :** Restreindre les capacités d'exécution de code en mémoire pour limiter l'efficacité des BOF.
* **Analyse des comportements :** Porter une attention particulière aux processus inconnus tentant de communiquer avec des serveurs de commande et contrôle (C2) et bloquer les extensions de navigateur non approuvées (type NexShield).

---
[Source](https://www.bleepingcomputer.com/news/security/stealthy-mistic-backdoor-linked-to-ransomware-access-broker-kongtuke/){:target="_blank"}
