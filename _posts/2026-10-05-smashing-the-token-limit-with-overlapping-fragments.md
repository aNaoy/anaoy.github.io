---
title: 'Smashing the token limit with overlapping fragments'
date: 2026-10-05
permalink: /posts/2026/10/05/smashing-the-token-limit-with-overlapping-fragments/
tags:
- veille-cyber
- zerodaysfans
---
### Exfiltration de jetons par injection CSS : La méthode des fragments superposés

Cette recherche démontre qu'il est possible d'exfiltrer des jetons (tokens) de plusieurs centaines de caractères via une injection CSS, sans recourir au chargement récursif de feuilles de style. En décomposant le jeton cible en courts fragments chevauchants, un attaquant peut reconstituer la chaîne complète à partir des rapports de présence de ces segments, utilisant la théorie des graphes pour assembler les morceaux dans l'ordre.

**Points clés :**
* **Efficacité accrue :** Contrairement aux méthodes précédentes nécessitant des gigaoctets de CSS pour quelques caractères, cette technique permet d'extraire des jetons de 210 à 640 caractères avec un budget CSS nettement plus contenu.
* **Reconstruction logique :** Le script de reconstruction traite les fragments isolés comme des vecteurs dans un graphe. Les chevauchements (ex: `c2e` suivi de `2e1`) permettent de tracer le cheminement logique du jeton.
* **Optimisation des requêtes :** L'utilisation de fragments de tailles variables (2, 3, 4, 5 ou 6 caractères) permet d'optimiser le nombre de règles CSS nécessaires tout en conservant une précision statistique élevée (jusqu'à 99% de réussite).

**Vulnérabilités :**
* **Injection CSS (Exploitation de canaux auxiliaires) :** La vulnérabilité réside dans la capacité d'un attaquant à injecter du CSS arbitraire pour tester la présence de caractères dans des éléments sensibles (jetons CSRF, clés API, etc.). Cette recherche montre que la limite théorique de longueur de l'exfiltration est bien plus élevée qu'estimé précédemment. Aucune CVE n'est associée, car il s'agit d'une technique d'exploitation de failles de conception (CSS Injection).

**Recommandations :**
* **Désinfection des entrées :** Assainir strictement les entrées utilisateur reflétées dans le DOM ou dans des attributs HTML pouvant être ciblés par des sélecteurs CSS.
* **Content Security Policy (CSP) :** Implémenter une politique CSP rigoureuse interdisant le chargement de feuilles de style provenant de domaines non approuvés ou empêchant l'injection de styles en ligne.
* **Protection des jetons :** S'assurer que les jetons sensibles ne sont pas exposés dans des parties du DOM facilement accessibles via des sélecteurs CSS (attributs `value`, `href`, `data-*`, etc.).
* **Outils de test :** Utiliser des outils automatisés comme *Burp AT* pour identifier si une application est vulnérable à l'exfiltration par injection CSS et valider l'exposition réelle des jetons.

---
[Source](https://portswigger.net/research/smashing-the-token-limit){:target="_blank"}
