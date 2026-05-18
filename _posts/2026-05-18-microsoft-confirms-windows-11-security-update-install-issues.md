---
title: 'Microsoft confirms Windows 11 security update install issues'
date: 2026-05-18
permalink: /posts/2026/05/18/microsoft-confirms-windows-11-security-update-install-issues/
tags:
- veille-cyber
- bleepingcomp
---
### Erreurs d'installation de la mise à jour KB5089549 sur Windows 11

Microsoft a confirmé que la mise à jour de sécurité de mai 2026, **KB5089549**, échoue sur certains systèmes Windows 11, provoquant une annulation automatique des changements et l'erreur **0x800f0922**.

**Points clés :**
*   **Cause technique :** Espace insuffisant (10 Mo ou moins) sur la partition système EFI (ESP).
*   **Symptômes :** L'installation s'arrête lors du redémarrage (vers 35-36 %) avec un message d'annulation des modifications et des logs indiquant des erreurs d'espace disque (`SpaceCheck`).
*   **Vulnérabilité :** Aucune CVE associée ; il s'agit d'un problème de gestion de partition lié à l'infrastructure de mise à jour.

**Recommandations :**
*   **Utilisateurs individuels :** Utiliser la fonctionnalité « Known Issue Rollback » (KIR) fournie par Microsoft pour annuler temporairement la modification causant le conflit.
*   **Environnements d'entreprise :** Déployer la stratégie de groupe (GPO) spécifique fournie par Microsoft via le fichier `.msi` dédié, puis redémarrer les machines pour appliquer le correctif et stabiliser le système.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-confirms-kb5089549-windows-11-security-update-install-issues/){:target="_blank"}
