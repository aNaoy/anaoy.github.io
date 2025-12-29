---
title: 'Trust Wallet says 2,596 wallets drained in $7 million crypto theft attack'
date: 2025-12-29
permalink: /posts/2025/12/29/trust-wallet-says-2596-wallets-drained-in-7-million-crypto-theft-attack/
tags:
- veille-cyber
- bleepingcomp
---
**Attaque par Extension Compromise : Vol de 7 Millions de Dollars en Cryptomonnaies**

Une extension de navigateur du portefeuille de cryptomonnaies Trust Wallet a été compromise peu avant Noël, entraînant la perte d'environ 7 millions de dollars auprès de près de 3 000 utilisateurs. La vulnérabilité provenait de la version 2.68.0 de l'extension Chrome, qui a été infectée par un fichier JavaScript malveillant. Ce fichier était destiné à exfiltrer des données sensibles des portefeuilles.

Les premières constatations indiquent que la version malveillante n'a pas suivi le processus de validation interne de Trust Wallet, mais a probablement été soumise via l'API du Chrome Web Store en utilisant une clé d'API compromise, contournant ainsi les contrôles de sécurité habituels. Le logiciel malveillant aurait été publié le 24 décembre 2025 à 12h32 UTC.

Suite à l'incident, Trust Wallet a révoqué toutes ses clés d'API de publication pour bloquer toute nouvelle soumission pendant deux semaines et a signalé le domaine d'exfiltration malveillant, qui a depuis été suspendu. Les attaquants ont ensuite lancé une campagne de phishing utilisant un site web imitant Trust Wallet pour inciter les utilisateurs à révéler leur phrase de récupération de portefeuille en échange d'une "mise à jour de sécurité".

**Points Clés :**

*   Plus de 200 millions de personnes utilisent Trust Wallet.
*   L'extension compromise était la version 2.68.0.
*   L'attaque a eu lieu juste avant Noël, le 24 décembre.
*   Environ 7 millions de dollars ont été dérobés.
*   Près de 3 000 portefeuilles ont été affectés (2 596 identifiés initialement).
*   Une campagne de phishing a exploité la panique post-attaque.

**Vulnérabilités :**

*   **Compromission de l'API du Chrome Web Store :** Une clé d'API de publication aurait été volée, permettant la soumission d'une version malveillante de l'extension de navigateur sans passer par les processus de validation habituels.
*   **Injection de JavaScript malveillant :** L'extension compromise contenait un script conçu pour voler les données sensibles des utilisateurs.

**Recommandations :**

*   **Mise à jour Immédiate :** Mettre à jour Trust Wallet vers la version 2.69 ou supérieure pour bloquer les tentatives de vol ultérieures.
*   **Ne Jamais Partager les Phrases de Récupération :** Les phrases de récupération (seed phrases) et les clés privées ne doivent jamais être partagées.
*   **Vérification des Liens et des Communications :** Vérifier attentivement les URL et utiliser uniquement les canaux de communication officiels de Trust Wallet.
*   **Prudence face aux Campagnes de Phishing :** Se méfier des sites web ou des messages prétendant offrir des mises à jour urgentes ou des compensations, surtout s'ils demandent des informations sensibles.
*   **Processus de Réclamation Transparent :** Trust Wallet a mis en place un formulaire de réclamation dédié pour les utilisateurs affectés, en insistant sur la vérification de la propriété des portefeuilles pour assurer un remboursement correct. Les utilisateurs sont invités à fournir des détails transactionnels mais pas leurs informations d'identification privées.

---
[Source](https://www.bleepingcomputer.com/news/security/trust-wallet-says-7-million-crypto-theft-attack-drained-2-596-wallets/){:target="_blank"}
