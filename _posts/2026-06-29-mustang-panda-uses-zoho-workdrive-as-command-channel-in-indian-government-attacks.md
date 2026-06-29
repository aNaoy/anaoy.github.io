---
title: 'Mustang Panda Uses Zoho WorkDrive as Command Channel in Indian Government Attacks'
date: 2026-06-29
permalink: /posts/2026/06/29/mustang-panda-uses-zoho-workdrive-as-command-channel-in-indian-government-attacks/
tags:
- veille-cyber
- hackernews
---
### Mustang Panda détourne Zoho WorkDrive pour espionner le gouvernement indien

Le groupe de cyberespionnage Mustang Panda mène actuellement des campagnes ciblées contre le secteur gouvernemental et énergétique indien, notamment les infrastructures hydroélectriques. Les attaquants utilisent des services cloud légitimes pour dissimuler leurs communications et exfiltrer des données sensibles liées à la diplomatie et à l'énergie.

**Points clés :**
* **Vecteur d'attaque :** Campagnes de spear-phishing utilisant des leurres thématiques (accords hydroélectriques, relations Inde-Taïwan).
* **Technique de dissimulation :** Utilisation de Zoho WorkDrive comme canal de commande et de contrôle (C2), permettant aux flux malveillants de se fondre dans le trafic cloud habituel.
* **Outils utilisés :**
    * **SHARDLOADER :** Chargeur exploitant le *DLL sideloading* via des binaires légitimes signés (Solid PDF Creator, Citrix Receiver).
    * **MINIRECON :** Backdoor évoluée communiquant via WebSockets sur HTTPS.
    * **ZOHOMURK :** Implant intégrant des identifiants OAuth Zoho codés en dur pour gérer les commandes et l'exfiltration via des dossiers de stockage partagés.
* **Cibles :** Hauts fonctionnaires et secteurs stratégiques indiens.

**Vulnérabilités :**
Aucune CVE spécifique n'est exploitée. L'attaque repose sur le détournement de fonctionnalités légitimes (abus de services cloud et techniques de *DLL sideloading*).

**Recommandations :**
* **Surveillance réseau :** Détecter les processus inhabituels (non-navigateurs) effectuant des appels aux API cloud ou des requêtes vers des domaines suspects tels que `couldinstallup[.]com`.
* **Analyse comportementale :** Surveiller le *DLL sideloading* initié par des applications signées et les tâches planifiées suspectes (ex: `SolidPDFPcl2Bmp`).
* **Durcissement :** Surveiller les clés de registre de persistance (ex: `RunOnece`) et limiter les accès sortants vers des services cloud tiers aux seuls processus légitimes autorisés.
* **Sensibilisation :** Renforcer la vigilance des employés face aux e-mails contenant des archives ZIP, particulièrement en période de tensions géopolitiques ou d'accords bilatéraux.

---
[Source](https://thehackernews.com/2026/06/mustang-panda-uses-zoho-workdrive-as.html){:target="_blank"}
