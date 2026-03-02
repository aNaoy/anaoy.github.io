---
title: 'mitmproxy for fun and profit: Interception and Analysis of Application Traffic'
date: 2026-03-02
permalink: /posts/2026/03/02/mitmproxy-for-fun-and-profit-interception-and-analysis-of-application-traffic/
tags:
- veille-cyber
- zerodaysfans
---
### Interception et analyse de trafic applicatif avec mitmproxy

Cet article présente `mitmproxy`, un outil open-source permettant d'intercepter, d'analyser et de modifier les communications réseau, notamment les protocoles HTTP et HTTPS. Il peut fonctionner en mode explicite, où le proxy est configuré sur l'appareil, ou en mode transparent, où le proxy est masqué. Pour décrypter les échanges HTTPS, l'installation du certificat racine de `mitmproxy` sur l'appareil est nécessaire, sauf en cas de contournement du mécanisme de validation des certificats (comme le certificate pinning).

L'outil propose trois interfaces : `mitmproxy` (en ligne de commande), `mitmweb` (interface web) et `mitmdump` (pour l'automatisation avec scripts). Une API de scripting permet des manipulations fines des requêtes et réponses.

La mise en place d'un environnement de laboratoire sur Linux est détaillée, utilisant les namespaces réseau pour isoler la pile réseau. Ce système permet de configurer un point d'accès Wi-Fi pour les appareils cibles et de rediriger le trafic (HTTP, HTTPS, DNS) vers `mitmproxy` via des règles `nftables`.

Des exemples concrets d'utilisation sont présentés :
*   **Modification du trafic Git sous Linux :** Il est possible de détourner des requêtes Git pour cloner un dépôt différent de celui initialement demandé, en modifiant les variables d'environnement `HTTP_PROXY`, `HTTPS_PROXY` et `GIT_SSL_CAINFO`.
*   **Interception et modification sous Android :** L'article explique comment surmonter le refus par défaut des certificats utilisateurs sur Android 7+ en utilisant un appareil rooté et un module Magisk (`Cert-Fixer`) pour installer le certificat `mitmproxy` en tant que certificat système. Un script `mitmproxy` est développé pour intercepter et modifier des requêtes gRPC envoyées à des serveurs Google, permettant de falsifier la localisation géographique.
*   **Analyse de l'application Mumble sous iOS :** Un serveur Mumble est déployé via Docker. Les échanges TLS entre l'application et le serveur sont interceptés. Grâce à la disponibilité du schéma Protobuf (`Mumble.proto`), les messages texte peuvent être décryptés et affichés en clair dans le terminal.

L'article conclut que `mitmproxy` est un outil puissant pour explorer et manipuler le trafic réseau, même chiffré, bien que des mécanismes de sécurité avancés comme le certificate pinning puissent rendre l'interception plus complexe.

**Points Clés :**

*   `mitmproxy` permet l'interception, l'analyse et la modification du trafic réseau (HTTP, HTTPS, TCP, UDP).
*   Deux modes de fonctionnement : explicite et transparent.
*   L'installation du certificat racine de `mitmproxy` est cruciale pour décrypter le trafic HTTPS.
*   Le certificate pinning est une mesure de sécurité rendant l'interception plus difficile.
*   L'API de scripting de `mitmproxy` est essentielle pour des manipulations avancées.
*   Les namespaces réseau sous Linux sont utiles pour créer des environnements d'interception isolés.
*   Sur Android, le root et des modules spécifiques sont nécessaires pour faire confiance aux certificats proxy pour certaines applications.
*   Protobuf est un format de sérialisation couramment utilisé, déchiffrable avec les schémas adéquats.

**Vulnérabilités (scénarios d'attaque démontrés) :**

*   **Modification de code source :** En détournant des requêtes Git, un attaquant peut faire en sorte que la victime télécharge un dépôt de code malveillant au lieu du dépôt légitime.
*   **Falsification de localisation géographique :** En modifiant les requêtes envoyées par des applications Android à des services comme Google Maps, il est possible de tromper ces services sur la position réelle de l'utilisateur.
*   **Surveillance de messages :** Pour des applications utilisant des protocoles non chiffrés au niveau applicatif (même si le canal TLS est sécurisé), il est possible d'espionner le contenu des communications.

**Recommandations :**

*   **Configuration sécurisée des applications :** Implémenter le certificate pinning pour les applications sensibles afin d'empêcher l'interception par des proxys non autorisés.
*   **Validation des signatures de code :** Pour les outils comme Git, s'assurer que les commits et les tags sont signés et que ces signatures sont vérifiées pour prévenir les détournements de code.
*   **Utilisation de réseaux privés et fiables :** Éviter de connecter des appareils à des réseaux Wi-Fi publics non sécurisés où des proxys malveillants pourraient être déployés.
*   **Gestion des certificats :** Être vigilant quant à l'installation de certificats racines sur les appareils, car ils accordent un niveau de confiance élevé aux communications.
*   **Chiffrement de bout en bout :** Utiliser des protocoles de chiffrement de bout en bout lorsque cela est possible, en complément du chiffrement au niveau du transport (TLS), pour garantir la confidentialité des données même en cas d'interception du trafic.

---
[Source](https://www.synacktiv.com/en/publications/mitmproxy-for-fun-and-profit-interception-and-analysis-of-application-traffic){:target="_blank"}
