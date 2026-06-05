---
title: 'The Evil MSI Background is Back&#x21;, (Fri, Jun 5th)'
date: 2026-06-05
permalink: /posts/2026/06/05/the-evil-msi-background-is-backx21-fri-jun-5th/
tags:
- veille-cyber
- sans-isc
---
### Résurgence de la technique du "MSI Background" : Analyse d'une nouvelle campagne de malwares

Une nouvelle campagne de phishing utilise des fichiers JavaScript malveillants (`.js`) distribués via des liens WeTransfer légitimes. Cette attaque repose sur une chaîne d'infection multi-étapes exploitant des services cloud légitimes pour héberger ses charges utiles.

**Points clés :**
*   **Vecteur initial :** Email de phishing contenant un lien WeTransfer pointant vers un fichier `.js` truffé de code inutile pour dissimuler la logique malveillante.
*   **Obfuscation :** Utilisation de ROT13 et de substitutions de caractères (remplacement de 'A' par '#' dans le Base64) pour contourner les outils de détection statique.
*   **Exécution :** Le script PowerShell est exécuté via WMI (`winmgmts`) avec des attributs masqués (`WindowStyle Hidden`).
*   **Infrastructure :** Utilisation intensive de services légitimes (Cloudflare Workers et Cloudflare R2) pour l'hébergement des composants malveillants, facilitant ainsi leur passage à travers les filtres de réputation.
*   **Charge utile :** Le script télécharge une image JPEG (technique de stéganographie) contenant une bibliothèque .NET modifiée (`Microsoft.Win32.TaskScheduler`) destinée à persister sur le système.

**Vulnérabilités :**
*   Bien qu'aucune CVE spécifique ne soit citée, l'attaque repose sur l'abus de fonctionnalités système légitimes (Living-off-the-Land) :
    *   **WMI (Windows Management Instrumentation) :** Utilisé pour l'exécution silencieuse de processus.
    *   **PowerShell :** Utilisation du `ExecutionPolicy Bypass` pour outrepasser les restrictions de sécurité.

**Recommandations :**
*   **Blocage des extensions :** Restreindre l'exécution automatique ou l'ouverture de fichiers `.js` via Windows Script Host.
*   **Filtrage réseau :** Surveiller et bloquer les requêtes sortantes vers des sous-domaines génériques de type `*.workers.dev` ou `*.r2.dev` s'ils ne sont pas nécessaires à l'activité métier.
*   **Politique d'exécution :** Appliquer une stratégie de groupe (GPO) imposant une politique d'exécution PowerShell restrictive (ex: `AllSigned` ou `RemoteSigned`) au lieu de permettre le `Bypass`.
*   **Sensibilisation :** Alerter les utilisateurs sur la méfiance vis-à-vis des liens de transfert de fichiers, même lorsqu'ils proviennent de services réputés comme WeTransfer.

---
[Source](https://isc.sans.edu/diary/rss/33054){:target="_blank"}
