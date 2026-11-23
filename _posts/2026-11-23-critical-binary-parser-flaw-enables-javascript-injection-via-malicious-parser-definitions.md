---
title: 'Critical binary-parser Flaw Enables JavaScript Injection via Malicious Parser Definitions'
date: 2026-11-23
permalink: /posts/2026/11/23/critical-binary-parser-flaw-enables-javascript-injection-via-malicious-parser-definitions/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'injection JavaScript dans binary-parser

La bibliothèque Node.js `binary-parser` est touchée par une vulnérabilité critique permettant l'exécution de code arbitraire. Cette faille survient lorsque des options de définition de parseur, contrôlées par l'utilisateur, sont injectées sans validation préalable dans le code JavaScript généré lors de la compilation du parseur.

**Points clés :**
*   **Impact :** Un attaquant peut exécuter du code JavaScript malveillant au sein du processus Node.js hôte.
*   **Vecteurs d'attaque :** L'injection est possible via des paramètres spécifiques malveillants, notamment `length`, `lengthInBytes`, `key`, `tag`, `offset`, ainsi que l'alias utilisé dans `namely()`.
*   **Contexte :** Cette vulnérabilité est considérée comme une correction incomplète d'une faille précédente (CVE-2026-1245).

**Vulnérabilité :**
*   **CVE-2026-134814 :** Score CVSS de 9.2 (critique). Concerne toutes les versions de `binary-parser` antérieures à la 2.3.1.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version 2.3.1 ou supérieure de la bibliothèque.
*   **Validation des entrées :** Les options de parseur doivent désormais être conformes au format d'identifiants (ex: `foo`, `$parent.len`). Les expressions complexes (ex: `len - 1`) sont désormais rejetées et doivent être remplacées par des fonctions.
*   **Sécurisation :** Bien que l'analyse de données binaires non fiables avec une définition de parseur sécurisée reste sûre, il est impératif de s'assurer que les définitions elles-mêmes proviennent de sources de confiance.

---
[Source](https://thehackernews.com/2026/11/critical-binary-parser-flaw-enables.html){:target="_blank"}
