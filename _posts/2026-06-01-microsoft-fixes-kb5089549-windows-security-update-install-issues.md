---
title: 'Microsoft fixes KB5089549 Windows security update install issues'
date: 2026-06-01
permalink: /posts/2026/06/01/microsoft-fixes-kb5089549-windows-security-update-install-issues/
tags:
- veille-cyber
- bleepingcomp
---
### Résolution des échecs d'installation de la mise à jour Windows KB5089549

Microsoft a corrigé un problème technique entravant l'installation de la mise à jour de sécurité de mai 2026 (KB5089549) sur Windows 11. Ce dysfonctionnement provoquait des erreurs lors du déploiement, entraînant une annulation automatique des modifications système.

**Points clés :**
* **Cause :** L'échec est dû à un espace libre insuffisant (10 Mo ou moins) sur la partition système EFI (ESP).
* **Symptômes :** Erreur `0x800f0922`, message "Something didn't go as planned", et échec constaté lors de la phase de redémarrage (environ 35-36 %).
* **Statut :** Le correctif est désormais inclus dans la mise à jour cumulative KB5089573 et sera intégré au "Patch Tuesday" de juin 2026.

**Vulnérabilités :**
* Aucune vulnérabilité de sécurité n'est associée à cet incident ; il s'agit d'un problème lié à la gestion de l'espace disque et au processus d'installation.

**Recommandations :**
* **Mise à jour directe :** Installer la mise à jour cumulative KB5089573 (ou toute version ultérieure publiée après le 26 mai 2026) pour résoudre le problème nativement.
* **Environnements d'entreprise :** Pour les administrateurs informatiques ne souhaitant pas déployer la mise à jour immédiate, utiliser le mécanisme de "Known Issue Rollback" (KIR) via la stratégie de groupe (GPO) fournie par Microsoft.
* **Maintenance :** Vérifier régulièrement l'espace disponible sur la partition système EFI si des erreurs de déploiement persistent.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-kb5089549-windows-security-update-install-issues/){:target="_blank"}
