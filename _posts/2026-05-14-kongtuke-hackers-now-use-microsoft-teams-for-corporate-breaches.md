---
title: 'KongTuke hackers now use Microsoft Teams for corporate breaches'
date: 2026-05-14
permalink: /posts/2026/05/14/kongtuke-hackers-now-use-microsoft-teams-for-corporate-breaches/
tags:
- veille-cyber
- bleepingcomp
---
### Infiltration de réseaux d'entreprise via Microsoft Teams : la menace KongTuke

Le groupe cybercriminel KongTuke a fait évoluer ses tactiques d'accès initial en exploitant Microsoft Teams pour mener des attaques d'ingénierie sociale. En se faisant passer pour le support informatique (via des techniques d'usurpation de noms par caractères Unicode), les attaquants convainquent les employés d'exécuter des commandes PowerShell malveillantes. Ce processus permet d'obtenir un accès persistant au réseau en moins de cinq minutes.

**Points clés :**
* **Vecteur d'attaque :** Messagerie instantanée Teams, utilisant des locataires Microsoft 365 légitimes pour contourner les blocages.
* **Payload :** Installation de *ModeloRAT*, un outil d'administration à distance basé sur Python, déployé via un environnement WinPython portable téléchargé depuis Dropbox.
* **Capacités du malware :** Collecte de données système, captures d'écran, exfiltration de fichiers et persistance multi-niveaux (clés de registre, raccourcis de démarrage, tâches planifiées).
* **Évolution de la menace :** La nouvelle version de ModeloRAT dispose d'une infrastructure C2 résiliente (cinq serveurs), de multiples canaux d'accès indépendants et d'une persistance robuste survivant aux routines de suppression standard.

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée ; l'attaque repose sur l'exploitation de la confiance humaine (ingénierie sociale) et l'exécution de scripts PowerShell autorisés par le système, détournés pour charger du code malveillant.

**Recommandations :**
* **Restriction des accès :** Restreindre la fédération Microsoft Teams en utilisant des listes d'autorisation (*allowlists*) pour empêcher les communications externes non sollicitées.
* **Sensibilisation :** Former les utilisateurs à la méfiance vis-à-vis des demandes inattendues du support technique demandant l'exécution de commandes.
* **Détection :** Surveiller les indicateurs de compromission (tâches planifiées suspectes, exécutions PowerShell inhabituelles et téléchargements depuis des services de stockage cloud publics) pour identifier les tentatives d'intrusion ou les traces de persistance.

---
[Source](https://www.bleepingcomputer.com/news/security/kongtuke-hackers-now-use-microsoft-teams-for-corporate-breaches/){:target="_blank"}
