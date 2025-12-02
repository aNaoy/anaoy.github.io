---
title: 'Solving Turb0’s XSS challenge using recursive object attributes'
date: 2025-12-02
permalink: /posts/2025/12/02/solving-turb0s-xss-challenge-using-recursive-object-attributes/
tags:
- veille-cyber
- zerodaysfans
---
Voici un résumé du contenu de l'article :

**Exploiter une faille XSS via une assignation d'attribut récursive**

Le challenge de cybersécurité proposé tourne autour d'une page web intégrant des bibliothèques Lodash et jQuery, ainsi qu'un script personnalisé. La page est protégée par une politique de sécurité de contenu (CSP) qui autorise l'évaluation de scripts (`'unsafe-eval'`). Le script principal écoute les messages envoyés via `postMessage`, traite un objet `data` contenant `base` et `mappings`. Il utilise Lodash (`_.get`) pour récupérer des valeurs à partir de l'objet `event` et les assigne à `base.reqBody[to]`. Le résultat est ensuite envoyé via une requête `POST` à une API fictive.

Les points clés de l'analyse révèlent :
*   L'utilisation de `_.get` permet d'accéder aux attributs d'objets en utilisant une notation de type chaîne de caractères.
*   Le `fetch` avec un corps d'objet non standard déclenche implicitement la méthode `toString()`, ouvrant une piste pour l'exécution de code.
*   La possibilité d'assigner des valeurs à des attributs comme `base.reqBody[to] = val` est le point d'entrée principal.
*   La CSP limite les actions, bloquant les navigations via `javascript:` et l'exécution de scripts en ligne. Cependant, les manipulations du DOM comme `innerHTML` ou `srcdoc` s'exécutent dans le contexte de la cible et ignorent la CSP de l'appelant.

La solution exploite une combinaison de ces éléments. En créant une page attaquante qui encapsule la page challenge et une page sans CSP (un 404, par exemple), il devient possible d'accéder au DOM de la page sans CSP. Le problème réside dans la manière d'utiliser l'assignation `base.reqBody[to] = val` pour déclencher une exécution de code de type XSS. L'astuce consiste à utiliser la récursivité des objets JavaScript. En définissant `payload.base.reqBody = payload.base`, une assignation ultérieure sur `reqBody` (par exemple, `base.reqBody["reqBody"] = ...`) permet à `base.reqBody` de pointer vers l'élément souhaité. Une deuxième assignation utilise ensuite le flux `innerHTML` pour injecter le code XSS dans le DOM de la fenêtre sans CSP.

**Points Clés:**

*   **Accès aux données via `_.get` et `postMessage`:** Utilisation de Lodash pour naviguer dans les objets `event` reçus via `postMessage`.
*   **Manipulation de CSP:** Exploitation du fait que les modifications du DOM (`innerHTML`) dans une fenêtre même d'origine mais sans CSP ne sont pas bloquées par la CSP de la fenêtre appelante.
*   **Récursivité d'objet pour l'overwrite:** La clé de la solution réside dans la création d'une structure d'objet récursive (`payload.base.reqBody = payload.base`) pour permettre à une assignation sur un attribut de modifier en réalité la structure de l'objet source lui-même, permettant ainsi de cibler des propriétés comme `innerHTML`.

**Vulnérabilités :**

*   Aucune vulnérabilité CVE spécifique n'est explicitement mentionnée pour ce challenge. L'article décrit une technique d'attaque XSS non conventionnelle exploitant le fonctionnement des assignations d'attributs, la gestion des messages inter-fenêtres et la CSP.

**Recommandations :**

*   **Sécuriser les communications inter-fenêtres:** Valider rigoureusement les données reçues via `postMessage`, en particulier lorsqu'elles sont utilisées pour manipuler des structures d'objets critiques.
*   **Comprendre les interactions CSP et DOM:** Être conscient que les opérations de manipulation du DOM dans des contextes différents (fenêtres avec ou sans CSP) peuvent avoir des implications de sécurité variées.
*   **Éviter les `unsafe-eval` dans la CSP:** Lorsque possible, restreindre davantage la CSP pour limiter l'exécution de code arbitraire.
*   **Attention aux méthodes implicites:** Être vigilant quant aux méthodes qui peuvent être appelées implicitement par le moteur JavaScript lors de la manipulation d'objets (comme `toString()` dans le cas du `fetch`).

---
[Source](https://joaxcar.com/blog/2025/12/02/solving-turb0s-xss-challenge-using-recursive-object-attributes/){:target="_blank"}
