---
title: 'Suspicious Polyfill login prompts pop up on Toshiba, Muji websites'
date: 2026-06-06
permalink: /posts/2026/06/06/suspicious-polyfill-login-prompts-pop-up-on-toshiba-muji-websites/
tags:
- veille-cyber
- bleepingcomp
---
### Menace persistante : Les sites de Toshiba et Muji ciblés par des fenêtres de connexion frauduleuses

De grandes entreprises japonaises, dont Toshiba et Muji, ont alerté leurs utilisateurs sur l'apparition de fenêtres de connexion suspectes lors de la navigation sur leurs sites. Ces invites sont générées par des traces persistantes du service `polyfill.io`, un ancien CDN pour scripts JavaScript dont le domaine avait été détourné pour injecter du code malveillant dès 2024.

**Points clés :**
* **Origine :** Bien que le domaine `polyfill.io` ait été neutralisé par le passé, des sites web n'ont pas totalement purgé leurs pages du code source faisant appel à ce CDN.
* **Mécanisme :** Le domaine, réactivé fin mai 2026, répond désormais aux navigateurs par des requêtes d'authentification (HTTP 401), provoquant l'affichage natif d'une invite de connexion trompeuse pour l'utilisateur.
* **Impact étendu :** Plusieurs autres entités, incluant Zojirushi, FiNC Technologies, et même certains téléviseurs Samsung, ont été confrontées à ce comportement.

**Vulnérabilités :**
* Absence de nettoyage des dépendances tierces obsolètes ou compromises après la désactivation d'un service.
* Utilisation de CDN externes non contrôlés pour charger des bibliothèques JavaScript critiques.

**Recommandations :**
* **Pour les administrateurs web :** Supprimer immédiatement toute référence aux scripts provenant de `polyfill.io` dans le code source de vos applications.
* **Pour les utilisateurs :** Ne jamais saisir d'identifiants dans une fenêtre de connexion inhabituelle ou surgissant de manière impromptue. Si des données ont été saisies, changer immédiatement de mot de passe sur le site concerné.

---
[Source](https://www.bleepingcomputer.com/news/security/suspicious-polyfill-login-prompts-pop-up-on-toshiba-muji-websites/){:target="_blank"}
