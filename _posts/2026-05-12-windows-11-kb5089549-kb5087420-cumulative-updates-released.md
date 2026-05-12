---
title: 'Windows 11 KB5089549 & KB5087420 cumulative updates released'
date: 2026-05-12
permalink: /posts/2026/05/12/windows-11-kb5089549-kb5087420-cumulative-updates-released/
tags:
- veille-cyber
- bleepingcomp
---
### Mise à jour cumulative Windows 11 : Correctifs de sécurité et optimisations système

Microsoft a déployé les mises à jour cumulatives obligatoires **KB5089549** (versions 25H2/24H2) et **KB5087420** (version 23H2) dans le cadre du "Patch Tuesday" de mai 2026. Ces mises à jour corrigent 120 vulnérabilités de sécurité identifiées au cours des mois précédents.

**Points clés :**
* **Sécurité des scripts :** Introduction d'un mode de traitement sécurisé pour les fichiers batch et les scripts CMD afin d'empêcher toute modification durant leur exécution.
* **Fonctionnalités :** Ajout d'un mode "Xbox" pour le bureau, expansion des formats d'archives supportés dans l'Explorateur de fichiers (uu, cpio, xar, nupkg) et intégration de retours haptiques pour certains périphériques d'entrée.
* **Améliorations système :** Optimisation de la fiabilité de la barre des tâches, de Windows Hello (reconnaissance faciale et empreinte digitale) et de la gestion de la mémoire pour l'optimisation de la distribution.
* **Stockage :** La limite de formatage des volumes FAT32 via la ligne de commande est étendue de 32 Go à 2 To.

**Vulnérabilités :**
L'article ne détaille pas les identifiants CVE spécifiques, mais confirme la correction de **120 failles de sécurité** découvertes récemment. Aucun "zero-day" n'a été exploité pour cette vague de correctifs.

**Recommandations :**
* **Installation :** Les utilisateurs sont invités à installer ces mises à jour obligatoires via **Paramètres > Windows Update > Rechercher des mises à jour**, ou manuellement via le Catalogue Microsoft Update.
* **Durcissement des scripts :** Pour activer la protection contre la modification des fichiers batch, les administrateurs peuvent configurer la clé de registre suivante :
    * `HKEY_LOCAL_MACHINE\Software\Microsoft\Command Processor`
    * Nom de la valeur : `LockBatchFilesWhenInUse`
    * Donnée : `1` (activé).

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-kb5089549-and-kb5087420-cumulative-updates-released/){:target="_blank"}
