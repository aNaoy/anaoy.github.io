---
title: 'Wikipedia hit by self-propagating JavaScript worm that vandalized pages'
date: 2026-03-06
permalink: /posts/2026/03/06/wikipedia-hit-by-self-propagating-javascript-worm-that-vandalized-pages/
tags:
- veille-cyber
- bleepingcomp
---
### Propagation d'un ver JavaScript sur Wikipédia

La Wikimedia Foundation a subi une attaque par un ver JavaScript auto-propagé ayant entraîné le vandalisme de près de 4 000 pages et la compromission des fichiers de scripts personnalisés d'environ 85 utilisateurs.

**Points clés :**
* **Origine :** L'incident a débuté par l'exécution d'un script malveillant (`test.js`) initialement hébergé sur Wikipédia en russe, potentiellement activé par erreur ou via un compte d'employé compromis lors de tests techniques.
* **Mécanisme :** Le ver exploitait les privilèges des utilisateurs connectés pour injecter des chargeurs malveillants dans les fichiers `common.js` individuels (persistance utilisateur) et dans le fichier `MediaWiki:Common.js` global (persistance sur le site).
* **Impact :** Une fois exécuté dans le navigateur d'un éditeur, le ver modifiait le fichier global, infectant ainsi tous les utilisateurs suivants, tout en vandalisant des pages aléatoires via l'insertion d'images et de code JavaScript masqué.
* **Réponse :** Les ingénieurs ont temporairement restreint les droits d'édition, annulé les modifications malveillantes et supprimé les scripts injectés pour restaurer l'intégrité du site.

**Vulnérabilités :**
* Absence de CVE spécifique identifiée ; il s'agit d'une exploitation de la logique des fonctionnalités de scripts personnalisés (MediaWiki) permettant une exécution de code arbitraire par des utilisateurs disposant de privilèges d'édition.

**Recommandations :**
* **Sécurisation des privilèges :** Restreindre strictement les accès en écriture sur les scripts globaux critiques (`MediaWiki:Common.js`) et limiter les permissions d'édition automatique.
* **Validation des scripts :** Implémenter une vérification stricte et un bac à sable (sandbox) pour l'exécution des scripts utilisateur afin d'empêcher toute injection de code côté client.
* **Audit des sessions :** Surveiller étroitement les modifications automatiques effectuées par des comptes privilégiés ou des scripts automatisés.

---
[Source](https://www.bleepingcomputer.com/news/security/wikipedia-hit-by-self-propagating-javascript-worm-that-vandalized-pages/){:target="_blank"}
