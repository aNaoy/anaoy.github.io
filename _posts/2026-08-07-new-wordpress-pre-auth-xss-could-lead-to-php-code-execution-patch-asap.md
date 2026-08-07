---
title: 'New WordPress Pre-Auth XSS Could Lead to PHP Code Execution - Patch ASAP'
date: 2026-08-07
permalink: /posts/2026/08/07/new-wordpress-pre-auth-xss-could-lead-to-php-code-execution-patch-asap/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique "XSS2Shell" dans WordPress

Une faille de type Cross-Site Scripting (XSS) réfléchi, pré-authentification, affecte l'écran de connexion de WordPress. Bien que l'injection XSS soit accessible sans privilèges, elle peut être exploitée de manière chaînée pour atteindre une exécution de code à distance (RCE) sur le serveur.

**Points clés :**
*   **Vulnérabilité identifiée :** CVE-2026-64638 (Score CVSS : 8.9).
*   **Mécanisme :** Une faille dans le traitement des erreurs de connexion permet d'injecter des éléments DOM malveillants via le champ identifiant. Ces éléments détournent les scripts de gestion de profil de WordPress pour effectuer des requêtes REST authentifiées à l'insu d'un administrateur connecté.
*   **Impact RCE :** En incitant un administrateur à interagir avec une page contrôlée par l'attaquant, celui-ci peut générer des mots de passe d'application, installer des extensions malveillantes (ZIP) ou exécuter du code PHP arbitraire avec les privilèges du serveur.
*   **Technique :** L'attaque, nommée "XSS2Shell", utilise une variante de la méthode *Same Origin Method Execution* (SOME) et contourne certaines mesures de sécurité comme le CSP (Content Security Policy).

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer la mise à jour vers la version **7.0.3** ou ultérieure.
*   **Backports :** Les versions de la branche 4.7 et supérieures bénéficient également d'un correctif.
*   **Importance :** Ne pas se reposer sur les mesures de durcissement (hardening) existantes, car elles ne bloquent pas le vecteur d'attaque XSS sous-jacent. Le déploiement du correctif officiel est indispensable.

---
[Source](https://thehackernews.com/2026/08/new-wordpress-pre-auth-xss-could-lead.html){:target="_blank"}
