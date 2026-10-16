---
title: 'Attackers Tampered with AOMEI Backuppers Update Servers for Minutes to Deliver a Backdoor'
date: 2026-10-16
permalink: /posts/2026/10/16/attackers-tampered-with-aomei-backuppers-update-servers-for-minutes-to-deliver-a-backdoor/
tags:
- veille-cyber
- hackernews
---
### Compromission éphémère de la chaîne d'approvisionnement AOMEI Backupper

Entre mai et juillet 2026, des attaquants ont infiltré les serveurs de mise à jour d'AOMEI Backupper pour diffuser une porte dérobée. En modifiant brièvement des fichiers de configuration sur le serveur, les attaquants ont forcé le logiciel à télécharger et exécuter des charges malveillantes sur les machines des utilisateurs lors de fenêtres de tir très courtes (5 à 10 minutes).

**Points clés :**
* **Attaque opportuniste :** Les victimes ont été touchées uniquement si leur logiciel vérifiait les mises à jour exactement au moment de la manipulation des fichiers serveurs.
* **Absence de vulnérabilité logicielle :** Aucune faille n'a été exploitée dans AOMEI ; le mécanisme de mise à jour lui-même était intrinsèquement non sécurisé (absence de vérification cryptographique des fichiers).
* **Persistance :** Une fois infecté, le logiciel installe une tâche planifiée exécutant un outil d'administration légitime (Radmin) détourné pour charger une porte dérobée (SHINYROAD) ou le framework Adaptix C2.
* **Technique WebDAV :** Une méthode a été utilisée pour dérober des jetons d'authentification NetNTLMv2 via un pop-up invisible, sans exécution de code supplémentaire.

**Vulnérabilités :**
* Aucune CVE n'est associée, car il s'agit d'un défaut de conception : les fichiers de configuration (`down_html.ini` et `Notifycfg.ini`) n'étant pas signés numériquement, le serveur a pu être utilisé pour distribuer du code malveillant en toute impunité.

**Recommandations :**
* **Ne pas se fier à l'état actuel des serveurs :** La correction côté serveur par AOMEI ne nettoie pas les machines déjà infectées.
* **Chasse aux menaces (Threat Hunting) :**
    * Rechercher des tâches planifiées suspectes nommées `RadminComponentRuntime` ou `NitroRuntime`.
    * Inspecter les dossiers locaux de l'application à la recherche de fichiers exécutables non signés.
* **Mesures réseau :** 
    * Bloquer les domaines malveillants identifiés : `storage-data[.]com`, `promotion.storage-data[.]com`, `aomei.storage-data[.]com`.
    * Bloquer les connexions SMB sortantes (TCP 445) et WebDAV vers des adresses IP externes inconnues pour prévenir le vol d'identifiants.
* **Analyse :** Utiliser les règles YARA (Mandiant) et Sigma (ManageEngine) publiées par les chercheurs pour identifier des traces d'infection antérieures sur les endpoints.

---
[Source](https://thehackernews.com/2026/10/attackers-tampered-with-aomei.html){:target="_blank"}
