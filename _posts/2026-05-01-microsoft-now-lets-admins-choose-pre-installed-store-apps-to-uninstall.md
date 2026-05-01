---
title: 'Microsoft now lets admins choose pre-installed Store apps to uninstall'
date: 2026-05-01
permalink: /posts/2026/05/01/microsoft-now-lets-admins-choose-pre-installed-store-apps-to-uninstall/
tags:
- veille-cyber
- bleepingcomp
---
### Gestion dynamique des applications préinstallées sous Windows 11

Microsoft a enrichi sa politique `RemoveDefaultMicrosoftStorePackages`, permettant désormais aux administrateurs informatiques de supprimer de manière dynamique n'importe quelle application MSIX/APPX préinstallée via la stratégie de groupe (GPO) ou une solution MDM (OMA-URI). Cette mise à jour offre une gestion plus granulaire du parc informatique en facilitant le nettoyage des applications inutilisées.

**Points clés :**
*   **Flexibilité accrue :** Les administrateurs peuvent cibler des applications spécifiques en utilisant leur *Package Family Name* (PFN), récupérable via PowerShell.
*   **Extension du support :** Initialement limitée à Windows 11 25H2, cette fonctionnalité est désormais rétrocompatible avec les éditions **Enterprise** et **Education de Windows 11 24H2**.
*   **Suppression de Copilot :** Une politique distincte (`RemoveMicrosoftCopilotApp`) a été introduite pour permettre la désinstallation de l'assistant IA sur les appareils d'entreprise.
*   **Disponibilité :** Nécessite l'installation des mises à jour non sécuritaires d'avril 2026. L'intégration complète dans Microsoft Intune est prévue pour les prochains mois.

**Vulnérabilités :**
*   Aucune vulnérabilité spécifique (CVE) n'est associée à cette mise à jour. Il s'agit d'une évolution fonctionnelle visant à améliorer la sécurité et la conformité des systèmes par la réduction de la surface d'attaque logicielle (réduction des applications inutiles).

**Recommandations :**
*   **Mise à jour :** Déployer les mises à jour système d'avril 2026 sur les parcs d'ordinateurs pour accéder à ces nouvelles options de contrôle.
*   **Gestion des PFN :** Utiliser la commande PowerShell `Get-AppxPackage *NomApp* | Select-Object PackageFamilyName` pour identifier précisément les applications à supprimer dans l'environnement de votre organisation.
*   **Application des politiques :** Configurer les GPO via l'éditeur de stratégie de groupe (`gpedit.msc`) sous *Configuration ordinateur > Modèles d'administration > Composants Windows > Déploiement de packages d'application*.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-now-lets-admins-choose-pre-installed-store-apps-to-uninstall/){:target="_blank"}
