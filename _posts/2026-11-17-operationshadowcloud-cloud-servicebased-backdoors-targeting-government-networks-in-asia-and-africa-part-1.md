---
title: 'Operation ShadowCloud: cloud service–based backdoors targeting government networks in Asia and Africa. Part 1'
date: 2026-11-17
permalink: /posts/2026/11/17/operationshadowcloud-cloud-servicebased-backdoors-targeting-government-networks-in-asia-and-africa-part-1/
tags:
- veille-cyber
- securelist
---
### Operation ShadowCloud : Des backdoors furtives exploitant des services cloud

L'opération **ShadowCloud** est une campagne d'intrusion active identifiée début 2026, ciblant principalement des réseaux gouvernementaux en Asie et en Afrique. Les attaquants utilisent l'utilitaire légitime **MeshAgent** pour déployer des backdoors modulaires (**GraphDoor** et **GitDoor**) dont le trafic de commande et de contrôle (C2) est dissimulé au sein de services cloud légitimes (**Microsoft SharePoint, GitHub et Ably**).

#### Points clés
*   **Furtivité :** Le trafic malveillant se fond dans le trafic réseau normal grâce à l'utilisation d'infrastructures cloud populaires, rendant la détection basée sur le réseau extrêmement difficile.
*   **Modularité :** Les backdoors chargent des plug-ins à la demande et injectent des "shellcodes" directement en mémoire (sans écriture sur le disque), facilitant l'évolution des capacités d'attaque (keylogging, capture d'écran, proxy, etc.).
*   **Techniques d'évasion :** Utilisation de DLL sideloading via des exécutables légitimes (ex: `javaw.exe`, `pythonw.exe`, `zoomit.exe`) et obfuscation du code par "Control Flow Flattening".
*   **Infrastructure :** Le groupe utilise des dépôts GitHub dédiés pour échanger les commandes et exfiltrer les données des victimes, avec une préparation d'infrastructure remontant au moins à fin 2024.

#### Vulnérabilités exploitées
*   **PetitPotam (abus du protocole EFSRPC) :** Utilisé pour forcer une cible à initier une authentification NTLM vers une destination contrôlée par l'attaquant.
*   **Détournement de DLL (DLL Sideloading) :** Exploitation de la méthode de recherche de bibliothèques Windows pour charger des loaders malveillants.

#### Recommandations
1.  **Surveillance du trafic réseau :** Surveiller les connexions inhabituelles vers GitHub et Ably, particulièrement celles initiées par des processus légitimes ou inhabituels.
2.  **Gestion des exécutables :** Limiter l'exécution de binaires tiers ou non signés, et surveiller particulièrement les services Windows créés ou modifiés récemment.
3.  **Audit des terminaux :** Inspecter la mémoire des processus suspects à la recherche de "shellcodes" injectés ou de segments de mémoire anormaux (`PAGE_EXECUTE_READWRITE`).
4.  **Durcissement (Hardening) :** Désactiver les fonctionnalités inutiles (ex: EFSRPC) et surveiller l'utilisation de PowerShell, des tâches planifiées et du Registre Windows pour détecter des activités de persistance.
5.  **Analyse comportementale :** Privilégier des solutions EDR capables de détecter les injections de processus en mémoire (ex: `CreateRemoteThread`, `NtQueueApcThread`) plutôt que la simple signature de fichiers.

---
[Source](https://securelist.com/operation-shadowcloud-gitdoor/122004/){:target="_blank"}
