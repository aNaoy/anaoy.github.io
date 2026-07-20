---
title: 'Windows KB5121767 OOB update fixes shutdowns on some Dell PCs'
date: 2026-07-20
permalink: /posts/2026/07/20/windows-kb5121767-oob-update-fixes-shutdowns-on-some-dell-pcs/
tags:
- veille-cyber
- bleepingcomp
---
### Correctif d'urgence Microsoft pour les pannes sur PC Dell

Microsoft a publié des mises à jour hors bande (OOB) pour résoudre un problème de stabilité critique touchant certains ordinateurs Dell sous Windows 11 (versions 25H2, 24H2 et LTSC 2024). Ce dysfonctionnement, identifié après l'installation des mises à jour de juillet 2026, provoquait des arrêts inopinés, une surchauffe, une décharge rapide de la batterie et des baisses de performance.

**Points clés :**
*   **Cause racine :** Une incompatibilité entre le nouveau gestionnaire de connexion USB-C de Windows et le pilote *Intel Innovation Platform Framework (IPF) Processor Participant*.
*   **Identification :** Les machines affectées affichent un point d'exclamation jaune sur le pilote Intel IPF dans le Gestionnaire de périphériques.
*   **Scope :** Le problème est limité aux appareils Dell ayant reçu la mise à jour cumulative KB5101650.

**Vulnérabilités :**
*   Aucun CVE associé. Il s'agit d'un conflit de pilotes et d'une instabilité système logicielle plutôt que d'une faille de sécurité exploitable.

**Recommandations :**
*   **Installation des correctifs :** Appliquer la mise à jour **KB5121767** (Windows 11 25H2/24H2) ou **KB5121768** (Windows 11 Enterprise LTSC 2024).
*   **Action ciblée :** Microsoft précise que ces mises à jour ne sont nécessaires que pour les systèmes réellement affectés ; aucune action n'est requise sur les machines stables.
*   **Gestion centralisée :** Les administrateurs IT peuvent accélérer le déploiement via Microsoft Intune ou laisser Windows Autopatch gérer l'installation automatique pour les flottes compatibles.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-windows-bug-causing-some-dell-pcs-to-shut-down/){:target="_blank"}
