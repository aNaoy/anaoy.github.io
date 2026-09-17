---
title: 'US takes down NightmareStresser DDoS-for-hire platform'
date: 2026-09-17
permalink: /posts/2026/09/17/us-takes-down-nightmarestresser-ddos-for-hire-platform/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement de la plateforme DDoS NightmareStresser

Le FBI a saisi les domaines de **NightmareStresser**, l'un des services de "DDoS-for-hire" (booter) les plus anciens et les plus actifs au monde, dans le cadre de l'opération internationale **PowerOFF**. Cette plateforme permettait à des utilisateurs peu expérimentés de louer des botnets composés de routeurs et d'objets connectés (IoT) compromis pour lancer des attaques par déni de service distribué.

**Points clés :**
* **Envergure :** NightmareStresser comptait plus de 566 000 utilisateurs inscrits et disposait de 52 serveurs dédiés.
* **Capacités :** La plateforme pouvait générer des attaques atteignant 200 Gbps, ciblant aussi bien les protocoles réseau (couche 4 : TCP/UDP) que les protocoles applicatifs (couche 7).
* **Historique :** Depuis 2022, le service a été impliqué dans des centaines de milliers d'attaques visant des écoles, des entreprises, des plateformes de jeux et des services gouvernementaux à travers le monde.
* **Opération PowerOFF :** Cette saisie s'inscrit dans une campagne coordonnée de longue haleine entre les autorités internationales pour neutraliser les infrastructures criminelles de "booters".

**Vulnérabilités :**
* L'infrastructure reposait sur l'exploitation massive d'objets connectés (IoT) et de routeurs grand public mal sécurisés, qui étaient détournés pour constituer des botnets à grande échelle. Bien qu'aucune CVE spécifique ne soit mentionnée dans cet article, ces botnets exploitent généralement les vulnérabilités classiques des firmwares IoT (défauts de configuration, identifiants par défaut ou failles non corrigées).

**Recommandations :**
* **Sécurisation des appareils IoT :** Changer systématiquement les mots de passe par défaut des routeurs et périphériques connectés.
* **Mises à jour :** Appliquer régulièrement les correctifs de sécurité sur le matériel réseau pour corriger les vulnérabilités connues pouvant être exploitées pour l'intégration dans des botnets.
* **Protection DDoS :** Les entreprises et services en ligne doivent mettre en place des solutions de filtrage du trafic (WAF, protection DDoS dédiée) pour atténuer les attaques volumétriques aux niveaux 4 et 7.

---
[Source](https://www.bleepingcomputer.com/news/security/fbi-seizes-nightmarestresser-service-linked-to-thousands-of-ddos-attacks/){:target="_blank"}
