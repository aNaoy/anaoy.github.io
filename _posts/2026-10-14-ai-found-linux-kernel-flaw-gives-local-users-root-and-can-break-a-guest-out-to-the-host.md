---
title: 'AI-Found Linux Kernel Flaw Gives Local Users Root, and Can Break a Guest Out to the Host'
date: 2026-10-14
permalink: /posts/2026/10/14/ai-found-linux-kernel-flaw-gives-local-users-root-and-can-break-a-guest-out-to-the-host/
tags:
- veille-cyber
- hackernews
---
### Vghost : Vulnérabilité critique dans le sous-système vhost de Linux

Une faille de sécurité majeure, baptisée **Vghost**, affecte le sous-système `vhost` du noyau Linux, utilisé pour optimiser les entrées/sorties des machines virtuelles et conteneurs. Cette vulnérabilité permet à un utilisateur local d'escalader ses privilèges jusqu'au niveau `root` ou, dans certains scénarios de virtualisation, de réaliser une évasion depuis une machine virtuelle vers l'hôte.

**Points clés :**
*   **Mécanisme :** La faille repose sur une gestion défaillante du cache des correspondances mémoire. Lors d'une reconfiguration des anneaux virtuels, le système continue d'utiliser d'anciennes adresses mémoires non validées, permettant une lecture/écriture hors limites dans la mémoire du noyau.
*   **Historique :** La vulnérabilité découle de modifications cumulées entre 2017 et 2020, rendant le code vulnérable pendant près de neuf ans.
*   **Détection :** La faille a été identifiée par le système de recherche automatisé par IA « Corvus AI » de Tencent Zhuque Lab.

**Vulnérabilité :**
*   **CVE-2026-74580** : Score CVSS oscillant entre 7.3 et 8.8 selon les éditeurs, en raison de son potentiel d'évasion de machine virtuelle vers l'hôte.
*   **Versions affectées :** Noyaux Linux de la branche 4.11 jusqu'à la 7.2-rc4.

**Recommandations :**
*   **Mise à jour :** Appliquer les correctifs du noyau fournis par les distributions Linux (le correctif upstream est disponible via le commit `de845981da67`). Un redémarrage est impératif.
*   **Atténuation immédiate :** En attendant la mise à jour, restreindre strictement l'accès aux nœuds de périphériques `/dev/vhost-net` et `/dev/vhost-vsock`. Supprimer les permissions d'accès universel (mode 0666) et limiter l'accès aux seuls services de virtualisation de confiance.

---
[Source](https://thehackernews.com/2026/10/ai-found-linux-kernel-flaw-gives-local.html){:target="_blank"}
