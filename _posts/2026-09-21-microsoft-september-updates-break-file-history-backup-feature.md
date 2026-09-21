---
title: 'Microsoft: September updates break File History backup feature'
date: 2026-09-21
permalink: /posts/2026/09/21/microsoft-september-updates-break-file-history-backup-feature/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnement de la fonctionnalité "Historique des fichiers" après les mises à jour de septembre 2026

Les mises à jour de sécurité de septembre 2026 déployées par Microsoft provoquent une instabilité majeure de la fonctionnalité native « Historique des fichiers » sous Windows 10 et 11. Cette défaillance empêche les utilisateurs d'effectuer ou de mettre à jour leurs sauvegardes sur des disques externes ou des serveurs NAS.

**Points clés :**
*   **Symptômes constatés :** Crashs de l'application (`FileHistory.exe`), messages d'erreur erronés invitant à « reconnecter le lecteur » alors que celui-ci est opérationnel, et impossibilité d'accéder aux versions précédentes des fichiers.
*   **Versions affectées :** Windows 11 (23H2 à 26H1) et Windows 10 (21H2, 22H2, ainsi que les éditions Enterprise LTSC 2016 et 2019).
*   **Contexte global :** Ce problème s'ajoute à une série de bugs introduits par les mises à jour de septembre, affectant également les services de bureau à distance (RDS), Hyper-V, les périphériques audio USB et l'authentification de domaine.

**Vulnérabilités :**
*   Aucune faille de sécurité (CVE) n'est associée à cet incident ; il s'agit d'une régression logicielle introduite par les correctifs de sécurité eux-mêmes.

**Recommandations :**
*   **Surveillance :** Les administrateurs système doivent vérifier les journaux d'événements (Event Viewer) pour identifier les erreurs liées à `FileHistory.exe` et `KERNELBASE.dll`.
*   **Attente de correctif :** Microsoft n'a pas encore publié de correctif spécifique pour ce bug. Il est conseillé de surveiller le tableau de bord « Windows Release Health » pour les futures mises à jour correctives.
*   **Mesures palliatives :** En cas d'impossibilité de sauvegarder les données, envisagez l'utilisation de solutions de sauvegarde tierces ou de méthodes alternatives de réplication de données jusqu'à la résolution du problème par l'éditeur.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-september-updates-break-file-history-backup-feature/){:target="_blank"}
