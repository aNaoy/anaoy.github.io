---
title: 'Microsoft fixes bug behind Windows Server 2025 automatic upgrades'
date: 2026-04-15
permalink: /posts/2026/04/15/microsoft-fixes-bug-behind-windows-server-2025-automatic-upgrades/
tags:
- veille-cyber
- bleepingcomp
---
# Résolution du problème de mise à niveau automatique vers Windows Server 2025

Microsoft a officiellement corrigé un dysfonctionnement majeur ayant provoqué des mises à niveau inattendues et non sollicitées de serveurs tournant sous Windows Server 2019 et 2022 vers Windows Server 2025. Identifié initialement en septembre 2024, ce problème avait suscité une vive inquiétude chez les administrateurs système, car il forçait le passage à une version du système d'exploitation pour laquelle les organisations ne disposaient parfois pas de licences.

### Points clés
* **Origine du problème :** Initialement attribué par Microsoft à une mauvaise configuration d'outils de gestion tiers, le problème a été contesté par ces derniers, qui ont pointé une erreur de classification et de gestion des mises à jour côté Microsoft.
* **Impact :** Des serveurs de production ont été mis à niveau automatiquement sans intervention humaine, entraînant des risques de conformité logicielle et de stabilité opérationnelle.
* **État actuel :** Le correctif a été déployé et Microsoft a réactivé l'offre de mise à niveau via le panneau de configuration Windows Update.

### Vulnérabilités
* Aucune CVE n'est associée à cet incident spécifique. Il s'agissait d'un défaut de processus et de logique de déploiement logiciel plutôt que d'une faille de sécurité exploitée.

### Recommandations
* **Vérification des serveurs :** Les administrateurs système doivent s'assurer que leurs serveurs n'ont pas subi de mise à niveau non désirée durant la période de latence du correctif.
* **Gestion des mises à jour :** Il est conseillé de consulter la documentation officielle sur les [mises à niveau sur place (in-place upgrades)](https://learn.microsoft.com/en-us/windows-server/get-started/upgrade-in-place?tabs=windows-update) pour valider les procédures de déploiement.
* **Surveillance du centre de santé :** Continuer de surveiller le [tableau de bord de santé des versions Windows](https://learn.microsoft.com/en-us/windows/release-health/status-windows-server-2025) pour toute nouvelle alerte concernant le cycle de vie de Windows Server.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-bug-behind-windows-server-2025-automatic-upgrades/){:target="_blank"}
