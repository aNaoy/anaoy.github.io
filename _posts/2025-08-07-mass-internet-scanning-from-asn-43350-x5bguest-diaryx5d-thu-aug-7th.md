---
title: 'Mass Internet Scanning from ASN 43350 &#x5b;Guest Diary&#x5d;, (Thu, Aug 7th)'
date: 2025-08-07
permalink: /posts/2025/08/07/mass-internet-scanning-from-asn-43350-x5bguest-diaryx5d-thu-aug-7th/
tags:
- veille-cyber
- sans-isc
---
**Anomalie de Trafic Internet Massif Provenant du Panama**

Une analyse des données de trafic d'un capteur DShield déployé dans AWS a révélé une concentration inhabituelle d'activité malveillante provenant du Panama. Pendant trois mois, plus de 65 % du trafic ciblant ce capteur émanait d'une source panaméenne, dépassant le volume combiné de toutes les autres origines.

Les pics de trafic les plus importants se sont avérés être causés par des adresses IP distinctes chaque jour, bien qu'une majorité d'entre elles soient issues du même sous-réseau (/24) et du même fournisseur d'accès à Internet (FAI), "NForce Entertainment B.V.". Ce FAI opère via le numéro de système autonome (ASN) 43350, qui représentait à lui seul 71,6 % des logs du capteur. NForce Entertainment est connu pour louer son espace IP à des fournisseurs de VPN et de proxys, comme Flyservers S.A., identifié par Scamalytics comme un FAI présentant un "risque de fraude potentiellement très élevé".

L'activité associée à ce FAI est fréquemment liée au phishing, aux malwares et aux scans. En tant que FAI néerlandais, il semble bénéficier d'une réglementation moins stricte, limitant la pression pour révoquer les services utilisés par des acteurs malveillants.

**Points Clés:**

*   Concentration massive de trafic malveillant provenant du Panama (65% du total).
*   Le sous-réseau 141.98.80.0/24 et l'ASN 43350 (NForce Entertainment B.V.) sont à l'origine d'une grande partie de cette activité.
*   Lien entre NForce Entertainment, Flyservers S.A. et des activités malveillantes (phishing, malwares, scans).
*   Manque de surveillance réglementaire aux Pays-Bas pour ce type d'activités.

**Vulnérabilités:**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est directement mentionnée dans l'article. Les vulnérabilités sous-jacentes sont liées aux méthodes d'exploitation des services exposés sur Internet et à l'utilisation d'infrastructures potentiellement compromises.

**Recommandations:**

*   Signaler le trafic provenant de NForce Entertainment, et en particulier de l'ASN 43350.
*   Bloquer l'accès à la RDP (Remote Desktop Protocol) depuis Internet.
*   Surveiller l'activité SSH provenant de l'ASN 43350 et configurer l'authentification par clé SSH.
*   Implémenter un pare-feu d'applications web (WAF) pour toutes les applications web et surveiller les requêtes suspectes.
*   Créer une alerte WAF pour un trafic élevé provenant d'une seule source.

---
[Source](https://isc.sans.edu/diary/rss/32180){:target="_blank"}
