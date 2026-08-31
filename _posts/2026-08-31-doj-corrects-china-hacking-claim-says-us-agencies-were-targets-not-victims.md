---
title: 'DoJ Corrects China Hacking Claim, Says U.S. Agencies Were Targets, Not Victims'
date: 2026-08-31
permalink: /posts/2026/08/31/doj-corrects-china-hacking-claim-says-us-agencies-were-targets-not-victims/
tags:
- veille-cyber
- hackernews
---
### Clarification sur les cyberattaques chinoises : Cibles versus victimes

Le ministère de la Justice américain (DoJ) a rectifié une déclaration initiale concernant les activités du groupe chinois **QTFY** (également connu sous le nom de QT et QTCYBER). Il est désormais établi que plusieurs agences gouvernementales américaines (NASA, Fed, etc.) ont été des **cibles** de reconnaissance, et non nécessairement des **victimes** d'intrusions réussies.

**Points clés :**
* **Attributions :** QTFY opère pour le compte de la société chinoise *Nanjing Xinjiuwei Network Technology*, avec des financements liés au ministère chinois de la Sécurité d'État (MSS).
* **Modes opératoires :** Le groupe agit comme un « intendant technique » fournissant des outils de scan (**QScan**) et de routage réseau (**QTRouter**) pour faciliter l'espionnage.
* **Infrastructures :** Utilisation massive de réseaux ORB (*Operational Relay Box*) composés d'appareils IoT infectés et de serveurs VPS pour masquer l'origine des attaques et se fondre dans le trafic légitime.
* **Actions :** Le FBI a neutralisé les domaines associés à QScan et QTRouter, perturbant ainsi le réseau « Fast Labyrinth ».

**Vulnérabilités exploitées :**
* **CVE-2019-11510 :** Vulnérabilité critique dans les solutions Pulse Secure VPN, utilisée par le groupe pour tenter des intrusions dès 2019.

**Recommandations :**
* **Surveillance des périphériques IoT :** Compte tenu de leur utilisation comme nœuds de botnets, il est crucial de durcir la sécurité des objets connectés.
* **Gestion des vulnérabilités :** Appliquer systématiquement les correctifs de sécurité sur les équipements réseau et les passerelles VPN (type Pulse Secure) afin de prévenir l'exploitation de failles connues.
* **Segmentation et inspection :** Mettre en œuvre des mesures de contrôle pour détecter les flux réseau suspects qui tentent de dissimuler du trafic malveillant derrière des nœuds de relais (proxy) légitimes.

---
[Source](https://thehackernews.com/2026/08/doj-corrects-china-hacking-claim-says.html){:target="_blank"}
