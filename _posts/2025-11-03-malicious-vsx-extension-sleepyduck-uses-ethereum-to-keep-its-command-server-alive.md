---
title: 'Malicious VSX Extension "SleepyDuck" Uses Ethereum to Keep Its Command Server Alive'
date: 2025-11-03
permalink: /posts/2025/11/03/malicious-vsx-extension-sleepyduck-uses-ethereum-to-keep-its-command-server-alive/
tags:
- veille-cyber
- hackernews
---
**SleepyDuck : une extension malveillante contourne la détection grâce à Ethereum**

Une nouvelle extension malveillante, baptisée SleepyDuck, a été découverte dans le registre Open VSX. Initialement présentée comme une bibliothèque inoffensive, elle a été mise à jour pour intégrer un cheval de Troie d'accès à distance (RAT). Cette extension, nommée juan-bianco.solidity-vlang, utilise une adresse Ethereum pour maintenir son serveur de commande et de contrôle actif, le rendant résilient aux tentatives de suppression.

Les chercheurs ont identifié que le malware se déclenche à l'ouverture d'une nouvelle fenêtre d'éditeur de code ou lors de la sélection d'un fichier `.sol`. Il interagit avec la blockchain Ethereum pour récupérer les informations du serveur de commande et de contrôle, qui communique avec l'adresse "sleepyduck[.]xyz". Les commandes sont récupérées via un contrat Ethereum spécifique (0xDAfb81732db454DA238e9cFC9A9Fe5fb8e34c465) à intervalles réguliers. De plus, SleepyDuck est capable de collecter des informations système (nom d'hôte, nom d'utilisateur, adresse MAC, fuseau horaire) et de les transmettre au serveur. Si le serveur de commande et de contrôle devient inaccessible, le malware peut utiliser le contrat Ethereum pour récupérer une nouvelle adresse de serveur.

Il est également mentionné que des campagnes distribuant des extensions malveillantes pour les développeurs Solidity ont été précédemment détectées, avec un cas où un développeur a perdu une quantité importante de cryptomonnaie. Les auteurs de ces extensions pourraient gonfler artificiellement les chiffres de téléchargement pour augmenter leur visibilité.

Par ailleurs, cinq autres extensions publiées sur le VS Code Extension Marketplace sous le nom de "developmentinc" ont été signalées. L'une d'elles, une bibliothèque sur le thème de Pokémon, télécharge un script de minage de cryptomonnaie dès son installation, le lance avec des privilèges administrateur et configure des exclusions pour Microsoft Defender Antivirus.

**Points clés :**

*   Découverte d'une nouvelle extension malveillante nommée SleepyDuck dans le registre Open VSX.
*   Utilisation d'Ethereum pour maintenir un serveur de commande et de contrôle (C2) résilient.
*   Collecte d'informations système et exfiltration vers le serveur C2.
*   Mécanismes de secours pour trouver de nouvelles adresses de serveur via Ethereum en cas de défaillance du C2.
*   Existence de campagnes antérieures visant les développeurs Solidity avec des extensions malveillantes.
*   Signalement d'autres extensions malveillantes qui installent des mineurs de cryptomonnaie.

**Vulnérabilités (avec CVE si possible) :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est détaillée dans l'article. L'article se concentre sur les techniques d'infection et le fonctionnement du malware.

**Recommandations :**

*   Faire preuve de prudence lors du téléchargement d'extensions pour les éditeurs de code.
*   S'assurer que les extensions proviennent d'éditeurs de confiance.
*   Surveiller les listes d'extensions retirées des marketplaces officielles (par exemple, la page `RemovedPackages` sur GitHub pour le marketplace de Microsoft).

---
[Source](https://thehackernews.com/2025/11/malicious-vsx-extension-sleepyduck-uses.html){:target="_blank"}
