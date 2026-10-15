---
title: 'Measuring Human Cryptanalysis Effort'
date: 2026-10-15
permalink: /posts/2026/10/15/measuring-human-cryptanalysis-effort/
tags:
- veille-cyber
- schneier
---
### Évaluer l'effort humain en cryptanalyse

Une nouvelle étude menée sous la direction de Matthew Green propose une méthodologie pour quantifier l'effort de recherche consacré à la cryptanalyse des algorithmes à clé publique. En s'appuyant sur l'analyse automatisée (via les modèles Claude et GPT) de près de 16 000 publications scientifiques, cette initiative tente d'estimer le volume d'heures-hommes investi dans l'étude de différentes primitives cryptographiques.

**Points clés :**
*   **Méthodologie :** Conversion du nombre d'articles de recherche en années-hommes de travail, en utilisant une cartographie des auteurs pour pondérer les contributions.
*   **Évolution des tendances :** Les algorithmes basés sur les réseaux (lattices) ont récemment dépassé les courbes elliptiques (ECDLP) en termes de cumul d'efforts de recherche.
*   **Limites de l'étude :** La mesure est basée uniquement sur la littérature académique publiée. Elle ne prend pas en compte les travaux cryptanalytiques confidentiels (agences de renseignement) ou les recherches académiques n'ayant pas abouti à une publication.
*   **Automatisation :** Le pipeline d'analyse et la rédaction ont été largement délégués à des modèles d'IA, supervisés par une méthodologie humaine.

**Vulnérabilités et recommandations :**
*   **Vulnérabilités :** L'article ne traite pas de vulnérabilités logicielles spécifiques (pas de CVE identifiée). Il se concentre sur la résilience théorique des primitives cryptographiques face à l'effort de recherche global.
*   **Recommandations :** Bien que cette étude soit une première tentative utile pour mesurer la maturité d'un algorithme, elle ne doit pas être utilisée comme preuve absolue de sécurité. Les organisations doivent continuer à privilégier les algorithmes ayant fait l'objet d'un examen public approfondi sur une longue période, tout en restant conscientes que l'absence de recherche publiée ne garantit pas l'absence d'attaques secrètes.

---
[Source](https://www.schneier.com/blog/archives/2026/10/measuring-human-cryptanalysis-effort.html){:target="_blank"}
