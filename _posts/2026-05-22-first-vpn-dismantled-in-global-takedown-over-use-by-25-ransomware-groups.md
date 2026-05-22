---
title: 'First VPN Dismantled in Global Takedown Over Use by 25 Ransomware Groups'
date: 2026-05-22
permalink: /posts/2026/05/22/first-vpn-dismantled-in-global-takedown-over-use-by-25-ransomware-groups/
tags:
- veille-cyber
- hackernews
---
### Démantèlement de "First VPN" : un outil clé pour le cybercrime international

Une opération coordonnée par Europol et Eurojust a conduit au démantèlement de **First VPN**, un service de réseau privé virtuel conçu spécifiquement pour les activités criminelles. Actif depuis 2014, ce réseau permettait à ses utilisateurs de masquer leur identité lors d'attaques par rançongiciel, de fraudes à grande échelle et de vols de données.

**Points clés :**
* **Portée mondiale :** L'enquête a impliqué 17 pays, dont la France et les Pays-Bas. L'infrastructure comprenait 33 serveurs et 32 nœuds de sortie répartis dans 27 pays.
* **Usage criminel :** Au moins 25 groupes de rançongiciels (dont Avaddon) ont utilisé ce service pour effectuer des reconnaissances réseau et des intrusions.
* **Stratégie d'anonymisation :** Le service promettait une absence totale de logs, acceptait des paiements anonymes (Bitcoin, Webmoney, etc.) et proposait des protocoles avancés comme « VLESS » et « Reality » pour dissimuler le trafic VPN sous forme de trafic HTTPS classique.
* **Action des autorités :** L'opération a permis l'interpellation de l'administrateur en Ukraine, la saisie des domaines (1vpns[.]com/net/org) et la neutralisation de l'infrastructure serveurs.

**Vulnérabilités exploitées :**
* L'article ne mentionne pas de CVE spécifique, mais souligne l'usage détourné de protocoles de communication légitimes (**OpenConnect, WireGuard, VLESS, Reality**) pour contourner les mécanismes de sécurité et échapper à la surveillance des autorités.

**Recommandations :**
* **Surveillance du trafic :** Les entreprises doivent être vigilantes face au trafic masqué sous le protocole HTTPS, particulièrement si celui-ci provient de plages d'adresses IP suspectes ou non identifiées comme des passerelles d'accès distantes légitimes.
* **Analyse des flux :** Il est recommandé de renforcer l'inspection profonde des paquets (DPI) pour identifier les usages anormaux de protocoles VPN dissimulés (type *obfuscation*).
* **Mise à jour de la Threat Intelligence :** Intégrer les indicateurs de compromission (IoC) liés à ce démantèlement dans les solutions de sécurité (SIEM/IDS) pour détecter d'éventuelles tentatives de connexion persistantes vers cette infrastructure désormais contrôlée par les autorités.

---
[Source](https://thehackernews.com/2026/05/first-vpn-dismantled-in-global-takedown.html){:target="_blank"}
