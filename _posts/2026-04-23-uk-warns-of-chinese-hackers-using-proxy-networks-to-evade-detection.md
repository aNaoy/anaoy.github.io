---
title: 'UK warns of Chinese hackers using proxy networks to evade detection'
date: 2026-04-23
permalink: /posts/2026/04/23/uk-warns-of-chinese-hackers-using-proxy-networks-to-evade-detection/
tags:
- veille-cyber
- bleepingcomp
---
### Menace accrue des botnets chinois : détournement d'appareils domestiques

Les agences de cybersécurité internationales, menées par le NCSC britannique, alertent sur l'utilisation croissante de réseaux de proxys massifs par des groupes de hackers liés à la Chine. Ces acteurs détournent des millions d'appareils grand public (routeurs SOHO, caméras IP, NAS) pour masquer leurs activités malveillantes, contourner la détection géographique et rendre inefficaces les blocages d'adresses IP statiques.

**Points clés :**
*   **Stratégie de dissimulation :** Les hackers font transiter leur trafic à travers des chaînes de nœuds compromis pour brouiller l'origine des attaques.
*   **Cibles privilégiées :** Appareils IoT et routeurs domestiques ou de petites entreprises.
*   **Groupes identifiés :** *Flax Typhoon* (botnet Raptor Train) et *Volt Typhoon* (KV-Botnet).
*   **Portée :** Des centaines de milliers d'appareils infectés utilisés pour viser des secteurs critiques (militaire, gouvernemental, défense, éducation).

**Vulnérabilités :**
*   L'article souligne l'exploitation massive d'appareils obsolètes ne recevant plus de correctifs de sécurité (notamment des routeurs Cisco et Netgear). 
*   *Note : Aucune CVE spécifique n'est mentionnée dans le rapport, l'exploitation reposant principalement sur l'utilisation d'appareils vulnérables non patchés et mal sécurisés.*

**Recommandations :**
*   **Sécurisation des accès :** Implémenter systématiquement l'authentification multifacteur (MFA).
*   **Architecture réseau :** Adopter des modèles « Zero Trust », utiliser des listes d'autorisation (allowlists) d'adresses IP et la vérification par certificats machine.
*   **Gestion du parc :** Cartographier précisément les équipements situés en périphérie de réseau et surveiller les flux entrants.
*   **Veille dynamique :** Délaisser les listes d'IP statiques au profit de flux de menaces dynamiques (Threat Intelligence) intégrant les indicateurs de compromission liés à ces réseaux de proxys.

---
[Source](https://www.bleepingcomputer.com/news/security/uk-warns-of-chinese-hackers-using-botnets-of-hijacked-consumer-devices-to-evade-detection/){:target="_blank"}
