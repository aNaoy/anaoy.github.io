---
title: 'Hackers hijack npm packages with 2 billion weekly downloads in supply chain attack'
date: 2025-09-08
permalink: /posts/2025/09/08/hackers-hijack-npm-packages-with-2-billion-weekly-downloads-in-supply-chain-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque d'envergure sur la chaîne d'approvisionnement npm

Une attaque par détournement de compte de mainteneur de package a entraîné l'injection de code malveillant dans plusieurs librairies npm, cumulativement téléchargées plus de 2 milliards de fois par semaine. Les attaquants ont utilisé des emails de phishing se faisant passer pour le support npm, menaçant de bloquer les comptes s'ils ne mettaient pas à jour leurs informations d'authentification à deux facteurs (2FA). Ces faux messages redirigeaient vers des sites web frauduleux qui collectaient les identifiants des utilisateurs.

Le code injecté agit comme un intercepteur basé sur le navigateur, ciblant spécifiquement les transactions de cryptomonnaies sur des blockchains telles qu'Ethereum, Bitcoin, Solana, Tron, Litecoin et Bitcoin Cash. Il est capable de surveiller et de modifier les transactions en cours, redirigeant les fonds vers les portefeuilles des attaquants avant que la transaction ne soit validée par l'utilisateur. Cette manipulation se fait de manière discrète, affectant à la fois le contenu affiché aux utilisateurs, les appels d'API et ce que les applications perçoivent comme étant signé.

Plusieurs packages populaires ont été affectés, notamment debug (357,6 millions de téléchargements hebdomadaires), ansi-styles (371,41 millions) et chalk (299,99 millions), ainsi qu'une liste étendue de librairies connexes à la gestion des couleurs et des styles de texte en console.

**Points Clés :**

*   **Vaste portée :** Plus de 2 milliards de téléchargements hebdomadaires affectés par le biais de librairies npm compromises.
*   **Méthode d'attaque :** Phishing ciblant les mainteneurs de packages npm pour obtenir l'accès à leurs comptes.
*   **Malware :** Code injecté dans les packages agissant comme un intercepteur de transactions de cryptomonnaies dans le navigateur.
*   **Objectif :** Redirection des fonds et des approbations de transactions vers les portefeuilles des attaquants.
*   **Détournement de la chaîne d'approvisionnement :** L'attaque exploite la confiance accordée aux librairies populaires utilisées par de nombreux développeurs.

**Vulnérabilités :**

*   Absence de détails spécifiques concernant des identifiants CVE pour cette attaque particulière. Cependant, la vulnérabilité réside dans la compromission des identifiants des mainteneurs via le phishing et l'injection de code malveillant dans des packages légitimes.

**Recommandations :**

*   **Vigilance accrue face au phishing :** Être extrêmement prudent avec les emails de demande de mise à jour d'informations sensibles, surtout s'ils proviennent de domaines inconnus ou suspects. Vérifier systématiquement les URL des liens.
*   **Sécurisation des comptes :** Activer et gérer correctement l'authentification à deux facteurs (2FA) sur toutes les plateformes, en particulier celles qui hébergent des dépôts de code. Utiliser des méthodes 2FA robustes (applications d'authentification, clés de sécurité physiques).
*   **Audit régulier des dépendances :** Les équipes de développement devraient envisager des outils d'analyse de sécurité de la chaîne d'approvisionnement pour détecter les comportements anormaux dans les dépendances npm.
*   **Mise à jour des packages :** Après la détection de l'incident, il est crucial de mettre à jour les packages vers les versions corrigées publiées par npm.
*   **Surveillance des transactions :** Les utilisateurs manipulant des cryptomonnaies doivent rester vigilants et vérifier attentivement les adresses de destination avant de confirmer toute transaction, même si le processus semble habituel.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-hijack-npm-packages-with-2-billion-weekly-downloads-in-supply-chain-attack/){:target="_blank"}
