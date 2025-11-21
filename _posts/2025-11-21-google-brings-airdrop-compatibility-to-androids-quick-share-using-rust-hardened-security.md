---
title: 'Google Brings AirDrop Compatibility to Android’s Quick Share Using Rust-Hardened Security'
date: 2025-11-21
permalink: /posts/2025/11/21/google-brings-airdrop-compatibility-to-androids-quick-share-using-rust-hardened-security/
tags:
- veille-cyber
- hackernews
---
**Interopérabilité Sécurisée entre Android et iOS pour le Partage de Fichiers**

Google a intégré la compatibilité entre son service Quick Share et AirDrop d'Apple, permettant le partage de fichiers entre appareils Android et iOS. Cette fonctionnalité, initialement disponible sur la gamme Pixel 10, sera étendue à d'autres appareils Android. La fonction nécessite que les appareils soient découvrables pendant 10 minutes pour faciliter le transfert.

La sécurité de cette interopérabilité repose sur une approche multicouche utilisant le langage Rust pour créer un canal de partage sécurisé, éliminant ainsi des classes entières de vulnérabilités liées à la gestion de la mémoire. Cette implémentation ne transite pas par des serveurs et ne renforce pas les vulnérabilités du protocole existant.

**Points Clés:**

*   Intégration de Quick Share (Android) et AirDrop (iOS/macOS).
*   Partage de fichiers entre plateformes croisées.
*   Sécurité renforcée par l'utilisation du langage Rust.
*   Absence de routage des données via des serveurs.

**Vulnérabilités:**

*   Une vulnérabilité de divulgation d'informations de faible gravité (CVSS: 2.1) a été identifiée. Elle permettait, avec un accès physique à l'appareil, d'accéder à des informations telles que des miniatures d'images et des hachages SHA256 de numéros de téléphone et d'adresses e-mail. Cette vulnérabilité a été corrigée par Google.

**Recommandations:**

*   S'assurer que les appareils sont configurés pour être découvrables pendant la durée du transfert de fichiers.
*   Google est ouvert à collaborer avec Apple pour implémenter un mode "Contacts uniquement" à l'avenir.

---
[Source](https://thehackernews.com/2025/11/google-adds-airdrop-compatibility-to.html){:target="_blank"}
