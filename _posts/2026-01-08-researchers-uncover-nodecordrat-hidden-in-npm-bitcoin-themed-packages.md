---
title: 'Researchers Uncover NodeCordRAT Hidden in npm Bitcoin-Themed Packages'
date: 2026-01-08
permalink: /posts/2026/01/08/researchers-uncover-nodecordrat-hidden-in-npm-bitcoin-themed-packages/
tags:
- veille-cyber
- hackernews
---
### Le Malware NodeCordRAT se Cache dans des Packages npm à Thème Bitcoin

Des chercheurs en cybersécurité ont découvert trois packages npm malveillants dissimulant un nouveau malware nommé NodeCordRAT. Ces packages, dont les noms évoquent des projets légitimes liés au Bitcoin, ont été retirés en novembre 2025.

Les packages identifiés sont :
*   bitcoin-main-lib
*   bitcoin-lib-js
*   bip40

Lors de l'installation des packages "bitcoin-main-lib" et "bitcoin-lib-js", un script "postinstall.cjs" est exécuté, téléchargeant et installant "bip40". C'est ce dernier qui contient le payload NodeCordRAT. Ce cheval de Troie d'accès à distance (RAT) est conçu pour voler des informations sensibles.

**Points Clés :**

*   **Vecteur d'infection :** L'écosystème npm (Node Package Manager).
*   **Nom du Malware :** NodeCordRAT.
*   **Fonctionnalités :** Vol de données, exécution de commandes à distance, prise de captures d'écran, téléversement de fichiers.
*   **Canal de Communication C2 :** Serveurs Discord, utilisant des tokens codés en dur pour communiquer via l'API Discord.
*   **Ciblage :** Identifiants de navigateur Google Chrome, tokens d'API, phrases secrètes de portefeuilles de cryptomonnaies (comme MetaMask).
*   **Stratégie de l'attaquant :** Utilisation de noms de packages similaires à des projets légitimes (bitcoinjs) pour tromper les développeurs.
*   **Plateformes ciblées :** Windows, Linux et macOS.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée directement dans le texte pour le malware NodeCordRAT lui-même. Cependant, le mécanisme d'exécution de scripts post-installation dans les packages npm est exploité.

**Recommandations :**

*   Vérifier attentivement les dépendances npm avant de les installer.
*   Être vigilant quant aux noms des packages, surtout s'ils ressemblent à des projets populaires.
*   Utiliser des outils d'analyse de sécurité pour détecter les comportements suspects des dépendances.
*   Garder à jour les systèmes et les environnements de développement.

---
[Source](https://thehackernews.com/2026/01/researchers-uncover-nodecordrat-hidden.html){:target="_blank"}
