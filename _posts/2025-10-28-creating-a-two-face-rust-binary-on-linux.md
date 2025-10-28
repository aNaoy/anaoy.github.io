---
title: 'Creating a "Two-Face" Rust binary on Linux'
date: 2025-10-28
permalink: /posts/2025/10/28/creating-a-two-face-rust-binary-on-linux/
tags:
- veille-cyber
- zerodaysfans
---
## Le Binaire "Deux Visages" sous Linux : Technique et Défenses

Cette approche permet de créer un exécutable unique sous Linux qui exécute un programme bénin par défaut, mais révèle un code distinct et caché lorsqu'il est déployé sur une machine cible spécifique. Le programme caché est également rendu plus difficile à analyser en mémoire.

### Points Clés

*   **Conception du binaire "schizophrène"**: Le binaire prend une décision au démarrage pour exécuter soit le programme "normal", soit le programme "caché".
*   **Dérivation de clé basée sur l'hôte**: Au lieu de stocker la clé de déchiffrement directement, elle est dérivée dynamiquement à partir de données d'identification uniques de la machine cible (par exemple, les UUIDs des partitions disque). Ceci garantit que le programme caché ne se déchiffre et ne s'exécute que sur la machine visée.
*   **Utilisation de Rust et de ses capacités de compilation**: Le framework utilise des *build scripts* Rust pour intégrer le chiffrement et l'intégration des binaires à la fois au moment de la compilation et de l'exécution.
*   **Exécution en mémoire**: Pour éviter la présence du binaire caché sur le système de fichiers, le mécanisme utilise `memfd_create` pour créer un descripteur de fichier en mémoire, puis `fexecve` pour le remplacer par le processus exécutable, rendant ainsi l'analyse plus complexe.
*   **Obfuscation de l'écriture en mémoire**: Des techniques comme `io_uring` ou `mmap` sont envisagées pour minimiser la visibilité des écritures du binaire déchiffré en mémoire, rendant l'analyse par des outils comme `strace` plus difficile.

### Vulnérabilités / Attaques Concernées

Bien qu'il ne s'agisse pas de vulnérabilités au sens traditionnel, la technique décrite vise à exploiter l'exécution conditionnelle d'un code malveillant et à masquer sa présence. Les méthodes analysées par l'article constituent une forme de contournement des mécanismes de détection standards.

*   **Exposition du code caché**: Une approche naïve laisse le programme caché et les conditions d'exécution accessibles dans le binaire.
*   **Analyse mémoire**: Le code caché, s'il est présent en clair en mémoire, peut être extrait.
*   **Détection par `strace`**: Les appels système `write` lors du déchiffrement et de l'écriture en mémoire peuvent être tracés.

### Recommandations

Pour atténuer ce type de technique, plusieurs pistes peuvent être explorées :

*   **Renforcement de l'analyse au démarrage (runtime)**: Examiner les comportements inhabituels des programmes à leur lancement, y compris les appels système liés à la mémoire (`memfd_create`, `mmap`).
*   **Surveillance des descripteurs de fichiers**: Surveiller la création et l'utilisation de descripteurs de fichiers créés via `memfd_create`.
*   **Analyse de bas niveau du noyau**: Pour des analyses plus poussées, examiner les données accessibles par le noyau, même si elles ne sont pas directement mappées en mémoire utilisateur.
*   **Obfuscation du build script**: La technique elle-même peut être rendue plus difficile à identifier par une obfuscation supplémentaire au niveau du script de compilation.
*   **Détection de la dérivation de clé**: Analyser les sources de données utilisées pour la dérivation de clés (comme les UUIDs de partitions) et rechercher des motifs suspects.

---
[Source](https://www.synacktiv.com/en/publications/creating-a-two-face-rust-binary-on-linux){:target="_blank"}
