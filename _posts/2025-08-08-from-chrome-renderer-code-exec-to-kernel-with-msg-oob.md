---
title: 'From Chrome renderer code exec to kernel with MSG_OOB'
date: 2025-08-08
permalink: /posts/2025/08/08/from-chrome-renderer-code-exec-to-kernel-with-msg-oob/
tags:
- veille-cyber
- zerodaysfans
---
### Exploitation d'une faille du noyau Linux depuis le sandbox Chrome

Une vulnérabilité de type Use-After-Free (UAF) découverte dans le noyau Linux (CVE-2025-38236), liée à la fonctionnalité `MSG_OOB` des sockets de domaine UNIX, a été exploitée avec succès pour passer de l'exécution de code dans le sandbox du rendu Chrome à l'obtention de privilèges au niveau du noyau. Cette faille découle d'une gestion incorrecte de la mémoire dans la fonction `manage_oob()`, qui traite les données "hors bande" (out-of-band).

**Points Clés :**

*   La fonctionnalité `MSG_OOB` des sockets de domaine UNIX, introduite dans le noyau Linux 5.15, permet d'envoyer un octet de données "hors bande".
*   Une interaction spécifique entre la réception de messages hors bande et le traitement des messages normaux a conduit à une situation où un pointeur vers un buffer de socket (SKB) pouvait devenir orphelin (dangling pointer).
*   L'exploitation réussie nécessite la création de deux buffers de socket avec une longueur restante de zéro, suivie de la réception d'un message hors bande, puis d'une réception normale. Cela déclenche un UAF qui laisse un pointeur invalide vers un SKB libéré.
*   L'UAF crée une primitive de lecture semi-arbitraire via la fonction `copy_to_user()` dans le noyau, permettant de lire des données à des adresses arbitraires du noyau, sous réserve de certaines protections.
*   Une primitive d'écriture est également rendue possible grâce à l'incrémentation d'un champ `consumed` dans la structure `unix_skb_parms` du SKB.
*   L'exploitation exploite la randomisation de la pile du noyau (`CONFIG_RANDOMIZE_KSTACK_OFFSET`) pour cibler un emplacement spécifique sur la pile d'une fonction du noyau, permettant d'écraser une variable liée à la copie de données (`copy_from_iter`).

**Vulnérabilités :**

*   **CVE-2025-38236 :** Use-After-Free dans la gestion de `MSG_OOB` dans les sockets de domaine UNIX. Le bug a été introduit par une correction d'un autre problème de `recv()` qui retournait 0 de manière erronée.

**Recommandations :**

*   **Restrictions d'accès aux fonctionnalités du noyau :** Le sandbox Chrome ne devrait exposer que les interfaces du noyau strictement nécessaires à son fonctionnement. L'exposition de fonctionnalités ésotériques ou rarement utilisées peut introduire des surfaces d'attaque supplémentaires et des vulnérabilités.
*   **Analyse de la sécurité des fonctionnalités ésotériques :** Les fonctionnalités moins courantes ou complexes du noyau, même si elles sont exposées via des interfaces courantes, doivent faire l'objet d'une analyse de sécurité approfondie pour éviter de telles expositions involontaires.
*   **Amélioration des fuzzers :** Les fuzzers pourraient bénéficier de stratégies visant à explorer plus en profondeur des sous-systèmes spécifiques du noyau, en se concentrant sur des interactions plus complexes entre les appels système, plutôt que de se fier uniquement à des chaînes aléatoires.
*   **Sécurité des primitives de copie :** Bien que des protections existent pour `copy_to_user()`, l'existence de vulnérabilités permettant d'y passer des pointeurs arbitraires rend leur efficacité dans ce contexte discutable. Une analyse plus poussée de la sécurité de ces opérations est nécessaire.
*   **Mitigations probabilistes :** Les mitigations probabilistes, comme la randomisation des piles de manière à chaque opération, peuvent être contournées par des attaquants disposant d'une primitive de lecture arbitraire. Des mécanismes de randomisation au démarrage ou des approches plus robustes sont à envisager.

---
[Source](https://googleprojectzero.blogspot.com/2025/08/from-chrome-renderer-code-exec-to-kernel.html){:target="_blank"}
