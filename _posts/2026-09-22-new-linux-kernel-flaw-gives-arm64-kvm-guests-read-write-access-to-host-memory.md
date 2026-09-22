---
title: 'New Linux Kernel Flaw Gives ARM64 KVM Guests Read-Write Access to Host Memory'
date: 2026-09-22
permalink: /posts/2026/09/22/new-linux-kernel-flaw-gives-arm64-kvm-guests-read-write-access-to-host-memory/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans KVM ARM64 : Escalade de privilèges depuis une machine virtuelle

Une faille de sécurité majeure a été découverte dans le sous-système KVM du noyau Linux pour l'architecture ARM64. Elle permet à un utilisateur malveillant de s'échapper d'une machine virtuelle (VM) pour exécuter du code sur la machine hôte.

**Points clés :**
*   **Cause technique :** Une erreur de calcul de taille dans le code gérant la virtualisation imbriquée (*nested virtualization*) entraîne une omission de l'invalidation du cache TLB. Cela laisse une page de mémoire hôte libre accessible en lecture/écriture par la VM.
*   **Vecteur d'attaque :** L'exploitation nécessite que la virtualisation imbriquée soit activée sur l'hôte ARM64. Elle peut être déclenchée par un utilisateur local disposant d'un accès à `/dev/kvm` ou par un attaquant compromettant une VM invitée.
*   **Contexte :** Cette fonctionnalité est désactivée par défaut sur ARM64, limitant la surface d'exposition. Aucun exploit public n'est actuellement répertorié.

**Vulnérabilité identifiée :**
*   **CVE-2026-89775 :** Permet une lecture/écriture dans la mémoire du noyau hôte et une potentielle évasion de machine virtuelle.

**Recommandations :**
*   **Mise à jour du noyau :** Appliquer les correctifs disponibles dans les versions Linux 6.18.51, 7.2.5 et 7.3-rc1 (ou les mises à jour spécifiques fournies par votre distribution Linux).
*   **Réduction de la surface d'attaque :** Si la virtualisation imbriquée n'est pas strictement nécessaire, désactivez-la sur les hôtes ARM64.
*   **Contrôle d'accès :** Restreindre l'accès à `/dev/kvm` aux utilisateurs de confiance sur les systèmes où cette restriction n'est pas appliquée par défaut.

---
[Source](https://thehackernews.com/2026/09/new-linux-kernel-flaw-gives-arm64-kvm.html){:target="_blank"}
