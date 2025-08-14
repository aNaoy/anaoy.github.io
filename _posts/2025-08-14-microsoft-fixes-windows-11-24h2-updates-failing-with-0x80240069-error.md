---
title: 'Microsoft fixes Windows 11 24H2 updates failing with 0x80240069 error'
date: 2025-08-14
permalink: /posts/2025/08/14/microsoft-fixes-windows-11-24h2-updates-failing-with-0x80240069-error/
tags:
- veille-cyber
- bleepingcomp
---
**Correction d'une erreur d'installation de la mise à jour Windows 11 24H2 via WSUS**

Un problème empêchant la bonne distribution de la mise à jour cumulative d'août 2025 pour Windows 11, version 24H2 (KB5063878), via Windows Server Update Services (WSUS) a été résolu par Microsoft. Cette défaillance, signalée par le code d'erreur 0x80240069, affectait principalement les environnements d'entreprise gérés par WSUS. Les messages d'erreur observés indiquaient l'arrêt inattendu du service Windows Update (wuauserv).

**Points clés :**

*   **Problème :** La mise à jour cumulative KB5063878 pour Windows 11 24H2 échoue lors de l'installation via WSUS avec l'erreur 0x80240069.
*   **Cause présumée :** Arrêt inattendu du service Windows Update.
*   **Cible :** Principalement les environnements d'entreprise utilisant WSUS.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article. L'article traite d'un problème de déploiement de mise à jour.

**Recommandations :**

*   **Pour les administrateurs d'entreprise :**
    *   Déployer la politique de "Known Issue Rollback" (KIR) via le Group Policy Editor pour les appareils Windows 11 24H2 concernés. Cela implique de cibler la version Windows appropriée dans la politique locale ou de domaine, puis de redémarrer les appareils.
    *   Microsoft a également publié un correctif sous forme de "Known Issue Rollback" déployé automatiquement sur les appareils gérés par l'entreprise.
*   **Solutions de contournement pour tous :**
    *   Installer manuellement la mise à jour KB5063878 via Windows Update.
    *   Télécharger et installer manuellement la mise à jour depuis le Microsoft Update Catalog.

Cet incident est similaire à un problème rencontré en avril pour les mises à jour de Windows 11 22H2/23H2 via WSUS, qui avait également été résolu par KIR en mai.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-windows-11-24h2-updates-failing-with-0x80240069-error/){:target="_blank"}
