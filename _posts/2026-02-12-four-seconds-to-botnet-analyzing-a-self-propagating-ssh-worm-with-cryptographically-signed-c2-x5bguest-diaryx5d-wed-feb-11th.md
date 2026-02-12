---
title: 'Four Seconds to Botnet - Analyzing a Self Propagating SSH Worm with Cryptographically Signed C2 &#x5b;Guest Diary&#x5d;, (Wed, Feb 11th)'
date: 2026-02-12
permalink: /posts/2026/02/12/four-seconds-to-botnet-analyzing-a-self-propagating-ssh-worm-with-cryptographically-signed-c2-x5bguest-diaryx5d-wed-feb-11th/
tags:
- veille-cyber
- sans-isc
---
## Verre à moitié plein : la propagation rapide d'un ver SSH

Une attaque observée démontre la rapidité avec laquelle des systèmes Linux, notamment des appareils IoT comme les Raspberry Pi, peuvent être compromis et transformés en botnets. L'exploitation repose sur la faiblesse des mots de passe SSH, permettant une intrusion et une exécution de malware en quelques secondes.

Le processus d'attaque comprend le **brute-force de mots de passe**, le déploiement d'un **malware multi-étapes**, l'établissement d'une **persistance** via une backdoor, un système de **commande et contrôle (C2) basé sur IRC** avec vérification cryptographique des commandes, et un **mouvement latéral automatisé**. L'intégralité de la séquence initiale, de la connexion à la propagation, peut se dérouler en moins de quatre secondes.

### Points clés

*   **Faiblesse des mots de passe SSH** : C'est le principal vecteur d'attaque. Des combinaisons par défaut ou faibles permettent un accès rapide.
*   **Rapidité d'exécution** : L'ensemble du cycle de compromission et de début de propagation peut être effectué en quelques secondes.
*   **Malware sophistiqué** : Le script malveillant établit la persistance, élimine les logiciels concurrents et configure un serveur C2.
*   **Système de C2 sécurisé** : Les commandes envoyées par le serveur C2 sont vérifiées à l'aide d'une clé RSA intégrée, ajoutant une couche de sécurité pour l'attaquant.
*   **Propagation rapide** : L'utilisation d'outils comme Zmap permet de scanner un grand nombre d'adresses IP à la recherche de systèmes vulnérables.
*   **Ciblage IoT** : Les appareils IoT, souvent configurés avec des identifiants par défaut, sont des cibles idéales pour les botnets.

### Vulnérabilités

Bien que des CVE spécifiques ne soient pas mentionnés dans cet article, la vulnérabilité principale est :

*   **Exploitation de mots de passe faibles/par défaut pour SSH** : Ceci est une faille de configuration plutôt qu'une vulnérabilité logicielle spécifique.

### Recommandations

Pour prévenir ce type d'attaques :

*   **Désactiver l'authentification par mot de passe** : Privilégier exclusivement l'utilisation de clés SSH.
*   **Supprimer les comptes par défaut** : Retirer les utilisateurs prédéfinis comme "pi" sur les appareils Raspberry Pi.
*   **Mettre en place Fail2Ban** : Configurer des systèmes pour bloquer les adresses IP effectuant des tentatives de connexion répétées.
*   **Segmenter les réseaux IoT** : Isoler les appareils IoT du réseau principal pour limiter la portée d'une compromission.
*   **Durcir la sécurité des systèmes Linux** : Appliquer des mesures de sécurité robustes, même pour les petits appareils et systèmes "hobbyistes".

---
[Source](https://isc.sans.edu/diary/rss/32708){:target="_blank"}
