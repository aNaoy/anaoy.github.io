---
title: '/proxy/ URL scans with IP addresses, (Mon, Mar 16th)'
date: 2026-03-16
permalink: /posts/2026/03/16/proxy-url-scans-with-ip-addresses-mon-mar-16th/
tags:
- veille-cyber
- sans-isc
---
### Exploitation des services de métadonnées cloud via des proxys mal configurés

Des campagnes récentes de scan ciblent les services de métadonnées cloud (169.254.169.254) en utilisant des serveurs proxy mal configurés. L'objectif est d'extraire des identifiants de sécurité et des informations sensibles sur les instances cloud via des attaques de type SSRF (*Server-Side Request Forgery*).

**Points clés :**
* **Technique d'évasion :** Les attaquants tentent de contourner les filtres de sécurité en utilisant des formats d'adresses IP variés : adresses IPv4 mappées en IPv6 (préfixe `::ffff:/96`), formes longues avec des zéros explicites, ou conversion de l'adresse IP en entier long non signé.
* **Cible :** Le service de métadonnées de l'instance cloud, qui délivre des informations d'authentification IAM si l'accès est réussi.
* **Vulnérabilité sous-jacente :** Une configuration inadéquate des proxys (API gateways, équilibreurs de charge, WAF, proxys CORS). Même si le service de métadonnées "v2" protège contre les SSRF basiques, un proxy mal configuré peut servir de relais complet et contourner ces protections.

**Vulnérabilités associées :**
* **SSRF (Server-Side Request Forgery) :** Bien qu'aucune CVE spécifique ne soit mentionnée, cette technique exploite les failles de logique d'accès aux services internes de cloud.

**Recommandations :**
* **Audit de configuration :** Tester la robustesse de vos proxys, passerelles API et équilibreurs de charge en utilisant les listes de chemins identifiées dans l'article pour vérifier s'ils autorisent l'accès aux segments réseaux internes (notamment 169.254.169.254).
* **Renforcement du service de métadonnées :** S'assurer que l'accès aux métadonnées des instances cloud est configuré pour exiger la version 2 (IMDSv2), qui impose des en-têtes personnalisés et des méthodes de requête spécifiques.
* **Filtrage en sortie :** Restreindre strictement les requêtes sortantes que vos proxys peuvent effectuer vers des adresses IP link-local ou des plages privées non routables.

---
[Source](https://isc.sans.edu/diary/rss/32800){:target="_blank"}
