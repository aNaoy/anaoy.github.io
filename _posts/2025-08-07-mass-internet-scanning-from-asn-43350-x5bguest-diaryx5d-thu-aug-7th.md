---
title: 'Mass Internet Scanning from ASN 43350 &#x5b;Guest Diary&#x5d;, (Thu, Aug 7th)'
date: 2025-08-07
permalink: /posts/2025/08/07/mass-internet-scanning-from-asn-43350-x5bguest-diaryx5d-thu-aug-7th/
tags:
- veille-cyber
- sans-isc
---
## Anomalie du trafic Internet : Le rôle de l'ASN 43350

Une analyse de trafic sur trois mois d'un capteur DShield déployé dans AWS a révélé une activité de scan Internet exceptionnellement élevée, provenant majoritairement du Panama. Plus de 65% du trafic total a été attribué à cette région, dépassant la somme de toutes les autres localités combinées.

Les pics de trafic massifs sur quelques jours spécifiques ont été identifiés comme la cause de ce volume. L'analyse des adresses IP responsables a mis en évidence qu'une grande partie de cette activité (59,4%) provenait du sous-réseau 141.98.80.0/24. Neuf des dix adresses IP les plus actives appartenaient au fournisseur d'accès à Internet (FAI) néerlandais "NForce Entertainment B.V.".

L'Autonomous System Number (ASN) 43350, associé à NForce Entertainment, a généré 71,6% des journaux du capteur. Ce FAI semble louer son espace IP à des fournisseurs de VPN et de proxy, comme Flyservers S.A., basé au Panama, qualifié de FAI à "risque de fraude potentiellement très élevé" par Scamalytics. L'activité de NForce Entertainment est fréquemment liée au phishing, aux malwares et aux scans. La nature de leur régulation aux Pays-Bas limiterait la pression pour révoquer l'utilisation de leurs services par des acteurs malveillants.

### Points Clés :

*   **Origine du trafic anormal :** Le Panama est identifié comme la source de plus de 65% du trafic malveillant ciblant le capteur DShield.
*   **Sous-réseau critique :** Le sous-réseau 141.98.80.0/24 est responsable de près de 60% du trafic total.
*   **FAI impliqué :** NForce Entertainment B.V. est le FAI principal, et son ASN 43350 représente la majorité du trafic détecté.
*   **Cause probable :** L'utilisation de l'espace IP par des services tiers comme Flyservers S.A., un fournisseur de VPN au Panama, est suspectée.
*   **Nature de l'activité :** L'activité est associée au phishing, aux malwares et aux scans.

### Vulnérabilités et Recommandations :

Aucune vulnérabilité spécifique avec identifiant CVE n'est explicitement mentionnée dans l'article. Les recommandations visent à atténuer l'impact de ce trafic anormal :

*   **Signalement du trafic :** Marquer le trafic provenant de NForce Entertainment et, plus spécifiquement, de l'ASN 43350.
*   **Blocage RDP :** Interdire l'accès au protocole de bureau à distance (RDP) depuis Internet.
*   **Surveillance SSH :** Surveiller l'activité SSH provenant de l'ASN 43350 et configurer l'authentification par clé pour SSH.
*   **Implémentation WAF :** Utiliser un pare-feu d'applications Web (WAF) pour toutes les applications web et surveiller les requêtes suspectes provenant de toutes les sources.
*   **Alertes WAF :** Configurer des seuils d'alerte WAF pour un trafic élevé provenant d'une seule source.

Bien que le blocage global du trafic de NForce Entertainment ne soit pas toujours réalisable, il est recommandé de bloquer spécifiquement les services sensibles et les points d'accès HTTP(S) qui facilitent les connexions.

---
[Source](https://isc.sans.edu/diary/rss/32180){:target="_blank"}
