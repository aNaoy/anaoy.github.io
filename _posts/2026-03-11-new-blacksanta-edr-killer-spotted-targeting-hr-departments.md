---
title: 'New ‘BlackSanta’ EDR killer spotted targeting HR departments'
date: 2026-03-11
permalink: /posts/2026/03/11/new-blacksanta-edr-killer-spotted-targeting-hr-departments/
tags:
- veille-cyber
- bleepingcomp
---
### Menace persistante : La campagne « BlackSanta » cible les départements RH

Des cybercriminels russophones mènent depuis plus d’un an une campagne sophistiquée ciblant les services des ressources humaines. Utilisant le spear-phishing pour diffuser des fichiers ISO dissimulés en CV, les attaquants déploient « BlackSanta », un outil capable de neutraliser les solutions EDR et antivirus au niveau du noyau (kernel).

**Points clés :**
*   **Vecteur d'attaque :** Fichiers ISO malveillants hébergés sur des services cloud, contenant des raccourcis .LNK, des scripts PowerShell et des fichiers dissimulés par stéganographie.
*   **Techniques d'évasion :** Utilisation du *DLL sideloading* (via SumatraPDF), détection d'environnements virtualisés (sandbox/VM) et *process hollowing* pour injecter des charges utiles dans des processus légitimes.
*   **Neutralisation de la sécurité :** BlackSanta modifie les exclusions Microsoft Defender, réduit la télémétrie Windows et utilise des pilotes vulnérables légitimes (BYOD - Bring Your Own Driver) pour forcer l'arrêt des processus de sécurité.
*   **Pilotes détournés :** Exploitation des pilotes *RogueKiller* (truesight.sys) et *IObitUnlocker.sys* pour obtenir des privilèges élevés et contourner les verrous système.

**Vulnérabilités exploitées :**
*   **BYOD (Bring Your Own Vulnerable Driver) :** Exploitation de pilotes signés mais vulnérables pour contourner les protections du noyau Windows. Aucune CVE unique n'est mentionnée, car la technique repose sur le détournement de fonctionnalités légitimes de pilotes tiers.

**Recommandations :**
*   **Contrôle des périphériques :** Restreindre le chargement de pilotes tiers non approuvés via le contrôle d'intégrité du code (HVCI/VBS).
*   **Gestion des emails :** Sensibiliser le personnel RH au risque des fichiers ISO reçus par email et bloquer systématiquement les extensions de fichiers suspectes au niveau de la passerelle mail.
*   **Surveillance système :** Surveiller les modifications suspectes apportées aux exclusions Microsoft Defender et aux valeurs de registre liées à la télémétrie.
*   **Durcissement :** Utiliser des solutions EDR configurées avec une protection renforcée contre la désactivation (tamper protection) et restreindre les droits d'exécution des scripts PowerShell pour les utilisateurs non administratifs.

---
[Source](https://www.bleepingcomputer.com/news/security/new-blacksanta-edr-killer-spotted-targeting-hr-departments/){:target="_blank"}
