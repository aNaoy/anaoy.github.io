---
title: 'Three Threat Groups Target Russian Enterprises With Backdoors, Ransomware, and Wipers'
date: 2026-09-16
permalink: /posts/2026/09/16/three-threat-groups-target-russian-enterprises-with-backdoors-ransomware-and-wipers/
tags:
- veille-cyber
- hackernews
---
### Vague de cyberattaques contre les entreprises russes : analyse de trois groupes de menaces

Les entreprises russes font actuellement face à une recrudescence d'attaques menées par trois groupes distincts : **NightEagle**, **Hacking Cat** et **Toy Ghouls**. Ces acteurs utilisent des techniques allant de la porte dérobée (*backdoor*) persistante au chiffrement destructeur (*ransomware/wiper*).

#### Points clés par groupe
*   **NightEagle (APT-Q-95) :** Spécialisé dans l'espionnage et l'accès prolongé. Il privilégie l'utilisation d'identifiants VPN compromis et le déploiement de *GhostContainer*, un outil modulaire injecté en mémoire dans Microsoft Exchange, capable de rediriger le trafic et d'exécuter des commandes arbitraires.
*   **Hacking Cat :** Groupe activiste pro-ukrainien ayant délaissé les défigurations de sites web pour des attaques destructrices. Il déploie *Gorilla RAT* pour le contrôle à distance et plusieurs variantes du ransomware *Monkey* (Rust, .NET, Go, C++). Certaines versions agissent comme des *wipers* (effaceurs) en détruisant les clés de déchiffrement.
*   **Toy Ghouls :** Groupe motivé par le gain financier ayant développé ses propres outils, notamment le ransomware *GenieLocker* et une nouvelle porte dérobée nommée *Bird Agent*, qui utilise des canaux de communication atypiques comme le protocole MQTT (HiveMQ) ou la messagerie chiffrée Matrix (Element).

#### Vulnérabilités exploitées
Les attaquants tirent parti de failles connues pour s'introduire dans les réseaux et assurer leur mouvement latéral :
*   **CVE-2020-0688 :** Vulnérabilité de Microsoft Exchange utilisée par NightEagle.
*   **CVE-2019-0708 (BlueKeep) :** Exploitée pour obtenir des privilèges élevés via les services de bureau à distance.
*   **CVE-2021-26855 & CVE-2026-42897 :** Failles Microsoft Exchange exploitées par Hacking Cat.

#### Recommandations de sécurité
*   **Sécurisation des accès :** Implémenter une authentification multifacteur (MFA) robuste sur tous les accès VPN et accès distants.
*   **Gestion des correctifs :** Appliquer prioritairement les mises à jour de sécurité pour les serveurs Microsoft Exchange afin de neutraliser les vecteurs d'attaque courants.
*   **Surveillance Active Directory :** Détecter les comportements suspects tels que les attaques DCSync, les modifications anormales de groupes administrateurs et l'utilisation de tickets Kerberos de longue durée.
*   **Durcissement des systèmes :** Désactiver les services inutilisés, restreindre l'exécution de scripts PowerShell non signés et surveiller les communications sortantes vers des services de tunnels (type Azure Dev Tunnels ou outils de messagerie utilisés comme C2).
*   **Sauvegardes :** Maintenir des sauvegardes immuables et hors ligne pour contrer les effets destructeurs des ransomwares et des outils de type *wiper*.

---
[Source](https://thehackernews.com/2026/09/three-threat-groups-target-russian.html){:target="_blank"}
