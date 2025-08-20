---
title: 'Airtell Router Scans, and Mislabeled usernames, (Wed, Aug 20th)'
date: 2025-08-20
permalink: /posts/2025/08/20/airtell-router-scans-and-mislabeled-usernames-wed-aug-20th/
tags:
- veille-cyber
- sans-isc
---
**Analyse des tentatives d'accès aux routeurs Airtel et autres anomalies**

Des analyses automatisées de routeurs, potentiellement des modèles Airtel, sont détectées via des honeypots. Des identifiants inhabituels, tels que "Airtel@123" utilisé comme nom d'utilisateur, sont observés. Il est probable que "Airtel@123" soit en réalité le mot de passe par défaut du Wi-Fi de certains routeurs Airtel, le nom d'utilisateur par défaut étant généralement "admin".

D'autres tentatives d'accès incluent l'utilisation de chaînes de caractères interprétées comme des en-têtes HTTP, suggérant une possible scan de serveurs web. Des tentatives d'injection ou de manipulation via des caractères spéciaux ("username"&'apos;, '"root"') et des variations de noms d'utilisateur et mots de passe standards (usernane "$oot" and password "$dmin") sont également constatées.

**Points clés :**

*   Les honeypots collectent des tentatives d'accès aux routeurs, y compris des identifiants inhabituels.
*   "Airtel@123" semble être un mot de passe Wi-Fi par défaut pour certains routeurs Airtel, souvent associé à "admin" comme nom d'utilisateur.
*   Les scanners automatisés peuvent envoyer des en-têtes HTTP comme identifiants, confondant les honeypots de différents services.
*   Des tentatives d'injection de code ou de manipulation de listes d'identifiants sont observées.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est directement mentionnée. Cependant, l'utilisation de mots de passe par défaut et la facilité avec laquelle ces routeurs peuvent être ciblés par des scans indiquent une exposition due à des configurations par défaut faibles.

**Recommandations :**

*   Modifier immédiatement les mots de passe par défaut, y compris ceux du Wi-Fi.
*   Ne pas se fier aux noms d'utilisateur et mots de passe par défaut pour sécuriser l'accès aux appareils.
*   Surveiller les journaux d'accès pour détecter des activités suspectes ou des tentatives d'accès non autorisées.

---
[Source](https://isc.sans.edu/diary/rss/32216){:target="_blank"}
