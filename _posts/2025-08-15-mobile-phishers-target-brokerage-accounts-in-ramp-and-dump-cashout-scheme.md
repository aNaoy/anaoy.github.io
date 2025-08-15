---
title: 'Mobile Phishers Target Brokerage Accounts in ‘Ramp and Dump’ Cashout Scheme'
date: 2025-08-15
permalink: /posts/2025/08/15/mobile-phishers-target-brokerage-accounts-in-ramp-and-dump-cashout-scheme/
tags:
- veille-cyber
- krebs
---
## Fraude boursière : Les escrocs détournent les données de cartes bancaires pour manipuler les marchés

Des groupes criminels informatiques exploitent des kits de hameçonnage sophistiqués pour détourner des données de cartes bancaires et les utiliser dans une escroquerie qualifiée de "ramp and dump". Ces fraudeurs ciblent désormais les clients des services de courtage en bourse. L'objectif est de manipuler les cours d'actions, notamment des introductions en bourse chinoises ou des "penny stocks".

Dans cette variante des fraudes "pump and dump", les escrocs achètent en masse une action pour en faire monter le prix artificiellement grâce à des transactions coordonnées depuis des comptes compromis. Ils revendent ensuite leurs actions à profit, entraînant une chute drastique de la valeur pour les investisseurs légitimes, les laissant avec des pertes irrécupérables.

Initialement, ces kits de hameçonnage ciblaient les clients de services tels que le Service Postal des États-Unis (USPS) ou des sociétés d'autoroutes pour collecter des identifiants de connexion et des codes d'authentification à usage unique (OTP). Ces OTP, reçus par SMS, servaient à enregistrer des cartes bancaires volées dans des portefeuilles mobiles contrôlés par les fraudeurs. Les téléphones ainsi équipés étaient ensuite vendus pour des transactions frauduleuses.

Les récentes évolutions montrent une adaptation de ces groupes, originaires de Chine, qui utilisent des plateformes comme Telegram pour vendre leurs kits de hameçonnage avancés. Le vendeur "Outsider" (anciennement "Chenlun") propose notamment des modèles ciblant les clients de plateformes de courtage comme Schwab, mais adaptables à d'autres.

**Points Clés et Vulnérabilités :**

*   **Schéma "Ramp and Dump" :** Manipulation des cours boursiers par des transactions coordonnées depuis des comptes compromis.
*   **Exploitation des OTP :** Les codes d'authentification à usage unique reçus par SMS sont détournés pour enregistrer des cartes bancaires dans des portefeuilles mobiles ou accéder à des comptes de courtage.
*   **Failles dans l'authentification multifacteur (MFA) :** De nombreuses institutions financières reposent sur un seul OTP "phishable" pour l'enregistrement de nouveaux portefeuilles mobiles ou pour des opérations sur les comptes de courtage. Des méthodes comme l'envoi d'un code par SMS ou l'approbation d'une demande de connexion via une application mobile sont exploitables.
*   **Maturité des Kits de Hameçonnage :** Les groupes utilisent des outils sophistiqués, y compris l'intelligence artificielle et les grands modèles linguistiques, pour développer et adapter rapidement leurs kits.
*   **Coordination des Attaques :** Les fraudeurs coordonnent leurs activités à travers des communautés en ligne, utilisant des infrastructures humaines pour gérer en temps réel l'envoi des leurres et la réception des OTP.

**Vulnérabilités spécifiques identifiées (pas de CVEs mentionnés dans l'article) :**

*   Dépendance à un unique code OTP pour l'enregistrement de portefeuilles mobiles.
*   Vulnérabilité des méthodes d'authentification multifacteur basées sur les SMS et les notifications push pour l'accès aux comptes de courtage.

**Recommandations :**

*   **Institutions Financières :** Renforcer les exigences d'authentification pour l'enregistrement de nouveaux portefeuilles mobiles (par exemple, en exigeant l'enregistrement via l'application bancaire). Surveiller activement les schémas suspects et mettre en œuvre des mesures pour les perturber. Les plateformes de courtage doivent continuellement évaluer et améliorer leurs mécanismes d'authentification.
*   **Utilisateurs :** Être vigilant face aux tentatives de hameçonnage par SMS ou e-mail, notamment celles prétendant provenir de services postaux, d'autoroutes ou de plateformes de courtage. Ne jamais partager de codes d'authentification à usage unique (OTP) reçus par SMS. Privilégier des méthodes d'authentification plus robustes lorsque disponibles, comme les clés de sécurité physiques (U2F) pour les comptes de courtage.

---
[Source](https://krebsonsecurity.com/2025/08/mobile-phishers-target-brokerage-accounts-in-ramp-and-dump-cashout-scheme/){:target="_blank"}
