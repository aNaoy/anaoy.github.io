---
title: 'New ‘BlackSanta’ EDR killer spotted targeting HR departments'
date: 2026-03-11
permalink: /posts/2026/03/11/new-blacksanta-edr-killer-spotted-targeting-hr-departments/
tags:
- veille-cyber
- bleepingcomp
---
### Menace persistante : La campagne « BlackSanta » cible les départements RH

Des cybercriminels russophones mènent depuis plus d’un an une campagne sophistiquée visant les départements des ressources humaines. Utilisant le hameçonnage ciblé (*spear-phishing*), les attaquants incitent les victimes à télécharger des fichiers ISO contenant de faux CV. Une fois exécutée, la chaîne d'infection déploie « BlackSanta », un outil redoutable conçu pour désactiver les solutions de sécurité avant l'installation de charges utiles malveillantes.

**Points clés :**
*   **Vecteur d'attaque :** Fichiers ISO malveillants hébergés sur des services cloud (Dropbox) dissimulés en documents PDF.
*   **Techniques d'évasion :** Utilisation de stéganographie pour extraire du code dans la mémoire système, *DLL sideloading* (via SumatraPDF) et détection d'environnements sandbox/VM pour stopper l'exécution si une analyse est suspectée.
*   **Capacités de BlackSanta :** Modification des exclusions Windows Defender, réduction de la télémétrie Microsoft, et surtout, neutralisation des outils de sécurité (EDR, antivirus, SIEM) au niveau du noyau.
*   **BYOVD (Bring Your Own Vulnerable Driver) :** Exploitation des pilotes légitimes *RogueKiller (truesight.sys)* et *IObitUnlocker.sys* pour obtenir des privilèges élevés et supprimer les verrous sur les processus de sécurité.

**Vulnérabilités exploitées :**
*   L'attaque repose sur l'exploitation de **pilotes légitimes vulnérables** (BYOVD) pour détourner les protections du noyau Windows. Aucun CVE spécifique n'est mentionné pour les pilotes eux-mêmes, mais l'usage détourné de ces outils permet de contourner les mécanismes de défense standards.

**Recommandations :**
*   **Sensibilisation :** Former le personnel RH à la vigilance face aux fichiers ISO ou aux liens de téléchargement inattendus, même s'ils semblent provenir de sources professionnelles.
*   **Filtrage des accès :** Bloquer ou restreindre l'exécution de fichiers ISO et le montage automatique de disques amovibles/images via les politiques de groupe (GPO).
*   **Contrôle des applications et pilotes :** Implémenter le contrôle des applications (AppLocker ou WDAC) pour empêcher l'exécution de binaires non approuvés et restreindre l'installation ou le chargement de pilotes tiers non signés ou connus pour être vulnérables.
*   **Surveillance :** Surveiller les modifications suspectes apportées aux exclusions de Windows Defender et aux valeurs de registre liées à la télémétrie.

---
[Source](https://www.bleepingcomputer.com/news/security/new-blacksanta-edr-killer-spotted-targeting-hr-departments/){:target="_blank"}
