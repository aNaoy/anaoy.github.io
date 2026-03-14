---
title: 'AppsFlyer Web SDK hijacked to spread crypto-stealing JavaScript code'
date: 2026-03-14
permalink: /posts/2026/03/14/appsflyer-web-sdk-hijacked-to-spread-crypto-stealing-javascript-code/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement du SDK Web AppsFlyer

Le SDK Web d'AppsFlyer, utilisé par 15 000 entreprises pour l'analyse marketing, a été temporairement détourné pour diffuser un code malveillant de type "crypto-stealer". Cette attaque par chaîne d'approvisionnement a permis d'injecter un script JavaScript obfusqué interceptant les adresses de portefeuilles de cryptomonnaies saisies par les utilisateurs pour les remplacer par celles des attaquants.

**Points clés :**
* **Nature de l'attaque :** Injection de code malveillant via le domaine officiel `websdk.appsflyer.com`.
* **Impact :** Ciblage des transactions Bitcoin, Ethereum, Solana, Ripple et TRON sur les sites utilisant le SDK.
* **Chronologie :** Activité suspecte détectée entre le 9 et le 11 mars 2026, suite à un incident lié au registraire de domaine d'AppsFlyer.
* **Portée :** Le SDK mobile reste épargné ; seule une partie des sites utilisant la version Web a été exposée.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée à cet incident, celui-ci résultant d'une compromission de la chaîne d'approvisionnement (fournisseur tiers) plutôt que d'une vulnérabilité logicielle classique.

**Recommandations :**
* **Audit des logs :** Examiner les journaux de télémétrie à la recherche de requêtes API suspectes provenant de `websdk.appsflyer.com` durant la période concernée.
* **Gestion des versions :** Si des comportements anormaux persistent, rétrograder vers une version du SDK préalablement validée comme saine.
* **Surveillance proactive :** Les organisations utilisant des SDK tiers doivent renforcer leur surveillance des dépendances externes pour détecter toute exécution de code non autorisée dans le navigateur des utilisateurs finaux.

---
[Source](https://www.bleepingcomputer.com/news/security/appsflyer-web-sdk-used-to-spread-crypto-stealer-javascript-code/){:target="_blank"}
