---
title: 'Scans for Solana (Surfpool&#x3f;) Endpoints, (Mon, Aug 10th)'
date: 2026-08-10
permalink: /posts/2026/08/10/scans-for-solana-surfpoolx3f-endpoints-mon-aug-10th/
tags:
- veille-cyber
- sans-isc
---
### Campagne de reconnaissance sur les points de terminaison Solana

Des acteurs malveillants mènent actuellement une campagne de scan visant à identifier et énumérer des points de terminaison d'API Solana exposés, potentiellement liés à l'implémentation de développement « surfpool ».

**Points clés :**
* **Méthodologie :** Les attaquants ciblent le port 80 en supposant l'utilisation de proxys ou de passerelles API redirigeant le trafic vers les services Solana (généralement sur le port 8899).
* **Technique :** Les scans utilisent des requêtes JSON-RPC (ex: `getHealth`, `getVersion`) pour identifier la présence d'API blockchain.
* **Recherche de vulnérabilités :** La campagne inclut une recherche systématique de fichiers sensibles (ex: `.env`, `.env.bak`) afin d'extraire des identifiants ou des configurations exposées.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, mais l'exposition directe d'API de développement ou de fichiers de configuration (`.env`) constitue une faille critique de sécurité par configuration.

**Recommandations :**
* **Limitation de l'accès :** Ne jamais exposer les API de développement ou les nœuds blockchain directement sur Internet sans authentification stricte.
* **Filtrage :** Restreindre l'accès aux API via des listes blanches d'adresses IP ou via un VPN/tunnel sécurisé.
* **Sécurisation des secrets :** S'assurer que les fichiers de configuration (type `.env`) ne sont pas accessibles via le serveur web et qu'ils ne contiennent pas d'informations sensibles stockées en clair.
* **Surveillance :** Surveiller les journaux (logs) du serveur pour détecter des scans récurrents sur les chemins d'API courants et les fichiers de configuration.

---
[Source](https://isc.sans.edu/diary/rss/33230){:target="_blank"}
