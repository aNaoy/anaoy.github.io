---
title: 'Microsoft: Recent Windows updates cause desktop loading issues'
date: 2026-09-25
permalink: /posts/2026/09/25/microsoft-recent-windows-updates-cause-desktop-loading-issues/
tags:
- veille-cyber
- bleepingcomp
---
### Problèmes de chargement du bureau sur Windows après les mises à jour d'août 2026

Des mises à jour récentes de Windows (août 2026) provoquent des erreurs de chargement du bureau et des écrans noirs, impactant principalement les environnements Azure Virtual Desktop (AVD) utilisant FSLogix.

**Points clés :**
*   **Symptômes :** Écran noir après la connexion et plantages récurrents de l'explorateur Windows (*explorer.exe*).
*   **Mises à jour incriminées :** KB5120996, KB5120998, KB5124008 et KB5122880.
*   **Vulnérabilités :** Aucune CVE identifiée ; il s'agit d'un dysfonctionnement logiciel lié à la gestion des profils utilisateurs.

**Recommandations :**
*   **Contournement immédiat :** Lancer manuellement le processus via le Gestionnaire des tâches (Ctrl+Shift+Esc > Exécuter une nouvelle tâche > saisir `explorer.exe`).
*   **Solution pour les entreprises :** Déployer la fonctionnalité *Known Issue Rollback* (KIR) via les stratégies de groupe (GPO) fournies par Microsoft :
    *   **KB5124006** pour Windows 11 26H1.
    *   **KB5124010** pour Windows 11 24H2, 25H2 et Windows Server 2025.
*   **Note :** Un redémarrage du système est nécessaire après l'application de la stratégie de groupe pour que la correction soit effective.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-recent-windows-updates-cause-desktop-loading-issues/){:target="_blank"}
