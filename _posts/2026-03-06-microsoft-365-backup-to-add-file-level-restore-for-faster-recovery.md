---
title: 'Microsoft 365 Backup to add file-level restore for faster recovery'
date: 2026-03-06
permalink: /posts/2026/03/06/microsoft-365-backup-to-add-file-level-restore-for-faster-recovery/
tags:
- veille-cyber
- bleepingcomp
---
### Optimisation de la restauration granulaire dans Microsoft 365 Backup

Microsoft améliore son service de sauvegarde pour SharePoint, OneDrive et Exchange en introduisant la restauration au niveau des fichiers et des dossiers, prévue pour une disponibilité générale entre fin avril et début mai 2026. Cette mise à jour vise à accélérer considérablement les processus de récupération face aux ransomwares, aux suppressions accidentelles ou aux corruptions de données.

**Points clés :**
*   **Granularité accrue :** Les administrateurs peuvent désormais rechercher et restaurer des éléments spécifiques au sein des points de restauration, évitant ainsi le processus long et complexe de restauration complète d'un site ou d'un lecteur.
*   **Contrôle administrateur :** La fonctionnalité est réservée aux utilisateurs disposant du rôle "SharePoint Backup Administrator". Les opérations sont invisibles pour les utilisateurs finaux.
*   **Conservation des politiques :** Cette nouveauté n'impacte ni l'emplacement, ni la méthode de stockage des données de sauvegarde existantes.

**Vulnérabilités :**
*   Aucune CVE associée. L'article se concentre sur une évolution fonctionnelle visant à atténuer les impacts opérationnels liés à la perte de données.

**Recommandations :**
*   **Audit de couverture :** Vérifier que les sites SharePoint et OneDrive critiques sont correctement couverts par les politiques Microsoft 365 Backup.
*   **Formation :** Familiariser les administrateurs avec le nouveau flux de travail de restauration granulaire.
*   **Mise à jour documentaire :** Réviser les procédures internes de récupération (runbooks) pour intégrer les scénarios de restauration ciblée au niveau des fichiers et dossiers.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-365-backup-to-add-file-level-restore-for-faster-recovery/){:target="_blank"}
