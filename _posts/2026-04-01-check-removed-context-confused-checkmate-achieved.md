---
title: 'CHECK Removed, Context Confused, Checkmate Achieved'
date: 2026-04-01
permalink: /posts/2026/04/01/check-removed-context-confused-checkmate-achieved/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse technique de CVE-2026-0899 : Exploitation d'une confusion de contexte dans V8

Cette vulnérabilité réside dans le moteur JavaScript V8 de Chrome et concerne la logique de reparsage (lazy compilation) des initialiseurs de classes lorsque des membres d'instance et des blocs statiques sont entremêlés.

**Points clés :**
*   **Cause racine :** Un mauvais alignement des identifiants (`function_literal_id`) lors du reparsage. Le moteur échoue à pré-allouer le scope de l'initialiseur "opposé" (statique vs instance), entraînant une association incorrecte entre l'identifiant et la fonction.
*   **Mécanisme d'exploitation :** Après avoir contourné un `CHECK` de sécurité bloquant, les chercheurs ont créé une confusion de type de contexte entre un `FunctionContext` et un `BlockContext`.
*   **Résultat :** Cette confusion permet d'écrire en dehors des limites d'un objet (`Out-of-Bounds`), écrasant le champ `length` d'un `JSArray`. Une fois la longueur corrompue, cela permet de lire et d'écrire arbitrairement dans la mémoire du processus (primitives AAR/AAW).

**Vulnérabilité :**
*   **CVE-2026-0899 :** Accès mémoire hors limites (OOB) dans le moteur V8.
*   **Composant affecté :** Logique de reparsage des initialiseurs de membres de classe dans `parser-base.h`.

**Recommandations :**
*   **Mise à jour :** Appliquer les correctifs fournis par l'équipe Chromium (patch v8/v8/+/7203465).
*   **Correction logicielle :** Le correctif introduit deux nouveaux variants `FunctionKind` (`kClassMembersInitializerFunctionPrecededByStatic` et `kClassStaticInitializerFunctionPrecededByMember`) pour encoder explicitement l'ordre de déclaration dans le scope.
*   **Pré-allocation :** Le compilateur doit désormais pré-allouer systématiquement les scopes des initialiseurs adjacents lors du reparsage pour garantir la cohérence des identifiants de fonctions, évitant ainsi le décalage observé lors de l'intercalage des membres.

---
[Source](https://starlabs.sg/blog/2026/04-check-removed-context-confused-checkmate-achieved/){:target="_blank"}
