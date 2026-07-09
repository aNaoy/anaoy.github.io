---
title: 'New GigaWiper Windows Backdoor Bundles Disk Wiping, Fake Ransomware, and Spyware'
date: 2026-07-09
permalink: /posts/2026/07/09/new-gigawiper-windows-backdoor-bundles-disk-wiping-fake-ransomware-and-spyware/
tags:
- veille-cyber
- hackernews
---
### GigaWiper : Une menace multifonctionnelle destructive

**Points clés**
*   **Nature de la menace :** GigaWiper (aussi identifié sous le nom de **BLUERABBIT**) est une porte dérobée (*backdoor*) modulaire développée en Go. Elle combine des capacités d'espionnage avancées et trois outils de destruction irréversibles.
*   **Mode opératoire :** Contrairement à un ransomware classique, il n'y a aucune intention financière. Le logiciel utilise des outils de destruction (effacement de disque, écrasement de données ou faux ransomware sans clé de déchiffrement) pour rendre les systèmes inutilisables.
*   **Techniques d'évasion :** Le malware se dissimule en se faisant passer pour le processus `OneDrive`, utilise des tâches planifiées persistantes et exploite des services légitimes (RabbitMQ, Redis, MinIO) pour son trafic C2 (Command & Control), rendant son activité difficile à distinguer d'un usage professionnel.
*   **Attribution :** Des liens techniques (réutilisation de code, notamment le malware *Crucio*) suggèrent une origine liée à des groupes de cyber-acteurs iraniens.

**Vulnérabilités**
*   Il ne s'agit pas d'une faille logicielle spécifique (CVE), mais d'un implant déployé une fois l'accès initial obtenu. La menace repose sur l'exploitation des privilèges système pour modifier des fichiers critiques (ex: `bootmgr`, `ntoskrnl.exe`).

**Recommandations**
*   **Détection :**
    *   Surveiller la présence d'une tâche planifiée nommée « OneDrive Update » s'exécutant chaque minute.
    *   Détecter tout trafic inhabituel vers des services comme RabbitMQ ou Redis provenant de postes de travail standards.
    *   Surveiller l'utilisation anormale des commandes `takeown` et `icacls` sur les fichiers de démarrage de Windows.
*   **Défense :**
    *   Maintenir des sauvegardes hors ligne (offline) intègres, car les données chiffrées ou effacées par GigaWiper sont irrécupérables.
    *   Activer les fonctionnalités de protection contre les falsifications (*tamper protection*) pour empêcher la désactivation de l'antivirus.
    *   Bloquer les adresses serveurs identifiées : `185.182.193[.]21` et `212.8.248[.]104`.
    *   Activer les solutions de détection et de réponse sur les terminaux (EDR) en mode blocage.

---
[Source](https://thehackernews.com/2026/07/new-gigawiper-windows-backdoor-bundles.html){:target="_blank"}
