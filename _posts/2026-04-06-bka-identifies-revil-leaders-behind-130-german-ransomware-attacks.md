---
title: 'BKA Identifies REvil Leaders Behind 130 German Ransomware Attacks'
date: 2026-04-06
permalink: /posts/2026/04/06/bka-identifies-revil-leaders-behind-130-german-ransomware-attacks/
tags:
- veille-cyber
- hackernews
---
### Identification des leaders du groupe de ransomware REvil

La police fédérale allemande (BKA) a officiellement identifié deux figures centrales du groupe cybercriminel **REvil** (également connu sous le nom de Sodinokibi), responsable de nombreuses campagnes de ransomware à l'échelle mondiale :

*   **Daniil Maksimovich Shchukin (alias "UNKN")** : Identifié comme l'un des leaders et porte-parole du groupe. Il gérait le recrutement et la promotion du ransomware sur les forums cybercriminels depuis 2019.
*   **Anatoly Sergeevitsch Kravchuk** : Identifié comme le développeur principal du code malveillant REvil.

**Points clés :**
*   **Impact en Allemagne :** Les deux suspects sont impliqués dans 130 attaques visant des cibles allemandes, causant plus de 35,4 millions d'euros de dommages financiers.
*   **Modèle économique :** REvil opérait sous un modèle de "Ransomware-as-a-Service" (RaaS), comptant jusqu'à 60 affiliés, avec des demandes de rançon massives en échange du déchiffrement des données.
*   **Fin des opérations :** Après des actions coordonnées des forces de l'ordre internationales (FBI, agences européennes) et une intervention des services de sécurité russes (FSB) en 2022, le groupe a cessé ses activités. Plusieurs membres ont été condamnés à des peines de prison en Russie en octobre 2024.

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifique, car les attaques REvil reposaient sur diverses techniques d'intrusion (exploitation de vulnérabilités zero-day, compromission de la chaîne d'approvisionnement ou accès par identifiants volés/VPN), visant à chiffrer les systèmes pour exiger des paiements.

**Recommandations :**
Bien que le groupe REvil soit démantelé, la menace des ransomwares persiste. Il est recommandé de :
*   **Appliquer une stratégie de sauvegarde 3-2-1 :** Maintenir trois copies des données, sur deux supports différents, dont une hors ligne (immuable).
*   **Renforcer l'accès aux réseaux :** Utiliser l'authentification multifacteur (MFA) pour tous les accès distants et limiter les privilèges d'administration.
*   **Gestion des correctifs :** Maintenir les logiciels, les serveurs et les équipements réseau (notamment les VPN) constamment à jour pour combler les failles de sécurité exploitables.
*   **Surveillance et détection :** Déployer des solutions EDR (Endpoint Detection and Response) pour identifier les comportements suspects typiques d'une infection par ransomware (chiffrement massif, exfiltration de données).

---
[Source](https://thehackernews.com/2026/04/bka-identifies-revil-leaders-behind-130.html){:target="_blank"}
