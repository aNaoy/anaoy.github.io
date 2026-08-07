---
title: 'New NatJack Attacks Hijack TCP Sessions and Spoof DNS by Manipulating NAT Tables'
date: 2026-08-07
permalink: /posts/2026/08/07/new-natjack-attacks-hijack-tcp-sessions-and-spoof-dns-by-manipulating-nat-tables/
tags:
- veille-cyber
- hackernews
---
### NatJack : Vulnérabilité majeure des tables NAT

La classe d'attaques **NatJack** exploite une faille conceptuelle dans la gestion du NAT (Network Address Translation), où les systèmes partagent une infrastructure réseau commune. Un attaquant disposant d'un accès privilégié sur une machine située derrière le même NAT peut manipuler les entrées de suivi de connexion pour intercepter des sessions TCP, usurper des réponses DNS, exposer des ports externes ou saturer les tables NAT par déni de service.

**Points clés :**
*   **Vulnérabilité conceptuelle :** Les implémentations NAT supposent à tort que les hôtes d'un même réseau local ne chercheront pas à manipuler l'état des connexions de leurs voisins.
*   **Impact :** Détournement de trafic, spoofing DNS, exposition de ports et saturation des ressources réseau (DoS).
*   **Portée :** Concerne de nombreux produits réseau et systèmes d'exploitation, dont Windows et Linux.

**Vulnérabilités identifiées :**
*   **CVE-2026-56181 (Score 8.3) :** Erreur de validation d'origine dans le NAT de Windows (utilisé par Hyper-V), permettant l'usurpation depuis un réseau adjacent.
*   **CVE-2026-63913 (Score 8.2) :** Faille dans le *conntrack* de Netfilter (Linux), où des paquets malveillants forcent la fermeture prématurée d'entrées NAT actives.

**Recommandations :**
*   **Mises à jour :** Appliquer les correctifs de sécurité Windows et Linux (versions du noyau Linux corrigées : 5.10.259, 5.15.210, 6.1.176, 6.6.143, 6.12.93, 6.18.35, 7.0.12, 7.1 ; Windows : mises à jour spécifiques selon les versions listées).
*   **Isolation :** Séparer les charges de travail non fiables des systèmes critiques partageant la même infrastructure NAT.
*   **Sécurisation des flux :** Chiffrer systématiquement le trafic, même au sein des réseaux internes.
*   **Filtrage :** Utiliser l'IP Source Guard sur les équipements réseau lorsque cela est techniquement possible.

---
[Source](https://thehackernews.com/2026/08/new-natjack-attacks-hijack-tcp-sessions.html){:target="_blank"}
