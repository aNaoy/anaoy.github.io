---
title: 'Driver of destruction: How a legitimate driver is being used to take down AV processes'
date: 2025-08-07
permalink: /posts/2025/08/07/driver-of-destruction-how-a-legitimate-driver-is-being-used-to-take-down-av-processes/
tags:
- veille-cyber
- securelist
---
**Désactivation des Défenses : Le Driver ThrottleStop au Service des Cyberattaques**

Une nouvelle menace cible les logiciels antivirus (AV) en exploitant un driver légitime, `ThrottleStop.sys` (renommé `ThrottleBlood.sys` dans ce contexte), pour désactiver leurs processus. Cette technique, connue sous le nom de BYOVD (Bring Your Own Vulnerable Driver), a été observée dans des attaques menées depuis octobre 2024, affectant principalement la Russie, la Biélorussie, le Kazakhstan, l'Ukraine et le Brésil.

**Points Clés :**

*   **Mode Opératoire :** L'attaquant utilise un driver signé légalement pour obtenir un accès en mode noyau et manipuler la mémoire du système. Un exécutable (comme `All.exe`) est ensuite utilisé pour lancer ce driver et cibler les processus antivirus identifiés par leurs noms.
*   **Attaque Initiale :** Une attaque typique commence par l'obtention de identifiants valides, souvent via des méthodes comme le credential dumping (Mimikatz) et des mouvements latéraux (pass-the-hash). Dans un cas documenté, l'intrusion a permis de déployer le ransomware MedusaLocker après avoir désactivé les protections AV.
*   **Fonctionnement du Driver :** Le driver `ThrottleStop.sys` expose deux fonctions IOCTL vulnérables permettant la lecture et l'écriture en mémoire physique. Ces fonctions sont accessibles par tout utilisateur disposant de privilèges administratifs.
*   **Exploitation du Noyau :** L'outil malveillant utilise des fonctions noyau comme `NtQuerySystemInformation` pour trouver les adresses des modules chargés, y compris le noyau Windows (`ntoskrnl.exe`). Il exploite ensuite le driver vulnérable pour injecter du code dans des fonctions noyau critiques (comme `NtAddAtom`) afin de pouvoir appeler d'autres fonctions noyau (`PsLookupProcessById`, `PsTerminateProcess`) pour terminer les processus de sécurité.

**Vulnérabilités Identifiées :**

*   **CVE-2025-7771 :** Vulnérabilité dans `ThrottleStop.sys` permettant à un utilisateur privilégié de lire et écrire en mémoire physique via des appels IOCTL.

**Recommandations :**

*   **Sécurité des Accès :** Mettre en place des politiques de mots de passe forts, désactiver l'accès RDP aux adresses IP publiques, et utiliser l'authentification multi-facteurs (MFA) pour tous les canaux d'accès à distance.
*   **Défense en Profondeur :** Utiliser des listes blanches d'applications, appliquer des principes de moindre privilège, segmenter le réseau pour contenir les brèches, et mettre en œuvre des systèmes de détection et de prévention d'intrusions (IDS/IPS).
*   **Surveillance et Détection :** Déployer des solutions Endpoint Detection and Response (EDR) pour une surveillance en temps réel, conserver des journaux complets et mettre en place des alertes.
*   **Gestion des Vulnérabilités :** Assurer une gestion régulière des correctifs et effectuer des analyses automatisées des vulnérabilités. Les solutions de sécurité devraient surveiller la présence de drivers connus comme étant vulnérables.
*   **Protection des Solutions de Sécurité :** Les logiciels de protection doivent intégrer des mécanismes d'auto-défense robustes pour empêcher la modification ou la terminaison de leurs processus et fichiers.

L'utilisation de drivers légitimes détournés pour désactiver les protections représente une tactique efficace pour les attaquants cherchant à masquer leurs activités et à faciliter le déploiement de charges utiles destructrices.

---
[Source](https://securelist.com/av-killer-exploiting-throttlestop-sys/117026/){:target="_blank"}
