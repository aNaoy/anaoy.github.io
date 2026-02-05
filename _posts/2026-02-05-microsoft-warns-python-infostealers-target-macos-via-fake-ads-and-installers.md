---
title: 'Microsoft Warns Python Infostealers Target macOS via Fake Ads and Installers'
date: 2026-02-05
permalink: /posts/2026/02/05/microsoft-warns-python-infostealers-target-macos-via-fake-ads-and-installers/
tags:
- veille-cyber
- hackernews
---
### Les pirates exploitent Python pour cibler les Mac avec des voleurs d'informations

Les attaques visant à dérober des informations personnelles s'étendent de plus en plus à l'environnement macOS, alors qu'elles ciblaient initialement Windows. Ces campagnes exploitent des langages multiplateformes comme Python, ainsi que des méthodes de distribution à grande échelle.

Des techniques d'ingénierie sociale, telles que les fausses publicités (malvertising) et les installateurs trompeurs, sont utilisées pour distribuer des logiciels malveillants, souvent via des moteurs de recherche ou des publicités sur Google Ads. Les utilisateurs à la recherche d'outils légitimes sont redirigés vers de faux sites qui les incitent à télécharger des installateurs dissimulant des familles de malwares voleurs d'informations. Ces campagnes ont recours à des techniques d'exécution sans fichier, à des utilitaires natifs macOS et à l'automatisation via AppleScript pour faciliter le vol de données sensibles.

Parmi les informations ciblées figurent les identifiants de connexion aux navigateurs web, les données de session, les clés d'accès iCloud et les secrets de développement. Des malwares comme Atomic macOS Stealer (AMOS), MacSync, DigitStealer, PXA Stealer et Eternidade Stealer sont cités. PXA Stealer, associé à des acteurs malveillants d'origine vietnamienne, peut voler des identifiants, des informations financières et des données de navigation. D'autres attaques utilisent des applications de messagerie populaires comme WhatsApp pour distribuer des malwares.

**Points Clés :**

*   Les voleurs d'informations exploitent Python pour cibler les systèmes macOS.
*   La distribution se fait via de fausses publicités, des installateurs trompeurs et des techniques d'ingénierie sociale.
*   Les données volées incluent des identifiants de connexion, des données de session, et des informations financières.
*   Les techniques d'exécution sans fichier et l'utilisation d'utilitaires natifs macOS sont employées.

**Vulnérabilités et Menaces :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article. L'attaque repose sur l'ingénierie sociale et la distribution de malwares.

**Recommandations :**

*   Sensibiliser les utilisateurs aux attaques d'ingénierie sociale, notamment les chaînes de redirection malveillantes, les faux installateurs et les invites trompeuses.
*   Surveiller l'activité suspecte dans le Terminal et les accès à iCloud Keychain.
*   Inspecter le trafic réseau sortant à la recherche de requêtes POST vers des domaines suspects ou nouvellement enregistrés.
*   Maintenir les systèmes à jour et utiliser des solutions de sécurité fiables.

---
[Source](https://thehackernews.com/2026/02/microsoft-warns-python-infostealers.html){:target="_blank"}
