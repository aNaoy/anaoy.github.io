---
title: 'Microsoft Store App Found Delivering Vinci RAT Capable of Remote System Control'
date: 2026-11-27
permalink: /posts/2026/11/27/microsoft-store-app-found-delivering-vinci-rat-capable-of-remote-system-control/
tags:
- veille-cyber
- hackernews
---
### Propagation de Vinci RAT via le Microsoft Store

Une campagne malveillante exploite le Microsoft Store pour distribuer « Vinci RAT », un cheval de Troie d'accès à distance (RAT). Les attaquants utilisent des sites de téléchargement contrefaits pour inciter les victimes à installer une application légitime en apparence, nommée « Setup Assistant », hébergée sur le magasin d'applications officiel.

**Points clés :**
*   **Vecteur d'attaque :** Redirection vers des sites frauduleux (ex: `codes-team.com`) imitant des logiciels populaires (Microsoft Teams, Roblox) pour télécharger un installeur signé.
*   **Mécanisme :** L'application "Setup Assistant" (développée en Electron) sert de porte dérobée. Elle surveille le dossier « Téléchargements » de la victime et exécute du code PowerShell ou JavaScript malveillant provenant d'un serveur de commande et contrôle (C2).
*   **Vinci RAT :** Une fois déployé, ce malware désactive l'interface d'analyse antimalware de Windows (AMSI), établit une persistance via des tâches planifiées, et permet un contrôle total de la machine (exécution de shellcode, vol de fichiers, reverse shell).
*   **Persistance :** Le malware utilise une tâche planifiée qui se réexécute toutes les 10 minutes pour maintenir l'accès.

**Vulnérabilités :**
*   Absence de CVE spécifique : L'attaque repose sur le détournement d'une application légitime (Shadow IT/Supply Chain) et le contournement de l'AMSI (Antimalware Scan Interface).
*   Failles de modération du Microsoft Store : L'application malveillante a été validée et hébergée par la plateforme malgré son comportement suspect.

**Recommandations :**
*   **Vigilance au téléchargement :** Ne télécharger des logiciels que depuis les sites officiels des éditeurs et éviter de cliquer sur des liens provenant de publicités ou de sites tiers non vérifiés.
*   **Surveillance système :** Détecter la création de tâches planifiées suspectes et surveiller les processus utilisant des scripts PowerShell ou JavaScript obfuscés.
*   **Contrôle des privilèges :** Restreindre l'exécution de scripts PowerShell non signés dans l'environnement d'entreprise.
*   **Analyse comportementale :** Utiliser des solutions EDR capables d'identifier les communications C2 anormales et les tentatives de désactivation de l'AMSI.

---
[Source](https://thehackernews.com/2026/11/microsoft-store-app-found-delivering.html){:target="_blank"}
