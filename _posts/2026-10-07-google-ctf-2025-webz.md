---
title: 'Google CTF 2025: webz'
date: 2026-10-07
permalink: /posts/2026/10/07/google-ctf-2025-webz/
tags:
- veille-cyber
- zerodaysfans
---
### Vulnérabilité et exploitation dans Google-zlib

L'article analyse une implémentation modifiée de la bibliothèque `zlib` (utilisée dans le challenge Google CTF 2025 "webz"), inspirée par la vulnérabilité critique découverte dans WebP en 2023.

#### Points clés
*   **Modification structurelle :** La bibliothèque supprime les vérifications de cohérence des arbres de Huffman (arbres "oversubscribed" ou incomplets) pour améliorer les performances, en augmentant la taille des tables allouées.
*   **Vecteur d'attaque :** Bien que les débordements de tampon (OOB) sur la table de Huffman soient évités par l'augmentation de la taille des buffers, l'absence de vérification des arbres incomplets permet de laisser des emplacements de la table non initialisés.
*   **Conséquences :** Ces emplacements non initialisés permettent une confusion de type entre les codes "LEN" (longueur) et "DIST" (distance), brisant les invariants internes de décompression rapide (*inffast*) et entraînant un dépassement de tampon linéaire.

#### Vulnérabilités
*   **Type de faille :** Confusion de types et dépassement de tampon (Buffer Overflow) liés à une gestion défectueuse des arbres de Huffman.
*   **CVE :** Aucune CVE spécifique n'est mentionnée, car il s'agit d'une implémentation personnalisée dans le cadre d'un challenge de cybersécurité.

#### Chaîne d'exploitation
1.  **Corruption :** Exploitation de la confusion de type pour provoquer un débordement linéaire via `inffast`.
2.  **Fuite d'informations :** Utilisation du dépassement pour corrompre l'objet `z_stream` et obtenir une fuite de mémoire relative.
3.  **Contrôle du flux :** Lecture arbitraire (`arb read`) suivie d'un écrasement du pointeur de fonction `zalloc`.
4.  **Exécution :** Exécution de code arbitraire via une technique de type `ret2libc`.

#### Recommandations
*   **Ne jamais supprimer les contrôles de validation :** Les vérifications de l'état "oversubscribed" ou "incomplet" des arbres de Huffman sont critiques pour la sécurité. Leur suppression, même compensée par une allocation mémoire plus importante, expose le système à des confusions de types complexes.
*   **Maintenir l'intégrité des structures de données :** S'assurer que chaque entrée d'une table de décompression est correctement initialisée avant usage pour éviter que des données résiduelles ne soient interprétées comme des codes valides.

---
[Source](https://github.com/google/google-ctf/tree/main/2025/quals/pwn-webz){:target="_blank"}
