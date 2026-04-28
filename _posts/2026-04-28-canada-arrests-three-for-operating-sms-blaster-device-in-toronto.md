---
title: 'Canada arrests three for operating “SMS blaster” device in Toronto'
date: 2026-04-28
permalink: /posts/2026/04/28/canada-arrests-three-for-operating-sms-blaster-device-in-toronto/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement d'un réseau de « SMS blasters » à Toronto

Les autorités canadiennes ont arrêté trois individus impliqués dans l'utilisation de « SMS blasters », des stations de base cellulaires illégitimes installées dans des véhicules. Ces dispositifs usurpent l'identité d'antennes légitimes pour intercepter les téléphones à proximité et diffuser massivement des messages de phishing (fraude bancaire ou gouvernementale).

**Points clés :**
* **Opération « Project Lighthouse » :** Enquête initiée suite à des activités suspectes à Toronto, ayant révélé environ 13 millions de tentatives d'interception réseau.
* **Fonctionnement :** Le matériel force les téléphones à se connecter au « faux » relais car il émet un signal plus puissant que les antennes réelles.
* **Risques collatéraux :** Outre le vol de données personnelles, les appareils connectés à ces dispositifs perdent l'accès au réseau de leur opérateur, ce qui bloque temporairement la capacité à contacter les services d'urgence.
* **Vulnérabilités :** Le protocole mobile est exploité via l'interception du signal radio. Il n'existe pas de CVE spécifique, car il s'agit d'une vulnérabilité structurelle liée à la conception des réseaux cellulaires (notamment l'exploitation des faiblesses des protocoles 2G/LTE/5G).

**Recommandations :**
* **Désactiver la 2G :** Sur Android, désactiver le support de la 2G permet d'atténuer certaines attaques basées sur les « Stingray » (bien que cela reste inefficace contre les attaques ciblant les signaux LTE/5G plus modernes).
* **Prudence avec les SMS :** Considérer les SMS comme un canal non sécurisé. Ne jamais cliquer sur des liens reçus par message.
* **Chiffrement :** Privilégier systématiquement des applications utilisant le chiffrement de bout en bout pour toutes les communications sensibles.

---
[Source](https://www.bleepingcomputer.com/news/security/canada-arrests-three-for-operating-sms-blaster-device-in-toronto/){:target="_blank"}
