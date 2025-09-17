---
title: 'WebSocket Turbo Intruder: Unearthing the WebSocket Goldmine'
date: 2025-09-17
permalink: /posts/2025/09/17/websocket-turbo-intruder-unearthing-the-websocket-goldmine/
tags:
- veille-cyber
- zerodaysfans
---
## Exploitation des Vulnérabilités WebSocket avec WebSocket Turbo Intruder

Cet article présente WebSocket Turbo Intruder, une extension pour Burp Suite conçue pour tester de manière approfondie les applications utilisant le protocole WebSocket. Il comble les lacunes des outils qui négligent ou analysent superficiellement ce protocole, permettant ainsi de découvrir des vulnérabilités courantes comme les problèmes de contrôle d'accès, les conditions de concurrence et les injections SQL, ainsi que des vulnérabilités spécifiques aux WebSockets.

**Points Clés :**

*   **Vitesse et Puissance :** L'outil permet l'envoi de milliers de messages par seconde grâce à son moteur d'attaque rapide.
*   **Intégration :** Il s'intègre avec les scanners HTTP existants via un adaptateur HTTP pour automatiser les tests.
*   **Filtrage Intelligent :** Des filtres personnalisables permettent de masquer le trafic non pertinent et de se concentrer sur les réponses intéressantes.
*   **Spécificités WebSocket :** Il est optimisé pour le protocole WebSocket, gérant la complexité des multiples réponses pour une seule requête.

**Vulnérabilités Détectées et Exploitations :**

*   **Pollution de Prototype côté Serveur (Server-Side Prototype Pollution) :** Notamment avec Socket.IO, en manipulant la propriété `initialPacket` pour déclencher une nouvelle réponse de salutation. Bien qu'aucun CVE spécifique ne soit mentionné pour cette application, le concept est lié à des recherches antérieures sur la pollution de prototype.
*   **Conditions de Concurrence (Race Conditions) :** Permet de tester ces vulnérabilités en utilisant un moteur "THREADED" qui ouvre plusieurs connexions simultanément pour simuler des scénarios de concurrence.
*   **"Ping of Death" (Déni de Service) :** Découvert dans une implémentation Java de WebSocket, où une taille de charge utile malformée dans l'en-tête d'un paquet peut entraîner une allocation mémoire excessive et un crash du serveur.

**Recommandations et Fonctionnalités :**

*   **Installation Facile :** Disponible via le BApp Store de Burp Suite.
*   **Tests Manuels et Automatisés :** Permet des tests interactifs via le moteur Turbo Intruder ou l'automatisation via l'adaptateur HTTP.
*   **Gestion des Réponses WebSocket :** Des décorateurs comme `@MatchRegex`, `@Pong` et `@PingPong` aident à filtrer et gérer les messages entrants.
*   **Interface en Ligne de Commande (CLI) :** Pour l'automatisation avancée et l'exécution hors Burp Suite.
*   **Mode de Débogage (WS Logger) :** Enregistre jusqu'à 1000 messages WebSocket pour faciliter le débogage des scripts et l'appariement des requêtes/réponses.
*   **Mise en Garde :** L'outil est puissant et doit être utilisé avec prudence pour éviter de surcharger ou de provoquer des dénis de service sur les serveurs cibles. Utiliser uniquement sur des cibles autorisées.

---
[Source](https://portswigger.net/research/websocket-turbo-intruder-unearthing-the-websocket-goldmine){:target="_blank"}
