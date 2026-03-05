---
title: 'Wikipedia hit by self-propagating JavaScript worm that vandalized pages'
date: 2026-03-05
permalink: /posts/2026/03/05/wikipedia-hit-by-self-propagating-javascript-worm-that-vandalized-pages/
tags:
- veille-cyber
- bleepingcomp
---
## Versement de Wikipédia par un ver JavaScript

La fondation Wikimedia a été victime d'une attaque de sécurité impliquant un ver JavaScript auto-répliquant qui a dégradé des pages et modifié des scripts d'utilisateurs sur plusieurs wikis. Les éditeurs ont signalé des modifications automatisées ajoutant des scripts cachés et du vandalisme à des pages aléatoires. Les ingénieurs de Wikimedia ont temporairement restreint les modifications pendant l'investigation et la restauration des changements.

### Points Clés

*   L'incident a débuté par l'exécution d'un script malveillant hébergé sur le Wikipédia russe.
*   Ce script a modifié un script JavaScript global de Wikipédia avec du code malveillant.
*   Le script malveillant, hébergé sur la page `User:Ololoshka562/test.js`, aurait été utilisé dans des attaques antérieures.
*   Il est supposé que le script a été exécuté pour la première fois par un compte employé de Wikimedia lors du test de la fonctionnalité de scripts utilisateur.
*   Le script s'auto-propague en injectant des chargeurs JavaScript malveillants dans le `common.js` de l'utilisateur connecté et dans le `MediaWiki:Common.js` global, affectant ainsi tous les utilisateurs.
*   Il modifie également des pages aléatoires en insérant une image et un chargeur JavaScript caché.
*   Environ 3 996 pages ont été modifiées et 85 utilisateurs ont eu leurs fichiers `common.js` remplacés.

### Vulnérabilités

L'article ne mentionne pas de CVE spécifiques. La vulnérabilité exploitée réside dans la manière dont les scripts JavaScript globaux et utilisateurs (`MediaWiki:Common.js` et `User:<username>/common.js`) sont exécutés dans les navigateurs des éditeurs pour personnaliser l'interface du wiki. L'exécution non vérifiée ou malveillante de ces scripts permet à un attaquant d'injecter du code préjudiciable.

### Recommandations

Bien que l'article se concentre sur l'incident et sa résolution, les actions entreprises par Wikimedia suggèrent les recommandations suivantes :

*   **Restriction temporaire des modifications :** En cas d'incident de sécurité majeur, il est nécessaire de restreindre temporairement les fonctionnalités critiques comme la modification de pages.
*   **Restauration des changements :** Mettre en place des processus efficaces pour identifier et annuler les modifications malveillantes.
*   **Suppression du code injecté :** Retirer activement tout code malveillant des scripts globaux et utilisateurs.
*   **"Suppression" des modifications :** Utiliser des mécanismes pour masquer les modifications malveillantes dans l'historique des versions afin d'éviter la confusion et la propagation ultérieure.
*   **Investigation approfondie :** Effectuer une analyse post-incident détaillée pour comprendre les causes profondes de l'exécution du script et les vecteurs de propagation.
*   **Renforcement de la sécurité des scripts :** Examiner et potentiellement renforcer les mécanismes de validation et de contrôle d'exécution des scripts ajoutés aux plateformes wiki.

---
[Source](https://www.bleepingcomputer.com/news/security/wikipedia-hit-by-self-propagating-javascript-worm-that-vandalized-pages/){:target="_blank"}
