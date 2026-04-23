---
title: 'Trigona ransomware attacks use custom exfiltration tool to steal data'
date: 2026-04-23
permalink: /posts/2026/04/23/trigona-ransomware-attacks-use-custom-exfiltration-tool-to-steal-data/
tags:
- veille-cyber
- bleepingcomp
---
### L'évolution furtive du ransomware Trigona

Le groupe à l'origine du ransomware Trigona a repris ses activités opérationnelles en utilisant un outil d'exfiltration propriétaire, `uploader_client.exe`, conçu pour contourner les solutions de détection classiques (comme Rclone ou MegaSync). Ce malware permet un vol de données optimisé et discret grâce à des connexions parallèles et une rotation de trafic TCP.

**Points clés :**
* **Stratégie d'exfiltration :** L'outil permet de filtrer les types de fichiers (ciblant les documents critiques comme les PDF et factures) et limite les connexions pour éviter les alertes de volume de données.
* **Techniques d'évasion :** Les attaquants exploitent des vulnérabilités au niveau du noyau (BYOVD - *Bring Your Own Vulnerable Driver*) pour désactiver les logiciels de sécurité en utilisant des outils comme HRSword, PCHunter ou StpProcessMonitor.
* **Persistance et accès :** Utilisation d'AnyDesk pour le contrôle à distance, de PowerRun pour l'élévation de privilèges, et de Mimikatz pour le vol d'identifiants.

**Vulnérabilités :**
* L'article ne mentionne pas de CVE spécifique, mais souligne l'usage massif de **pilotes noyau vulnérables** (BYOVD) pour neutraliser les protections des terminaux.

**Recommandations :**
* **Surveillance des processus :** Surveiller l'exécution de pilotes suspects ou non signés et les activités de bas niveau liées à des outils comme `HRSword`, `PCHunter` ou `Gmer`.
* **Contrôle des accès :** Restreindre l'utilisation d'outils d'administration à distance (AnyDesk) et limiter les privilèges des utilisateurs pour empêcher l'exécution de `PowerRun`.
* **Analyse IoC :** Consulter les indicateurs de compromission (IoCs) fournis par Symantec pour identifier les communications réseau vers les serveurs codés en dur associés à `uploader_client.exe`.
* **Segmentation réseau :** Isoler les serveurs contenant des données critiques pour limiter l'impact d'une exfiltration automatisée.

---
[Source](https://www.bleepingcomputer.com/news/security/trigona-ransomware-attacks-use-custom-exfiltration-tool-to-steal-data/){:target="_blank"}
