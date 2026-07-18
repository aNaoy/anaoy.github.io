---
title: 'New wp2shell WordPress Core Flaw Lets Unauthenticated Attackers Run Code'
date: 2026-07-18
permalink: /posts/2026/07/18/new-wp2shell-wordpress-core-flaw-lets-unauthenticated-attackers-run-code/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique "wp2shell" dans le cœur de WordPress

Une faille de sécurité majeure, baptisée **wp2shell**, permet à un attaquant non authentifié d'exécuter du code arbitraire (RCE) sur une installation WordPress standard, sans plugin requis. La vulnérabilité repose sur le chaînage de deux failles distinctes.

**Points clés :**
*   **Mécanisme :** L'attaque combine une confusion de route dans l'API REST (`/wp-json/batch/v1`) et une injection SQL dans `WP_Query`.
*   **Impact :** Un attaquant peut exécuter du code à distance. L'exploitation est facilitée par la disponibilité publique d'un PoC (Proof-of-Concept) sur GitHub.
*   **Portée :** Les versions 6.9.x et 7.0.x sont vulnérables à la chaîne complète RCE. Les versions 6.8.x sont uniquement exposées à l'injection SQL.
*   **Atténuation naturelle :** Les sites utilisant un cache d'objets persistant (type Redis ou Memcached) pourraient être épargnés par le vecteur d'exécution de code, mais restent vulnérables à l'injection SQL.

**Vulnérabilités identifiées :**
*   **CVE-2026-63030 :** Confusion de route par lot (batch-route) dans l'API REST.
*   **CVE-2026-60137 :** Injection SQL dans le cœur de WordPress.

**Recommandations :**
1.  **Mise à jour immédiate :** Appliquer les correctifs WordPress versions **6.8.6, 6.9.5 ou 7.0.2** selon votre branche actuelle. Vérifiez manuellement que la mise à jour automatique a bien été effectuée.
2.  **Filtrage WAF :** En attendant la mise à jour, bloquez les accès aux routes `/wp-json/batch/v1` et `rest_route=/batch/v1` via votre pare-feu applicatif.
3.  **Mesures d'urgence :** Désactiver l'API REST pour les utilisateurs non authentifiés ou installer un plugin de sécurité bloquant les requêtes anonymes vers le endpoint `/batch/v1`.
4.  **Vérification :** Utiliser des outils de scan pour identifier si votre site est vulnérable, bien que la priorité absolue demeure l'installation du correctif officiel.

---
[Source](https://thehackernews.com/2026/07/new-wp2shell-wordpress-core-flaw-lets.html){:target="_blank"}
