---
title: 'Microsoft rolls out native Sysmon monitoring in Windows 11'
date: 2026-02-05
permalink: /posts/2026/02/05/microsoft-rolls-out-native-sysmon-monitoring-in-windows-11/
tags:
- veille-cyber
- bleepingcomp
---
**Intégration Native de Sysmon dans Windows 11**

Microsoft déploie progressivement la fonctionnalité Sysmon (System Monitor) directement dans Windows 11, initialement auprès des utilisateurs inscrits au programme Windows Insider. Sysmon est un outil gratuit qui surveille et enregistre les activités suspectes ou malveillantes sur le système dans le journal d'événements Windows. Il peut suivre des événements tels que la création et la terminaison de processus, la création de fichiers exécutables, les tentatives de modification de processus, les changements dans le presse-papiers Windows et même la sauvegarde automatique des fichiers supprimés.

Jusqu'à présent, Sysmon nécessitait une installation manuelle sur chaque appareil, ce qui compliquait son déploiement à grande échelle. L'intégration native simplifiera donc la gestion et le déploiement dans les environnements informatiques importants.

Bien que désormais nativement intégré, Sysmon est désactivé par défaut. Les utilisateurs doivent l'activer explicitement via les "Fonctionnalités facultatives" dans les Paramètres de Windows 11 ou via des commandes PowerShell/Invite de commandes (après avoir désinstallé toute version antérieure de Sysmon installée manuellement). Cette nouvelle fonctionnalité est en cours de déploiement pour les canaux Beta et Dev du programme Insider avec des versions spécifiques de Windows 11 Preview.

**Points Clés :**

*   Microsoft intègre Sysmon nativement dans Windows 11.
*   Sysmon surveille et enregistre les activités système pour la détection de menaces.
*   L'intégration native facilite le déploiement et la gestion en entreprise.
*   Sysmon est désactivé par défaut et nécessite une activation manuelle.
*   Le déploiement est actuellement limité aux participants du programme Windows Insider.

**Vulnérabilités :**

Aucune vulnérabilité spécifique (avec CVE) n'est mentionnée dans l'article concernant cette intégration. Sysmon est lui-même un outil de sécurité destiné à identifier les activités potentiellement malveillantes.

**Recommandations :**

*   Pour les utilisateurs du programme Windows Insider, envisagez d'activer la fonctionnalité Sysmon pour bénéficier d'une surveillance système renforcée.
*   Assurez-vous de désinstaller toute version précédente de Sysmon installée manuellement avant d'activer la version intégrée.
*   Les administrateurs informatiques devraient planifier l'adoption de cette fonctionnalité native pour améliorer la sécurité des systèmes Windows 11 dans leurs environnements.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-rolls-out-native-windows-11-sysmon-security-monitoring/){:target="_blank"}
