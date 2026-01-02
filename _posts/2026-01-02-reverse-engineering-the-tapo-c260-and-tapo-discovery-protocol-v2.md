---
title: 'Reverse Engineering the Tapo C260 and Tapo Discovery Protocol v2'
date: 2026-01-02
permalink: /posts/2026/01/02/reverse-engineering-the-tapo-c260-and-tapo-discovery-protocol-v2/
tags:
- veille-cyber
- zerodaysfans
---
## Exploration du Protocole de Découverte Tapo v2 sur la Caméra C260

Une analyse approfondie de la caméra TP-Link Tapo C260 a permis de détailler le processus d'ingénierie inverse de son firmware et du protocole de découverte Tapo version 2.

### Points Clés

*   **Démontage Physique :** L'accès aux composants internes de la caméra C260 s'avère complexe en raison d'un boîtier sans vis apparentes, nécessitant l'usage d'outils spécifiques pour le déclipser. La caméra est dotée de multiples cartes pour ses diverses fonctionnalités (4K, IA, Wi-Fi, etc.). Les ports UART ne sont pas fonctionnels par défaut.
*   **Extraction et Analyse Statique du Firmware :** La puce de mémoire flash ESMT F50L1G41LB a été lue après des ajustements matériels pour l'adaptateur. Le firmware, chiffré, a été déchiffré en utilisant une méthode (AES-128-CFB1) et une clé similaires à celles utilisées sur le modèle C200. Le système de fichiers SquashFS a été décompressé pour analyser le binaire principal (`/bin/main`).
*   **Protocole de Découverte Tapo v2 :** Le binaire `main` contient des fonctions dédiées à ce protocole, notamment `tdpd_listen_thread` qui écoute sur les ports UDP 20002 et 20010. La version 2 introduit des différences notables par rapport à la v1 : endianness big-endian, checksum CRC32 (au lieu d'un checksum custom) et une fonction `tdpd_get_encrypt_info_v2` utilisant le chiffrement RSA pour une transmission plus détaillée des informations système.
*   **Émulation et Test :** L'émulation du firmware à l'aide du framework Qiling a permis de tester le protocole. Des adaptations ont été nécessaires, comme l'interception de la fonction `read_config` pour initialiser des valeurs manquantes, la redirection de l'exécution vers la fonction de gestion du protocole (`tdpd_handle`), et la modification de la fonction de log pour afficher les messages sur la sortie standard. L'injection de paquets UDP générés a été réalisée en interceptant l'appel `recvfrom`.

### Vulnérabilités

Aucune vulnérabilité spécifique avec identifiant CVE n'est détaillée dans cet article, car l'auteur ne souhaite pas encore partager ces informations en attendant les correctifs. Il mentionne cependant avoir découvert plusieurs RCE (Remote Code Execution) et autres vulnérabilités intéressantes lors d'un concours de sécurité IoT.

### Recommandations

Bien que l'article se concentre sur l'ingénierie inverse et le protocole, les points suivants peuvent être considérés comme des recommandations implicites ou des pistes pour améliorer la sécurité des appareils de ce type :

*   **Sécurisation du Démontage Physique :** Rendre plus difficile l'accès aux composants internes pourrait dissuader les attaquants physiques.
*   **Protection du Firmware :** Renforcer les mécanismes de chiffrement et d'intégrité du firmware pour empêcher les modifications non autorisées.
*   **Surveillance des Ports :** Être attentif aux ports réseau utilisés pour la découverte et la communication, et les sécuriser si nécessaire.
*   **Mise à Jour des Protocoles :** Les protocoles de découverte doivent être régulièrement revus et mis à jour pour intégrer des mesures de sécurité robustes, comme le chiffrement RSA utilisé dans le protocole v2.
*   **Gestion des Informations Sensibles :** Les informations système sensibles doivent être protégées via des méthodes cryptographiques fortes.

---
[Source](https://spaceraccoon.dev/reverse-engineer-tapo-c260-tdp-v2/){:target="_blank"}
