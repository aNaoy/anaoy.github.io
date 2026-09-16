---
title: 'Malcious Admin Menu Editor Pro plugin backdoors 1,500 WordPress sites'
date: 2026-09-16
permalink: /posts/2026/09/16/malcious-admin-menu-editor-pro-plugin-backdoors-1500-wordpress-sites/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement : Admin Menu Editor Pro

Le site officiel du plugin WordPress *Admin Menu Editor Pro* a été compromis par un acteur malveillant, entraînant la distribution de versions piégées (2.35 et 2.36) à environ 1 500 sites web. L'attaquant a pu injecter un *web shell* et créer des comptes administrateurs cachés pour maintenir un accès persistant. Aucune CVE n'a été attribuée à cet incident, car il s'agit d'une compromission directe des serveurs de mise à jour du développeur plutôt que d'une vulnérabilité logicielle classique.

**Points clés :**
*   **Vecteur d'attaque :** Accès de niveau "root" au serveur de l'éditeur ayant permis de remplacer les fichiers de mise à jour officiels.
*   **Impact :** Au moins 230 clients touchés sur 1 500 sites web.
*   **Comportement malveillant :** Création d'un utilisateur factice (nommé avec le préfixe `wp_`) et ajout d'un script `wp-user-consent.php` agissant comme porte dérobée.

**Indicateurs de compromission :**
*   Présence du fichier `includes/wp-user-consent.php` dans le répertoire du plugin.
*   Apparition d'un répertoire `/wp-content/object-cache/`.
*   Utilisateurs suspects commençant par `wp_` dans la table `wp_users`.
*   Entrées dans la table `wp_options` commençant par `wp_ocache`.

**Recommandations :**
*   **Action prioritaire :** Restaurer le site à partir d'une sauvegarde saine antérieure au 14 septembre.
*   **Nettoyage manuel :** Si la restauration est impossible, supprimer le plugin, effacer le répertoire `/wp-content/object-cache/` et supprimer manuellement les entrées corrompues dans les tables `wp_users` et `wp_options`.
*   **Mise à jour :** S'assurer d'utiliser une version du plugin postérieure à la correction (la version 2.34 est considérée comme la dernière version saine avant l'incident).

---
[Source](https://www.bleepingcomputer.com/news/security/malcious-admin-menu-editor-pro-plugin-backdoors-1-500-wordpress-sites/){:target="_blank"}
