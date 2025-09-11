---
title: 'DDoS defender targeted in 1.5 Bpps denial-of-service attack'
date: 2025-09-11
permalink: /posts/2025/09/11/ddos-defender-targeted-in-15-bpps-denial-of-service-attack/
tags:
- veille-cyber
- bleepingcomp
---
**Attaque massive visant un fournisseur de services de défense DDoS**

Un fournisseur européen de services de mitigation DDoS a été la cible d'une attaque par déni de service distribué (DDoS) d'une ampleur sans précédent, atteignant 1,5 milliard de paquets par seconde (Bpps). Cette attaque, l'une des plus importantes jamais divulguées publiquement en termes de débit de paquets, a été lancée à partir de milliers d'appareils IoT et de routeurs MikroTik compromis.

Le trafic malveillant était principalement une inondation UDP (UDP flood) émanant de plus de 11 000 réseaux uniques à travers le monde. L'objectif était d'épuiser les capacités de traitement du destinataire et de provoquer une interruption de service.

**Points clés :**

*   Une attaque DDoS a atteint 1,5 milliard de paquets par seconde.
*   L'attaque provenait de milliers d'appareils IoT et de routeurs MikroTik compromis.
*   Un fournisseur européen de services de mitigation DDoS a été ciblé.
*   FastNetMon a détecté et aidé à mitiger l'attaque.
*   L'attaque était principalement une inondation UDP.
*   Cette attaque fait suite à une autre attaque DDoS massive de 11,5 Tbps et 5,1 Bpps rapportée par Cloudflare.

**Vulnérabilités :**

*   L'attaque a exploité la compromission d'équipements terminaux de clients (CPE), notamment des appareils IoT et des routeurs. Ces appareils, lorsqu'ils sont compromis, peuvent être utilisés comme des plateformes d'envoi massif de trafic malveillant.
*   Bien qu'aucun CVE spécifique ne soit mentionné dans l'article, l'exploitation de vulnérabilités dans les firmwares de ces appareils est implicitement la cause de leur compromission. Les routeurs MikroTik, en particulier, ont été identifiés comme une source d'attaque.

**Recommandations :**

*   **Intervention au niveau des fournisseurs d'accès à Internet (FAI) :** Il est nécessaire de mettre en place des mécanismes de détection au niveau des FAI pour filtrer le trafic sortant malveillant avant qu'il n'atteigne une échelle massive.
*   **Filtrage proactif par les FAI :** Les FAI doivent jouer un rôle actif dans le filtrage du trafic sortant malveillant afin d'empêcher la "militarisation" à grande échelle du matériel grand public compromis.
*   **Mesures de mitigation chez le client :** Le fournisseur ciblé a utilisé des listes de contrôle d'accès (ACL) sur les routeurs périphériques pour contrer l'attaque, soulignant l'importance de telles mesures dans les installations de mitigation DDoS.

---
[Source](https://www.bleepingcomputer.com/news/security/ddos-defender-targeted-in-15-bpps-denial-of-service-attack/){:target="_blank"}
