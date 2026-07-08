---
title: 'New Januscape Linux flaw allows VM escape on Intel, AMD devices'
date: 2026-07-08
permalink: /posts/2026/07/08/new-januscape-linux-flaw-allows-vm-escape-on-intel-amd-devices/
tags:
- veille-cyber
- bleepingcomp
---
### Januscape : Une faille critique d'évasion de machine virtuelle sur Linux

Une vulnérabilité majeure présente depuis 16 ans dans le noyau Linux, baptisée **Januscape**, permet à un attaquant de s'échapper d'une machine virtuelle (VM) pour exécuter du code arbitraire sur l'hôte physique. Cette faille touche aussi bien les processeurs Intel qu'AMD, posant une menace directe pour les environnements de cloud public multi-locataires.

**Points clés :**
* **Impact :** Un attaquant possédant les privilèges root dans une VM peut compromettre l'hôte physique, prendre le contrôle de toutes les autres instances invitées sur la même machine, ou provoquer un crash du système (déni de service).
* **Portée :** Contrairement à d'autres exploits, Januscape est agnostique au matériel et affecte les architectures x86 et x86_64.
* **Accessibilité :** Sur certaines distributions où `/dev/kvm` est accessible en écriture, même un utilisateur non privilégié peut exploiter la faille pour obtenir des droits root.
* **Chaînage d'attaques :** La vulnérabilité peut être combinée avec l'exploit "Dirty Frag" pour permettre une compromission totale du système, même sans accès root initial dans la VM.

**Vulnérabilité :**
* **CVE-2026-53359 :** Vulnérabilité de type *use-after-free* située dans l'émulation MMU (Memory Management Unit) de l'ombre de KVM/x86.

**Recommandations :**
* **Mise à jour :** Les administrateurs de serveurs KVM/x86 doivent impérativement vérifier que le correctif associé au commit `81ccda30b4e8` est appliqué au noyau de l'hôte.
* **Sécurisation des accès :** Restreindre les permissions d'accès au périphérique `/dev/kvm` pour empêcher les utilisateurs non autorisés d'interagir avec l'hyperviseur.

---
[Source](https://www.bleepingcomputer.com/news/linux/new-januscape-linux-kernel-flaw-allows-vm-escape-on-intel-amd-devices/){:target="_blank"}
