---
title: 'CryptoJS Weak RNG Behind $5.7 Million in Drains Affects Five Crypto Wallet Apps'
date: 2026-08-06
permalink: /posts/2026/08/06/cryptojs-weak-rng-behind-57-million-in-drains-affects-five-crypto-wallet-apps/
tags:
- veille-cyber
- hackernews
---
### Failles dans CryptoJS : 5,7 millions de dollars dérobés via des portefeuilles cryptos

Une vulnérabilité critique au sein de la bibliothèque JavaScript **CryptoJS** a permis le vol d'au moins 5,7 millions de dollars en cryptomonnaies. La fonction `CryptoJS.lib.WordArray.random()` générait des clés privées et des phrases de récupération (seed phrases) avec une entropie extrêmement faible, rendant ces dernières facilement devinables par des attaquants.

**Points clés :**
*   **Vulnérabilité :** L'entropie réduite (passant de 2^128/256 à 2^39/47) permet une énumération rapide des clés sur du matériel informatique standard.
*   **Historique :** Le problème provient d'un retour en arrière dans le code de la bibliothèque (version 3.3.0) qui a réintroduit un générateur de nombres aléatoires faible. La correction définitive n'a été établie qu'à partir de la version 4.0.0.
*   **Impact :** Cinq applications identifiées (RRWallet, Bexo Wallet, NanChat, Bitcoin Libre, Milo). D'autres applications, désormais retirées des stores, pourraient également être concernées.

**Vulnérabilité associée :**
*   **CVE :** GHSA-rg76-677x-56q9 (Score CVSS : 9.0 - Critique).

**Recommandations :**
*   **Action immédiate :** Si vous avez généré une phrase de récupération avec l'une des applications concernées (ou une version obsolète), considérez vos fonds comme compromis.
*   **Migration :** Créer immédiatement un nouveau portefeuille sécurisé (via une solution matérielle ou un logiciel à jour) et transférer les fonds vers cette nouvelle adresse.
*   **Attention :** Une simple mise à jour de l'application ne suffit pas à sécuriser une phrase de récupération déjà générée, car l'entropie faible est ancrée dans la clé elle-même.
*   **Vérification :** Utiliser l'outil de vérification mis à disposition sur [illbloom.org](https://illbloom.org/) pour vérifier si une adresse est présente dans les jeux de données compromis.

---
[Source](https://thehackernews.com/2026/08/cryptojs-weak-rng-behind-57-million-in.html){:target="_blank"}
