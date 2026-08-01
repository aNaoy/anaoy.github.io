---
title: 'Rails patches critical Active Storage flaw with RCE potential'
date: 2026-08-01
permalink: /posts/2026/08/01/rails-patches-critical-active-storage-flaw-with-rce-potential/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique RCE dans Rails Active Storage

Une faille de sécurité critique au sein du composant Active Storage de Rails permet à un attaquant non authentifié de lire des fichiers arbitraires sur un serveur, ouvrant la voie à une exécution de code à distance (RCE). Cette vulnérabilité concerne principalement les applications utilisant la bibliothèque de traitement d'image `libvips` pour générer des miniatures.

**Points clés :**
*   **Vecteur d'attaque :** L'envoi d'une image malveillante permet d'accéder aux secrets de l'application (clés de chiffrement, identifiants de base de données). Une fois la clé `secret_key_base` compromise, un attaquant peut usurper des sessions et obtenir un contrôle total (RCE) sur le serveur.
*   **Contexte :** `libvips` étant la bibliothèque par défaut dans les images Docker officielles de Rails et sur Debian/Ubuntu, l'exposition est large.
*   **Vulnérabilité :** CVE-2026-66066.
*   **Versions impactées :** Active Storage avant 7.2.3.2, 8.0.x avant 8.0.5.1, et 8.1.x avant 8.1.3.1. Rails 6.x est impacté sous réserve d'une configuration spécifique.

**Recommandations :**
*   **Mise à jour :** Appliquer immédiatement les correctifs de sécurité fournis par Rails.
*   **Sécurisation de `libvips` :** Mettre à jour vers la version 8.13 ou ultérieure. Pour les versions 8.13+, activer la protection temporaire via la variable d'environnement `VIPS_BLOCK_UNTRUSTED` ou la fonction `Vips.block_untrusted(true)`.
*   **Rotation des secrets :** En cas de compromission suspectée ou confirmée, renouveler impérativement la `secret_key_base`, ainsi que tous les identifiants de bases de données et services cloud accessibles par l'application.
*   **WAF :** Déployer des règles de pare-feu applicatif (WAF) pour filtrer les tentatives d'exploitation, bien que cette mesure ne soit que palliative.

---
[Source](https://www.bleepingcomputer.com/news/security/rails-patches-critical-active-storage-flaw-with-rce-potential/){:target="_blank"}
