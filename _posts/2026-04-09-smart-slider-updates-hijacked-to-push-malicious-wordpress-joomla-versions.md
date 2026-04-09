---
title: 'Smart Slider updates hijacked to push malicious WordPress, Joomla versions'
date: 2026-04-09
permalink: /posts/2026/04/09/smart-slider-updates-hijacked-to-push-malicious-wordpress-joomla-versions/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement : Smart Slider 3 Pro

Le système de mise à jour du plugin Smart Slider 3 Pro pour WordPress et Joomla a été piraté, entraînant la distribution de la version malveillante **3.5.1.35**. Cette attaque par chaîne d'approvisionnement a permis d'installer un kit d'outils sophistiqué tout en conservant les fonctionnalités légitimes du plugin.

**Points clés :**
*   **Vecteur d'attaque :** Mise à jour légitime compromise, distribuée le 7 avril.
*   **Impact :** Accès distant sans authentification via des en-têtes HTTP contrefaits, création de comptes administrateurs cachés et vol automatisé d'identifiants.
*   **Persistance multi-niveaux :** Utilisation de "must-use plugins" (invisibles dans le tableau de bord), modification du fichier `functions.php` du thème actif et injection de fichiers PHP imitant des composants système légitimes dans `wp-includes`.
*   **Vulnérabilité :** Aucune CVE spécifique attribuée, il s'agit d'une injection de code malveillant via une mise à jour compromise.

**Recommandations :**
*   **Mise à jour immédiate :** Passer impérativement à la version **3.5.1.36** ou revenir à une version antérieure à 3.5.1.35.
*   **Restauration :** Si le site est infecté, restaurer une sauvegarde datant d'avant le 5 avril.
*   **Nettoyage approfondi :** En cas d'absence de sauvegarde, supprimer le plugin, réinstaller les composants WordPress (cœur, thèmes, plugins) à partir de sources fiables, et supprimer manuellement les utilisateurs et fichiers suspects.
*   **Sécurisation post-incident :** 
    *   Renouveler l'ensemble des accès (mots de passe WP, base de données, FTP/SSH, emails).
    *   Régénérer les clés de sécurité (salts) WordPress.
    *   Activer l'authentification à deux facteurs (2FA).
    *   Effectuer un scan complet du serveur à la recherche de traces résiduelles de malware.

---
[Source](https://www.bleepingcomputer.com/news/security/smart-slider-updates-hijacked-to-push-malicious-wordpress-joomla-versions/){:target="_blank"}
