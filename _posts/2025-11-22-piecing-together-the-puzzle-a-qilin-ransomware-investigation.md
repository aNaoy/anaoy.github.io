---
title: 'Piecing Together the Puzzle: A Qilin Ransomware Investigation'
date: 2025-11-22
permalink: /posts/2025/11/22/piecing-together-the-puzzle-a-qilin-ransomware-investigation/
tags:
- veille-cyber
- bleepingcomp
---
**L'enquête sur le rançongiciel Qilin : Reconstruction d'une attaque avec des données limitées**

Une analyse post-incident d'une infection par le rançongiciel Qilin a été menée malgré une visibilité réduite, le déploiement de l'outil d'analyse n'ayant eu lieu qu'après la compromission et sur un seul point de terminaison. L'absence de données EDR (Endpoint Detection and Response) ou SIEM (Security Information and Event Management) a nécessité l'exploitation d'autres sources, notamment les alertes antivirus et les journaux système.

L'attaquant a initialement accédé au système le 8 octobre 2025, installant le "Total Software Deployment Service" et une instance non autorisée de "ScreenConnect RMM" pointant vers l'adresse IP 94.156.232[.]40. Une activité notable inclut le transfert de trois fichiers via ScreenConnect le 11 octobre : "r.ps1", "s.exe" et "ss.exe". Le script "r.ps1", destiné à collecter des informations sur les connexions RDP, n'a pas pu être exécuté en raison des restrictions de script.

Les fichiers "s.exe" et "ss.exe", absents du système, ont pu être identifiés grâce aux artefacts des journaux du "Program Compatibility Assistant" (PCA) et à l'analyse sur VirusTotal. "s.exe" semble être un infostealer qui a échoué lors de son exécution. "ss.exe" a également échoué à se lancer, provoquant le lancement de l'application légitime "werfault.exe".

Avant ces tentatives, l'attaquant avait désactivé la protection en temps réel de Windows Defender. La détection ultérieure de notes de rançongiciel par Windows Defender, suivie d'une tentative de connexion à distance, suggère que l'exécutable du rançongiciel a été lancé à partir d'un autre point de terminaison, ciblant potentiellement les partages réseau.

Qilin est une variante de ransomware-as-a-service (RaaS), impliquant des modèles d'attaque variés selon les affiliés. L'exploitation de multiples sources de données, même limitées, a permis de mieux comprendre les tentatives de l'attaquant, de valider les découvertes et de fournir une image plus précise de l'incident.

**Points Clés :**

*   Installation d'une instance non autorisée de ScreenConnect RMM.
*   Tentative de déploiement de fichiers malveillants, dont un infostealer.
*   Désactivation temporaire de Windows Defender.
*   Exécution du rançongiciel Qilin, probablement à partir d'un autre point de terminaison.
*   Importance de la corrélation de différentes sources de données pour une analyse complète.

**Vulnérabilités / Mécanismes d'attaque exploités :**

*   Utilisation d'une instance non autorisée de logiciel de gestion à distance (RMM) pour la pénétration et le déploiement.
*   Désactivation des protections de sécurité (Windows Defender).
*   Exécution de scripts et d'exécutables malveillants.
*   Potentialité d'attaques par mouvement latéral via les partages réseau.

**Recommandations / Indicateurs de Compromission (IOCs) :**

*   **IOCs :**
    *   Identifiant de l'instance ScreenConnect non autorisée.
    *   Hashes des fichiers s.exe et ss.exe.
    *   Contenu des notes de rançongiciel Qilin.
*   **Recommandations :**
    *   Utiliser et déployer des outils de sécurité (EDR, SIEM) sur tous les points de terminaison.
    *   Surveiller l'activité des logiciels de gestion à distance et détecter les installations non autorisées.
    *   Mettre en place des politiques de sécurité robustes pour empêcher la désactivation des protections antivirus.
    *   Valider les découvertes d'un incident en croisant les informations provenant de diverses sources de données pour une compréhension précise de l'attaque.

---
[Source](https://www.bleepingcomputer.com/news/security/piecing-together-the-puzzle-a-qilin-ransomware-investigation/){:target="_blank"}
