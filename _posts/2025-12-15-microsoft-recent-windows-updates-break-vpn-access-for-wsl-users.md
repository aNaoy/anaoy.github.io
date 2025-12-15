---
title: 'Microsoft: Recent Windows updates break VPN access for WSL users'
date: 2025-12-15
permalink: /posts/2025/12/15/microsoft-recent-windows-updates-break-vpn-access-for-wsl-users/
tags:
- veille-cyber
- bleepingcomp
---
**Mises à jour Windows impacting WSL et l'accès VPN**

Des mises à jour récentes de sécurité pour Windows 11 provoquent des dysfonctionnements dans l'accès réseau VPN pour les utilisateurs du Sous-système Windows pour Linux (WSL), particulièrement dans un contexte professionnel. Ce problème affecte les utilisateurs ayant installé les mises à jour KB5067036 (octobre 2025) et KB5072033 (décembre 2025), ainsi que toute mise à jour ultérieure. Les utilisateurs rencontrent des problèmes de connectivité avec certaines applications VPN tierces lorsque le mode réseau "mirrored" est activé, empêchant ainsi l'accès aux ressources de l'entreprise.

**Points Clés :**

*   Des mises à jour Windows récentes perturbent le fonctionnement du VPN pour les utilisateurs WSL.
*   Le problème concerne spécifiquement le mode réseau "mirrored" de WSL, introduit pour améliorer la compatibilité VPN.
*   Les utilisateurs reçoivent des erreurs de type "No route to host" dans WSL, alors que l'hôte Windows fonctionne correctement.
*   Le défaut provient de l'incapacité des interfaces réseau virtuelles des applications VPN à répondre aux requêtes ARP (Address Resolution Protocol).
*   Ce bug affecte principalement les solutions VPN d'entreprise comme OpenVPN et Cisco Secure Client.

**Vulnérabilités :**

Aucune CVE (Common Vulnerabilities and Exposures) spécifique n'est mentionnée dans l'article pour ce problème particulier. Le problème est décrit comme un défaut de fonctionnement causé par les mises à jour logicielles.

**Recommandations :**

*   Microsoft est au courant du problème et enquête activement.
*   Aucune solution de contournement ou délai pour une correction n'a encore été communiqué.
*   Il est conseillé de suivre les communications de Microsoft pour obtenir des informations supplémentaires lorsque celles-ci seront disponibles.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-recent-windows-updates-cause-wsl-networking-issues/){:target="_blank"}
