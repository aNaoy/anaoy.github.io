---
title: 'Driver of destruction: How a legitimate driver is being used to take down AV processes'
date: 2025-08-06
permalink: /posts/2025/08/06/driver-of-destruction-how-a-legitimate-driver-is-being-used-to-take-down-av-processes/
tags:
- veille-cyber
- securelist
---
## Désactivation des Défenses Antivirus par Injection de Pilote

Une nouvelle menace informatique exploite un pilote système légitime, `ThrottleStop.sys`, pour désactiver les processus antivirus sur les systèmes compromis. Cette technique, connue sous le nom de BYOVD (Bring Your Own Vulnerable Driver), permet aux attaquants de neutraliser les défenses avant de déployer des charges utiles malveillantes, comme des ransomwares.

**Points Clés :**

*   **Méthode d'attaque initiale :** L'accès initial à un réseau a été obtenu via des identifiants RDP valides, suivi de l'extraction d'autres identifiants à l'aide de Mimikatz et de mouvements latéraux par la technique "pass-the-hash".
*   **Outils utilisés :** Le pirate a déployé un programme `All.exe` et le pilote `ThrottleStop.sys` (rebaptisé `ThrottleBlood.sys`).
*   **Fonctionnement du pilote :** Le pilote `ThrottleStop.sys`, développé par TechPowerUp et utilisé par l'application du même nom, est chargé en tant que service. Il crée un canal de communication utilisateur-noyau via un périphérique `.\.\ThrottleStop`.
*   **Vulnérabilité du pilote :** Le pilote expose deux fonctions IOCTL vulnérables qui permettent la lecture et l'écriture en mémoire physique à l'aide de la fonction `MmMapIoSpace`. Cette vulnérabilité, identifiée comme **CVE-2025-7771**, permet à tout utilisateur disposant de privilèges administratifs d'accéder à ces fonctions.
*   **Mécanisme d'action :** L'outil `All.exe` utilise ce pilote pour intercepter des fonctions noyau, notamment en injectant un shellcode qui redirige vers des fonctions comme `PsLookupProcessById` et `PsTerminateProcess` afin de terminer les processus antivirus identifiés. Il exploite également `NtQuerySystemInformation` pour obtenir des informations sur le noyau et `SuperFetch` pour traduire les adresses virtuelles en adresses physiques.
*   **Cibles :** Le malware contient une liste prédéfinie de processus antivirus à cibler, incluant ceux de solutions populaires comme Avast, AVG, Bitdefender, CrowdStrike, ESET, Kaspersky, McAfee, Microsoft Defender, Quick Heal, Symantec, Panda Security, SentinelOne, et Sophos.
*   **Impact :** Dans le cas étudié, cette attaque a précédé le déploiement du ransomware MedusaLocker.

**Vulnérabilités :**

*   **CVE-2025-7771 :** Vulnérabilité d'accès mémoire physique dans le pilote `ThrottleStop.sys` due à l'exposition de fonctions IOCTL permettant des lectures et écritures non sécurisées en mémoire.

**Recommandations :**

*   **Renforcement des politiques de sécurité :** Mettre en œuvre des pratiques de durcissement robustes, notamment la limitation de l'accès RDP aux adresses IP publiques et l'application de politiques de mots de passe forts.
*   **Défense en profondeur :** Utiliser plusieurs couches de sécurité. Cela inclut :
    *   L'autorisation de programmes (Application Whitelisting) et le principe du moindre privilège.
    *   La segmentation et l'isolement du réseau.
    *   L'authentification multifacteur (MFA) pour tous les accès distants.
    *   La gestion régulière des correctifs et l'analyse automatisée des vulnérabilités.
    *   Les systèmes de détection et de prévention d'intrusion (IDS/IPS).
    *   Les solutions de détection et de réponse sur les points d'extrémité (EDR).
    *   La journalisation, la surveillance et l'alerte complètes.
    *   Des évaluations de sécurité et des tests d'intrusion périodiques.
*   **Surveillance des pilotes :** Les solutions de sécurité devraient surveiller la présence de pilotes connus pour être vulnérables dans le système d'exploitation.
*   **Mécanismes d'auto-défense :** Les produits de protection antivirus doivent intégrer des mécanismes d'auto-défense pour empêcher la modification ou la terminaison de leurs processus, la suppression de leurs fichiers, et les modifications du registre système.

---
[Source](https://securelist.com/av-killer-exploiting-throttlestop-sys/117026/){:target="_blank"}
