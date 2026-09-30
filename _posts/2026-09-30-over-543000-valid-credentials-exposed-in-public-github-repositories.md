---
title: 'Over 543,000 valid credentials exposed in public GitHub repositories'
date: 2026-09-30
permalink: /posts/2026/09/30/over-543000-valid-credentials-exposed-in-public-github-repositories/
tags:
- veille-cyber
- bleepingcomp
---
### Plus de 543 000 identifiants valides exposés sur GitHub

Une analyse menée par Truffle Security sur 224 millions de dépôts GitHub a révélé l'existence de plus de 543 000 identifiants (clés API, jetons d'accès, chaînes de connexion) toujours actifs et publiquement accessibles. Cette exposition persistante concerne des secrets parfois vieux de plus de six ans, avec une densité de fuites en constante augmentation malgré les mesures de protection de la plateforme.

**Points clés :**
*   **Volume massif :** 543 699 identifiants uniques ont été identifiés dans plus de 1,1 million de fichiers.
*   **Persistance :** La durée de vie médiane d'un identifiant exposé est de 784 jours.
*   **Limites de la protection :** Bien que l'outil « Push Protection » de GitHub réduise les fuites dans les catégories qu'il couvre (baisse de 53 %), plus de 51 % des secrets exposés appartiennent à des types non pris en charge, comme les chaînes de connexion à des bases de données ou certains jetons Google API.
*   **Inégalité de révocation :** La réactivité varie selon les services ; par exemple, presque tous les jetons `npm` exposés ont été invalidés, tandis qu'une majorité de comptes de service Google Cloud sont restés opérationnels.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, car il s'agit d'une problématique de **fuite de secrets (Secret Sprawl)** liée à des erreurs humaines lors de la gestion des dépôts de code source et non d'une faille logicielle intrinsèque.

**Recommandations :**
*   **Rotation immédiate :** Révoquer et renouveler systématiquement tout identifiant ayant été exposé dans un dépôt public, même temporairement.
*   **Nettoyage de l'historique :** Assainir les dépôts en supprimant les secrets de l'historique des commits, et non seulement des fichiers actuels.
*   **Expiration automatique :** Mettre en œuvre des durées de vie limitées pour tous les secrets et jetons d'accès.
*   **Audit continu :** Utiliser des outils de détection automatisée pour scanner régulièrement les dépôts de code à la recherche de secrets avant et après chaque déploiement.

---
[Source](https://www.bleepingcomputer.com/news/security/over-543-000-valid-credentials-exposed-in-public-github-repositories/){:target="_blank"}
