---
title: 'New Attack Against RSA'
date: 2026-09-28
permalink: /posts/2026/09/28/new-attack-against-rsa/
tags:
- veille-cyber
- schneier
---
### Vulnérabilité majeure : Attaque par falsification de signatures RSA

Une nouvelle implémentation d'une technique de cryptanalyse datant de 2007 permet de falsifier des signatures numériques RSA sans avoir à factoriser la clé privée. Bien que cette méthode soit plus rapide que les approches classiques, elle reste complexe et limitée dans son application pratique.

**Points clés :**
* **Nature de l'attaque :** Il s'agit d'une attaque par falsification de signature et non d'une méthode de récupération de clé privée.
* **Complexité :** L'algorithme est de nature sous-exponentielle. La falsification d'une signature RSA 1024-bit nécessite des ressources de calcul massives (1380 années-cœur de CPU, soit environ cinq mois de calcul intensif).
* **Contexte restreint :** La vulnérabilité ne concerne que les signatures "pures", c'est-à-dire celles dépourvues de mécanismes de formatage ou de remplissage (padding).

**Vulnérabilités :**
* Aucune CVE n'est associée à cette découverte, car il s'agit d'une avancée académique portant sur les fondements mathématiques de l'algorithme RSA plutôt que sur une faille logicielle spécifique.

**Recommandations :**
* **Utiliser des standards de padding :** Le risque est nul pour les implémentations RSA modernes qui utilisent des méthodes de remplissage standardisées (comme PKCS#1 v1.5 ou PSS).
* **Transition cryptographique :** Bien que cette attaque spécifique soit limitée, elle souligne l'importance de migrer progressivement vers des algorithmes cryptographiques plus robustes face aux évolutions de la puissance de calcul.

---
[Source](https://www.schneier.com/blog/archives/2026/09/new-attack-against-rsa.html){:target="_blank"}
