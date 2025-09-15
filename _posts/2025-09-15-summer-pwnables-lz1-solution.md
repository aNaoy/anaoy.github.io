---
title: 'Summer Pwnables: lz1 Solution'
date: 2025-09-15
permalink: /posts/2025/09/15/summer-pwnables-lz1-solution/
tags:
- veille-cyber
- zerodaysfans
---
## Transformation d'un compresseur en outil d'exécution de commandes

Cet article détaille l'exploitation d'une vulnérabilité de dépassement de tampon dans la fonction de décompression de la bibliothèque `lz1/lz77`. En construisant des données compressées malveillantes, il est possible de provoquer un débordement de la pile et d'enchaîner des gadgets ROP (Return-Oriented Programming) pour obtenir l'exécution de code.

### Points Clés

*   **Principe de LZ77 :** L'algorithme LZ77 compresse des séquences d'octets répétées en utilisant des "pointeurs" qui spécifient une position et une longueur dans les données déjà décompressées.
*   **Paramètres de compression :** La taille des bits allouée à la position et à la longueur dans les pointeurs est configurable. Cette flexibilité est essentielle pour l'exploitation.
*   **Allocation mémoire :** La fonction `file_lz77_decompress` utilise initialement `malloc` pour allouer de la mémoire pour les données compressées et décompressées. Le passage à `alloca` déplace cette allocation sur la pile.
*   **Exploitation de la pile :** L'objectif est de créer une séquence compressée qui, lors de la décompression, écrase les données sur la pile, y compris l'adresse de retour.
*   **ROP Chain :** Une chaîne ROP est construite pour modifier les permissions de la pile afin de la rendre exécutable, puis transférer le contrôle vers un shellcode.
*   **Configuration optimale :** L'utilisation de 7 bits pour la position et 9 bits pour la longueur s'est avérée optimale, permettant un débordement suffisant pour écraser l'adresse de retour et disposer d'une chaîne ROP de taille conséquente (128 octets).
*   **Désactivation de la protection de pile :** La compilation sans protection de pile (comme le ASLR) simplifie l'exploitation.

### Vulnérabilités

*   **Dépassement de tampon dans la décompression LZ77 :** La fonction `lz77_decompress` présente un débordement potentiel. L'une des boucles itère sur `coding_pos` jusqu'à `uncompressed_size`, mais la copie des données référencées par les pointeurs (`uncompressed_text[coding_pos++] = uncompressed_text[pointer_offset++]`) n'est pas bornée par `uncompressed_size`. En fournissant une valeur `uncompressed_size` plus petite que la longueur du contenu décompressé via les pointeurs, il est possible de dépasser la taille allouée pour `uncompressed_text` et d'écraser la pile.
    *   **CVE :** Non spécifié dans l'article.

### Recommandations

*   **Correction du dépassement de tampon :** Implémenter des vérifications rigoureuses pour s'assurer que l'écriture dans `uncompressed_text` ne dépasse jamais les limites allouées, en particulier lors de la copie de données référencées par des pointeurs. La boucle de copie devrait être bornée par `uncompressed_size`.
*   **Utilisation de fonctions de sécurité :** Privilégier des fonctions de copie mémoire sûres qui vérifient les tailles des tampons pour éviter les dépassements.
*   **Compilation avec protections :** Compiler les programmes avec les protections de sécurité activées (ASLR, Stack Canaries, PIE) pour rendre l'exploitation plus difficile.
*   **Revue de code approfondie :** Effectuer des revues de code régulières pour identifier les vulnérabilités potentielles, en particulier dans les fonctions de traitement d'entrée utilisateur ou de données externes.

---
[Source](https://starlabs.sg/blog/2025/09-lz1-solution/){:target="_blank"}
