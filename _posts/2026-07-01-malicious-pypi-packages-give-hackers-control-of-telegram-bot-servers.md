---
title: 'Malicious PyPI packages give hackers control of Telegram bot servers'
date: 2026-07-01
permalink: /posts/2026/07/01/malicious-pypi-packages-give-hackers-control-of-telegram-bot-servers/
tags:
- veille-cyber
- bleepingcomp
---
### Operation Navy Ghost : Compromission de serveurs via PyPI

Une campagne malveillante, baptisée « Operation Navy Ghost », cible les développeurs Python utilisant le framework Pyrogram pour créer des bots Telegram. Depuis novembre 2025, des versions corrompues du projet (forks) ont été publiées sur le répertoire PyPI, intégrant une porte dérobée permettant aux attaquants de prendre le contrôle total des serveurs infectés.

**Points clés :**
*   **Mode opératoire :** La porte dérobée, dissimulée dans un module nommé `secret.py`, s'active dès le lancement du bot. Elle enregistre des commandes Telegram cachées qui permettent l'exécution arbitraire de code Python ou de commandes shell.
*   **Portée :** Les attaquants peuvent exfiltrer des fichiers, accéder aux variables d'environnement, consulter les discussions Telegram, extraire des bases de données et installer une persistance sur le serveur.
*   **Ciblage :** L'attaque vise spécifiquement les comptes de bots en production pour accéder à des infrastructures sensibles (API cloud, identifiants, données clients).
*   **Attribution :** Bien que diffusés via divers comptes PyPI, les paquets partagent une liste identique d'identifiants Telegram (« OWNERS ») utilisée pour piloter les bots compromis, confirmant une origine unique.

**Vulnérabilités :**
*   Il ne s'agit pas d'une faille CVE classique, mais d'une **attaque par empoisonnement de la chaîne d'approvisionnement logicielle (Supply Chain Attack)**. Les paquets malveillants usurpant Pyrogram incluent : `VLifeGram`, `VLife-Gram`, `pyrogram-navy`, `pyrogram-styled`, `pyrogram-zeeb`, `kelragram`, `sepgram` et `pyrogram-kelra`.

**Recommandations :**
*   **Suppression immédiate :** Désinstaller tout paquet suspect et revenir aux versions officielles et maintenues.
*   **Rotation des secrets :** Renouveler tous les jetons (tokens) des bots Telegram, les clés API, les mots de passe et autres identifiants présents sur les serveurs ayant utilisé ces bibliothèques.
*   **Audit de sécurité :** Examiner les journaux serveurs pour détecter toute activité suspecte initiée par ces paquets.
*   **Vigilance sur les dépendances :** Vérifier systématiquement l'origine et la réputation des bibliothèques open-source avant intégration, particulièrement pour les projets non maintenus.

---
[Source](https://www.bleepingcomputer.com/news/security/malicious-pypi-packages-give-hackers-control-of-telegram-bot-servers/){:target="_blank"}
