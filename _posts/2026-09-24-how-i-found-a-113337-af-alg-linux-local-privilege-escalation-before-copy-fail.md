---
title: 'How I Found a $113,337 AF_ALG Linux Local Privilege Escalation Before Copy Fail'
date: 2026-09-24
permalink: /posts/2026/09/24/how-i-found-a-113337-af-alg-linux-local-privilege-escalation-before-copy-fail/
tags:
- veille-cyber
- zerodaysfans
---
### Escalade de privilèges via AF_ALG dans le noyau Linux

Une vulnérabilité critique (CVE-2025-39964) a été découverte dans l'API `AF_ALG` du noyau Linux, présente depuis 2011. Cette faille permet à un utilisateur non privilégié d'obtenir les droits root ou de s'échapper d'un conteneur Docker.

#### Points clés
* **Nature de la faille :** Une condition de concurrence (race condition) lors d'écritures simultanées sur une même socket `AF_ALG`.
* **Mécanisme :** Lorsque deux threads tentent d'écrire simultanément via `sendmsg()`, le verrouillage du socket est temporairement relâché pour attendre de l'espace mémoire. Cela permet à un thread de modifier l'état interne (`af_alg_ctx`) de manière incohérente, menant à une lecture hors limites (out-of-bounds) lors du calcul des pointeurs de la liste de dispersion (scatterlist).
* **Exploitation :** L'accès hors limites permet de lire des données à un emplacement arbitraire dans le tas du noyau. En utilisant `memcpy_from_msg()` comme un oracle (via des erreurs `EFAULT`), les attaquants peuvent cartographier la mémoire et transformer cette lecture hors limites en une primitive d'écriture arbitraire dans le noyau, utilisée ici pour écraser `core_pattern` et exécuter du code arbitraire en tant que root.

#### Vulnérabilité
* **CVE-2025-39964 :** Dépassement de tampon et corruption de mémoire par condition de concurrence dans `crypto/af_alg.c`.

#### Recommandations
* **Mise à jour :** Appliquer le correctif officiel disponible dans le commit [1b34cbbf4f01](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=1b34cbbf4f011a121ef7b2d7d6e6920a036d5285).
* **Correctif :** La correction impose l'exclusivité des écritures sur une socket `AF_ALG` en introduisant un drapeau d'état (`ctx->write`) qui rejette les écritures concurrentes avec `-EBUSY`.
* **Audit :** Surveiller les sous-systèmes du noyau accessibles par des utilisateurs non privilégiés (API socket, etc.) qui gèrent des états complexes sur plusieurs appels système.

---
[Source](https://starlabs.sg/blog/2026/09-how-i-found-a-113337-af_alg-linux-local-privilege-escalation-before-copy-fail/){:target="_blank"}
