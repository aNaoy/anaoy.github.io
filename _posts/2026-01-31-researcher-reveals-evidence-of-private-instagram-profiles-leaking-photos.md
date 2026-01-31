---
title: 'Researcher reveals evidence of private Instagram profiles leaking photos'
date: 2026-01-31
permalink: /posts/2026/01/31/researcher-reveals-evidence-of-private-instagram-profiles-leaking-photos/
tags:
- veille-cyber
- bleepingcomp
---
## Fuite de photos sur Instagram : des profils privés exposés

Un chercheur en cybersécurité a découvert que des photos issues de certains profils privés Instagram étaient accessibles aux visiteurs non authentifiés. Le mécanisme de confidentialité de la plateforme, censé limiter l'accès aux abonnés approuvés, a échoué dans certains cas, intégrant des liens vers ces contenus privés directement dans les réponses des serveurs.

Meta a corrigé le problème après le rapport initial, mais l'a ensuite qualifié de "non applicable", affirmant ne plus pouvoir reproduire la vulnérabilité.

**Points clés :**

*   Des liens vers des photos privées et leurs légendes étaient incorporés dans le corps des réponses HTML pour des profils privés, lorsqu'ils étaient accédés depuis certains appareils mobiles par des utilisateurs non connectés.
*   Une preuve de concept vidéo a été partagée pour démontrer la fuite de données.
*   Le chercheur a constaté qu'environ 28 % des comptes privés testés présentaient cette faille.
*   Meta a été informé en octobre 2025. Le chercheur soutient qu'il ne s'agissait pas d'un problème de mise en cache CDN, mais d'un échec d'autorisation côté serveur.
*   Bien que l'exploitation ait cessé quelques jours après le rapport, Meta a clos le cas sans fournir d'analyse des causes profondes, soulevant des inquiétudes quant à la résolution complète du problème.

**Vulnérabilités :**

*   Pas de CVE spécifique mentionné dans l'article. La vulnérabilité peut être décrite comme une *exposition d'informations privées due à un manque de vérification d'autorisation côté serveur*.

**Recommandations :**

*   Les plateformes de réseaux sociaux doivent impérativement s'assurer que les mécanismes de contrôle d'accès et d'autorisation sont robustes et appliqués correctement côté serveur pour protéger le contenu privé des utilisateurs.
*   Une communication transparente et une enquête approfondie des causes profondes sont essentielles lors de la gestion des rapports de vulnérabilités, même si le problème semble résolu.

---
[Source](https://www.bleepingcomputer.com/news/security/researcher-reveals-evidence-of-private-instagram-profiles-leaking-photos/){:target="_blank"}
