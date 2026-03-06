---
title: 'China-Linked Hackers Use TernDoor, PeerTime, BruteEntry in South American Telecom Attacks'
date: 2026-03-06
permalink: /posts/2026/03/06/china-linked-hackers-use-terndoor-peertime-bruteentry-in-south-american-telecom-attacks/
tags:
- veille-cyber
- hackernews
---
### Cyber-espionnage contre les télécoms en Amérique du Sud : Analyse de la menace UAT-9244

Le groupe de cyberespionnage **UAT-9244**, lié à des acteurs chinois, mène depuis 2024 des campagnes visant les infrastructures de télécommunications en Amérique du Sud. Ce groupe, dont les tactiques se rapprochent de *FamousSparrow*, utilise un arsenal de trois implants sophistiqués pour compromettre des environnements Windows, Linux et des dispositifs réseau en périphérie.

**Points clés :**
*   **TernDoor (Windows) :** Backdoor déployée via *DLL side-loading* (utilisation du processus légitime `wsprint.exe`). Elle intègre un pilote Windows pour masquer ses activités et manipuler les processus.
*   **PeerTime (Linux) :** Backdoor P2P (disponible en C++ et Rust) utilisant le protocole BitTorrent pour ses communications C2. Elle est conçue pour infecter divers systèmes embarqués et vérifier la présence de Docker avant exécution.
*   **BruteEntry (Edge Devices) :** Scanner basé en Go, déployé sur des équipements réseau pour transformer ceux-ci en nœuds relais (ORB). Il effectue des attaques par force brute contre des services Postgres, SSH et Tomcat.
*   **Origine :** L'implication d'acteurs chinois est corroborée par la découverte de chaînes de débogage en chinois simplifié dans les outils d'instrumentation.

**Vulnérabilités exploitées :**
*   Bien que les méthodes d'accès initiales précises ne soient pas documentées dans cette campagne, le groupe cible historiquement des versions obsolètes de **Windows Server** et **Microsoft Exchange Server** pour déployer des web shells. Aucune CVE spécifique n'est mentionnée, mais l'exploitation de serveurs non patchés reste le vecteur principal.

**Recommandations :**
*   **Mise à jour des systèmes :** Appliquer immédiatement les correctifs de sécurité sur les serveurs Windows et Microsoft Exchange pour prévenir l'installation de web shells.
*   **Surveillance des processus :** Auditer les activités suspectes liées au *DLL side-loading* (ex: processus légitimes lançant des DLL non signées) et surveiller les tâches planifiées ou les clés de registre de persistance.
*   **Sécurisation de la périphérie :** Durcir les configurations des équipements réseau (edge devices), restreindre les accès SSH/Tomcat/Postgres et surveiller les flux réseau inhabituels (notamment le trafic lié au protocole BitTorrent).
*   **Audit des conteneurs :** Vérifier régulièrement les environnements Docker pour détecter la présence de scripts d'instrumentation ou de binaires malveillants (PeerTime).

---
[Source](https://thehackernews.com/2026/03/china-linked-hackers-use-terndoor.html){:target="_blank"}
