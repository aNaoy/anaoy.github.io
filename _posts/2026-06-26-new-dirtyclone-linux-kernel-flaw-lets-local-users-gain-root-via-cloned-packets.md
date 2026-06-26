---
title: 'New DirtyClone Linux Kernel Flaw Lets Local Users Gain Root via Cloned Packets'
date: 2026-06-26
permalink: /posts/2026/06/26/new-dirtyclone-linux-kernel-flaw-lets-local-users-gain-root-via-cloned-packets/
tags:
- veille-cyber
- hackernews
---
### DirtyClone : Vulnérabilité d'élévation de privilèges dans le noyau Linux

**Points clés**
*   **DirtyClone** est une faille d'élévation de privilèges locale (LPE) affectant le noyau Linux.
*   Elle permet à un attaquant de corrompre la mémoire mappée par fichier en manipulant des paquets réseau clonés, lui octroyant les droits root.
*   L'exploitation ne laisse aucune trace sur le disque et n'est pas détectable par les outils d'intégrité classique, car la modification n'existe que dans la copie en mémoire du noyau.
*   La vulnérabilité découle d'un problème de conception récurrent : lors de certaines opérations réseau (zero-copy), un drapeau de sécurité indiquant que la mémoire est partagée est incorrectement supprimé, permettant une écriture non autorisée.

**Vulnérabilité**
*   **CVE-2026-43503** (Score CVSS : 8.8) : Causée par une mauvaise gestion des drapeaux de fragments réseau dans des fonctions comme `__pskb_copy_fclone()` et `skb_shift()`.

**Recommandations**
*   **Mise à jour immédiate :** Appliquer les correctifs du noyau fournis par votre distribution (le patch est disponible depuis la version Linux v7.1-rc5 et a été rétroporté dans les branches stables).
*   **Restriction des espaces de noms :** Si le patch est impossible, désactiver les espaces de noms utilisateur non privilégiés (ex: `sysctl -w kernel.unprivileged_userns_clone=0` sur Debian/Ubuntu) pour bloquer le vecteur d'attaque.
*   **Contournement temporaire :** Blacklister les modules `esp4`, `esp6` et `rxrpc` si les fonctionnalités IPsec/AFS ne sont pas nécessaires, bien que cela ne soit qu'une mesure d'atténuation partielle.

---
[Source](https://thehackernews.com/2026/06/new-dirtyclone-linux-kernel-flaw-lets.html){:target="_blank"}
