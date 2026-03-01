---
title: 'QuickLens Chrome extension steals crypto, shows ClickFix attack'
date: 2026-03-01
permalink: /posts/2026/03/01/quicklens-chrome-extension-steals-crypto-shows-clickfix-attack/
tags:
- veille-cyber
- bleepingcomp
---
**Extension Chrome Compromise : Vol de Cryptomonnaies et Attaques ClickFix**

Une extension Chrome populaire, initialement conçue pour faciliter les recherches avec Google Lens, a été détournée pour diffuser des logiciels malveillants et cibler les cryptomonnaies de ses utilisateurs. Renommée "QuickLens - Search Screen with Google Lens", cette extension, qui comptait environ 7 000 utilisateurs et avait bénéficié d'une mise en avant par Google, a vu sa version 5.8 publier le 17 février 2026 contenir des scripts malveillants.

Après un changement de propriétaire sur une plateforme de vente d'extensions, la nouvelle version de QuickLens a demandé des autorisations étendues, notamment `declarativeNetRequestWithHostAccess` et `webRequest`. Elle a également désactivé des en-têtes de sécurité essentiels tels que la Politique de Sécurité du Contenu (CSP), X-Frame-Options et X-XSS-Protection sur tous les sites web visités, ouvrant la porte à l'exécution de scripts indésirables.

L'extension communiquait avec un serveur de commande et de contrôle (C2) situé à `api.extensionanalyticspro[.]top`. Elle recueillait des informations sur l'utilisateur, telles qu'un identifiant unique, sa localisation, son système d'exploitation et son navigateur, afin de recevoir des instructions. Des utilisateurs ont signalé l'apparition de fausses alertes de mise à jour Google sur toutes les pages qu'ils visitaient.

Les scripts malveillants livrés par le serveur C2 étaient exécutés discrètement sur chaque chargement de page grâce à une technique d'insertion "pixel onload". La désactivation des en-têtes de sécurité permettait cette exécution, même sur des sites qui auraient normalement bloqué ce type d'activité.

Un premier script amenait les utilisateurs vers un site proposant une fausse mise à jour Google. Cliquer sur ce bouton déclenchait une attaque de type ClickFix, incitant l'utilisateur à exécuter du code sur son ordinateur. Pour les utilisateurs Windows, cela pouvait mener au téléchargement d'un exécutable malveillant signé par une entité chinoise. Ce programme lançait ensuite des commandes PowerShell pour tenter de télécharger et exécuter des charges utiles supplémentaires, bien que les liens de seconde phase étaient inactifs lors de l'analyse.

Un autre script malveillant était spécifiquement conçu pour voler les informations des portefeuilles de cryptomonnaies (MetaMask, Phantom, Coinbase Wallet, Trust Wallet, etc.), y compris les phrases de récupération, afin de détourner les actifs numériques. D'autres scripts étaient capables de capturer des identifiants de connexion, des informations de paiement et d'autres données sensibles soumises dans des formulaires. Des charges utiles additionnelles visaient à extraire des données de boîtes mail Gmail, des comptes publicitaires Facebook Business Manager et des informations de chaînes YouTube. Des allégations non vérifiées font état d'un ciblage des utilisateurs macOS avec l'infostealer AMOS.

Google a depuis retiré l'extension du Chrome Web Store et l'a automatiquement désactivée pour les utilisateurs affectés.

**Points Clés :**

*   Une extension Chrome légitime a été compromise.
*   Elle a été mise à jour avec des fonctionnalités malveillantes le 17 février 2026.
*   L'extension a détourné les autorisations pour désactiver les protections de sécurité du navigateur.
*   Elle utilisait un serveur C2 pour recevoir des instructions et livrer des charges utiles malveillantes.
*   Des fausses alertes de mise à jour Google ont été diffusées, menant à des attaques ClickFix.
*   L'extension visait le vol de cryptomonnaies et d'informations sensibles.

**Vulnérabilités :**

*   L'absence de validation rigoureuse des mises à jour d'extensions par les plateformes (ici, le Chrome Web Store).
*   La capacité de l'extension à modifier les autorisations demandées après installation.
*   La désactivation des en-têtes de sécurité du navigateur (CSP, X-Frame-Options, X-XSS-Protection) par l'extension.
*   L'exploitation de la confiance des utilisateurs dans les mises à jour de logiciels légitimes.

**Recommandations :**

*   Les utilisateurs ayant installé QuickLens doivent la désinstaller complètement.
*   Effectuer une analyse antivirus complète de l'appareil.
*   Réinitialiser les mots de passe enregistrés dans le navigateur.
*   Pour les utilisateurs de portefeuilles de cryptomonnaies mentionnés, transférer les fonds vers un nouveau portefeuille sécurisé.
*   Faire preuve de vigilance quant aux extensions installées et aux autorisations demandées.
*   Se fier aux canaux officiels pour les mises à jour de logiciels.

---
[Source](https://www.bleepingcomputer.com/news/security/quicklens-chrome-extension-steals-crypto-shows-clickfix-attack/){:target="_blank"}
