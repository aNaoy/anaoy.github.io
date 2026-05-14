---
title: 'New Fragnesia Linux flaw lets attackers gain root privileges'
date: 2026-05-14
permalink: /posts/2026/05/14/new-fragnesia-linux-flaw-lets-attackers-gain-root-privileges/
tags:
- veille-cyber
- bleepingcomp
---
### Fragnasia : Nouvelle faille d'élévation de privilèges sous Linux

Une vulnérabilité critique affectant le noyau Linux, baptisée **Fragnasia**, permet à un utilisateur local non privilégié d'exécuter du code arbitraire avec les droits "root". Cette faille exploite une erreur de logique dans le sous-système `XFRM ESP-in-TCP`, permettant l'écriture d'octets arbitraires dans le cache de page du noyau pour des fichiers en lecture seule.

**Points clés :**
*   **Nature :** Vulnérabilité d'élévation locale de privilèges (LPE).
*   **Classe :** Appartient à la famille des vulnérabilités "Dirty Frag".
*   **Exploitation :** Un code de preuve de concept (PoC) est déjà public, permettant de corrompre la mémoire du binaire `/usr/bin/su` pour obtenir un accès root.
*   **Impact :** Concerne tous les noyaux Linux publiés avant le 13 mai 2026.

**Vulnérabilités associées :**
*   **CVE-2026-46300 (Fragnasia) :** Faille logique dans `XFRM ESP-in-TCP`.
*   **CVE-2026-43284 & CVE-2026-43500 :** Composantes de la vulnérabilité "Dirty Frag" (impliquant `xfrm-ESP` et `RxRPC`).

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs du noyau fournis par les distributions Linux dès que possible.
*   **Atténuation temporaire :** En cas d'impossibilité de patcher, désactiver les modules vulnérables (`esp4`, `esp6` et `rxrpc`) via la commande `rmmod` et les empêcher de se charger au démarrage en ajoutant les directives `install <module> /bin/false` dans `/etc/modprobe.d/dirtyfrag.conf`.
*   **Avertissement :** La désactivation de ces modules interrompra le fonctionnement des systèmes de fichiers réseau AFS et des VPN IPsec.

---
[Source](https://www.bleepingcomputer.com/news/security/new-fragnesia-linux-flaw-lets-attackers-gain-root-privileges/){:target="_blank"}
