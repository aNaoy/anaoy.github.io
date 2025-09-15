---
title: 'Summer Pwnables: Temporal Paradox Engine Solution'
date: 2025-09-15
permalink: /posts/2025/09/15/summer-pwnables-temporal-paradox-engine-solution/
tags:
- veille-cyber
- zerodaysfans
---
**Détournement d'une Vulnérabilité Temporelle dans le Noyau Linux**

Un défi de sécurité avancé a été créé pour le concours Summer Pwnables, centré sur l'exploitation du noyau Linux via un pilote vulnérable, le "paradox_engine". Ce pilote simule une gestion complexe d'événements temporels et de dépendances, permettant aux utilisateurs d'interagir avec le noyau par le biais d'appels système (`ioctl`). L'objectif était de concevoir un défi complexe, nécessitant plusieurs jours de résolution et potentiellement résistant aux solutions automatisées par IA.

**Points Clés :**

*   **Fonctionnalité du Pilote :** Le module crée des "événements temporels" (`temporal_event`) organisés en "lignes de temps" (`timeline`) au sein d'une "session" (`paradox_session_data`). Les événements peuvent avoir des dépendances causales, créant une structure de graphe.
*   **Interfaces Utilisateur :** Les opérations `open` et `release` initialisent et nettoient la session. L'interface `ioctl` permet de créer de nouvelles lignes de temps (`PARADOX_CREATE_TIMELINE`) et de nouveaux événements (`PARADOX_CREATE_EVENT`), en spécifiant des dépendances causales.
*   **Allocation Mémoire :** Les objets `temporal_event` sont alloués à partir d'un cache `kmem_cache` dédié, `temporal_event_cache`.

**Vulnérabilité Principale :**

La vulnérabilité réside dans la fonction `PARADOX_CREATE_EVENT`. Après l'ajout d'un nouvel événement à la liste chaînée des événements d'une ligne de temps (`list_add_tail`), le code recherche l'événement causal spécifié (`req.cause_event_id`). Si le `cause_event_id` correspond à l'ID de l'événement nouvellement ajouté, cela crée une dépendance cyclique où un événement dépend de lui-même.

*   **CVE :** Aucune CVE spécifique n'est mentionnée dans l'article pour cette vulnérabilité.
*   **Impact :** Lors de la libération de la session (appel à `paradox_engine_release`), le pilote tente de libérer tous les événements et leurs dépendances. Si la vulnérabilité cyclique est exploitée, le code d'effacement des événements entre dans une boucle infinie. La fonction `refcount_dec_and_test` gère le décompte des références, mais dans le cas de la boucle, le compteur de référence peut atteindre une valeur saturée (représentée par `REFCOUNT_SATURATED`), empêchant une libération correcte et conduisant à un blocage du système.

**Recommandations et Solutions :**

La résolution du défi implique généralement deux approches principales pour surmonter le blocage induit par la vulnérabilité :

1.  **Exploitation Cross-Cache :**
    *   **Principe :** Tirer parti du fait que les objets `temporal_event` sont alloués dans un cache dédié. L'idée est de faire libérer une page mémoire utilisée par le cache d'événements, puis de la réutiliser avec un autre objet (par exemple, un "pipe"). Cela permet de modifier la page mémoire et, potentiellement, d'annuler la dépendance causale cyclique.
    *   **Technique :** L'approche implique de manipuler les listes de pages libres par CPU (`pcp freelist`) pour s'assurer que la page libérée par l'événement cyclique soit récupérable par un autre cœur de traitement, évitant ainsi qu'elle ne soit immédiatement réutilisée par le cœur bloqué. Une fois la page récupérée, on peut modifier les données de l'événement pour annuler la dépendance.
    *   **Outils :** Des techniques comme le "spraying" (pulvérisation) de mémoire, l'utilisation de `msg_msg` ou `pipe_buffer` sont mentionnées.

2.  **Use-After-Free via `kfree` et Page de Pipe :**
    *   **Principe :** Exploiter le comportement de `kfree` lorsqu'il est appliqué à de la mémoire non gérée par un cache spécifique (comme la mémoire d'un pipe). `kfree` peut alors libérer la page mémoire sous-jacente.
    *   **Technique :** En construisant une chaîne d'événements, il est possible de déclencher la libération d'une page mémoire contenant un événement vulnérable, puis de la réutiliser avec un objet pipe. Cet objet pipe conserve une référence à la page libérée, créant une condition de "use-after-free". Cette vulnérabilité peut ensuite être pivotée vers d'autres objets partagés par le même cache, comme `pipe_buffer`, permettant potentiellement une lecture/écriture arbitraire dans le noyau.
    *   **Fiabilité :** Cette méthode peut avoir une fiabilité limitée (environ 50%) en raison de la nature des allocations mémoire et de la réinitialisation des listes de libres.

Les trois étudiants qui ont résolu le défi ont utilisé des approches créatives, parfois différentes des solutions prévues, démontrant l'importance de la persévérance et de la compréhension des mécanismes du noyau pour la résolution de problèmes d'exploitation complexes.

---
[Source](https://starlabs.sg/blog/2025/09-temporal-paradox-engine-solution/){:target="_blank"}
