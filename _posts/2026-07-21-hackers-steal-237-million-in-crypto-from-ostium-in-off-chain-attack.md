---
title: 'Hackers steal $23.7 million in crypto from Ostium in off-chain attack'
date: 2026-07-21
permalink: /posts/2026/07/21/hackers-steal-237-million-in-crypto-from-ostium-in-off-chain-attack/
tags:
- veille-cyber
- bleepingcomp
---
# Vol de 23,7 millions de dollars sur la plateforme Ostium

La plateforme de trading décentralisée Ostium a subi une attaque informatique visant son infrastructure hors-chaîne (off-chain), entraînant le détournement de 23,75 millions de dollars en USDC depuis son coffre-fort de liquidités.

### Points clés
* **Méthode d'attaque :** Les assaillants ont compromis les flux de données externes (oracles) alimentant la plateforme en prix. En soumettant de faux rapports de prix, ils ont généré des profits artificiels via l'ouverture et la fermeture rapide de positions à fort levier.
* **Impact :** Les fonds du coffre-fort de liquidités ont été siphonnés. Les fonds déposés par les utilisateurs (collatéraux) ainsi que leurs positions de trading actives sont restés intacts, bien que temporairement gelés.
* **Blanchiment :** Les fonds volés ont été convertis en Ethereum, dont une grande partie a été transférée vers le mixeur de cryptomonnaies Tornado Cash.
* **Vulnérabilités :** Aucune CVE spécifique n'a été assignée, l'incident relevant d'une faille de sécurité dans l'infrastructure de gestion des flux de prix (off-chain) et non d'une vulnérabilité directe du contrat intelligent (smart contract) sur la blockchain Arbitrum.

### Recommandations
* **Sécurisation des oracles :** Renforcer la validation et la redondance des flux de données externes pour empêcher l'injection de prix manipulés.
* **Infrastructure décentralisée :** Auditer et durcir les systèmes hors-chaîne qui interagissent avec les protocoles décentralisés afin de limiter les points de défaillance uniques.
* **Réponse aux incidents :** Maintenir des protocoles de suspension automatique des transactions en cas d'anomalie détectée sur les prix, comme l'a fait Ostium en arrêtant les échanges moins d'une heure après l'attaque.
* **Analyse technique :** Il est conseillé aux développeurs de plateformes DeFi d'attendre le rapport post-mortem détaillé d'Ostium pour identifier des vecteurs d'attaque similaires au sein de leurs propres architectures.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-steal-237-million-in-crypto-from-ostium-in-off-chain-attack/){:target="_blank"}
