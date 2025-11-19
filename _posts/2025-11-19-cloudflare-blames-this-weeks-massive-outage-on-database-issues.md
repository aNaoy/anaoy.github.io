---
title: 'Cloudflare blames this weeks massive outage on database issues'
date: 2025-11-19
permalink: /posts/2025/11/19/cloudflare-blames-this-weeks-massive-outage-on-database-issues/
tags:
- veille-cyber
- bleepingcomp
---
**Incident Cloudflare : Un dysfonctionnement de base de données**

Un changement apporté aux autorisations d'accès à une base de données a déclenché une défaillance en cascade sur le réseau mondial de Cloudflare, entraînant une interruption majeure des services pendant près de six heures. Cet incident, le plus grave de l'entreprise en six ans, n'a pas été causé par une cyberattaque.

Les modifications des permissions ont conduit à une augmentation excessive d'un fichier de configuration utilisé par le système de gestion des bots de Cloudflare. Ce fichier, en raison de doublons générés par une requête de base de données, a dépassé les limites intégrées du système, provoquant le crash du logiciel de routage du trafic. La propagation de ce fichier volumineux a également déclenché des erreurs système et des pannes du système proxy principal.

L'incident a impacté les services essentiels de Cloudflare tels que le CDN, la sécurité, Turnstile, Workers KV, l'accès au tableau de bord, la sécurité de la messagerie et l'authentification. Les systèmes ont été rétablis après que les ingénieurs aient identifié la cause et remplacé le fichier problématique par une version antérieure.

**Points clés :**

*   Interruption massive des services Cloudflare due à un changement de configuration de base de données.
*   Aucune cyberattaque n'est à l'origine de l'incident.
*   Défaillance causée par un fichier de configuration surdimensionné généré par le système de gestion des bots.
*   Impact sur de nombreux services Cloudflare et sur l'accès à des sites web et plateformes en ligne.

**Vulnérabilités :**

*   Les changements de permissions dans les bases de données peuvent avoir des conséquences imprévues et systémiques.
*   Les limites de taille hardcodées dans les systèmes logiciels peuvent être dépassées, entraînant des plantages.
*   La propagation de fichiers de configuration erronés à travers un réseau distribué peut causer des pannes généralisées.

**Recommandations :**

*   Mettre en place des processus de vérification et de validation rigoureux pour les changements de configuration des bases de données et des systèmes critiques.
*   Tester minutieusement les modifications dans des environnements de préproduction avant leur déploiement en production.
*   Améliorer la gestion des limites de taille des fichiers de configuration et prévoir des mécanismes de détection et de prévention des dépassements.
*   Établir des procédures de retour arrière rapides et efficaces en cas de détection de problèmes post-déploiement.

---
[Source](https://www.bleepingcomputer.com/news/technology/cloudflare-blames-this-weeks-massive-outage-on-database-issues/){:target="_blank"}
