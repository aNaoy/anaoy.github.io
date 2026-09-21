---
title: 'TASK#STOMP PowerShell Backdoor Steals Documents, Wi-Fi Passwords, and Clipboard Data'
date: 2026-09-21
permalink: /posts/2026/09/21/taskstomp-powershell-backdoor-steals-documents-wi-fi-passwords-and-clipboard-data/
tags:
- veille-cyber
- hackernews
---
### TASK#STOMP : Une menace persistante basée sur PowerShell

La campagne **TASK#STOMP** déploie un backdoor sophistiqué utilisant des composants natifs de Windows pour infiltrer des systèmes, exfiltrer des données sensibles (documents, mots de passe Wi-Fi, presse-papiers, captures d'écran) et exécuter des commandes à distance.

**Points clés :**
* **Persistance multi-niveaux :** Utilisation de tâches planifiées aux noms trompeurs (*Local Credential Manager*, *Windows Display Manager*) et du dossier de démarrage pour assurer la résilience de l'infection.
* **Architecture robuste :** Le malware utilise deux modules PowerShell distincts avec une relation de « chien de garde » mutuelle : si l'un est arrêté, l'autre le relance.
* **Techniques d'évasion :** Emploi du *timestomping* (modification des horodatages), exécution masquée et utilisation d'outils légitimes (VBScript, PowerShell, WScript) pour se fondre dans l'activité système.
* **C2 redondant :** Communication avec des serveurs de commande et de contrôle authentifiés par jetons, rendant l'analyse et la neutralisation complexes.

**Vulnérabilités exploitées :**
Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'abus détourné de fonctionnalités système légitimes (« Living off the Land ») :
* **Windows Script Host (wscript.exe) :** Exécution de scripts VBS malveillants.
* **PowerShell :** Exécution de charges utiles encodées en mémoire.
* **Planificateur de tâches Windows :** Maintien de la persistance.

**Recommandations de sécurité :**
* **Surveillance des processus :** Auditer étroitement l'exécution de `wscript.exe` et `powershell.exe`, particulièrement lorsqu'ils lancent des scripts aux noms aléatoires ou suspects depuis des dossiers temporaires.
* **Contrôle du Planificateur de tâches :** Surveiller la création de nouvelles tâches planifiées, surtout celles utilisant des noms imitant des services système.
* **Filtrage réseau :** Bloquer les connexions sortantes vers des domaines suspects (ex: `corecloudfileshare[.]xyz`, `attachmentsharingdrive[.]xyz`).
* **Analyse comportementale :** Déployer des solutions EDR capables de détecter des comportements anormaux (ex: un processus tentant de modifier ses propres horodatages ou de surveiller le presse-papiers).
* **Durcissement :** Restreindre l'exécution de scripts PowerShell non signés et limiter les privilèges des utilisateurs pour empêcher l'installation de tâches planifiées persistantes.

---
[Source](https://thehackernews.com/2026/09/taskstomp-powershell-backdoor-steals.html){:target="_blank"}
