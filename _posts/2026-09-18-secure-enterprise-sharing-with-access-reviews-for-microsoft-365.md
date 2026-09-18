---
title: 'Secure enterprise sharing with access reviews for Microsoft 365'
date: 2026-09-18
permalink: /posts/2026/09/18/secure-enterprise-sharing-with-access-reviews-for-microsoft-365/
tags:
- veille-cyber
- bleepingcomp
---
### Sécurisation des accès et gouvernance dans Microsoft 365

La facilité de partage au sein des suites collaboratives comme Microsoft 365 (M365) crée un risque sécuritaire majeur : la persistance inutile des accès. Le partage étant contextuel et souvent temporaire, les autorisations octroyées à des collaborateurs internes ou externes sont fréquemment oubliées, créant une surface d'exposition importante pour les données sensibles.

**Points clés :**
* **Obsolescence des accès :** Une majorité d'entreprises peine à identifier qui a accès à quoi, les autorisations dépassant souvent la durée de vie du projet initial.
* **Insuffisance des outils natifs :** Les rapports de Microsoft 365 (SharePoint Advanced Management ou rapports par site) sont soit trop généraux, soit trop chronophages à analyser manuellement, empêchant une gouvernance efficace.
* **Le besoin de visibilité centralisée :** La gestion des accès doit passer par une vision d'ensemble permettant d'identifier les partages problématiques et de déléguer la responsabilité aux propriétaires des données.

**Vulnérabilités :**
* Bien qu'il n'y ait pas de CVE spécifique mentionnée, l'article souligne une faille structurelle : la **gestion inadéquate du cycle de vie des accès** ("Privilege Creep"). Cela conduit à des accès non autorisés ou abusifs, augmentant le risque de fuite de données par des tiers dont les droits n'ont jamais été révoqués.

**Recommandations :**
* **Mise en place de revues d'accès régulières :** Impliquer systématiquement les propriétaires des fichiers ou des dossiers dans le processus de validation, car ils sont les seuls à connaître le contexte métier nécessaire pour justifier le maintien d'un accès.
* **Automatisation du cycle de vie :** Utiliser des solutions de gouvernance des identités et des accès (IGA) pour centraliser la visibilité sur OneDrive, SharePoint et Teams.
* **Délégation de la gouvernance :** Décentraliser la revue des accès vers les utilisateurs métiers (non-IT) via des tableaux de bord simplifiés pour garantir que les audits sont rapides, précis et à jour.

---
[Source](https://www.bleepingcomputer.com/news/security/secure-enterprise-sharing-with-access-reviews-for-microsoft-365/){:target="_blank"}
