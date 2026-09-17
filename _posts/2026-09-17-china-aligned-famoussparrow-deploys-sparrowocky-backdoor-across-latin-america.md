---
title: 'China-Aligned FamousSparrow Deploys SparroWocky Backdoor Across Latin America'
date: 2026-09-17
permalink: /posts/2026/09/17/china-aligned-famoussparrow-deploys-sparrowocky-backdoor-across-latin-america/
tags:
- veille-cyber
- hackernews
---
### Espionnage cybernétique : Le groupe FamousSparrow déploie le backdoor SparroWocky en Amérique latine

Le groupe de cyberespionnage FamousSparrow, lié à des intérêts étatiques chinois, a substitué son ancien malware « SparrowDoor » par une nouvelle porte dérobée modulaire en C++ nommée **SparroWocky**. Active depuis 2019, cette menace cible principalement des entités gouvernementales en Amérique latine (Argentine, Équateur, Guatemala, Honduras, Panama, Pérou, Porto Rico, Venezuela) depuis juillet 2025.

**Points clés :**
*   **Architecture avancée :** Le malware intègre directement des outils open source (Mbed TLS, MinHook, COFF Loader, SilentMoonwalk) pour sécuriser ses communications C2, contourner les outils de sécurité et charger des plugins en mémoire.
*   **Fonctionnalités :** Exécution de commandes et de fichiers, proxy TCP, exfiltration de données, captures d'écran, et capacité d'auto-suppression.
*   **Mode opératoire :** Utilisation de la technique de *DLL sideloading* (chargement latéral de DLL) pour charger la charge utile principale via un exécutable légitime.

**Vulnérabilités :**
*   Le vecteur d'accès initial demeure inconnu.
*   Le malware exploite le *DLL sideloading* pour l'exécution, une technique courante liée à la configuration des systèmes Windows ciblés plutôt qu'à une CVE spécifique.

**Recommandations :**
*   **Surveillance du réseau :** Bloquer ou surveiller le trafic vers l'adresse IP associée au serveur de commande et de contrôle identifiée : `216.238.110.120`.
*   **Gestion des DLL :** Auditer les répertoires applicatifs pour détecter la présence de DLL suspectes placées à côté d'exécutables légitimes.
*   **Détection comportementale :** Mettre en œuvre des solutions EDR capables de détecter les comportements suspects liés au *hooking* d'API (via MinHook) et aux manipulations de piles d'appels (*call stack spoofing*).
*   **Analyse de la mémoire :** Porter une attention particulière aux processus qui chargent des objets COFF dynamiquement en mémoire, une technique utilisée par SparroWocky pour dissimuler ses activités.

---
[Source](https://thehackernews.com/2026/09/china-aligned-famoussparrow-deploys.html){:target="_blank"}
