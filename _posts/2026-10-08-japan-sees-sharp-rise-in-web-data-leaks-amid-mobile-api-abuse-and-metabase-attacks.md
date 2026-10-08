---
title: 'Japan Sees Sharp Rise in Web Data Leaks Amid Mobile API Abuse and Metabase Attacks'
date: 2026-10-08
permalink: /posts/2026/10/08/japan-sees-sharp-rise-in-web-data-leaks-amid-mobile-api-abuse-and-metabase-attacks/
tags:
- veille-cyber
- hackernews
---
### Recrudescence des fuites de données au Japon : Abus d'API et vulnérabilités logicielles

Le JPCERT/CC a alerté sur une augmentation significative des fuites de données personnelles au Japon, ciblant principalement des applications mobiles, des outils de Business Intelligence (BI) et des systèmes de gestion internes. Les attaques se sont intensifiées depuis juillet 2026.

#### Points clés
*   **Mode opératoire :** Les attaquants exploitent les failles des API (ingénierie inverse d'applications mobiles, injection NoSQL, accès non autorisé aux endpoints internes) et scannent les serveurs à la recherche de vulnérabilités connues ou de mauvaises configurations.
*   **Cible identifiée :** Le logiciel de BI **Metabase** est spécifiquement visé pour l'extraction de données.
*   **Étendue :** Plus de 80 incidents ont été recensés depuis juillet 2026, incluant des fuites massives chez des services de mobilité et de restauration.

#### Vulnérabilités majeures
*   **CVE-2026-72898 :** Faille d'injection SQL critique (score CVSS 10.0) dans Metabase permettant d'obtenir un accès administrateur sans authentification, menant à l'exportation de bases de données.

#### Recommandations de sécurité

**Pour les API :**
*   Appliquer des contrôles d'accès stricts sur **tous** les endpoints (publics et privés).
*   Mettre en place un *rate limiting* et des limites d'usage spécifiques sur les fonctions sensibles (login, recherche, réinitialisation de mot de passe).
*   Appliquer le principe du moindre privilège aux jetons API et utiliser des jetons à durée de vie limitée.
*   Ne jamais intégrer de clés API ou identifiants de base de données directement dans le code source des applications mobiles.

**Pour Metabase :**
*   Mettre à jour vers les versions correctives minimales préconisées (ex: 0.63.13, 0.62.16, etc.).
*   En cas d'impossibilité de mise à jour immédiate, bloquer temporairement l'accès à l'endpoint `/api/session/reset_password`.
*   En cas de compromission avérée : révoquer les sessions, purger les clés API, réinitialiser les identifiants de bases de données et auditer les journaux d'activité.

**Mesures générales :**
*   Auditer les journaux de logs à la recherche de pics de trafic, de réponses d'erreurs répétées (403/404/503) ou d'accès suspects aux fonctions d'administration.
*   Désactiver les fonctionnalités d'administration inutiles sur l'Internet public.
*   Limiter l'accès aux services par zone géographique lorsque cela est pertinent.

---
[Source](https://thehackernews.com/2026/10/japan-sees-sharp-rise-in-web-data-leaks.html){:target="_blank"}
