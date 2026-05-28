---
title: 'Pirates in the crosshairs: how one cybercrime gang has been infecting book, movie, and TV show fans for years'
date: 2026-05-28
permalink: /posts/2026/05/28/pirates-in-the-crosshairs-how-one-cybercrime-gang-has-been-infecting-book-movie-and-tv-show-fans-for-years/
tags:
- veille-cyber
- securelist
---
### Campagne de cybercriminalité : Distribution massive de mineurs de cryptomonnaie via le streaming illégal

Une campagne persistante, active depuis au moins 2022, cible les utilisateurs de sites de streaming illégal (films, séries) et de bibliothèques numériques. En utilisant de fausses mises à jour de lecteurs vidéo, les attaquants infectent les machines pour y déployer des mineurs de cryptomonnaie et des outils d'administration à distance (RAT).

**Points clés :**
*   **Vecteur d'infection :** Téléchargement d'une archive ZIP contenant un exécutable légitime et une DLL malveillante, exploitant le *DLL side-loading*.
*   **Propagation :** Le malware utilise des sites à fort trafic (jusqu'à 40 millions de visites mensuelles cumulées).
*   **Techniques de dissimulation :** Utilisation de codes "junk" pour gonfler la taille des fichiers, exécution par *process hollowing* et *reflective loading* (chargement en mémoire sans écriture disque).
*   **Persistance :** Création de services système factices (ex: `GoogleUpdateTaskMachineQC`) et modification du registre.
*   **Communication C2 :** Utilisation de tunnels DNS, de domaines générés par algorithme (DGA) basés sur la date, et chiffrement AES-CBC pour masquer les échanges.

**Vulnérabilités exploitées :**
*   **Dépassement de tampon (Buffer Overflow) :** La DLL contient une fonction `SmashStack` qui écrase un tampon de 64 octets sans vérification de taille, permettant l'injection et l'exécution de *shellcode* via une chaîne ROP.
*   **Détournement de processus :** Exploitation du *DLL Side-loading* et du *Process Hollowing*.
*(Note : Aucune CVE spécifique n'est mentionnée dans le rapport pour ces vulnérabilités logicielles).*

**Recommandations :**
*   **Abstention :** Éviter l'accès aux sites de contenu piraté, principaux vecteurs de cette menace.
*   **Prudence face aux mises à jour :** Ne jamais installer de plugins ou de mises à jour de lecteurs vidéo proposés par des sites tiers non officiels.
*   **Sécurité des processus :** Surveiller les processus suspects tels que `conhost.exe` ou `explorer.exe` effectuant des connexions réseau inhabituelles.
*   **Protection système :** Maintenir les solutions antivirus à jour ; les signatures génériques (ex: `HEUR:Trojan.Win64.DllHijack.gen`) permettent de détecter cette menace.
*   **Hygiène informatique :** En cas d'infection, terminer prioritairement le module *Watchdog* (exécuté dans `explorer.exe`) avant toute tentative de suppression manuelle, sous peine de réinstallation automatique par le malware.

---
[Source](https://securelist.com/video-books-pirates-miners-rat/119943/){:target="_blank"}
