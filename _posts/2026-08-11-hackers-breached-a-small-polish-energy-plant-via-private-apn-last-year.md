---
title: 'Hackers breached a small Polish energy plant via private APN last year'
date: 2026-08-11
permalink: /posts/2026/08/11/hackers-breached-a-small-polish-energy-plant-via-private-apn-last-year/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque inédite contre une centrale thermique polonaise via un APN privé

Fin 2025, un groupe de pirates informatiques (probablement lié au groupe Electrum) a infiltré le réseau opérationnel (OT) d’une centrale de cogénération polonaise en exploitant une vulnérabilité de réseau mobile. Cette intrusion a permis d'arrêter une turbine à vapeur et le système de traitement des eaux, bien que les services aient pu être rétablis rapidement.

**Points clés :**
*   **Vecteur d'attaque novateur :** Utilisation d'un APN (Access Point Name) privé comme passerelle pour se déplacer latéralement entre différents sites industriels.
*   **Méthodologie :** Les assaillants ont compromis un pare-feu FortiGate sur un premier site, utilisé un routeur cellulaire Teltonika pour atteindre l'APN privé, puis scanné le réseau à la recherche d'équipements exposés.
*   **Cibles OT :** Les attaquants ont pris le contrôle de contrôleurs programmables (PLC) de marque WAGO et Siemens, les basculant en mode « STOP » et verrouillant l'accès par mot de passe.
*   **Destruction de preuves :** Les attaquants ont délibérément corrompu ou réinitialisé les journaux et les équipements (pare-feu, routeurs, contrôleurs) pour entraver l'analyse forensique.

**Vulnérabilités identifiées :**
*   **Absence d'isolation client :** L'APN privé permettait une communication libre entre tous les appareils connectés.
*   **Exposition réseau :** Interface web d'un automate (WAGO PFC200) exposée directement sur le réseau APN.
*   **Configuration faible :** Utilisation d'identifiants administrateurs par défaut sur les équipements industriels.
*   **Services non sécurisés :** Protocoles d'administration (SSH/Telnet) activés et accessibles sans filtrage strict.

**Recommandations :**
*   **Zéro confiance (Zero Trust) :** Considérer les APN privés comme des réseaux externes non sécurisés.
*   **Isolation :** Activer impérativement l'isolation entre les clients au sein d'un APN privé.
*   **Filtrage :** Implémenter des listes d'autorisation (*allowlists*) pour restreindre strictement le trafic entre les passerelles APN et les systèmes OT.
*   **Durcissement :** Désactiver les services d'administration à distance (SSH, Telnet) lorsqu'ils ne sont pas nécessaires et bannir l'usage des identifiants par défaut sur tous les PLC et routeurs industriels.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-breached-a-small-polish-energy-plant-via-private-apn-last-year/){:target="_blank"}
