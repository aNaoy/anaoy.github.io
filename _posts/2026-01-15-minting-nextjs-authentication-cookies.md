---
title: 'Minting Next.js Authentication Cookies'
date: 2026-01-15
permalink: /posts/2026/01/15/minting-nextjs-authentication-cookies/
tags:
- veille-cyber
- zerodaysfans
---
### Exploitation des Cookies d'Authentification Next.js

Une faille de sécurité potentielle dans les applications Next.js utilisant la bibliothèque `next-auth` (ou `Auth.js`) permet à un attaquant de créer de faux cookies d'authentification, lui accordant ainsi un accès persistant en tant que n'importe quel utilisateur.

Cette vulnérabilité peut être exploitée en combinaison avec la faille `React2Shell` (CVE-2025-55182), une vulnérabilité de désérialisation permettant l'exécution de code arbitraire. L'exploitation de `React2Shell` peut permettre à un attaquant de récupérer des informations sensibles, telles que les `client_id` et `client_secret` OAuth, et surtout, le `NEXTAUTH_SECRET` (ou `AUTH_SECRET` dans les versions récentes).

Ce `NEXTAUTH_SECRET` est le seul élément nécessaire pour qu'un attaquant puisse signer et créer des cookies de session `next-auth` valides. Le processus de création de ces cookies utilise le nom du cookie comme valeur de sel, et la clé de chiffrement est dérivée du `NEXTAUTH_SECRET` via la fonction `HKDF`.

**Points Clés :**

*   Une faille `React2Shell` peut conduire à la révélation du `NEXTAUTH_SECRET`.
*   Le `NEXTAUTH_SECRET` est suffisant pour permettre à un attaquant de créer des cookies d'authentification pour n'importe quel utilisateur.
*   Cela permet un accès persistant à l'application sans avoir besoin de se connecter via les méthodes d'authentification traditionnelles.

**Vulnérabilités :**

*   **CVE-2025-55182** : `React2Shell` (une vulnérabilité de désérialisation).

**Recommandations :**

*   **Rotation régulière des secrets :** Il est impératif de faire pivoter régulièrement le `NEXTAUTH_SECRET` (ou `AUTH_SECRET`). Cette rotation devrait être automatisée pour plus de fiabilité.
*   **Surveillance des sessions :** Mettre en place des mécanismes de détection pour repérer les anomalies, tels que :
    *   Journalisation de l'identifiant JWT par session et alerte en cas de doublons provenant d'adresses IP différentes.
    *   Détection des déplacements impossibles (changements de localisation géographiques irréalistes).
    *   Surveillance des sessions sans événements de connexion correspondants dans les journaux d'authentification.
    *   Alertes sur les accès en dehors des heures ouvrables ou les chaînes d'agent utilisateur inhabituelles.

Même si les identifiants OAuth sont sécurisés et régulièrement changés, laisser le `NEXTAUTH_SECRET` inchangé constitue une porte dérobée durable.

---
[Source](https://embracethered.com/blog/posts/2026/minting-next-auth-nextjs-auth-cookies-react2shell-threat/){:target="_blank"}
