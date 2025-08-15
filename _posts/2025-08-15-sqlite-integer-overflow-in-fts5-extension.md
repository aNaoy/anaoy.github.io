---
title: 'SQLite - Integer Overflow in FTS5 Extension'
date: 2025-08-15
permalink: /posts/2025/08/15/sqlite-integer-overflow-in-fts5-extension/
tags:
- veille-cyber
- zerodaysfans
---
## Dépassement d'entier dans l'extension FTS5 de SQLite

Une vulnérabilité a été découverte dans l'extension FTS5 de SQLite, permettant potentiellement l'écriture hors limites de données partiellement contrôlées. Elle survient lors du calcul de la taille d'un tableau de pointeurs de "tombstones" (éléments supprimés), où la valeur est tronquée en un entier de 32 bits.

**Points Clés:**

*   La faille se situe dans la fonction `fts5SegIterAllocTombstone`.
*   La variable `nByte`, représentant la taille du tableau, est un entier signé de 32 bits.
*   Le calcul de `nByte` utilise une macro `SZ_FTS5TOMBSTONEARRAY` qui, bien qu'utilisant une multiplication sur 64 bits, tronque le résultat en 32 bits si la valeur dépasse 2^32 - 1.
*   La valeur `pIter->pSeg->nPgTombstone`, qui contrôle la taille effective du tableau de "tombstones", est entièrement sous le contrôle de l'attaquant.
*   Lorsque `nByte` est insuffisant pour contenir le nombre de "tombstones" spécifié par `nPgTombstone`, l'accès au tableau via un index calculé (par exemple, dans `fts5MultiIterIsDeleted`) peut dépasser les limites allouées.
*   Si l'entrée à l'index hors limites est nulle, une structure est allouée et un pointeur vers celle-ci est écrit hors limites.

**Vulnérabilités:**

*   <strong>Dépassement d'entier (Integer Overflow)</strong> dans le calcul de l'allocation mémoire pour les "tombstones" de l'extension FTS5.
*   Aucun identifiant CVE spécifique n'est mentionné dans l'article.

**Gravité:**

*   Modérée. La vulnérabilité peut être exploitée par un attaquant capable d'exécuter des requêtes arbitraires ou de faire traiter une base de données SQLite contrôlée par une application vulnérable.

**Recommandations:**

*   Appliquer le correctif disponible à l'adresse : `https://sqlite.org/src/info/63595b74956a9391`.

**Chronologie:**

*   Rapportée le : 15/07/2025
*   Corrigée le : 16/07/2025
*   Divulguée le : 15/08/2025

---
[Source](https://github.com/google/security-research/security/advisories/GHSA-v2c8-vqqp-hv3g){:target="_blank"}
