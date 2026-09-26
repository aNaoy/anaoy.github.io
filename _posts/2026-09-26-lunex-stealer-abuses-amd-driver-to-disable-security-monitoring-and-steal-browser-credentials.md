---
title: 'Lunex Stealer Abuses AMD Driver to Disable Security Monitoring and Steal Browser Credentials'
date: 2026-09-26
permalink: /posts/2026/09/26/lunex-stealer-abuses-amd-driver-to-disable-security-monitoring-and-steal-browser-credentials/
tags:
- veille-cyber
- hackernews
---
### Menace Lunex : Une nouvelle plateforme de vol d'informations via BYOVD

La plateforme de malware-as-a-service (MaaS) **Lunex** (utilisant le malware *Psychedelic Stealer*) cible principalement des utilisateurs russophones et ukrainiens. Son architecture sophistiquée repose sur une chaîne d'attaque en quatre étapes, utilisant des techniques d'ingénierie sociale (ClickFix) pour inciter les victimes à télécharger des installateurs MSI piégés.

**Points clés :**
* **Persistence avancée :** Le malware installe un hôte de messagerie native (NMH) basé sur PowerShell dans le navigateur, permettant un accès persistant au système de fichiers, même après redémarrage.
* **Neutralisation des EDR :** Lunex utilise la technique **BYOVD** (*Bring Your Own Vulnerable Driver*) pour charger un pilote légitime mais vulnérable afin de désactiver silencieusement les solutions de sécurité (les rendant aveugles sans pour autant les arrêter).
* **Vol de données :** Cible les identifiants de sept navigateurs basés sur Chromium, les portefeuilles de cryptomonnaies (desktop et extensions) et manipule les préférences du navigateur pour injecter des extensions malveillantes.
* **Expansion mondiale :** Identifiée initialement en juin 2026, la plateforme a proliféré avec 28 panneaux de commande (C2) détectés dans 13 pays, incluant des capacités de phishing et d'usurpation de marque.

**Vulnérabilités exploitées :**
* **CVE-2023-20598 :** Exploitation du pilote noyau vulnérable `PDFWKRNL.sys` (logiciel AMD Radeon) pour obtenir une élévation de privilèges et désactiver les processus de sécurité. 

**Recommandations :**
* **Surveillance des pilotes :** Bien que les listes de blocage de pilotes vulnérables (Microsoft Vulnerable Driver Blocklist) soient utiles, cette attaque montre qu'elles ne sont pas exhaustives. Une surveillance comportementale stricte au niveau du noyau est nécessaire.
* **Gestion des privilèges :** Restreindre l'installation de logiciels non signés ou suspects par les utilisateurs finaux pour empêcher l'exécution de loaders.
* **Protection des navigateurs :** Auditer régulièrement les extensions installées et les configurations des "Native Messaging Hosts" (NMH) au sein des navigateurs.
* **Sensibilisation :** Former les utilisateurs à la méfiance face aux pages de type "ClickFix" ou aux captchas suspects sur des sites web, même légitimes.

---
[Source](https://thehackernews.com/2026/09/lunex-stealer-abuses-amd-driver-to.html){:target="_blank"}
