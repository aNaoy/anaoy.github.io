---
title: 'Ukrainian Network FDN3 Launches Massive Brute-Force Attacks on SSL VPN and RDP Devices'
date: 2025-09-02
permalink: /posts/2025/09/02/ukrainian-network-fdn3-launches-massive-brute-force-attacks-on-ssl-vpn-and-rdp-devices/
tags:
- veille-cyber
- hackernews
---
Voici les informations extraites de l'article :

**Des réseaux ukrainiens ciblent massivement les connexions sécurisées**

Entre juin et juillet 2025, des chercheurs en cybersécurité ont identifié un réseau basé en Ukraine, FDN3 (AS211736), menant des campagnes intensives d'attaques par force brute et de "password spraying" ciblant des appareils SSL VPN et RDP. Cette activité proviendrait d'une infrastructure plus large incluant d'autres réseaux ukrainiens (VAIZ-AS - AS61432, ERISHENNYA-ASN - AS210950) et un réseau basé aux Seychelles (TK-NET - AS210848). Ces réseaux échangent fréquemment des préfixes IP pour contourner les listes de blocage et poursuivre leurs activités malveillantes. Certains de ces préfixes IP ont des antécédents avec des réseaux russes et des fournisseurs de solutions d'hébergement "bulletproof" américains.

**Points clés:**

*   **Origine des attaques:** Réseau FDN3 (AS211736) en Ukraine, lié à d'autres réseaux ukrainiens et seychellois.
*   **Méthodes utilisées:** Attaques par force brute et "password spraying".
*   **Cibles:** Appareils SSL VPN et RDP.
*   **Période d'activité:** Juin et juillet 2025.
*   **Objectif potentiel:** Accès initial aux réseaux d'entreprise, souvent utilisé par des groupes de ransomware-as-a-service (RaaS).
*   **Stratégie:** Échange de préfixes IP entre réseaux pour échapper aux blocages, utilisation de sociétés écrans pour l'hébergement "bulletproof".
*   **Lien suspecté:** Association avec une société russe (Alex Host LLC) et des fournisseurs d'hébergement "bulletproof" connus pour héberger des infrastructures malveillantes.

**Vulnérabilités:**

L'article ne mentionne pas de CVE spécifiques pour les vulnérabilités exploitées. Cependant, les cibles (SSL VPN et RDP) sont des points d'entrée courants pour les attaques. Les méthodes de force brute et de "password spraying" exploitent des mots de passe faibles ou réutilisés.

**Recommandations:**

Bien que l'article ne fournisse pas de recommandations directes, les pratiques suivantes sont implicitement suggérées pour atténuer ce type de menaces :

*   **Renforcement des politiques de mots de passe:** Utiliser des mots de passe forts, uniques et complexes pour tous les accès, y compris VPN et RDP.
*   **Authentification multifacteur (MFA):** Implémenter l'MFA pour tous les accès, en particulier pour les VPN.
*   **Surveillance des journaux d'accès:** Examiner et surveiller régulièrement les journaux d'accès aux VPN et RDP pour détecter toute activité suspecte (tentatives de connexion multiples, échecs répétés).
*   **Gestion des accès:** Appliquer le principe du moindre privilège et révoquer les accès inutiles.
*   **Mises à jour et correctifs:** S'assurer que les dispositifs VPN et les configurations RDP sont à jour avec les derniers correctifs de sécurité.
*   **Filtrage IP et blocage:** Mettre en place des mesures de sécurité au niveau du réseau pour bloquer les adresses IP ou les plages d'adresses connues pour être malveillantes, bien que les attaquants changent souvent de provenance.

---
[Source](https://thehackernews.com/2025/09/ukrainian-network-fdn3-launches-massive.html){:target="_blank"}
