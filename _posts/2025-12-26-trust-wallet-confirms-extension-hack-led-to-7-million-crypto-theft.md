---
title: 'Trust Wallet confirms extension hack led to $7 million crypto theft'
date: 2025-12-26
permalink: /posts/2025/12/26/trust-wallet-confirms-extension-hack-led-to-7-million-crypto-theft/
tags:
- veille-cyber
- bleepingcomp
---
**Le Pillage de Trust Wallet : Une Mise à Jour Compromise Provoque un Vol Massif**

Une mise à jour de l'extension Chrome de Trust Wallet, publiée le 24 décembre, a été compromise, entraînant le vol de 7 millions de dollars en cryptomonnaies. Les utilisateurs ont constaté que leurs portefeuilles étaient vidés peu après avoir interagi avec l'extension. Binance, par le biais de son fondateur Changpeng "CZ" Zhao, a confirmé l'incident et annoncé que Trust Wallet couvrirait les pertes, assurant que les fonds des utilisateurs étaient sécurisés. L'enquête porte sur la manière dont les pirates ont pu soumettre une nouvelle version malveillante.

Parallèlement, des acteurs malveillants ont lancé une campagne de phishing ciblant les utilisateurs paniqués, proposant une fausse correction de vulnérabilité qui visait en réalité à dérober leurs phrases de récupération de portefeuille.

**Points Clés :**

*   **Nature de l'attaque :** Attaque de la chaîne d'approvisionnement via une mise à jour compromise de l'extension de navigateur.
*   **Montant du vol :** Au moins 7 millions de dollars en cryptomonnaies.
*   **Extension affectée :** Version 2.68.0 de l'extension Chrome de Trust Wallet.
*   **Mécanisme d'exfiltration :** Code dissimulé dans un fichier JavaScript (4482.js) qui téléchargeait secrètement des données de portefeuille, notamment la phrase de récupération, vers un serveur externe (api.metrics-trustwallet[.]com).
*   **Campagne de phishing connexe :** Domaines frauduleux (comme fix-trustwallet[.]com) imitant Trust Wallet pour inciter les utilisateurs à révéler leur phrase de récupération.
*   **Impact :** Les utilisateurs de l'extension Chrome version 2.68.0 sont les seuls affectés ; les applications mobiles et autres versions d'extensions de navigateur ne sont pas concernées.

**Vulnérabilités :**

*   Une version malveillante (2.68.0) de l'extension Chrome de Trust Wallet a été distribuée, contenant du code caché pour exfiltrer des données sensibles. Le détail spécifique de la vulnérabilité n'est pas associé à un numéro CVE dans l'article.

**Recommandations :**

*   **Mise à jour immédiate :** Les utilisateurs de l'extension Chrome de Trust Wallet doivent impérativement désactiver la version 2.68.0 et mettre à jour vers la version 2.69. Il est conseillé de ne pas ouvrir l'extension avant la mise à jour.
*   **Processus de mise à jour sécurisé :** Se rendre dans les paramètres d'extensions du navigateur Chrome, désactiver Trust Wallet, activer le "mode développeur", puis cliquer sur "Mettre à jour". Vérifier que la version est la 2.69.
*   **Déplacer les fonds :** Les utilisateurs dont les portefeuilles pourraient avoir été compromis doivent immédiatement transférer les fonds restants vers un nouveau portefeuille créé avec une phrase de récupération fraîche.
*   **Considérer les phrases de récupération exposées comme non sécurisées :** Toute phrase de récupération qui aurait pu être exposée suite à l'incident doit être traitée comme définitivement compromise.
*   **Vigilance face au phishing :** Se méfier des sites prétendant offrir des correctifs et ne jamais partager sa phrase de récupération via des formulaires en ligne.

---
[Source](https://www.bleepingcomputer.com/news/security/trust-wallet-confirms-extension-hack-led-to-7-million-crypto-theft/){:target="_blank"}
