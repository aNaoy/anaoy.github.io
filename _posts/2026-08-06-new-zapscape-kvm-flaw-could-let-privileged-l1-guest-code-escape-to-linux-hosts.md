---
title: 'New Zapscape KVM Flaw Could Let Privileged L1 Guest Code Escape to Linux Hosts'
date: 2026-08-06
permalink: /posts/2026/08/06/new-zapscape-kvm-flaw-could-let-privileged-l1-guest-code-escape-to-linux-hosts/
tags:
- veille-cyber
- hackernews
---
### Zapscape : Vulnérabilité d'évasion de machine virtuelle KVM

La faille **Zapscape** permet à un attaquant disposant de privilèges noyau au sein d'une machine virtuelle (L1) de s'échapper de l'isolation KVM pour exécuter du code arbitraire sur l'hôte avec des privilèges root. Cette vulnérabilité concerne principalement les environnements utilisant la virtualisation imbriquée (nested virtualization).

**Points clés :**
* **Origine technique :** Il s'agit d'un problème de vérification de "stale-root" (racine obsolète) dans la gestion du *shadow MMU* (Memory Management Unit) de KVM, conduisant à une corruption mémoire de type *use-after-free*.
* **Mécanisme :** Lors du traitement d'un défaut de page, KVM peut réclamer des pages MMU et invalider la racine utilisée. Si le processus continue sans vérifier à nouveau cette racine, des pages enfants invalides sont créées, provoquant une double référence et une écriture post-libération.
* **Conditions d'exploitation :** Nécessite des privilèges root dans la machine virtuelle invitée. Sur les systèmes Intel, cela exige l'exposition des longueurs de parcours de page EPT 4 et 5.

**Vulnérabilité :**
* **CVE-2026-64561** (Score CVSS préliminaire : 7.0)
* **CWE-825** (Expired pointer dereference)
* **Versions affectées :** Linux 5.9 jusqu'aux versions corrigées (ex: 6.6.148, 6.12.101, 6.18.42, 7.1.6, 7.2-rc5).

**Recommandations :**
* **Mise à jour :** Appliquer les correctifs fournis par les distributions Linux dès que possible. La correction amont (commit `2abd5287f083`) force KVM à redémarrer le traitement du défaut de page (`RET_PF_RETRY`) si la racine est invalidée durant le processus.
* **Atténuation :** Pour les administrateurs ne pouvant pas mettre à jour immédiatement, il est recommandé de désactiver la virtualisation imbriquée pour les invités non fiables.

---
[Source](https://thehackernews.com/2026/08/new-zapscape-kvm-flaw-could-let.html){:target="_blank"}
