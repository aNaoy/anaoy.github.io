---
title: 'Microsoft fixes Windows Server 2016 security update failures'
date: 2026-06-18
permalink: /posts/2026/06/18/microsoft-fixes-windows-server-2016-security-update-failures/
tags:
- veille-cyber
- bleepingcomp
---
### Résolution des échecs de mise à jour sur Windows Server 2016

Microsoft a corrigé un bug affectant l'installation des mises à jour de sécurité de juin 2026 sur Windows Server 2016. Ce problème empêchait le déploiement de la mise à jour **KB5094122** si la mise à jour précédente, **KB5087537**, n'avait pas été installée au préalable.

**Points clés :**
*   **Symptômes :** Les systèmes touchés rencontraient des erreurs d'installation signalées par le code **0x80070002** (FILE_NOT_FOUND).
*   **Contexte :** Ce problème de dépendance entre mises à jour a été officiellement résolu par Microsoft.
*   **Instabilités récurrentes :** L'article souligne une série de problèmes récents liés aux mises à jour Windows, notamment des erreurs liées à l'espace disque sur la partition EFI, des blocages de BitLocker, et des conflits avec le programme d'installation WUSA.
*   **Incident en cours :** Microsoft enquête actuellement sur un bug empêchant le lancement des applications Office (Word, Excel, etc.) par des logiciels tiers suite aux déploiements de juin 2026.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée à cet incident, il s'agit d'un problème fonctionnel lié au processus de déploiement des correctifs.

**Recommandations :**
*   **Appliquer l'ordre des mises à jour :** S'assurer de maintenir les serveurs à jour avec les correctifs cumulatifs des mois précédents pour éviter les erreurs de dépendance.
*   **Surveillance :** Pour les environnements utilisant des suites bureautiques, tester les mises à jour de juin 2026 dans un environnement hors production avant un déploiement général, afin d'anticiper les problèmes de lancement d'applications Office.
*   **Gestion des erreurs :** En cas d'échec, vérifier les journaux d'erreurs (codes 0x80070002, 0x800f0922 ou 0x80073712) pour identifier si le problème est lié à une dépendance manquante ou à une insuffisance d'espace disque.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-windows-server-2016-security-update-failures/){:target="_blank"}
