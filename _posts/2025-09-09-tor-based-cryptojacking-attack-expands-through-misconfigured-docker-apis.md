---
title: 'TOR-Based Cryptojacking Attack Expands Through Misconfigured Docker APIs'
date: 2025-09-09
permalink: /posts/2025/09/09/tor-based-cryptojacking-attack-expands-through-misconfigured-docker-apis/
tags:
- veille-cyber
- hackernews
---
**Une nouvelle menace exploite les API Docker mal configurées pour la cryptomine et la création de botnets**

Une campagne de cryptojacking évoluée utilise le réseau TOR pour cibler les API Docker mal configurées. Cette variante, découverte récemment, vise à prendre le contrôle de systèmes vulnérables pour miner des cryptomonnaies, mais pourrait également jeter les bases d'un botnet complexe.

L'attaque débute par l'accès à des API Docker exposées et mal configurées. Un nouveau conteneur est créé, le système de fichiers de l'hôte est monté, et un script est téléchargé via un domaine TOR. Ce script assure la persistance en modifiant les configurations SSH et installe des outils pour la reconnaissance, la communication avec un serveur de commande et contrôle (C2), et le téléchargement d'un exécutable compilé en langage Go.

Cet exécutable, écrit en Go, contient directement le contenu qu'il doit déployer. Il analyse le fichier `utmp` pour identifier les utilisateurs connectés, potentiellement à l'aide de modèles linguistiques avancés comme l'indique l'utilisation d'emojis dans le code source. Il utilise ensuite le scanner `Masscan` pour rechercher d'autres API Docker ouvertes sur le port 2375, propageant ainsi l'infection.

L'analyse révèle également une logique préparée pour exploiter les ports Telnet (23) et le port de débogage à distance de Chromium (9222). Bien que ces fonctions ne soient pas encore pleinement opérationnelles pour la propagation, elles suggèrent des intentions futures d'exploitation. L'exploitation potentielle du port 9222, en particulier, pourrait permettre l'intégration d'appareils dans un botnet pour la distribution de charges utiles supplémentaires, telles que le vol de données ou des attaques par déni de service distribué (DDoS).

**Points Clés :**

*   Exploitation du réseau TOR pour masquer les activités malveillantes.
*   Ciblage des API Docker mal configurées et exposées sur Internet.
*   Création de conteneurs pour exécuter des charges utiles malveillantes.
*   Installation d'outils de reconnaissance et de persistance.
*   Possibilité d'établir un botnet pour des attaques futures.
*   Indices d'utilisation de modèles linguistiques avancés dans la création des outils malveillants.

**Vulnérabilités (CVE non spécifiées dans l'article) :**

*   API Docker mal configurées et exposées publiquement.
*   Port 2375 de l'API Docker ouvert sur Internet.
*   Ports Telnet (23) et de débogage à distance de Chromium (9222) potentiellement exploitables.

**Recommandations :**

*   Segmenter les réseaux pour limiter l'exposition des services.
*   Restreindre l'accès aux services, y compris les API Docker, depuis Internet.
*   Sécuriser les identifiants par défaut pour les appareils et services.

---
[Source](https://thehackernews.com/2025/09/tor-based-cryptojacking-attack-expands.html){:target="_blank"}
