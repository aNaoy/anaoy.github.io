---
title: 'Microsoft enables Windows settings backup by default for orgs'
date: 2026-10-01
permalink: /posts/2026/10/01/microsoft-enables-windows-settings-backup-by-default-for-orgs/
tags:
- veille-cyber
- bleepingcomp
---
### Automatisation de la sauvegarde des paramètres Windows en entreprise

Microsoft a activé par défaut la sauvegarde des paramètres Windows sur tous les systèmes professionnels joints à Microsoft Entra (ou hybrides) mis à niveau vers Windows 11 26H2. Cette fonctionnalité permet de restaurer les préférences utilisateur et la liste des applications Microsoft Store en cas de réinitialisation, de remplacement ou de mise à niveau de l'appareil.

**Points clés :**
* **Déploiement :** La mesure concerne les appareils sous Windows 11 26H2 n'ayant pas de configuration explicite (activée ou désactivée) définie par l'administrateur.
* **Exceptions géographiques et techniques :** La sauvegarde automatique ne s'applique pas aux pays régis par le *Digital Markets Act* (DMA) de l'UE, ni aux environnements cloud souverains ou restreints.
* **Contrôle administratif :** La configuration via Intune ou les stratégies de groupe (GPO) reste prioritaire sur ce nouveau comportement par défaut.
* **Restauration :** Bien que la sauvegarde soit automatique, le processus de restauration des données nécessite toujours une autorisation explicite de l'administrateur.

**Vulnérabilités :**
* Aucune vulnérabilité CVE n'est associée à cette mise à jour ; il s'agit d'une évolution fonctionnelle et non d'un correctif de sécurité.

**Recommandations :**
* **Audit des politiques :** Les administrateurs IT doivent vérifier si la politique de sauvegarde des paramètres Windows est déjà configurée dans leur environnement (Intune/GPO) pour éviter tout conflit avec le nouveau comportement par défaut.
* **Gestion des données :** Si la politique de sauvegarde automatique ne correspond pas aux exigences de conformité ou de confidentialité de l'organisation, il est recommandé de désactiver explicitement la fonctionnalité via les outils de gestion de flotte (MDM).

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-enables-windows-settings-backup-by-default-for-orgs/){:target="_blank"}
