---
title: 'SNI5GECT: Sniffing and Injecting 5G Traffic Without Rogue Base Stations, (Thu, Aug 14th)'
date: 2025-08-15
permalink: /posts/2025/08/15/sni5gect-sniffing-and-injecting-5g-traffic-without-rogue-base-stations-thu-aug-14th/
tags:
- veille-cyber
- sans-isc
---
## SNI5GECT : Une Nouvelle Approche de la Surveillance et de l'Injection dans les Réseaux 5G

Un nouveau framework, baptisé SNI5GECT, permet de capturer en temps réel les communications 5G avant authentification et d'injecter des charges utiles malveillantes dans les flux descendants vers les équipements utilisateurs (UE). Contrairement aux approches précédentes, SNI5GECT n'a pas besoin de stations de base non autorisées (rogue gNodeB), ce qui simplifie sa mise en œuvre et améliore sa discrétion. Il peut être utilisé pour identifier des appareils, mener des attaques par déni de service ou des attaques par rétrogradation de service.

Le framework est composé de plusieurs modules : Syncher (synchronisation temps/fréquence), Broadcast Worker (décodage des informations de diffusion), UETracker (suivi des connexions UE-base), UE DL Worker (décodage des messages vers l'UE), GNB UL Worker (décodage des messages vers la base) et GNB DL Injector (encodage et injection de messages).

Une nouvelle attaque par rétrogradation à plusieurs étapes, identifiée sous la référence CVD-2024-0096, a été découverte lors du développement de SNI5GECT. Elle consiste à intercepter une requête d'authentification légitime, puis à la rejouer avec un numéro de séquence invalide. L'UE, recevant ce message falsifié, répond par un échec d'authentification, démarre un timer spécifique (T3520), et peut rejeter la station de base actuelle si la procédure d'authentification échoue répétitivement. Si aucune autre station de base 5G ou 4G avec la même configuration n'est disponible, l'UE peut se déconnecter du réseau 5G et se connecter à une station 4G. Le framework SNI5GECT maintient cette attaque en injectant le message de requête d'authentification rejoué après chaque requête d'enregistrement ou message d'échec d'authentification reçu, forçant ainsi l'UE à abandonner la connexion et à rejeter la station de base.

**Points Clés:**

*   **Capacités :** Sniffing et injection de trafic 5G, sans nécessiter de stations de base non autorisées.
*   **Attaques possibles :** Fingerprinting, déni de service, rétrogradation de service.
*   **Nouveau scénario d'attaque :** Rétrogradation multi-étapes vers la 4G en exploitant les procédures d'authentification.
*   **Composants :** Syncher, Broadcast Worker, UETracker, UE DL Worker, GNB UL Worker, GNB DL Injector.

**Vulnérabilités :**

*   **CVD-2024-0096 :** Attaque par rétrogradation à plusieurs étapes exploitant les procédures d'authentification 5G. L'injection d'une requête d'authentification avec un numéro de séquence invalide peut entraîner la déconnexion de l'UE et son basculement vers une technologie antérieure (4G) ou le rejet de la station de base.

**Recommandations :**

Bien que l'article ne contienne pas de recommandations explicites de mitigation contre SNI5GECT, son existence suggère la nécessité de renforcer les mécanismes de détection des activités suspectes sur le réseau 5G et de revoir la robustesse des protocoles d'authentification face aux techniques d'injection et de rejeu. L'utilisation de matériels compatibles tels que les SDR USRP B210 ou x310 est mentionnée.

**Limitations de SNI5GECT :**

*   Ne prend en charge que la 5G et l'injection en aval.
*   La précision du sniffing et de l'injection est affectée par la distance et l'environnement.
*   Ne peut pas exploiter les messages post-authentification car ils sont chiffrés.
*   Ne peut pas sniffing le trafic des connexions existantes (post-RAR) car il se base sur le suivi du RNTI depuis le début du PRACH.
*   Ne peut pas distinguer les modèles de smartphones ou les utilisateurs individuels basés uniquement sur le RNTI pour cibler des attaques.

---
[Source](https://isc.sans.edu/diary/rss/32202){:target="_blank"}
