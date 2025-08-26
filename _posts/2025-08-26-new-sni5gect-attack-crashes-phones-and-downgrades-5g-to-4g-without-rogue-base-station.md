---
title: 'New Sni5Gect Attack Crashes Phones and Downgrades 5G to 4G without Rogue Base Station'
date: 2025-08-26
permalink: /posts/2025/08/26/new-sni5gect-attack-crashes-phones-and-downgrades-5g-to-4g-without-rogue-base-station/
tags:
- veille-cyber
- hackernews
---
### Nouvelle attaque Sni5Gect : dégradation de la 5G sans station de base compromise

Des chercheurs ont développé un nouveau framework logiciel open-source, nommé Sni5Gect, permettant de dégrader une connexion 5G vers une génération précédente (comme la 4G) sans nécessiter l'utilisation d'une station de base pirate. Cette méthode agit comme un tiers dans la communication, capturant les messages non chiffrés entre la station de base et l'équipement utilisateur (téléphone). En décodant ces messages lors de la procédure d'attachement, Sni5Gect identifie l'état de la connexion et injecte ensuite des charges utiles malveillantes.

L'attaque exploite la phase initiale de connexion, avant le chiffrement des communications, permettant ainsi de sniffer le trafic et d'injecter des messages sans connaître les identifiants de l'utilisateur. Les chercheurs ont démontré la capacité de Sni5Gect à faire planter le modem d'un téléphone, à identifier des appareils ciblés (fingerprinting) et à rétrograder la connexion à la 4G, ouvrant la voie à un suivi de localisation plus facile.

L'Association GSMA a reconnu cette vulnérabilité sous l'identifiant CVD-2024-0096.

**Points Clés :**

*   Développement d'une nouvelle attaque, Sni5Gect, pour compromettre les connexions 5G.
*   Permet la dégradation de la 5G vers la 4G sans station de base compromise.
*   Exploite la phase non chiffrée des communications initiales.
*   Fonctionnalités de sniffing de trafic et d'injection de messages over-the-air.
*   Capable de faire planter les modems, de réaliser du fingerprinting et de faciliter le suivi de localisation.

**Vulnérabilités :**

*   L'attaque Sni5Gect exploite les messages non chiffrés échangés entre la station de base (gNB) et l'équipement utilisateur (UE) avant l'établissement du contexte de sécurité NAS.
*   Il s'agit d'une extension des travaux précédents sur les failles 5Ghoul, qui avaient identifié 14 vulnérabilités dans les firmwares de modems MediaTek et Qualcomm.
*   L'attaque a été identifiée par la GSMA sous l'identifiant **CVD-2024-0096**.

**Recommandations :**

*   Sni5Gect est présenté comme un outil fondamental pour la recherche en sécurité 5G, permettant l'exploitation over-the-air.
*   Il encourage l'avancement de la recherche sur la détection et l'atténuation des intrusions au niveau paquet dans la 5G, ainsi que sur les améliorations de sécurité de la couche physique et au-delà.
*   Les chercheurs suggèrent que le développement de Sni5Gect aidera à améliorer les défenses et les futurs mécanismes de sécurité 5G.

---
[Source](https://thehackernews.com/2025/08/new-sni5gect-attack-crashes-phones-and.html){:target="_blank"}
