---
title: 'Residential proxies evaded IP reputation checks in 78% of 4B sessions'
date: 2026-04-02
permalink: /posts/2026/04/02/residential-proxies-evaded-ip-reputation-checks-in-78-of-4b-sessions/
tags:
- veille-cyber
- bleepingcomp
---
### L'invisibilité des proxies résidentiels face à la réputation IP

Les systèmes de réputation IP classiques sont mis en échec par l'utilisation massive de proxies résidentiels dans les cyberattaques. Une analyse de GreyNoise sur 4 milliards de sessions malveillantes révèle que 78 % du trafic provenant de réseaux domestiques échappe aux listes de blocage, rendant la distinction entre utilisateurs légitimes et attaquants de plus en plus complexe.

**Points clés :**
* **Éphémérité :** Les adresses IP résidentielles sont utilisées très brièvement (89,7 % sont actives moins d'un mois) et tournent constamment, empêchant leur identification et leur catalogage à temps.
* **Diversité et volume :** Le trafic provient de 683 fournisseurs d'accès (FAI) différents, avec une forte concentration géographique en Chine, en Inde et au Brésil.
* **Origine du trafic :** Ce réseau repose sur deux écosystèmes : les botnets IoT et les appareils d'utilisateurs infectés par des logiciels (VPN gratuits, bloqueurs de publicité) qui revendent leur bande passante.
* **Nature des menaces :** Ces proxies servent principalement à la reconnaissance et au scan réseau. Seule une fraction infime (0,1 %) est utilisée pour des exploits directs, bien que certains visent le "credential stuffing" ou les accès VPN d'entreprise.
* **Résilience :** Même après le démantèlement de grands réseaux comme IPIDEA, le trafic se déplace rapidement vers d'autres infrastructures, démontrant une forte capacité de récupération.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, car il s'agit d'un problème structurel lié à l'abus de protocoles légitimes et à l'exploitation de terminaux domestiques infectés (IoT et postes de travail).

**Recommandations :**
* **Dépasser la réputation IP :** Abandonner l'IP comme signal de confiance principal.
* **Analyse comportementale :** Détecter les scans et sondages séquentiels provenant d'IP résidentielles changeantes.
* **Filtrage des protocoles :** Bloquer les protocoles inappropriés au sein des plages IP des FAI (ex: SMB).
* **Empreinte numérique :** Mettre en place le suivi des "fingerprints" d'appareils, qui persistent souvent malgré la rotation des adresses IP.

---
[Source](https://www.bleepingcomputer.com/news/security/residential-proxies-evaded-ip-reputation-checks-in-78-percent-of-4b-sessions/){:target="_blank"}
