---
title: 'Three Threat Groups Target Russian Enterprises With Backdoors, Ransomware, and Wipers'
date: 2026-09-16
permalink: /posts/2026/09/16/three-threat-groups-target-russian-enterprises-with-backdoors-ransomware-and-wipers/
tags:
- veille-cyber
- hackernews
---
### Campagne cybercriminelle contre les entreprises russes

Les entreprises russes sont actuellement la cible de trois groupes de menaces distincts — **NightEagle**, **Hacking Cat** et **Toy Ghouls** — utilisant des méthodes sophistiquées incluant des backdoors, des rançongiciels et des logiciels destructeurs (wipers).

#### Points clés
*   **NightEagle (APT-Q-95) :** Axé sur l'espionnage et le maintien d'une persistance à long terme. Le groupe privilégie l'accès via des identifiants VPN compromis et l'utilisation de tunnels réseau (Microsoft dev tunnels, rdp2tcp) pour le mouvement latéral.
*   **Hacking Cat :** Groupe activiste pro-ukrainien ayant pivoté vers des attaques destructrices. Ils déploient le trojan *Gorilla RAT* et diverses familles de rançongiciels (*Monkey*, *ClearWater*), utilisant parfois des outils de développement assistés par IA, parfois peu optimisés.
*   **Toy Ghouls :** Groupe motivé par l'appât du gain, ayant abandonné les outils publics (Babuk/LockBit) pour un développement interne. Ils utilisent désormais le *Bird Agent*, un backdoor personnalisé exploitant des protocoles de communication non conventionnels (MQTT et Matrix/Element).

#### Vulnérabilités exploitées
Les attaquants tirent parti de failles connues pour l'accès initial et l'escalade de privilèges :
*   **CVE-2020-0688 :** Vulnérabilité critique dans Microsoft Exchange utilisée par NightEagle.
*   **CVE-2019-0708 (BlueKeep) :** Exploitée pour obtenir des accès administrateur sur les systèmes ciblés.
*   **CVE-2021-26855 et CVE-2026-42897 :** Utilisées par Hacking Cat pour l'intrusion initiale sur les serveurs Exchange.

#### Recommandations
1.  **Sécurisation des accès :** Imposer l'authentification multifacteur (MFA) sur tous les accès VPN et interfaces de messagerie.
2.  **Gestion des correctifs :** Appliquer en priorité les mises à jour de sécurité pour les serveurs Microsoft Exchange et corriger les vulnérabilités liées aux services Bureau à distance (RDP).
3.  **Surveillance réseau :** Détecter les comportements suspects liés à l'utilisation de tunnels (dev tunnels, rdp2tcp, MQTT) et surveiller les connexions sortantes inhabituelles vers des plateformes comme Matrix.
4.  **Défense Active Directory :** Auditer les configurations Active Directory pour prévenir les attaques de type DCSync et limiter les privilèges d'administration locale.
5.  **Sauvegardes :** Maintenir des sauvegardes hors ligne, isolées du réseau, pour contrer l'impact des rançongiciels et des outils de type wiper.

---
[Source](https://thehackernews.com/2026/09/three-threat-groups-target-russian.html){:target="_blank"}
