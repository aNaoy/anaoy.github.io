---
title: 'Dead Domain Discovery: Discover Expired or Unregistered Domains'
date: 2025-11-01
permalink: /posts/2025/11/01/dead-domain-discovery-discover-expired-or-unregistered-domains/
tags:
- veille-cyber
- zerodaysfans
---
### Découverte de Domaines Expirés pour la Sécurité

La découverte de domaines arrivés à expiration ou non enregistrés, appelés "dead domains", constitue une classe de vulnérabilités souvent négligée mais aux impacts potentiellement graves. Ces failles peuvent permettre des attaques telles que le Cross-Site Scripting (XSS), la divulgation d'informations sensibles, voire l'exécution de code à distance. Les attaquants exploitent ces faiblesses en enregistrant des domaines qui appartenaient autrefois à des entités légitimes.

Face à ce défi, des outils ont été développés pour aider les chercheurs en sécurité et les testeurs d'intrusion à identifier ces domaines de manière efficace. Ces outils visent à détecter les domaines expirés ou non enregistrés "à la volée".

**Points Clés et Outils :**

*   **Dead Domain Discovery - Extension Chrome :** Cette extension pour le navigateur Chromium identifie les domaines potentiellement abandonnés référencés sur les sites web, que ce soit dans des iframes, des scripts ou des sources CSS. Elle analyse les références en interrogeant des services DNS publics. Lorsqu'un domaine semble non enregistré ou expiré, une notification est envoyée à l'utilisateur. L'extension est disponible via le Chrome Web Store et son code est open source.

*   **Dead Domain Discovery DNS - Forwarder DNS :** Il s'agit d'un léger forwarder DNS UDP conçu pour signaler les domaines potentiellement expirés ou non enregistrés en observant les requêtes DNS sans réponse. Ce serveur re-tente les requêtes auprès de résolveurs secondaires et gère un mécanisme de temporisation pour éviter les alertes excessives, diffusant ses découvertes via divers canaux. Développé en Python, il est idéal pour être intégré dans des configurations de tests d'intrusion existantes ou utilisé comme service autonome. Son efficacité le rend adapté à une surveillance continue, et il est recommandé de l'exécuter sur des appareils à faible consommation.

**Vulnérabilités potentielles non spécifiées avec CVE :**

*   Cross-Site Scripting (XSS)
*   Divulgation d'informations
*   Exécution de code à distance (RCE)

**Recommandations :**

*   Utiliser l'extension Chrome "Dead Domain Discovery" pour une détection lors de la navigation et l'analyse de sites web.
*   Déployer le forwarder DNS "Dead Domain Discovery DNS" pour une surveillance au niveau du réseau, particulièrement utile lors de tests d'intrusion et pour une surveillance continue.
*   Installer l'extension Chrome via le Chrome Web Store ou manuellement via le dépôt GitHub.
*   Suivre les instructions du dépôt GitHub pour installer et configurer le forwarder DNS.

---
[Source](https://security.lauritz-holtmann.de/tools/dead-domain-discovery/){:target="_blank"}
