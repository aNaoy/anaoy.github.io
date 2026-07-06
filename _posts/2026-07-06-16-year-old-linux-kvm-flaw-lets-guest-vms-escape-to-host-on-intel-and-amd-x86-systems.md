---
title: '16-Year-Old Linux KVM Flaw Lets Guest VMs Escape to Host on Intel and AMD x86 Systems'
date: 2026-07-06
permalink: /posts/2026/07/06/16-year-old-linux-kvm-flaw-lets-guest-vms-escape-to-host-on-intel-and-amd-x86-systems/
tags:
- veille-cyber
- hackernews
---
### Januscape : Une vulnérabilité critique de 16 ans dans l'hyperviseur KVM

Une faille de type *use-after-free* découverte dans l'implémentation de la mémoire virtuelle (MMU) de l'hyperviseur Linux KVM permet à un utilisateur malveillant, depuis une machine virtuelle invitée, de compromettre l'hôte ou de provoquer son arrêt brutal.

**Points clés :**
*   **Vulnérabilité :** Baptisée "Januscape", cette faille affecte le code de gestion des *shadow pages* partagé par les architectures Intel et AMD.
*   **Historique :** La vulnérabilité était présente dans le noyau Linux depuis août 2010.
*   **Mécanisme :** KVM réutilisait des pages de suivi de mémoire en se basant uniquement sur l'adresse, sans vérifier le type de page. Cette confusion permet une corruption mémoire sur l'hôte.
*   **Impact :** Une attaque réussie peut provoquer un plantage total de l'hôte (DDoS) ou, dans le pire des cas, une exécution de code arbitraire avec les privilèges du noyau sur la machine hôte.
*   **Conditions d'exploitation :** L'attaque nécessite l'activation de la virtualisation imbriquée (*nested virtualization*) et un accès root au sein de la machine virtuelle invitée.

**Vulnérabilité identifiée :**
*   **CVE-2026-53359**

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer le correctif inclus dans les versions du noyau sorties le 4 juillet 2026 (notamment 7.1.3, 6.18.38, 6.12.95, 6.6.144, 6.1.177, 5.15.211, et 5.10.260).
*   **Vérification :** S'assurer que le correctif correspondant au commit `81ccda30b4e8` est bien présent, en consultant les journaux de modifications (changelogs) de votre distribution Linux.
*   **Mesure d'atténuation temporaire :** Si le patch ne peut être appliqué immédiatement, désactiver la virtualisation imbriquée sur les hôtes KVM utilisant des environnements multi-locataires (`kvm_intel.nested=0` ou `kvm_amd.nested=0`).

---
[Source](https://thehackernews.com/2026/07/16-year-old-linux-kvm-flaw-lets-guest.html){:target="_blank"}
