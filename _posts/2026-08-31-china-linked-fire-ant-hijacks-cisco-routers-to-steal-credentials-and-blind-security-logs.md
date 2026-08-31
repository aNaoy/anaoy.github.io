---
title: 'China-Linked Fire Ant Hijacks Cisco Routers to Steal Credentials and Blind Security Logs'
date: 2026-08-31
permalink: /posts/2026/08/31/china-linked-fire-ant-hijacks-cisco-routers-to-steal-credentials-and-blind-security-logs/
tags:
- veille-cyber
- hackernews
---
### Expansion des cyber-espions Fire Ant : compromission d'infrastructures réseau Cisco

Le groupe de cyber-espionnage lié à la Chine, **Fire Ant**, a étendu ses capacités d'attaque au-delà des hyperviseurs VMware pour cibler des routeurs Cisco IOS XR, des serveurs TACACS et des systèmes de gestion Linux. L'objectif est de transformer ces équipements en plateformes de collecte pour intercepter le trafic, dérober des identifiants et masquer toute trace d'activité malveillante.

#### Points clés
*   **Contrôle du réseau :** En prenant le contrôle des routeurs, le groupe obtient une vision transversale du trafic réseau, facilitant le mouvement latéral vers des environnements critiques.
*   **Techniques d'évasion :** Les attaquants suppriment les journaux d'événements, filtrent les sorties de commandes CLI pour cacher leurs tunnels et désactivent les mécanismes de sécurité (SELinux).
*   **Persistance furtive :** Utilisation de logiciels malveillants sur mesure, de rootkits (Medusa, REPTILE) et de déguisements de processus (usurpation d'identité d'outils comme SentinelOne ou Zabbix).
*   **Développement d'outils :** 
    *   **TacTap :** Injection de bibliothèque dans le processus `tac_plus` pour capturer des identifiants.
    *   **BridgeAgent :** Porte dérobée Linux communiquant via TLS sur le port 443.

#### Vulnérabilités
*   Aucune CVE spécifique n'est mentionnée, car l'accès initial reste indéterminé. Toutefois, le groupe exploite une logique de conception système (injection de bibliothèques et détournement de flux d'exécution) pour contourner les contrôles d'intégrité standards des systèmes Cisco et Linux.

#### Recommandations
*   **Approche Forensique Multicouche :** Ne pas se fier à une seule source de télémétrie. Il est impératif de corréler les journaux système avec l'analyse de la mémoire, des disques, du trafic réseau et des configurations.
*   **Supervision des actifs critiques :** Traiter les routeurs, les serveurs d'authentification (TACACS) et les serveurs de gestion comme des actifs de sécurité de premier plan.
*   **Audit d'intégrité :** Vérifier régulièrement la présence de fichiers suspects, de processus aux noms trompeurs (ex: `/usr/bin/gnome-shell` sur un serveur) et de modifications inexpliquées dans les configurations ou les services système (`systemd`).
*   **Détection d'IoC :** Rechercher les indicateurs fournis (SHA1, noms de fichiers comme `acppid`, `libseconfd.so` ou la présence de clés XOR `0xEF` dans les fichiers journaux).

---
[Source](https://thehackernews.com/2026/08/china-linked-fire-ant-hijacks-cisco.html){:target="_blank"}
