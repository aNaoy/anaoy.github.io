---
title: 'The Double-Edged Sword of Non-Human Identities'
date: 2026-02-05
permalink: /posts/2026/02/05/the-double-edged-sword-of-non-human-identities/
tags:
- veille-cyber
- bleepingcomp
---
## Identités Non Humaines : Une Épée à Double Tranchant pour la Sécurité

Une analyse récente a révélé plus de 10 000 images de conteneurs Docker Hub contenant des secrets sensibles tels que des clés API de production, des jetons cloud, des identifiants CI/CD et des jetons d'accès aux modèles d'IA. Ces informations étaient souvent involontairement exposées dans des dépôts publics.

Les identités non humaines (NHI), incluant les jetons, les clés API et les comptes de service, sont essentielles au fonctionnement des infrastructures modernes. Contrairement aux utilisateurs humains, elles s'authentifient en continu, souvent avec des privilèges étendus et une durée de vie indéterminée.

### Points Clés

*   L'exposition des NHI n'est pas un cas isolé mais une défaillance structurelle dans la construction et l'exploitation des logiciels.
*   Les NHI, lorsqu'elles sont exposées, offrent aux attaquants un accès silencieux, durable et légitime, souvent sans déclencher d'alertes car l'activité semble normale.
*   Le cycle de vie des NHI n'est pas géré comme celui des utilisateurs humains, ce qui les rend persistantes et potentiellement dangereuses si elles sont compromises.

### Vulnérabilités et Incidents

Bien que l'article ne mentionne pas explicitement de CVE, il détaille des incidents significatifs dus à l'exposition de NHI :

*   **Breach Snowflake (2024) :** Environ 165 organisations compromises par l'abus de credentials (comptes d'automatisation, identités d'accès aux données) collectés sur des années via des malwares et des marchés criminels. Ces identifiants, souvent sans MFA et à durée de vie illimitée, ont permis l'accès à des données sensibles.
*   **Exposition Home Depot (2025) :** Un seul jeton d'accès GitHub exposé publiquement a maintenu l'accès aux systèmes internes pendant plus d'un an. Ce jeton, doté de droits étendus, offrait un accès à des dépôts privés, à l'infrastructure cloud et aux systèmes d'exploitation.
*   **Breach Red Hat GitLab (2025) :** Des dépôts privés et des rapports clients exposés contenaient des credentials intégrés (jetons, clés de service, URIs de base de données), transformant les dépôts de code en stores d'identifiants involontaires.
*   **Docker Hub Secrets (fin 2025) :** Plus de 10 000 images de conteneurs contenaient des clés exposées dans diverses catégories : IA, cloud, bases de données, accès, API, SCM/CI, communication, et paiements.

### Recommandations

Pour les équipes de sécurité, l'impératif est le suivant :

*   **Traiter les images de conteneurs comme du code ET des credentials :** Ce sont des vecteurs potentiels de fuite de clés sensibles.
*   **Intégrer le scan automatisé des secrets à chaque étape du cycle de vie du développement logiciel (SDLC) :** Détecter les fuites avant la publication.
*   **Adopter des credentials éphémères et de courte durée :** Privilégier la fédération d'identités plutôt que les jetons statiques intégrés aux images.
*   **Surveiller les clés exposées dans les registres publics :** Révoquer proactivement les identifiants compromis.
*   **Traiter les identités non humaines comme des identités humaines :** Surveiller leur comportement, limiter leur accès et les supprimer lorsqu'elles ne sont plus nécessaires.

Des outils spécialisés, tels que les plateformes de gestion de l'exposition aux menaces, sont désormais essentiels pour scanner en continu les registres publics et les dépôts de code afin de détecter et de remédier rapidement aux identifiants exposés.

---
[Source](https://www.bleepingcomputer.com/news/security/the-double-edged-sword-of-non-human-identities/){:target="_blank"}
