---
title: 'StrikeShark: investigating a new campaign delivering Cobalt Strike through SharkLoader'
date: 2026-06-24
permalink: /posts/2026/06/24/strikeshark-investigating-a-new-campaign-delivering-cobalt-strike-through-sharkloader/
tags:
- veille-cyber
- securelist
---
### Analyse de la campagne StrikeShark : Déploiement de Cobalt Strike via SharkLoader

La campagne « StrikeShark » utilise une nouvelle famille de malwares appelée **SharkLoader** pour déployer des instances de Cobalt Strike Beacon sur des systèmes compromis. Cette activité, observée mondialement (Indonésie, Taïwan, Liban, etc.), cible des organisations gouvernementales, diplomatiques et des entreprises de développement logiciel.

#### Points clés
*   **Vecteurs d'infection :** Exploitation de vulnérabilités connues dans des applications exposées sur Internet et utilisation de droppers malveillants se faisant passer pour des logiciels légitimes (Google Update, Cisco AnyConnect).
*   **Mécanismes avancés :** SharkLoader utilise une technique de « Perfect DLL Hijacking » pour contourner le verrou du chargeur Windows (*loader lock*) et installe de nombreux hooks d'API via *Microsoft Detours* pour masquer ses activités, intercepter des données et échapper à la détection (notamment en désactivant les logs ETW).
*   **Persistance :** Mise en place via des tâches planifiées Windows ou des clés de registre « Run ».
*   **Post-exploitation :** Utilisation d'outils open-source (FScan, Searchall, Pillager) pour la reconnaissance, l'énumération Active Directory et le vol de credentials (LSASS, NTDS).
*   **Attribution :** Bien que des outils développés par des individus sinophones soient utilisés, aucune preuve formelle ne permet d'attribuer cette campagne à un groupe APT spécifique.

#### Vulnérabilités exploitées (CVE)
Le groupe exploite principalement des preuves de concept (PoC) publiques pour les vulnérabilités suivantes :
*   **RCE :** CVE-2021-26855 (ProxyLogon), CVE-2023-32315, CVE-2024-36401, CVE-2016-4437 (Apache Shiro), CVE-2021-36260 (Hikvision), CVE-2021-27076, CVE-2022-27925 (Zimbra), CVE-2022-41082, CVE-2023-46747 (F5), CVE-2024-21762 (Fortinet), CVE-2025-55182.
*   **Contournement d'authentification :** CVE-2022-40684 (Fortinet), CVE-2023-20198 (Cisco IOS XE).

#### Recommandations
*   **Gestion des correctifs :** Appliquer en priorité les correctifs pour les vulnérabilités critiques mentionnées, particulièrement sur les applications exposées sur Internet (Exchange, SharePoint, Openfire, FortiOS, etc.).
*   **Surveillance :** Surveiller la création de tâches planifiées suspectes et l'exécution de binaires système (ex: `SystemSettings.exe`) depuis des répertoires inhabituels (`%APPDATA%`).
*   **Analyse mémoire et comportementale :** Détecter les hooks d'API suspects et les injections de code en mémoire, techniques caractéristiques de l'exécution de Cobalt Strike via SharkLoader.
*   **Renforcement Active Directory :** Auditer les accès privilégiés et surveiller l'utilisation d'outils de reconnaissance réseau suspects dans l'environnement.

---
[Source](https://securelist.com/strikeshark-campaign/120326/){:target="_blank"}
