---
title: 'Free Apps Are Quietly Turning Smart TVs Into Web-Scraping Proxies for AI'
date: 2026-06-06
permalink: /posts/2026/06/06/free-apps-are-quietly-turning-smart-tvs-into-web-scraping-proxies-for-ai/
tags:
- veille-cyber
- hackernews
---
### Les Smart TV transformées en nœuds de scraping pour l'IA

Des recherches récentes ont révélé que certains kits de développement logiciel (SDK), notamment celui de l'entreprise Bright Data, intègrent des applications gratuites pour transformer les appareils des consommateurs — dont les Smart TV — en nœuds de sortie pour un réseau de serveurs mandataires (proxy) résidentiels. Ce réseau est massivement utilisé pour le moissonnage de données (web-scraping) destiné à entraîner des modèles d'IA, exploitant la bande passante domestique des utilisateurs à leur insu ou via un consentement ambigu.

**Points clés :**
* **Infiltration :** Les appareils (Smart TV, smartphones) deviennent des relais pour du trafic externe, contournant souvent les mesures de sécurité locales.
* **Le modèle économique :** Bright Data revend l'accès à ces adresses IP résidentielles pour contourner les protections anti-bot des sites web, qui bloquent généralement les centres de données.
* **Risques techniques :** Sur iOS, le SDK peut contourner les VPN configurés et opérer en arrière-plan sans surveillance. Le canal de communication du SDK ne présente aucune authentification robuste, rendant ces appareils vulnérables.
* **Obsolescence du consentement :** Bien qu'un écran d'acceptation soit présent, les limites réelles de consommation (jusqu'à 200 Go/mois) et le comportement du SDK dépassent largement ce qui est annoncé aux utilisateurs.

**Vulnérabilités :**
* Absence d'authentification sur le canal de contrôle du SDK.
* Contournement des VPN sur les appareils mobiles.
* Absence de visibilité du trafic dans les outils de surveillance réseau standards.
*(Note : Aucune CVE spécifique n'est associée, car il s'agit d'un comportement métier légitime de l'application et non d'une faille logicielle classique).*

**Recommandations :**
* **Blocage DNS :** Utiliser des outils comme Pi-hole ou NextDNS au niveau du routeur pour bloquer les domaines de communication du SDK, notamment : `proxyjs.brdtnet.com`, `proxyjs.luminatinet.com`, `proxyjs.bright-sdk.com`, `clientsdk.bright-sdk.com` et `clientsdk.brdtnet.com`.
* **Audit d'applications :** Examiner les conditions d'utilisation des applications gratuites, particulièrement sur les Smart TV et appareils mobiles, pour détecter toute mention de partage de connexion ou de réseau "peer-to-peer".
* **Surveillance réseau :** Pour les entreprises, auditer les terminaux mobiles à la recherche de SDK de proxy tiers, tout en gardant à l'esprit que le trafic sur réseau mobile (4G/5G) échappe aux filtrages Wi-Fi internes.

---
[Source](https://thehackernews.com/2026/06/free-apps-are-quietly-turning-smart-tvs.html){:target="_blank"}
