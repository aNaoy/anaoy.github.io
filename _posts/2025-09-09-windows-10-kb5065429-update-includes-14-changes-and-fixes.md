---
title: 'Windows 10 KB5065429 update includes 14 changes and fixes'
date: 2025-09-09
permalink: /posts/2025/09/09/windows-10-kb5065429-update-includes-14-changes-and-fixes/
tags:
- veille-cyber
- bleepingcomp
---
### Mise à Jour de Sécurité Windows 10 : Correctifs Essentiels

La mise à jour cumulative KB5065429 pour Windows 10 (versions 22H2 et 21H2) a été publiée, apportant quatorze modifications et correctifs. Elle intègre les mises à jour de sécurité de septembre 2025 de Microsoft, corrigeant notamment deux vulnérabilités zero-day exploitées publiquement et 81 autres failles.

**Points Clés :**

*   La mise à jour est obligatoire et contient des correctifs de sécurité essentiels.
*   Elle vise à résoudre des problèmes de performance dans le logiciel de streaming NDI et des invites UAC inattendues.
*   Elle inclut de nouvelles fonctionnalités et améliorations relatives à la compatibilité SMB, aux mises à jour de sécurité étendues (ESU) et à la sauvegarde pour les entreprises.

**Vulnérabilités et Correctifs Mentionnés :**

*   **CVE-2025-55234 | Windows SMB Elevation of Privilege Vulnerability** : Ce correctif permet d'activer l'audit de la compatibilité des clients SMB pour la signature du serveur SMB et l'EPA du serveur SMB. Cela permet aux clients d'évaluer leur environnement et d'identifier les problèmes potentiels de compatibilité avant de déployer des mesures de renforcement.
*   **Problèmes d'invites UAC inattendues** : Les utilisateurs non administrateurs recevaient des invites UAC non sollicitées lors d'actions personnalisées d'installateurs MSI, empêchant l'installation ou la réparation de certaines applications (ex: Office Professional Plus 2010, logiciels Autodesk). Ce correctif réduit la nécessité de ces invites et permet aux administrateurs de les désactiver pour des applications spécifiques via une liste blanche.

**Recommandations :**

*   Installer la mise à jour KB5065429 dès que possible pour bénéficier des correctifs de sécurité et des améliorations de stabilité.
*   Il est possible de programmer le redémarrage nécessaire à l'installation pour minimiser les interruptions.
*   La mise à jour peut être téléchargée et installée manuellement depuis le catalogue Microsoft Update.

Il n'y a pas de problèmes connus associés à cette mise à jour.

---
[Source](https://www.bleepingcomputer.com/news/security/windows-10-kb5065429-update-includes-14-changes-and-fixes/){:target="_blank"}
