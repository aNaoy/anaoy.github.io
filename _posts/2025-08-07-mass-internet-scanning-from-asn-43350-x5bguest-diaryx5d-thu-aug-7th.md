---
title: 'Mass Internet Scanning from ASN 43350 &#x5b;Guest Diary&#x5d;, (Thu, Aug 7th)'
date: 2025-08-07
permalink: /posts/2025/08/07/mass-internet-scanning-from-asn-43350-x5bguest-diaryx5d-thu-aug-7th/
tags:
- veille-cyber
- sans-isc
---
**Anomalie de Trafic Scanné depuis Panama**

Une analyse des données collectées par un capteur DShield durant trois mois a révélé une concentration de trafic de scan et d'attaques anormalement élevée provenant du Panama. Plus de 65% du trafic total a été attribué à cette localisation, surpassant la somme de toutes les autres régions combinées. Des pics de trafic massifs ont été identifiés, principalement causés par des adresses IP uniques au cours de journées spécifiques.

**Points Clés :**

*   Le Panama a représenté plus de 65% du trafic analysé ciblant le capteur DShield.
*   Une grande partie de cette activité provenait d'un sous-réseau (/24) spécifique (141.98.80.0/24), responsable de 59,4% des logs.
*   L'Autonomous System Number (ASN) 43350, identifié comme appartenant à NForce Entertainment B.V., a été la source de 71,6% du trafic total.
*   NForce Entertainment est suspecté de louer son espace IP à des fournisseurs de VPN et de proxy, dont Flyservers S.A. au Panama, classé comme un ISP à "risque de fraude potentiellement très élevé".
*   L'activité de NForce Entertainment est fréquemment associée au phishing, aux malwares et aux scans.

**Vulnérabilités / Risques identifiés :**

*   L'utilisation d'espace IP loué à des fournisseurs de services à haut risque de fraude par des acteurs malveillants.
*   L'opacité et le manque de régulation stricte pour certains fournisseurs d'accès à Internet (ISP) dans leur pays d'origine (Pays-Bas pour NForce Entertainment).
*   L'exposition potentielle via des services comme le Bureau à distance (RDP).

**Recommandations :**

*   Marquer le trafic provenant de NForce Entertainment et de l'ASN 43350.
*   Bloquer l'accès à distance au Bureau (RDP) depuis Internet.
*   Surveiller l'activité SSH provenant de l'ASN 43350 et privilégier l'authentification par clé.
*   Mettre en place un pare-feu d'applications Web (WAF) pour toutes les applications web et surveiller les requêtes suspectes.
*   Configurer des alertes WAF pour un trafic élevé provenant d'une seule source.

---
[Source](https://isc.sans.edu/diary/rss/32180){:target="_blank"}
