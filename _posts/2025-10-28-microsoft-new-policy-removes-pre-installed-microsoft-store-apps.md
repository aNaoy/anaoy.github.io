---
title: 'Microsoft: New policy removes pre-installed Microsoft Store apps'
date: 2025-10-28
permalink: /posts/2025/10/28/microsoft-new-policy-removes-pre-installed-microsoft-store-apps/
tags:
- veille-cyber
- bleepingcomp
---
**Gestion simplifiée des applications préinstallées sous Windows 11**

Une nouvelle politique introduite par Microsoft permet désormais aux administrateurs informatiques de supprimer les applications préinstallées du Microsoft Store (également appelées applications intégrées) sur les éditions Windows 11 Enterprise 25H2 et Windows 11 Education 25H2. Cette fonctionnalité simplifie la gestion des appareils en éliminant le besoin de créer des images d'installation personnalisées ou d'utiliser des scripts complexes. Les administrateurs peuvent sélectionner les applications à supprimer à partir d'une liste prédéfinie, et la politique, une fois appliquée, déprovisionne et supprime automatiquement les packages et les données locales des applications concernées. La politique est désactivée par défaut et doit être explicitement activée par les administrateurs via des outils comme Microsoft Intune, les objets de stratégie de groupe (GPO) ou le fournisseur de services de configuration (CSP).

**Points Clés :**

*   Microsoft a introduit une nouvelle politique pour la suppression des applications préinstallées du Microsoft Store.
*   Applicable aux versions Windows 11 Enterprise 25H2 et Windows 11 Education 25H2.
*   Simplifie la gestion en évitant les scripts personnalisés et les images d'installation complexes.
*   Permet aux administrateurs de sélectionner les applications à supprimer à partir d'une liste prédéfinie.
*   La suppression est automatique et supprime les données locales associées.
*   La politique est désactivée par défaut et nécessite une activation explicite.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec des identifiants CVE n'est mentionnée dans cet article concernant la nouvelle politique de suppression d'applications.

**Recommandations :**

*   Les administrateurs des environnements Windows 11 Enterprise et Education (version 25H2) devraient évaluer la pertinence de cette nouvelle politique pour optimiser la gestion de leurs appareils.
*   Il est conseillé d'activer explicitement cette politique si la suppression d'applications préinstallées est une exigence organisationnelle.
*   Consulter la documentation de Microsoft pour obtenir la liste complète des applications prises en charge et les instructions détaillées d'application via les différents outils de gestion (Intune, GPO, CSP).

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-now-lets-admins-remove-pre-installed-microsoft-store-apps-via-policy/){:target="_blank"}
