---
title: 'Probabilistic analysis of MTE tagging schemes'
date: 2026-10-01
permalink: /posts/2026/10/01/probabilistic-analysis-of-mte-tagging-schemes/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse probabiliste des mécanismes de marquage MTE

L'extension de marquage de mémoire (MTE) d'ARM sécurise la gestion mémoire en associant des étiquettes (tags) aux pointeurs et aux granules de mémoire. Lorsqu'un pointeur est déréférencé, ses tags doivent correspondre ; dans le cas contraire, une erreur est générée. L'implémentation actuelle au sein de `hardened_malloc` utilise une sélection aléatoire de tags tout en excluant le tag précédent et ceux des voisins directs pour maximiser les chances de détection des accès après libération (UAF) et des débordements.

#### Points clés
* **Modèle probabiliste :** Avec 15 tags disponibles (le `0` étant réservé), la stratégie aléatoire actuelle offre une probabilité de collision (évasion de sécurité) comprise entre **7,1 % et 8,3 %** à chaque réutilisation.
* **Risque de cyclicité :** L'implémentation d'un schéma cyclique (incrémenter le tag à chaque réutilisation) garantit l'absence de collision à court terme, mais conduit à une certitude de collision (100 %) au bout de 13 à 15 cycles, selon les contraintes de voisinage.
* **Complexité vs Sécurité :** Bien qu'un schéma hybride (cyclique temporaire) semble séduisant, il augmente la complexité du code sans apporter de gain substantiel pour les applications à longue durée de vie, où un attaquant peut manipuler le taux de recyclage.
* **Comparaison des méthodes :** Les schémas alternatifs, comme l'alternance pair/impair, augmentent mathématiquement la probabilité de collision (jusqu'à 16,2 %) par rapport à la méthode aléatoire basée sur l'exclusion du tag précédent.

#### Vulnérabilités
* **Utilisation après libération (Use-After-Free) :** Bien que MTE aide à la détection, une probabilité non nulle d'évasion subsiste. Le risque est lié à la réutilisation des tags sur des objets ayant la même adresse mémoire.
* **Débordements linéaires :** Les débordements sont neutralisés par l'exclusion des tags des voisins directs, garantissant une détection déterministe tant que les tags des objets adjacents sont distincts.

#### Recommandations
* **Privilégier l'aléatoire :** Le maintien d'un schéma de sélection aléatoire (excluant uniquement le tag précédent et les voisins immédiats) reste supérieur au schéma cyclique ou à l'alternance pair/impair, car il évite la prédictibilité absolue des collisions à long terme.
* **Gestion du cycle de vie :** Le maintien d'une liste d'exclusion (précédent, voisins, tag 0) demeure la mesure de protection la plus robuste pour limiter les risques de collisions accidentelles tout en maintenant une performance élevée.

---
[Source](https://dustri.org/b/probabilistic-analysis-of-mte-tagging-schemes.html){:target="_blank"}
