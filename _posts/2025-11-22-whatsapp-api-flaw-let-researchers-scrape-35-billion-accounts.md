---
title: 'WhatsApp API flaw let researchers scrape 3.5 billion accounts'
date: 2025-11-22
permalink: /posts/2025/11/22/whatsapp-api-flaw-let-researchers-scrape-35-billion-accounts/
tags:
- veille-cyber
- bleepingcomp
---
**Des milliards de comptes WhatsApp exposés par une faille d'API**

Des chercheurs ont découvert qu'une vulnérabilité dans l'interface de programmation d'application (API) de WhatsApp permettait de collecter un grand nombre de numéros de téléphone d'utilisateurs et d'informations associées. En exploitant une fonction de découverte de contacts qui ne limitait pas le débit des requêtes, les chercheurs ont pu interroger l'API sur des milliards de numéros.

Malgré l'ampleur des requêtes, WhatsApp n'a pas bloqué les comptes des chercheurs ni restreint leur trafic. L'exploitation a permis d'identifier 3,5 milliards de comptes WhatsApp actifs à travers le monde. En plus de confirmer l'existence d'un compte, d'autres API ont été utilisées pour extraire des photos de profil, des statuts ("about text") et des informations sur les appareils associés aux numéros.

Cette méthode d'abus d'API, particulièrement l'absence de limitation de débit, n'est pas nouvelle et a été observée dans des cas similaires impliquant Facebook, Twitter et Dell, entraînant des fuites massives de données personnelles.

**Points Clés :**

*   Une API de découverte de contacts WhatsApp a été exploitée pour identifier 3,5 milliards de numéros de téléphone associés à des comptes WhatsApp actifs.
*   Des informations supplémentaires comme les photos de profil et les statuts ("about text") ont pu être collectées.
*   La faille principale réside dans l'absence de limitation de débit des requêtes sur l'API.
*   Cette vulnérabilité a été corrigée par WhatsApp.
*   L'incident souligne un problème plus large d'abus d'API sur diverses plateformes.

**Vulnérabilités :**

*   Manque de limitation de débit (rate limiting) sur l'API `GetDeviceList` de WhatsApp, permettant une énumération à grande échelle.
*   Autres API comme `GetUserInfo`, `GetPrekeys`, et `FetchPicture` ont été utilisées pour collecter des données supplémentaires.

**Recommandations :**

*   Implémenter et renforcer des mécanismes de limitation de débit (rate limiting) sur toutes les API exposant des données utilisateur ou permettant des recherches.
*   Surveiller l'activité anormale sur les API pour détecter et bloquer les tentatives d'énumération ou de scraping à grande échelle.
*   Pour les utilisateurs, être conscient que les informations publiques (comme les statuts) peuvent être collectées.

---
[Source](https://www.bleepingcomputer.com/news/security/whatsapp-api-flaw-let-researchers-scrape-35-billion-accounts/){:target="_blank"}
