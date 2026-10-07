---
title: 'Ransomware has a new target. Is your backup ready?'
date: 2026-10-07
permalink: /posts/2026/10/07/ransomware-has-a-new-target-is-your-backup-ready/
tags:
- veille-cyber
- bleepingcomp
---
### La vulnérabilité des sauvegardes : nouvelle cible prioritaire des rançongiciels

Les groupes de cybercriminels (tels qu'ALPHV/BlackCat, BlackMatter et Gunra) font désormais de la destruction des sauvegardes une étape préalable au chiffrement des données. En neutralisant les points de restauration, ils suppriment toute alternative à la rançon, augmentant considérablement la pression sur les victimes.

**Points clés :**
* **Stratégie d'attaque :** Les attaquants ciblent en priorité l'infrastructure de sauvegarde pour empêcher toute récupération.
* **Facteurs aggravants :** Partage des mêmes réseaux et identifiants entre l'environnement de production et les sauvegardes, défaut de mise à jour des serveurs de secours, et manque de surveillance dédiée sur ces systèmes.
* **Impact financier :** Une perte de sauvegarde transforme une interruption gérable en une crise majeure, avec des coûts moyens dépassant les 5 millions de dollars par incident.

**Vulnérabilités identifiées :**
* **Absence d'authentification multifacteur (MFA) :** Accès facilité via des portails distants non sécurisés.
* **Surprivilèges et segmentation réseau :** L'utilisation de comptes administrateurs communs permet aux attaquants de localiser et supprimer l'intégralité des copies de secours sur un même segment réseau.
* **Obsolescence logicielle :** Les logiciels de sauvegarde sont souvent oubliés des cycles de correctifs de sécurité (ex: vulnérabilités non patchées exploitées pendant plus d'un an).

**Recommandations :**
* **Immuabilité des données :** Utiliser des stockages "write-once" (lecture seule) empêchant toute modification ou suppression, même par un administrateur compromis.
* **Isolation stricte :** Séparer physiquement ou logiquement les sauvegardes de l'environnement de production. Appliquer le contrôle d'accès basé sur les rôles (RBAC) et le MFA.
* **Cycle de patchs rigoureux :** Intégrer les serveurs et logiciels de sauvegarde dans les mêmes cycles de maintenance corrective que les systèmes de production.
* **Tests de restauration réguliers :** Valider l'intégrité des données via des exercices de simulation d'attaque pour identifier les failles avant qu'elles ne soient exploitées.

---
[Source](https://www.bleepingcomputer.com/news/security/ransomware-has-a-new-target-is-your-backup-ready/){:target="_blank"}
