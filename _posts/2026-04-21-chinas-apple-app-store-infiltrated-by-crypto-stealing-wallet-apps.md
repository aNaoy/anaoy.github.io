---
title: 'Chinas Apple App Store infiltrated by crypto-stealing wallet apps'
date: 2026-04-21
permalink: /posts/2026/04/21/chinas-apple-app-store-infiltrated-by-crypto-stealing-wallet-apps/
tags:
- veille-cyber
- bleepingcomp
---
### Infiltration de portefeuilles de cryptomonnaies sur l'App Store d'Apple

Une campagne malveillante baptisée « FakeWallet », associée à l'opération *SparkKitty*, a récemment exploité l'App Store d'Apple en Chine pour dérober des cryptomonnaies. Vingt-six applications frauduleuses, se faisant passer pour des portefeuilles légitimes (Metamask, Coinbase, Trust Wallet, Ledger), ont été identifiées. Ces applications étaient masquées sous des apparences de jeux ou de calculatrices pour contourner les restrictions locales.

**Points clés :**
*   **Méthodologie :** Utilisation de typosquatting et de branding usurpé pour tromper les utilisateurs.
*   **Technique d'infection :** Les applications redirigent les victimes vers des pages de phishing poussant à l'installation de profils de configuration d'entreprise (*provisioning profiles*), permettant le déploiement de logiciels malveillants par contournement de l'App Store.
*   **Vol de données :** Le code malveillant intercepte les phrases mnémoniques (seed phrases) lors de la configuration ou incite l'utilisateur à les saisir manuellement via de fausses interfaces de vérification.
*   **Impact :** Une fois la phrase de récupération obtenue, les attaquants peuvent restaurer le portefeuille sur leurs propres appareils et vider les fonds de manière irréversible.
*   **Statut :** Apple a supprimé les 26 applications concernées suite au signalement de Kaspersky.

**Vulnérabilités :**
Aucune CVE spécifique n'est associée, l'attaque repose sur l'abus de fonctionnalités légitimes d'iOS (profils de provisionnement d'entreprise) et sur l'ingénierie sociale plutôt que sur une faille logicielle directe.

**Recommandations :**
*   **Vérification rigoureuse :** Toujours vérifier l'identité de l'éditeur avant d'installer une application, même depuis un magasin officiel.
*   **Sources officielles :** Utiliser exclusivement les liens de téléchargement fournis directement sur les sites web officiels des services de cryptomonnaies.
*   **Sécurité des clés :** Ne jamais saisir sa phrase de récupération (seed phrase) sur une application ou un site web non reconnu ; une application légitime ne demande jamais ce code pour une « vérification ».
*   **Gestion des profils :** Être extrêmement vigilant face aux demandes d'installation de profils de configuration iOS, qui peuvent donner des accès privilégiés à des tiers malveillants.

---
[Source](https://www.bleepingcomputer.com/news/security/chinas-apple-app-store-infiltrated-by-crypto-stealing-wallet-apps/){:target="_blank"}
