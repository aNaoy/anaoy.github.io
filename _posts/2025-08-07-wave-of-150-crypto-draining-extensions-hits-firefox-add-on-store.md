---
title: 'Wave of 150 crypto-draining extensions hits Firefox add-on store'
date: 2025-08-07
permalink: /posts/2025/08/07/wave-of-150-crypto-draining-extensions-hits-firefox-add-on-store/
tags:
- veille-cyber
- bleepingcomp
---
## Extensions Malveillantes : Un Nouveau Vecteur d'Attaques Cryptées sur Firefox

Une campagne de cybercriminalité nommée 'GreedyBear' a ciblé les utilisateurs de Firefox en introduisant environ 150 extensions malveillantes dans le magasin d'add-ons Mozilla. Ces extensions, qui usurpaient l'identité de portefeuilles de cryptomonnaies populaires (MetaMask, TronLink, Rabby, etc.), ont réussi à dérober près d'un million de dollars.

Les extensions étaient initialement publiées sous une forme bénigne afin d'être acceptées par Firefox, accumulant ensuite de faux avis positifs. Plus tard, les éditeurs modifiaient le contenu, injectant du code malveillant pour subtiliser les identifiants de portefeuille des utilisateurs et leurs adresses IP. Ce code agissait comme un enregistreur de frappe, capturant les informations saisies dans les champs de formulaires et les popups de l'extension avant de les envoyer à un serveur contrôlé par les attaquants.

Outre les extensions, la campagne utilisait des sites web de logiciels piratés distribuant des exécutables malveillants variés (troyens, voleurs d'informations comme LummaStealer, voire ransomwares) et des sites web imitant des services de portefeuille (Trezor, Jupiter Wallet) ou de réparation de portefeuille. L'ensemble de ces activités était centralisé autour d'une adresse IP unique, 185.208.156.66, servant de centre de commande et de contrôle pour l'opération GreedyBear.

Des éléments suggèrent l'utilisation de l'IA dans la création de ces campagnes, facilitant leur mise à l'échelle, la diversification des charges utiles et l'évasion des détections. La facilité avec laquelle ces extensions ont pu être introduites sur le magasin Firefox, malgré les systèmes de détection déjà en place, soulève des inquiétudes quant à la sécurité des plateformes d'add-ons. Des signes indiquent également une possible expansion de cette campagne vers le Chrome Web Store.

### Points Clés :

*   **Campagne 'GreedyBear'**: Lancement d'environ 150 extensions malveillantes sur le magasin Firefox.
*   **Usurpation d'identité**: Imitation de portefeuilles de cryptomonnaies connus.
*   **Méthode d'attaque**: Introduction initiale bénigne, suivie d'une injection de code malveillant pour voler des identifiants et des IP.
*   **Diversification**: Utilisation conjointe de sites de logiciels piratés et de faux sites de services liés aux cryptomonnaies.
*   **Technologie IA**: Indication de l'utilisation de l'IA pour l'automatisation et l'efficacité des attaques.
*   **Expansion potentielle**: Signalement d'activités similaires sur le Chrome Web Store.
*   **Impact financier**: Estimation d'un million de dollars de préjudice.

### Vulnérabilités :

*   Absence de CVE spécifique mentionnée dans l'article pour ces extensions. La vulnérabilité réside dans la capacité des extensions à être modifiées après approbation et à exploiter la confiance des utilisateurs dans les portefeuilles légitimes.

### Recommandations :

*   **Vérification approfondie**: Lire plusieurs avis d'utilisateurs et vérifier les détails de l'extension et de son éditeur avant l'installation.
*   **Source officielle**: Obtenir les extensions de portefeuille directement sur les sites officiels des projets correspondants, qui peuvent soit les héberger, soit fournir des liens vers les plateformes d'add-ons légitimes.

---
[Source](https://www.bleepingcomputer.com/news/security/wave-of-150-crypto-draining-extensions-hits-firefox-add-on-store/){:target="_blank"}
