---
title: 'Chrome Web Store extensions caught stealing crypto, browser data'
date: 2026-08-30
permalink: /posts/2026/08/30/chrome-web-store-extensions-caught-stealing-crypto-browser-data/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de malwares via des extensions navigateurs compromises

Une campagne malveillante exploitant des extensions Google Chrome et Microsoft Edge a été identifiée. Des extensions initialement légitimes ont été rachetées par des attaquants, puis infectées via des mises à jour automatiques pour dérober des données sensibles.

**Points clés :**
* **Modus Operandi :** Les extensions utilisent une connexion WebSocket chiffrée avec des serveurs de commande et de contrôle (C2) pour injecter des scripts malveillants et contourner la politique de sécurité du contenu (CSP) des sites visités.
* **Cibles :** Utilisateurs de portefeuilles de cryptomonnaies (EVM, Solana, Tron), comptes de plateformes d'échange (Binance, Coinbase, etc.), réseaux sociaux (Facebook, LinkedIn) et données de navigation.
* **Techniques :** Utilisation de l'attaque "ClickFix" (fausses mises à jour), remplacement de sites officiels (Ledger, Trezor) par des pages de phishing, et interception des boutons de connexion de portefeuilles.
* **Vulnérabilités :** Bien qu'il s'agisse d'une campagne de type "Supply Chain" logicielle plutôt que d'une exploitation CVE spécifique, le mécanisme repose sur l'abus de confiance envers les extensions ayant déjà une base d'utilisateurs établie.

**Recommandations :**
* **Suppression immédiate :** Désinstaller toute extension listée dans le rapport (notamment celles liées aux cryptomonnaies ou à l'optimisation web).
* **Réinitialisation des accès :** Considérer tous les identifiants, mots de passe et jetons de session utilisés sur le navigateur comme compromis. Procéder à un changement immédiat des mots de passe.
* **Sécurisation des actifs :** Les détenteurs de cryptomonnaies ayant installé ces extensions doivent impérativement transférer leurs fonds vers un nouveau portefeuille sécurisé (nouveaux seed phrases).
* **Vigilance :** Avant d'installer une extension, vérifier sa réputation et la date de sa dernière mise à jour. Soyez prudent face aux changements soudains de permissions demandés par des extensions déjà installées.

---
[Source](https://www.bleepingcomputer.com/news/security/chrome-web-store-extensions-caught-stealing-crypto-browser-data/){:target="_blank"}
