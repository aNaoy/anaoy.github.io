---
title: 'Antino Backdoor Uses Outlook and OneDrive for C2 in China-Nexus Espionage Campaign'
date: 2026-10-02
permalink: /posts/2026/10/02/antino-backdoor-uses-outlook-and-onedrive-for-c2-in-china-nexus-espionage-campaign/
tags:
- veille-cyber
- hackernews
---
### Campagne d'espionnage "Antino" : Utilisation détournée de Microsoft 365

Le groupe de menace "UAT-11587", lié à des intérêts chinois, déploie le logiciel malveillant **Antino**, une porte dérobée (backdoor) écrite en Rust, pour cibler des organisations gouvernementales et des think tanks en Asie (Taïwan, Inde, Philippines, etc.). Cette campagne se distingue par l'utilisation exclusive des services **Microsoft 365 (Outlook et OneDrive)** comme infrastructure de commande et de contrôle (C2), dissimulant ainsi ses activités derrière un trafic légitime.

**Points clés :**
*   **Vecteur d'attaque :** Hameçonnage ciblé (spear-phishing) hautement personnalisé utilisant des leurres imitant l'interface de prévisualisation des pièces jointes de Gmail.
*   **Technique d'exécution :** Utilisation de fichiers HTA/WSF, suivie d'une désérialisation .NET et du chargement latéral de DLL (*DLL side-loading*) via un exécutable Microsoft légitime (`GatherOsState.exe`).
*   **C2 furtif :** Antino interagit avec l'API Microsoft Graph. Il récupère des commandes dans les courriels Outlook (`command_req_[session_id]`) et utilise OneDrive pour l'exfiltration de fichiers et les pulsations (heartbeats).
*   **Fonctionnalités :** Reconnaissance système, exécution de scripts PowerShell, chargement de shellcode en mémoire, transfert de fichiers et persistance.

**Vulnérabilités exploitées :**
*   L'article mentionne l'exploitation d'une vulnérabilité non corrigée dans les raccourcis Windows (utilisée par le downloader associé), bien que le code CVE spécifique ne soit pas cité.
*   Détournement du *Windows Scripted Diagnostics Framework* pour exécuter du PowerShell malveillant via des composants système.

**Recommandations :**
*   **Surveillance des logs :** Auditer les logs Microsoft 365 pour détecter des activités anormales via l'API Graph (accès inhabituels aux boîtes mail ou à OneDrive).
*   **Filtrage E-mail :** Renforcer les politiques SPF, DKIM et DMARC pour contrer l'usurpation d'identité et sensibiliser les utilisateurs aux leurres de prévisualisation d'e-mails.
*   **Détection comportementale :** Surveiller l'utilisation de `GatherOsState.exe` dans des chemins inhabituels ou son exécution associée à des fichiers `.dll` locaux, signe de *DLL side-loading*.
*   **Endpoint Security :** Bloquer ou limiter l'exécution de fichiers HTA et WSF non autorisés via les politiques de contrôle d'application (AppLocker ou Windows Defender Application Control).

---
[Source](https://thehackernews.com/2026/10/antino-backdoor-uses-outlook-and.html){:target="_blank"}
