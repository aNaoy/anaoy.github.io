---
title: 'Malicious Script That Gets Rid of ADS, (Wed, Apr 1st)'
date: 2026-04-02
permalink: /posts/2026/04/02/malicious-script-that-gets-rid-of-ads-wed-apr-1st/
tags:
- veille-cyber
- sans-isc
---
### Évasion par suppression des flux de données alternatifs (ADS)

Certains logiciels malveillants exploitent une technique de persistance via le registre Windows (`Run`) tout en dissimulant leurs traces. Une fois le script malveillant copié vers un répertoire local, il exécute une commande PowerShell ciblant le flux de données alternatif (ADS) nommé `:Zone.Identifier`.

**Points clés :**
* **Technique d'évasion :** Le malware supprime délibérément le flux `:Zone.Identifier` (appelé "Mark-of-the-Web" ou MotW) attaché au fichier.
* **Objectif :** Ce flux indique l'origine d'un fichier (ex: Internet). En le supprimant, le fichier semble provenir d'une source locale et légitime, rendant le malware moins suspect lors des analyses forensiques.
* **Persistance :** Le script utilise les clés de registre `Run` pour assurer son exécution au démarrage du système.
* **Charge utile :** Le script sert de vecteur pour déployer ultérieurement un *DonutLoader* sur la machine compromise.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, il s'agit d'une technique d'évasion utilisant des fonctionnalités natives de Windows (NTFS ADS et PowerShell) pour contourner les mécanismes de sécurité basés sur le marquage des fichiers téléchargés.

**Recommandations :**
* **Surveillance des journaux :** Auditer les exécutions PowerShell suspectes, notamment celles utilisant les paramètres `-w h` (hidden) et les commandes visant `Remove-Item` sur des fichiers suivis de `:Zone.Identifier`.
* **Analyse Forensique :** Lors d'investigations, vérifier systématiquement la présence et l'intégrité du flux `:Zone.Identifier` sur les exécutables et scripts suspects.
* **Sécurité des points de terminaison (EDR/AV) :** Configurer les outils de sécurité pour détecter les modifications non autorisées dans les clés de registre de démarrage (`HKCU\Software\Microsoft\Windows\CurrentVersion\Run`).
* **Politique d'exécution :** Restreindre l'utilisation de PowerShell dans les environnements où cela n'est pas strictement nécessaire, notamment pour les utilisateurs standards.

---
[Source](https://isc.sans.edu/diary/rss/32854){:target="_blank"}
