---
title: 'Mass Internet Scanning from ASN 43350 &#x5b;Guest Diary&#x5d;, (Thu, Aug 7th)'
date: 2025-08-07
permalink: /posts/2025/08/07/mass-internet-scanning-from-asn-43350-x5bguest-diaryx5d-thu-aug-7th/
tags:
- veille-cyber
- sans-isc
---
### Anomalie de Trafic Internet Massif Identifiée

Une analyse des données d'un capteur DShield déployé sur AWS a révélé une activité de scan Internet massive provenant d'un fournisseur unique. Sur les trois derniers mois, une seule localisation, le Panama, a représenté plus de 65% du trafic total dirigé vers le capteur. Cette concentration de trafic est inhabituelle, dépassant le volume combiné de toutes les autres origines.

Des pics de trafic significatifs ont été observés certains jours, chacun étant attribué à une adresse IP différente. Cependant, une tendance plus large s'est dégagée : six des dix adresses IP les plus actives provenaient d'un même sous-réseau (/24), spécifiquement 141.98.80.0/24, responsable de près de 60% des logs collectés. De plus, neuf des dix principales adresses IP appartenaient au même fournisseur d'accès Internet (FAI), NForce Entertainment B.V.

L'étude a ensuite identifié que le numéro de système autonome (ASN) 43350, appartenant à NForce Entertainment, était à l'origine de 71,6% des logs du capteur. NForce Entertainment louerait son espace IP à des fournisseurs de VPN et de proxy, notamment Flyservers S.A. basée au Panama, que Scamalytics catégorise comme un FAI à "risque de fraude potentiellement très élevé". Cette activité est souvent associée à du phishing, des malwares et des scans. L'article suggère que le manque de surveillance réglementaire stricte aux Pays-Bas, pays d'origine de NForce Entertainment, permettrait à ces activités de persister.

**Points Clés :**

*   Anomalie de trafic Internet massif provenant du Panama.
*   Concentration de l'activité sur un ASN spécifique (43350) et un FAI (NForce Entertainment B.V.).
*   Association de cette activité à des pratiques malveillantes comme le phishing, les malwares et le scanning.
*   Implication potentielle de fournisseurs de VPN/proxy (Flyservers S.A.).
*   Facteurs atténuants potentiels liés à la réglementation aux Pays-Bas.

**Vulnérabilités / Menaces Identifiées :**

L'article ne mentionne pas de vulnérabilités spécifiques avec des identifiants CVE. Cependant, les comportements observés indiquent une menace liée à :

*   **Scanning de masse :** Exploitation des réseaux pour identifier des cibles potentielles.
*   **Tentatives d'intrusion :** Utilisation d'adresses IP à haut risque pour mener des attaques.
*   **Activités de malwares et de phishing :** Utilisation d'infrastructures compromises pour distribuer des malwares ou des campagnes de phishing.

**Recommandations :**

*   Marquer le trafic provenant de NForce Entertainment, et en particulier de l'ASN 43350.
*   Bloquer l'accès à la RDP (Remote Desktop Protocol) depuis Internet.
*   Surveiller l'activité SSH provenant de l'ASN 43350 et configurer l'authentification par clés SSH.
*   Mettre en place un pare-feu d'application web (WAF) pour toutes les applications web et surveiller les requêtes suspectes.
*   Établir un seuil d'alerte WAF pour un trafic élevé provenant d'une source unique.

---
[Source](https://isc.sans.edu/diary/rss/32180){:target="_blank"}
