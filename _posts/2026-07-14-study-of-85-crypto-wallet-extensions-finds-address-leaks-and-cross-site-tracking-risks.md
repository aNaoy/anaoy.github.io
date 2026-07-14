---
title: 'Study of 85 Crypto Wallet Extensions Finds Address Leaks and Cross-Site Tracking Risks'
date: 2026-07-14
permalink: /posts/2026/07/14/study-of-85-crypto-wallet-extensions-finds-address-leaks-and-cross-site-tracking-risks/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités de confidentialité dans les extensions de portefeuilles crypto

Une étude menée par la KU Leuven sur 85 extensions de navigateurs dédiées aux cryptomonnaies révèle que le fonctionnement standard de ces outils compromet l'anonymat des utilisateurs. Le problème ne réside pas dans des failles de piratage, mais dans une conception qui favorise le traçage et la corrélation d'identités.

**Points clés :**
* **Fuite de données :** Les portefeuilles communiquent des adresses publiques à des serveurs tiers, permettant de lier plusieurs adresses entre elles et de dresser un profil financier complet.
* **Persistance des accès :** La déconnexion d'un site web est souvent inefficace. Les autorisations d'accès à l'adresse restent actives malgré la fermeture de session ou le vidage des cookies, transformant l'adresse en traceur permanent.
* **Traçage inter-sites :** Certains portefeuilles permettent à des scripts tiers de lire l'adresse de l'utilisateur via des cadres invisibles (*iframes*), facilitant le recoupement entre une identité réelle (nom/email) et un profil crypto.
* **Réaction de l'industrie :** La majorité des éditeurs minimisent ces risques, arguant que ce comportement est inhérent à l'interopérabilité du Web3.

**Vulnérabilités identifiées :**
* **Fuite d'adresses multiples :** Regroupement d'adresses distinctes dans des requêtes réseau, permettant une corrélation immédiate.
* **Revocation défaillante :** Absence de commande réelle de révocation d'accès lors de la déconnexion.
* **Exploitation via iFrame :** Accès non autorisé aux données de portefeuille depuis des sites tiers intégrés.
*(Note : Aucune CVE spécifique n'est associée, car il s'agit de défauts de conception logicielle et non d'une vulnérabilité logicielle isolée).*

**Recommandations :**
* **Gestion manuelle des accès :** Vérifier régulièrement la liste des "sites connectés" dans les paramètres du portefeuille pour révoquer manuellement les autorisations obsolètes.
* **Isolation des activités :** Utiliser des portefeuilles distincts ou des profils de navigateur séparés pour isoler les différentes activités financières.
* **Prudence accrue :** Utiliser un portefeuille "jetable" pour les interactions avec des sites peu familiers afin d'éviter d'exposer vos actifs principaux à une corrélation d'identité.

---
[Source](https://thehackernews.com/2026/07/study-of-85-crypto-wallet-extensions.html){:target="_blank"}
