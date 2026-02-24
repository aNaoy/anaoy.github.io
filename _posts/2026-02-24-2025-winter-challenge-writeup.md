---
title: '2025 winter challenge writeup'
date: 2026-02-24
permalink: /posts/2026/02/24/2025-winter-challenge-writeup/
tags:
- veille-cyber
- zerodaysfans
---
## Le défi du Quinindrome ELF

Ce challenge de cybersécurité, organisé par Synacktiv, consistait à créer un "quinindrome" : un binaire ELF qui soit à la fois un palindrome (symétrique en octets) et une "quine" (imprime son propre code source lors de son exécution), tout en se terminant proprement. Le but était d'obtenir le binaire le plus petit possible.

### Points clés

*   **Objectif :** Créer un binaire ELF palindrome et quine, de taille minimale.
*   **Format du binaire :** ELF (Executable and Linkable Format).
*   **Exigences :**
    *   Le binaire doit être un palindrome d'octets.
    *   Le binaire doit s'exécuter et imprimer son propre contenu sur la sortie standard.
    *   L'exécution doit se terminer sans erreur (segfault) et avec un code de retour de 0.
*   **Mécanismes exploités :** La façon dont le noyau Linux charge les binaires ELF est assez permissive, ne vérifiant pas tous les champs des en-têtes ELF et des en-têtes de programme. Des techniques d'optimisation (code golfing) et des astuces d'assembleur x86 32 bits sont utilisées pour minimiser la taille.
*   **Contraintes du noyau Linux :**
    *   Les en-têtes ELF et de programme doivent respecter certains formats et valeurs.
    *   Les segments chargés (`PT_LOAD`) ont des contraintes sur leurs offsets, adresses virtuelles, tailles et permissions.
    *   La gestion des pages mémoire et des permissions (notamment pour `PROT_EXEC` sans `PROT_READ` ou `PROT_WRITE`) a des implications, particulièrement avec le support des Memory Protection Keys (PKU).

### Vulnérabilités et Contournements

*   **Contournement du `shebang` :** L'utilisation simple de `#!/bin/cat` suivi du contenu inversé du fichier ne fonctionne pas car l'environnement d'exécution du challenge ne contient pas l'interpréteur `cat`.
*   **Lenité du chargeur ELF :** Le noyau Linux est tolérant quant à certains champs des en-têtes ELF et de programme, permettant des manipulations pour réduire la taille. Par exemple, les en-têtes peuvent se chevaucher, et certains champs peuvent être ignorés ou manipulés.
*   **Fonctionnalités de segmentation et alignement :** Les fonctions comme `elf_map` et `vm_mmap` alignent les adresses et tailles sur des pages mémoire (4096 octets sur x86), ce qui offre une certaine flexibilité sur les `p_offset` et `p_vaddr`.
*   **Permissions d'exécution et PKU :** Le chargement d'un segment marqué uniquement comme exécutable (`PROT_EXEC` sans `PROT_READ`/`WRITE`) peut poser problème sur des systèmes supportant les Memory Protection Keys (PKU), menant à un `EFAULT` lors des appels système comme `write`, alors qu'il fonctionne sur des systèmes sans PKU. C'est ce qui a conduit à des soumissions qui fonctionnaient dans l'environnement de développement mais échouaient chez les organisateurs.
*   **Injection de commande dans le `Containerfile` (par XeR) :** Une vulnérabilité dans le script de test permettait d'injecter des commandes dans la construction de l'image Docker, menant à la définition du `ENTRYPOINT` et à la configuration du `PATH` pour exécuter le binaire compromis. Le score de 67 a été obtenu ainsi.

### Recommandations (inspirées des solutions)

*   **Comprendre le format ELF :** Une connaissance approfondie de la structure des fichiers ELF (en-têtes, en-têtes de programme, segments) est cruciale.
*   **Maîtriser l'assembleur bas niveau :** Savoir manipuler les registres, les syscalls (`int 0x80`), et les instructions pour minimiser la taille du code est essentiel pour le code golfing.
*   **Analyser le comportement du noyau :** Comprendre comment le noyau Linux charge et exécute les binaires ELF, y compris les spécificités liées aux architectures et aux fonctionnalités matérielles (comme PKU), est important pour identifier les points de faiblesse et les opportunités d'optimisation.
*   **Tester dans différents environnements :** S'assurer que les solutions fonctionnent dans divers environnements d'exécution, en particulier ceux qui activent des fonctionnalités matérielles comme PKU, pour éviter les défaillances "ça marche sur ma machine".
*   **Attention aux injections de commande :** Lors de la création de scripts automatisés, il est vital de valider et d'échapper correctement toutes les entrées utilisateur pour prévenir les vulnérabilités d'injection de commande.

### Meilleures Solutions et Scores

Le classement final a vu plusieurs participants atteindre des scores remarquables :

*   **IooNag : 81 octets** (utilisant des astuces de manipulation d'en-têtes ELF et d'alignement de pages, avec un code assembleur optimisé).
*   **XeR : 67 octets** (via injection de commande dans le `Containerfile`).
*   **matt : 77 octets** (nécessitant des privilèges élevés et un mappage du segment à l'adresse 0x00).
*   **Synacktiv (organisateur) : 83 octets** (solution de référence).

Les solutions les plus performantes ont réussi à créer des binaires ELF de petite taille qui respectent les contraintes de palindrome, de quine, et les exigences de chargement du noyau Linux.

---
[Source](https://www.synacktiv.com/en/publications/2025-winter-challenge-writeup){:target="_blank"}
