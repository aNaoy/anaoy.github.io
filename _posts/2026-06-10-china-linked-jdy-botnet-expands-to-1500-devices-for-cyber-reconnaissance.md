---
title: 'China-Linked JDY Botnet Expands to 1,500+ Devices for Cyber Reconnaissance'
date: 2026-06-10
permalink: /posts/2026/06/10/china-linked-jdy-botnet-expands-to-1500-devices-for-cyber-reconnaissance/
tags:
- veille-cyber
- hackernews
---
### Expansion du botnet JDY : Une menace persistante pour l'infrastructure réseau

Le botnet JDY, lié à des acteurs étatiques chinois (notamment associés au groupe Volt Typhoon), a considérablement étendu ses capacités. Initialement une composante du « KV-botnet », il opère désormais de manière indépendante avec plus de 1 500 appareils compromis. Ce réseau est utilisé comme un outil industriel de reconnaissance, de cartographie et de détection de vulnérabilités « à la demande » pour identifier des cibles prioritaires.

**Points clés :**
*   **Infrastructure diversifiée :** Le botnet ne se limite plus aux routeurs Cisco, mais cible désormais une vaste gamme de matériel (Ubiquiti, Draytek, Hikvision, Linksys, etc.).
*   **Évitement des défenses :** En utilisant des appareils légitimes de type SOHO (petits bureaux/domicile) et IoT, les attaquants contournent les géofencings, les listes de blocage IP et se fondent dans le trafic réseau normal.
*   **Mode opératoire :** Les serveurs de commande et contrôle (C2) utilisent des nœuds Tor pour diriger les bots. Le malware, une fois lancé en mémoire pour éviter toute persistance sur disque, adapte sa méthode de scan selon ses privilèges (scan SYN haute vitesse avec accès root ou connexions standard).
*   **Réactivité :** Le botnet est capable d'analyser l'infrastructure mondiale quelques heures seulement après la divulgation publique de nouvelles vulnérabilités.

**Vulnérabilités :**
*   L'article mentionne l'exploitation de vulnérabilités « zero-day » ou récemment divulguées sur des périphériques de périphérie, citant notamment **CVE-2026-35616** comme exemple de vecteur d'infection.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer systématiquement les correctifs de sécurité sur tous les équipements réseau (routeurs, pare-feux) et objets connectés, en particulier ceux exposés sur Internet.
*   **Segmentation réseau :** Isoler les appareils IoT et SOHO du réseau critique pour limiter l'impact en cas de compromission.
*   **Surveillance du trafic :** Mettre en place une surveillance du trafic sortant inhabituel vers des nœuds Tor ou des serveurs inconnus, comportement typique des bots cherchant à communiquer avec leur C2.
*   **Durcissement :** Désactiver les services d'administration à distance (SSH, interface web) sur l'interface WAN des routeurs et périphériques réseau.

---
[Source](https://thehackernews.com/2026/06/china-linked-jdy-botnet-expands-to-1500.html){:target="_blank"}
