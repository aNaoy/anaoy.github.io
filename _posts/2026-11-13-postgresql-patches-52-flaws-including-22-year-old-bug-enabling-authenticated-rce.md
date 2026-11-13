---
title: 'PostgreSQL Patches 52 Flaws, Including 22-Year-Old Bug Enabling Authenticated RCE'
date: 2026-11-13
permalink: /posts/2026/11/13/postgresql-patches-52-flaws-including-22-year-old-bug-enabling-authenticated-rce/
tags:
- veille-cyber
- hackernews
---
### Correction critique : PostgreSQL corrige 52 vulnérabilités dont une faille RCE historique

Le projet PostgreSQL a publié des mises à jour correctives adressant 52 vulnérabilités, incluant une faille critique de confusion de type vieille de 22 ans permettant une exécution de code à distance (RCE) sous certaines conditions.

**Points clés :**
*   **Vulnérabilité majeure :** Une faille de confusion de type dans la gestion des types composites permet à un utilisateur authentifié (disposant de droits de création d'objets) d'exécuter du code avec les privilèges du processus PostgreSQL.
*   **Portée :** Le problème est lié à la manipulation des types de champs, rendant possible la lecture de valeurs obsolètes comme si elles possédaient un nouveau type. 
*   **Historique :** La racine du problème remonte à 2004, avec un vecteur d'exploitation facilité par une modification du code en 2015.
*   **Autres risques :** Outre la RCE, d'autres failles corrigées concernent les outils clients (ex: `pg_restore`, `psql`), permettant l'exécution de code via des archives ou serveurs sources compromis. Une vulnérabilité (CVE-2026-116322) permet également à un client non authentifié de provoquer un redémarrage des serveurs en version 18.

**Vulnérabilités identifiées :**
*   **CVE-2026-6460 :** Faille de confusion de type (Score CVSS : 8.8), permettant potentiellement une RCE.
*   **CVE-2026-116322 :** Risque de déni de service (redémarrage non autorisé) sur PostgreSQL 18.

**Versions corrigées :**
La mise à jour concerne les versions 18.7, 17.12, 16.16, 15.20 et 14.25. (Note : la version 14 atteint sa fin de vie avec cette mise à jour).

**Recommandations :**
1.  **Mise à jour immédiate :** Appliquer les patchs vers les versions listées ci-dessus.
2.  **Reconstruction des extensions :** Il est impératif de reconstruire ou mettre à jour toutes les extensions en langage C. Celles construites avec d'anciennes versions pourraient ne pas être protégées contre les nouvelles vulnérabilités.
3.  **Outils clients :** Mettre à jour les outils tels que `pg_dump`, `pg_restore`, `reindexdb` et `vacuumdb` sur toutes les machines clientes.
4.  **Maintenance post-mise à jour :** Effectuer les procédures de réindexation recommandées et réaliser une nouvelle sauvegarde complète (full backup) pour garantir l'intégrité des sauvegardes incrémentielles.
5.  **Sécurité :** Ne pas désactiver les nouveaux contrôles de sécurité (`composite_type_mismatch`) introduits par le correctif.

---
[Source](https://thehackernews.com/2026/11/postgresql-patches-52-flaws-including.html){:target="_blank"}
