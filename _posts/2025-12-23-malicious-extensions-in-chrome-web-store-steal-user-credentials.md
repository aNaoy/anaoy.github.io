---
title: 'Malicious extensions in Chrome Web store steal user credentials'
date: 2025-12-23
permalink: /posts/2025/12/23/malicious-extensions-in-chrome-web-store-steal-user-credentials/
tags:
- veille-cyber
- bleepingcomp
---
**Extensions Malveillantes : Vol d'Identifiants sur le Chrome Web Store**

Deux extensions du Chrome Web Store, nommées 'Phantom Shuttle', se font passer pour des plugins de service proxy afin de détourner le trafic des utilisateurs et de voler des données sensibles. Ces extensions sont disponibles depuis au moins 2017 et ciblent particulièrement les utilisateurs en Chine.

**Fonctionnalités Clandestines de Vol de Données :**

*   **Détournement de trafic :** Les extensions redirigent tout le trafic web de l'utilisateur via des proxys contrôlés par l'attaquant. Le code malveillant est intégré à la bibliothèque jQuery légitime et dissimule les identifiants des proxys grâce à un schéma d'encodage personnalisé.
*   **Interception de données :** Via un écouteur de trafic web, les extensions interceptent les défis d'authentification HTTP sur tous les sites, capturant ainsi des informations telles que les identifiants, les détails de cartes bancaires, les mots de passe et les informations personnelles. Elles peuvent également voler les cookies de session et extraire des jetons d'API.
*   **Configuration dynamique des proxys :** Les extensions reconfigurent dynamiquement les paramètres proxy de Chrome à l'aide d'un script d'auto-configuration pour acheminer le trafic de l'utilisateur vers les proxys de l'attaquant.
*   **Ciblage de domaines à haute valeur :** En mode "smarty", plus de 170 domaines de grande valeur, incluant des plateformes de développement, des consoles de services cloud, des réseaux sociaux et des sites pour adultes, sont routés via le réseau de proxys. Les réseaux locaux et le domaine de commande et contrôle sont exclus pour éviter la détection.

**Recommandations :**

*   Faire confiance uniquement aux extensions publiées par des éditeurs réputés.
*   Consulter plusieurs avis d'utilisateurs avant d'installer une extension.
*   Examiner attentivement les autorisations demandées lors de l'installation.

---
[Source](https://www.bleepingcomputer.com/news/security/malicious-extensions-in-chrome-web-store-steal-user-credentials/){:target="_blank"}
