---
title: 'Trust Wallet Chrome Extension Breach Caused $7 Million Crypto Loss via Malicious Code'
date: 2025-12-26
permalink: /posts/2025/12/26/trust-wallet-chrome-extension-breach-caused-7-million-crypto-loss-via-malicious-code/
tags:
- veille-cyber
- hackernews
---
**Vol de 7 millions de dollars suite à une faille dans l'extension Chrome de Trust Wallet**

Une "incident de sécurité" affectant la version 2.68 de l'extension Chrome de Trust Wallet a entraîné la perte d'environ 7 millions de dollars en cryptomonnaies. Les utilisateurs de cette version spécifique sont invités à la mettre à jour vers la version 2.69 dans les plus brefs délais. Les versions mobiles et les extensions pour d'autres navigateurs ne sont pas concernées.

**Points Clés :**

*   **Victimes et Pertes :** Environ 7 millions de dollars ont été perdus, affectant des centaines de victimes. Les fonds dérobés incluent du Bitcoin, de l'Ethereum et du Solana.
*   **Méthode d'Attaque :** Du code malveillant a été introduit dans la version 2.68 de l'extension Chrome, spécifiquement dans la logique d'analyse (analytics). Ce code récupérait les phrases mnémoniques des portefeuilles après leur déchiffrement avec le mot de passe ou la passkey de déverrouillage, puis les envoyait à un serveur contrôlé par l'attaquant (api.metrics-trustwallet[.]com). La bibliothèque open-source `posthog-js` a été exploitée pour exfiltrer ces données.
*   **Origine de la Faille :** La modification du code source interne de l'extension, et non une dépendance tierce compromise.
*   **Possibilité d'un Acteur Étatique ou d'un Initié :** Trust Wallet suggère qu'un acteur étatique pourrait être impliqué, ou que les attaquants ont pu obtenir un accès aux appareils de développeurs ou aux permissions de déploiement. Changpeng Zhao (Binance) a évoqué la possibilité d'une implication interne.
*   **Laundering des Fonds :** Les fonds volés ont été dirigés vers des plateformes d'échange centralisées (CEX) comme ChangeNOW, FixedFloat et KuCoin pour être blanchis.

**Vulnérabilités :**

*   Il n'y a pas de CVE spécifiquement mentionné dans l'article pour cette vulnérabilité. La faille réside dans une modification du code source de l'extension Trust Wallet elle-même, qui a permis l'injection de code malveillant.

**Recommandations :**

*   **Mise à jour Immédiate :** Les utilisateurs de l'extension Chrome de Trust Wallet doivent impérativement mettre à jour vers la version 2.69.
*   **Prudence avec les Communications :** S'abstenir d'interagir avec des messages ne provenant pas des canaux officiels de Trust Wallet.
*   **Vérification des Dépendances :** Bien que l'article stipule que ce n'est pas une dépendance tierce compromise, une vigilance générale quant aux bibliothèques utilisées reste pertinente.
*   **Utilisateurs Mobiles et Autres Navigateurs :** Ces utilisateurs ne sont pas concernés par cet incident particulier.

---
[Source](https://thehackernews.com/2025/12/trust-wallet-chrome-extension-bug.html){:target="_blank"}
