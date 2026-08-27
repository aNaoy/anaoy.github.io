---
title: 'A polymorphic phishing page (that occasionally breaks itself), (Thu, Aug 27th)'
date: 2026-08-27
permalink: /posts/2026/08/27/a-polymorphic-phishing-page-that-occasionally-breaks-itself-thu-aug-27th/
tags:
- veille-cyber
- sans-isc
---
### Analyse d'une campagne de phishing polymorphe défaillante

Une campagne de phishing récente a révélé l'utilisation d'un mécanisme de polymorphisme générant des variantes uniques de pages de vol d'identifiants à chaque requête. Bien que cette technique vise à contourner les signatures statiques, des erreurs de programmation dans l'obfuscation JavaScript rendent parfois les pages inopérantes.

**Points clés :**
* **Polymorphisme dynamique :** Chaque accès à l'URL génère un code source distinct (noms de variables, ordre des fonctions, constantes, titres de page), rendant les signatures basées sur le hash ou les chaînes de caractères inefficaces.
* **Erreur d'implémentation :** L'obfuscateur utilise des variables globales non déclarées (ex: `k`) comme compteurs de boucle. Lorsqu'une fonction imbriquée utilise la même variable, elle réinitialise le compteur de la boucle parente, provoquant une boucle infinie.
* **Impact sur la cible :** Le dysfonctionnement entraîne un blocage du navigateur et une saturation du processeur, empêchant le rendu de la page de phishing. Environ 4 % des échantillons testés étaient corrompus.
* **Origine probable :** L'analyse suggère un moteur d'obfuscation classique plutôt qu'une IA générative, en raison du caractère systématique des erreurs et des transformations.

**Vulnérabilités :**
* **Fuite de portée (Variable Scope) :** L'utilisation de variables globales (`k`) dans des boucles imbriquées sans déclaration locale (`let` ou `var`) crée des collisions logiques.
* **Dépendance aux signatures statiques :** La surveillance repose trop souvent sur des artefacts figés (hash, structure), vulnérables aux techniques de mutation automatique.

**Recommandations :**
* **Détection comportementale :** Privilégier l'analyse comportementale (URL, redirection, appels API, interactions de formulaires) plutôt que l'analyse statique du code source, inefficace face au polymorphisme.
* **Analyse de performance :** Surveiller les processus navigateurs consommant anormalement les ressources CPU lors de l'accès à des sites suspects, car cela peut révéler des scripts de déchiffrement en échec.
* **Bonnes pratiques de développement :** Pour les développeurs, le respect strict de la portée des variables est essentiel ; l'utilisation de `use strict` en JavaScript aurait permis de détecter immédiatement ces erreurs de déclaration globale.

---
[Source](https://isc.sans.edu/diary/rss/33290){:target="_blank"}
