---
title: 'INC ransomware opsec fail allowed data recovery for 12 US orgs'
date: 2026-01-22
permalink: /posts/2026/01/22/inc-ransomware-opsec-fail-allowed-data-recovery-for-12-us-orgs/
tags:
- veille-cyber
- bleepingcomp
---
**Faille de Sécurité INC Ransomware Permet la Récupération de Données**

Une erreur opérationnelle de la part du groupe INC Ransom a involontairement permis la récupération de données dérobées à douze organisations américaines. L'analyse forensique a révélé une infrastructure de stockage mal sécurisée utilisée par les attaquants.

Les chercheurs de Cyber Centaurs ont découvert que le groupe utilisait l'outil de sauvegarde Restic de manière non conventionnelle. Des scripts PowerShell, exécutant Restic et contenant des clés d'accès ainsi que des configurations de dépôts, ont été retrouvés. L'hypothèse est que ces dépôts ont été conservés après les attaques, servant de stockage persistant pour les données exfiltrées.

Après avoir validé cette théorie par une procédure d'énumération non destructive, l'équipe a confirmé la présence de données chiffrées provenant de douze victimes distinctes, issues des secteurs de la santé, de la fabrication, de la technologie et des services. Ces données ont été déchiffrées et conservées, et les autorités compétentes ont été contactées.

INC Ransom est une opération de ransomware-as-a-service (RaaS) active depuis mi-2023, connue pour avoir ciblé des entités comme Yamaha Motor, Xerox Business Solution et le système de santé écossais NHS.

**Points Clés :**

*   Une défaillance de sécurité opérationnelle d'INC Ransom a mené à la découverte de leur infrastructure de stockage de données volées.
*   L'outil de sauvegarde Restic a été utilisé par les attaquants pour exfiltrer et stocker des données de manière persistante.
*   Douze organisations américaines ont vu leurs données dérobées récupérées grâce à cette faille.
*   INC Ransom est un acteur de RaaS ayant visé plusieurs organisations notables.

**Vulnérabilités :**

*   Absence de nettoyage des infrastructures de stockage après les opérations de rançongiciel.
*   Stockage d'identifiants et de configurations sensibles en clair dans des scripts d'exécution.

**Recommandations :**

*   Mettre en place des règles YARA et Sigma pour détecter l'utilisation suspecte de l'outil Restic ou de ses binaires renommés, ainsi que leur exécution depuis des emplacements inhabituels.
*   Effectuer des analyses forensiques approfondies lors d'incidents pour identifier des artefacts potentiels révélant l'infrastructure des attaquants.
*   Surveiller et sécuriser activement les dépôts de sauvegarde et les accès aux outils d'exfiltration.

---
[Source](https://www.bleepingcomputer.com/news/security/inc-ransomware-opsec-fail-allowed-data-recovery-for-12-us-orgs/){:target="_blank"}
