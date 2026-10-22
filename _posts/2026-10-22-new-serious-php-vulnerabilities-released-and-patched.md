---
title: 'New Serious PHP Vulnerabilities Released and Patched'
date: 2026-10-22
permalink: /posts/2026/10/22/new-serious-php-vulnerabilities-released-and-patched/
tags:
- veille-cyber
- schneier
---
### Vulnérabilités critiques de RCE dans PHP : Mise à jour urgente requise

Les responsables de PHP ont publié des correctifs pour deux vulnérabilités critiques permettant l'exécution de code à distance (RCE) sans authentification. Toutes les installations traitant des requêtes web (PHP-FPM, Apache mod_php, php-cgi, FrankenPHP et LiteSpeed) sont concernées, avec une exposition maximale pour les configurations utilisant `mod_php`.

**Vulnérabilités identifiées :**
*   **CVE-2026-109618 (RCE via corruption OOM) :** Une gestion défaillante de la mémoire (out-of-memory) interrompt PHP pendant l'initialisation des données de requête, conduisant au traitement de données invalides lors du nettoyage.
*   **CVE-2026-109619 (RCE via état global obsolète) :** Persistance d'un état interne après libération de la mémoire, permettant à une requête ultérieure traitée par le même processus de manipuler ces données avant réinitialisation.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer sans délai les versions corrigées : PHP 8.5.12, 8.4.27, 8.3.36 ou 8.2.35.
*   **Action requise :** La mise à jour logicielle est l'unique mesure de remédiation efficace pour corriger ces failles.

---
[Source](https://www.schneier.com/blog/archives/2026/10/new-serious-php-vulnerabilities-released-and-patched.html){:target="_blank"}
