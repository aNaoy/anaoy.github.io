---
title: 'Critical Rails Flaw Could Let Unauthenticated Attackers Read Server Files via Image Uploads'
date: 2026-07-29
permalink: /posts/2026/07/29/critical-rails-flaw-could-let-unauthenticated-attackers-read-server-files-via-image-uploads/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans Ruby on Rails : Fuite de fichiers via Active Storage

Une faille critique découverte dans Ruby on Rails permet à des attaquants non authentifiés de lire des fichiers arbitraires sur les serveurs applicatifs via des téléchargements d'images malveillantes.

**Points clés :**
*   **Vulnérabilité :** CVE-2026-66066 (Score CVSS : 9.5).
*   **Cause :** Une mauvaise gestion des entrées utilisateur au sein d'Active Storage lors de l'utilisation de la bibliothèque de traitement d'images `libvips`. Rails permettait l'exécution d'opérations "non sécurisées" sur des fichiers non fiables.
*   **Impact :** Exposition de secrets critiques (`secret_key_base`, clés de chiffrement, mots de passe de bases de données, jetons API), pouvant mener à une exécution de code à distance (RCE) ou à des mouvements latéraux dans le réseau.
*   **Versions affectées :** Rails 6.0 à 8.1.3 (lorsque `libvips` est utilisé). Les applications utilisant `MiniMagick` ne sont pas exposées.

**Recommandations :**
*   **Mises à jour :** Passer immédiatement aux versions corrigées : **Rails 7.2.3.2, 8.0.5.1, ou 8.1.3.1**.
*   **Dépendances :** S'assurer que `libvips` est en version 8.13 ou supérieure et, le cas échéant, `ruby-vips` en version 2.2.1 ou supérieure.
*   **Rotation des secrets :** Étant donné qu'une compromission peut déjà avoir eu lieu, il est impératif de renouveler tous les secrets, clés de chiffrement, mots de passe de bases de données et jetons d'accès potentiellement exposés.
*   **Atténuation temporaire :** Si la mise à jour n'est pas immédiatement possible, configurer la variable d'environnement `VIPS_BLOCK_UNTRUSTED` ou appeler `Vips.block_untrusted(true)` dans le code pour bloquer les opérations risquées.

---
[Source](https://thehackernews.com/2026/07/critical-rails-flaw-could-let.html){:target="_blank"}
