---
title: 'Malicious Script That Gets Rid of ADS, (Wed, Apr 1st)'
date: 2026-04-01
permalink: /posts/2026/04/01/malicious-script-that-gets-rid-of-ads-wed-apr-1st/
tags:
- veille-cyber
- sans-isc
---
### Dissimulation de malware par suppression des flux de données alternatifs (ADS)

Certains malwares assurent leur persistance en copiant des scripts malveillants dans des répertoires système (ex: `%APPDATA%`) pour une exécution au démarrage via les clés `Run` du registre. Pour éviter d'être détectés lors d'investigations numériques, ces scripts utilisent une commande PowerShell visant à supprimer le flux de données alternatif (ADS) nommé `:Zone.Identifier`.

**Points clés :**
* **Persistance :** Les attaquants copient des scripts malveillants vers des répertoires locaux et enregistrent leur exécution automatique dans le registre Windows.
* **Technique de camouflage :** Le flux `:Zone.Identifier` (appelé "Mark-of-the-Web") est conservé lors de la copie d'un fichier. Ce flux indique l'origine du fichier (Internet, zone de confiance, etc.).
* **Objectif :** En supprimant cet ADS, l'attaquant fait apparaître le fichier comme s'il avait été créé localement sur la machine, évitant ainsi de lever des alertes lors de recherches de fichiers téléchargés potentiellement malveillants.
* **Charge utile :** Le script analysé finit par déployer un *DonutLoader* pour poursuivre l'infection.

**Vulnérabilités :**
* Il ne s'agit pas d'une vulnérabilité logicielle (CVE) au sens strict, mais d'une exploitation des fonctionnalités natives de Windows (NTFS ADS et persistance par registre) pour masquer des activités malveillantes.

**Recommandations :**
* **Surveillance du registre :** Surveiller étroitement les clés de démarrage (`HKCU\Software\Microsoft\Windows\CurrentVersion\Run`) pour détecter toute exécution inhabituelle.
* **Analyse DFIR :** Lors des investigations, ne pas se fier uniquement à l'absence de `:Zone.Identifier`. Rechercher des incohérences dans les dates de création de fichiers dans les répertoires sensibles (`%APPDATA%`, `%TEMP%`).
* **EDR/Logging :** Configurer des alertes sur l'utilisation de commandes PowerShell tentant d'accéder aux flux de données alternatifs (`Remove-Item` avec le suffixe `:Zone.Identifier`).

---
[Source](https://isc.sans.edu/diary/rss/32854){:target="_blank"}
