---
title: 'WordPress Adds Automated Plugin Reviews to Block High-Risk Updates Before Distribution'
date: 2026-09-14
permalink: /posts/2026/09/14/wordpress-adds-automated-plugin-reviews-to-block-high-risk-updates-before-distribution/
tags:
- veille-cyber
- hackernews
---
### Renforcement de la sécurité des extensions WordPress : automatisation des contrôles

WordPress a instauré un système d'analyse automatisée de sécurité pour chaque mise à jour d'extension avant sa distribution officielle. Ce dispositif vise à prévenir l'introduction de codes malveillants ou de vulnérabilités critiques après la validation initiale d'un plugin.

**Points clés :**
*   **Période de latence (Cooldown) :** Chaque mise à jour subit un délai de six heures avant déploiement.
*   **Analyse automatisée :** Durant ce délai, les modifications sont inspectées par des modèles d'IA et l'outil Jetpack Scan.
*   **Blocage préventif :** Un score de risque est généré ; si celui-ci dépasse un seuil critique, la mise à jour est automatiquement bloquée.
*   **Notification :** Les développeurs reçoivent une notification par e-mail en cas de blocage, détaillant les motifs de l'échec.

**Vulnérabilités ciblées (non exhaustif) :**
Bien qu'aucune CVE spécifique ne soit mentionnée, le système détecte les failles classiques, notamment :
*   Absence de vérification des droits d'accès sur les endpoints (REST, AJAX, admin-post).
*   Requêtes SQL non sécurisées (utilisation de `$wpdb->prepare()` manquante).
*   Manipulation dangereuse de chemins de fichiers basée sur des données utilisateur.
*   Utilisation de `unserialize()` sur des données externes.
*   Code obfusqué ou évaluation dynamique de code à l'exécution.

**Recommandations pour les développeurs :**
*   **Standards de codage :** Respecter strictement les *WordPress Coding Standards* et les règles de *PHP_CodeSniffer* (PHPCS).
*   **Outils de test :** Utiliser la plateforme *Quality Insights Toolkit* (QIT) pour les extensions WooCommerce.
*   **Correction autonome :** En cas de blocage, la méthode la plus rapide pour rétablir la mise à jour consiste à corriger les vulnérabilités identifiées et à soumettre une nouvelle version, plutôt que de demander un examen manuel.

---
[Source](https://thehackernews.com/2026/09/wordpress-adds-automated-plugin-reviews.html){:target="_blank"}
