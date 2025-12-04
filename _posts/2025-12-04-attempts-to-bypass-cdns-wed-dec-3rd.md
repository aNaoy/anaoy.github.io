---
title: 'Attempts to Bypass CDNs, (Wed, Dec 3rd)'
date: 2025-12-04
permalink: /posts/2025/12/04/attempts-to-bypass-cdns-wed-dec-3rd/
tags:
- veille-cyber
- sans-isc
---
**Tentatives de contournement des protections CDN**

Les réseaux de diffusion de contenu (CDN) sont couramment utilisés pour la protection DDoS et le filtrage de bots. Ils redirigent le trafic vers le serveur d'origine. Cependant, si l'adresse IP du serveur d'origine est découverte, un attaquant peut potentiellement contourner le CDN et l'atteindre directement.

Pour contrer cela, il est possible de restreindre l'accès aux seules adresses IP du CDN, bien que ces listes puissent être vastes et dynamiques. Une méthode plus fiable consiste à utiliser des en-têtes personnalisés spécifiques au CDN, dont la valeur est souvent aléatoire et vérifiée. L'utilisation d'en-têtes génériques identifiant le CDN est déconseillée car les attaquants peuvent les usurper facilement.

Des analyses récentes ont révélé une augmentation des requêtes incluant des en-têtes liés aux CDN, suggérant des tentatives actives de contournement. Parmi les en-têtes observés figurent :

*   **Cf-Warp-Tag-Id** : Associé au service VPN Cloudflare Warp.
*   **X-Fastly-Request-Id** : Utilisé par le CDN Fastly.
*   **X-Akamai-Transformed** : Ajouté par Akamai.
*   **X-T0Ken-Inf0** : Utilité inconnue, potentiellement lié à une authentification.
*   **x-sfdc-request-id** et **x-sfdc-lds-endpoints** : Utilisés par Salesforce pour le suivi des requêtes.
*   En-têtes commençant par "Xiao9-" : Utilisation inconnue.

**Points clés :**

*   Les CDN sont une première ligne de défense efficace mais ont une faiblesse si l'adresse IP du serveur d'origine est exposée.
*   Les attaques visent à contourner cette protection en renvoyant des en-têtes spécifiques aux CDN.

**Vulnérabilités :**

*   La principale faiblesse réside dans la possibilité d'identifier et d'atteindre le serveur d'origine directement, en contournant la protection CDN. L'article ne mentionne pas de CVE spécifiques, mais fait référence à des en-têtes potentiellement mal vérifiés ou usurpés.

**Recommandations :**

*   Restreindre l'accès au serveur d'origine aux seules adresses IP connues du CDN.
*   Implémenter et vérifier des en-têtes personnalisés uniques et aléatoires fournis par le CDN pour chaque requête.
*   Éviter de se fier à des en-têtes génériques facilement imitables qui identifient simplement la présence d'un CDN.

---
[Source](https://isc.sans.edu/diary/rss/32532){:target="_blank"}
