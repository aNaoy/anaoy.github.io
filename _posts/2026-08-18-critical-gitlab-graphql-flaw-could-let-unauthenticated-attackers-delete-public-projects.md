---
title: 'Critical GitLab GraphQL Flaw Could Let Unauthenticated Attackers Delete Public Projects'
date: 2026-08-18
permalink: /posts/2026/08/18/critical-gitlab-graphql-flaw-could-let-unauthenticated-attackers-delete-public-projects/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans l'interface GraphQL de GitLab

GitLab a publié des correctifs urgents pour corriger deux failles de sécurité affectant ses instances auto-hébergées (Community et Enterprise Edition). Ces vulnérabilités permettent à des attaquants non authentifiés d'interagir avec les serveurs via des requêtes GraphQL.

**Points clés :**
* Les services GitLab.com et GitLab Dedicated sont déjà protégés et ne nécessitent aucune intervention.
* Les correctifs concernent exclusivement les installations auto-hébergées.
* Aucune preuve d'exploitation active n'a été signalée à ce jour.
* Les détails techniques complets seront rendus publics par GitLab environ 90 jours après le correctif.

**Vulnérabilités :**
* **CVE-2026-19478 (Score CVSS : 9.4 - Critique) :** Une faille dans une directive GraphQL permettant à un attaquant non authentifié de modifier ou de supprimer à distance des projets publics et des données utilisateur sans aucune interaction de la victime.
* **CVE-2026-19650 (Score CVSS : 7.1 - Élevée) :** Une vulnérabilité de type CSRF (Cross-Site Request Forgery) liée à une mauvaise validation des requêtes dans le gestionnaire GraphQL, permettant l'exécution de mutations via des requêtes GET (nécessite une interaction utilisateur).

**Recommandations :**
* Mettre immédiatement à jour les instances auto-hébergées vers les versions corrigées suivantes :
    * **19.2.4**
    * **19.1.6**
    * **19.0.8**
    * **18.11.11**
* Vérifier la version actuelle du déploiement, car les branches 18.2 à 18.10 ne sont pas supportées par ces correctifs et restent vulnérables.
* L'installation des correctifs ne nécessite pas de migrations et ne devrait pas entraîner d'interruption de service pour les déploiements multi-nœuds.

---
[Source](https://thehackernews.com/2026/08/critical-gitlab-graphql-flaw-could-let.html){:target="_blank"}
