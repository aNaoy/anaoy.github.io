---
title: 'The skb that wasnt freed - the Fragnesia primitive via Open vSwitch'
date: 2026-09-17
permalink: /posts/2026/09/17/the-skb-that-wasnt-freed-the-fragnesia-primitive-via-open-vswitch/
tags:
- veille-cyber
- zerodaysfans
---
### Escalade de privilèges via Open vSwitch (Fragnesia-bis)

Cette vulnérabilité permet à un utilisateur non privilégié d'écrire du contenu arbitraire dans le cache de pages (page cache) de fichiers appartenant au root, entraînant une escalade de privilèges locale (LPE) déterministe. Elle exploite une faille dans la gestion du marqueur de propriété `SKBFL_SHARED_FRAG` au sein du sous-système réseau du noyau Linux.

#### Points clés
*   **Mécanisme :** Le noyau utilise le marqueur `SKBFL_SHARED_FRAG` pour interdire le déchiffrement "in-place" (sur place) de paquets ESP dont les données sont partagées (non privées). Si le marqueur est perdu, le noyau déchiffre le paquet directement sur les pages du cache, permettant à l'attaquant de corrompre le contenu d'un fichier root.
*   **Déclencheur :** Le module `openvswitch` déclenche par erreur une suppression de ce marqueur lors d'une erreur d'upcall, tout en continuant à transférer le paquet. La suppression se produit via `skb_tx_error()`, qui efface trop largement les drapeaux zerocopy, y compris celui protégeant l'intégrité de la mémoire.
*   **Conditions d'exploitation :**
    *   `openvswitch` chargé (ou autoloadable via les espaces de noms utilisateur).
    *   Support des espaces de noms utilisateur (unprivileged user namespaces) activé par défaut.
    *   Attaque basée sur `MSG_ZEROCOPY` et l'encapsulation ESP-in-UDP.

#### Vulnérabilités (CVE)
*   **CVE-2026-90049**
*   **CVE-2026-89487**
*   **CVE-2026-80977**

#### Recommandations
1.  **Mise à jour :** Appliquer les correctifs du noyau fournis par votre distribution (le correctif a été intégré dans le mainline et les versions stables début septembre 2026).
2.  **Blocage du module :** Si Open vSwitch n'est pas nécessaire, empêcher son chargement via `/etc/modprobe.d/no-openvswitch.conf` :
    ```text
    install openvswitch /bin/false
    ```
3.  **Restriction de surface :** Désactiver les espaces de noms utilisateur non privilégiés si l'environnement le permet :
    *   *Mainline :* `sysctl -w user.max_user_namespaces=0`
    *   *Debian/ dérivés :* `sysctl -w kernel.unprivileged_userns_clone=0`
    *   *Ubuntu :* `sysctl -w kernel.apparmor_restrict_unprivileged_userns=1`

---
[Source](https://blog.doyensec.com/2026/09/17/ovs.html){:target="_blank"}
