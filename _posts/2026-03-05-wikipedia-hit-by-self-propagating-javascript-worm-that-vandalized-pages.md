---
title: 'Wikipedia hit by self-propagating JavaScript worm that vandalized pages'
date: 2026-03-05
permalink: /posts/2026/03/05/wikipedia-hit-by-self-propagating-javascript-worm-that-vandalized-pages/
tags:
- veille-cyber
- bleepingcomp
---
### Propagation d'un ver JavaScript sur Wikipédia

La Wikimedia Foundation a subi une attaque par un ver JavaScript auto-réplicant ayant entraîné le vandalisme de près de 4 000 pages et la compromission des fichiers de configuration utilisateur (*common.js*) de 85 contributeurs. Le vecteur initial serait l'exécution accidentelle ou volontaire d'un script malveillant par un compte employé lors de tests de fonctionnalités.

**Points clés :**
*   **Mécanisme de propagation :** Le script exploite les permissions de l'utilisateur connecté pour modifier son fichier `common.js` (persistance utilisateur) et, si les privilèges le permettent, le fichier `MediaWiki:Common.js` (persistance globale).
*   **Comportement malveillant :** Une fois actif, le ver modifie aléatoirement des pages Wikipédia en y injectant une image et une charge utile JavaScript supplémentaire, permettant une diffusion virale à chaque chargement de page par un éditeur authentifié.
*   **Réponse :** Wikimedia a temporairement restreint les capacités d'édition, annulé les modifications malveillantes et restauré les fichiers *common.js* compromis.

**Vulnérabilités :**
*   Bien qu'aucune CVE spécifique ne soit mentionnée, l'incident repose sur une faille logique permettant l'exécution de code arbitraire via la manipulation des fichiers de configuration JavaScript MediaWiki (`common.js`), couplée à une élévation de privilèges via des comptes utilisateurs disposant de droits d'administration sur les scripts globaux.

**Recommandations :**
*   **Renforcement des permissions :** Restreindre strictement les capacités de modification des scripts système (MediaWiki:Common.js) aux seuls administrateurs système et mettre en œuvre une révision humaine obligatoire avant toute mise en production de scripts.
*   **Sandboxing :** Isoler l'environnement de test des scripts utilisateur de l'environnement de production pour éviter qu'un test ne déclenche une propagation globale.
*   **Surveillance :** Implémenter des alertes sur les modifications apportées aux fichiers de configuration critiques des utilisateurs et du site.

---
[Source](https://www.bleepingcomputer.com/news/security/wikipedia-hit-by-self-propagating-javascript-worm-that-vandalized-pages/){:target="_blank"}
