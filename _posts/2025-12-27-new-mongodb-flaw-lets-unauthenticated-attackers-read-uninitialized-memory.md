---
title: 'New MongoDB Flaw Lets Unauthenticated Attackers Read Uninitialized Memory'
date: 2025-12-27
permalink: /posts/2025/12/27/new-mongodb-flaw-lets-unauthenticated-attackers-read-uninitialized-memory/
tags:
- veille-cyber
- hackernews
---
## Vulnérabilité Critique dans MongoDB : Fuite de Mémoire Non Initialisée

Une faille de sécurité majeure a été identifiée dans MongoDB, permettant à des attaquants non authentifiés d'accéder à de la mémoire non initialisée.

**Points Clés :**

*   La vulnérabilité, référencée **CVE-2025-14847** avec un score CVSS de 8.7, résulte d'une mauvaise gestion des paramètres de longueur dans les en-têtes de protocole compressés par Zlib.
*   Un client non authentifié peut exploiter cette incohérence pour lire des données de la mémoire vive (heap) non initialisée du serveur.
*   Cette fuite peut potentiellement révéler des informations sensibles, des pointeurs ou des données d'état internes, facilitant ainsi des attaques ultérieures.

**Vulnérabilités :**

*   **CVE-2025-14847** : Vulnérabilité d'incohérence dans la gestion des paramètres de longueur Zlib, permettant la lecture de mémoire non initialisée.

**Versions Affectées :**

*   MongoDB 8.2.0 à 8.2.3
*   MongoDB 8.0.0 à 8.0.16
*   MongoDB 7.0.0 à 7.0.26
*   MongoDB 6.0.0 à 6.0.26
*   MongoDB 5.0.0 à 5.0.31
*   MongoDB 4.4.0 à 4.4.29
*   Toutes les versions de MongoDB Server v4.2, v4.0, et v3.6.

**Recommandations :**

*   **Mise à jour immédiate :** Installer les versions corrigées : 8.2.3, 8.0.17, 7.0.28, 6.0.27, 5.0.32, et 4.4.30.
*   **Désactivation de la compression Zlib (solution de contournement) :** Si une mise à jour immédiate n'est pas possible, il est recommandé de désactiver la compression Zlib via les options de configuration `networkMessageCompressors` ou `net.compression.compressors`, en utilisant `snappy` ou `zstd` comme alternatives si nécessaire.

---
[Source](https://thehackernews.com/2025/12/new-mongodb-flaw-lets-unauthenticated.html){:target="_blank"}
