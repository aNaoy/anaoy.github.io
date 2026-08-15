---
title: 'New Evooo1Bot Linux botnet turns routers into traffic relay nodes'
date: 2026-08-15
permalink: /posts/2026/08/15/new-evooo1bot-linux-botnet-turns-routers-into-traffic-relay-nodes/
tags:
- veille-cyber
- bleepingcomp
---
### Menace Evooo1Bot : Transformation de routeurs en relais de trafic

Evooo1Bot est un nouveau botnet modulaire basé sur Mirai qui cible les passerelles réseau et les appareils connectés (IoT). Il transforme les périphériques infectés en nœuds de relais SOCKS5 tout en offrant des fonctionnalités étendues de cyberattaque.

**Points clés :**
*   **Fonctionnalités avancées :** En plus de servir de proxy, le malware assure le vol d'identifiants, le scan SSH par force brute, l'exécution d'attaques DDoS (16 méthodes supportées) et l'installation d'un shell interactif.
*   **Persistance et évasion :** Utilise des techniques variées (systemd, cron, rc.local) pour se maintenir actif et intègre des mécanismes de détection pour éviter les sandboxes, les outils de sécurité et les honeypots.
*   **Communication :** Utilise des communications chiffrées (C2) sur le port 443.
*   **Cibles :** Large éventail d'équipements incluant des marques telles qu'Alcatel, NETGEAR, Tenda, Mitsubishi Electric, Telesquare, D-Link, Hikvision, TP-Link, Zyxel, ainsi que des environnements Kubernetes et Atlassian Confluence.

**Vulnérabilités :**
Bien que l'article mentionne l'exploitation de nombreuses vulnérabilités connues (notamment dans PHP-CGI, WSO2 et divers firmwares), il ne liste pas de CVE spécifiques. Le botnet utilise une bibliothèque d'exploits intégrée pour compromettre les appareils via leurs failles logicielles connues ou des accès par force brute.

**Recommandations :**
*   **Mise à jour :** Appliquer systématiquement les correctifs de firmware pour tous les appareils IoT.
*   **Gestion des accès :** Modifier les identifiants d'administration par défaut et désactiver les interfaces d'accès distant lorsqu'elles ne sont pas nécessaires.
*   **Cycle de vie :** Remplacer les équipements arrivés en fin de support par le constructeur, car ils ne reçoivent plus les correctifs de sécurité critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/new-evooo1bot-linux-botnet-turns-routers-into-traffic-relay-nodes/){:target="_blank"}
