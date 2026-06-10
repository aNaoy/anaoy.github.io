---
title: 'China-linked JDY botnet expands targeting of U.S. military networks'
date: 2026-06-10
permalink: /posts/2026/06/10/china-linked-jdy-botnet-expands-targeting-of-us-military-networks/
tags:
- veille-cyber
- bleepingcomp
---
### Expansion du botnet JDY : Menace ciblée contre les réseaux militaires américains

Le botnet JDY, lié à des acteurs malveillants chinois (notamment Volt Typhoon), a vu sa capacité doubler, passant de 650 à plus de 1 500 appareils compromis. Contrairement à un réseau de botnet classique, JDY se spécialise dans la reconnaissance distribuée et le fingerprinting (identification d'empreintes) pour permettre à des groupes APT de cibler rapidement les infrastructures vulnérables après la publication de nouvelles failles.

**Points clés :**
* **Cible privilégiée :** Les réseaux militaires américains et entités associées.
* **Fonctionnement :** Utilise des services Tor cachés pour son infrastructure de commande et contrôle (C2). Les nœuds effectuent du scan TCP/UDP/SSL, la collecte de bannières et de certificats TLS.
* **Technique avancée :** Capacité à effectuer des scans SYN haute vitesse et furtifs lorsque le malware dispose de privilèges root ou administrateur.
* **Équipements touchés :** Divers appareils SOHO et IoT (Cisco, Hikvision, Ubiquiti, DrayTek, Linksys, etc.).

**Vulnérabilités :**
* Le botnet est conçu pour réagir quasi instantanément à toute nouvelle divulgation de faille. Un exemple récent documenté est le ciblage de la vulnérabilité **CVE-2026-35616** concernant FortiClient EMS.

**Recommandations :**
* **Mises à jour :** Maintenir les routeurs, pare-feux et appareils IoT à jour avec les derniers correctifs de sécurité.
* **Réduction de la surface d'attaque :** Désactiver les interfaces d'administration exposées inutilement sur internet.
* **Gestion des accès :** Restreindre l'accès à la gestion à distance et remplacer systématiquement les identifiants par défaut.
* **Surveillance :** Surveiller les comportements suspects de trafic sortant à partir des appareils de périphérie (edge devices), pouvant indiquer qu'ils sont utilisés pour des scans de reconnaissance.

---
[Source](https://www.bleepingcomputer.com/news/security/china-linked-jdy-botnet-expands-targeting-of-us-military-networks/){:target="_blank"}
