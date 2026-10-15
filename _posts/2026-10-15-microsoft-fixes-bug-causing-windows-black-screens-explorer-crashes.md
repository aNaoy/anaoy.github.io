---
title: 'Microsoft fixes bug causing Windows black screens, Explorer crashes'
date: 2026-10-15
permalink: /posts/2026/10/15/microsoft-fixes-bug-causing-windows-black-screens-explorer-crashes/
tags:
- veille-cyber
- bleepingcomp
---
### Correction du bug d'écran noir sur Windows 11

Microsoft a résolu un problème technique impactant principalement les environnements Azure Virtual Desktop (AVD) utilisant FSLogix. Ce dysfonctionnement, survenu après l'installation des mises à jour de Windows 11 depuis août 2026, provoquait des écrans noirs au démarrage, des difficultés de chargement du bureau et des plantages de l'Explorateur Windows.

**Points clés :**
*   **Cause identifiée :** Conflit logiciel entre les mises à jour Windows et la solution de gestion de profils FSLogix.
*   **Impact :** Impossibilité d'accéder au bureau après la connexion et instabilité de l'Explorateur Windows.
*   **Vulnérabilité :** Il ne s'agit pas d'une faille de sécurité exploitable, mais d'un bug de fonctionnement (aucune CVE associée).

**Recommandations :**
*   **Solution définitive :** Installer les mises à jour cumulatives publiées lors du "Patch Tuesday" d'octobre 2026 (ou toute version ultérieure).
*   **Contournement manuel :** En cas d'impossibilité de mise à jour, lancer manuellement le processus `explorer.exe` via le Gestionnaire des tâches (Ctrl+Shift+Esc > Exécuter une nouvelle tâche).
*   **Pour les administrateurs IT :** Déployer les correctifs via le *Known Issue Rollback* (KIR) en utilisant les stratégies de groupe (GPO) spécifiques aux versions de Windows 11 concernées (KB5124006 ou KB5124010) pour désactiver temporairement le changement incriminé.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-bug-causing-windows-black-screens-explorer-crashes/){:target="_blank"}
