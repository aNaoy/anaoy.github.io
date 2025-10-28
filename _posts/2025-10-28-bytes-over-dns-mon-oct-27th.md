---
title: 'Bytes over DNS, (Mon, Oct 27th)'
date: 2025-10-28
permalink: /posts/2025/10/28/bytes-over-dns-mon-oct-27th/
tags:
- veille-cyber
- sans-isc
---
**Utilisation Abusive des Requêtes DNS pour Exfiltration de Données**

Des chercheurs ont exploré la possibilité d'exfiltrer des données via des requêtes DNS en exploitant des caractères non standards dans les labels des noms de domaine. En s'appuyant sur des infrastructures DNS tierces (comme celles de CloudFlare ou Google), il est possible de transmettre des séquences d'octets, potentiellement pour des communications C2 de logiciels malveillants.

**Points Clés :**

*   Les labels DNS ont des restrictions de caractères (alphanumériques et trait d'union).
*   Certains caractères non standards peuvent être transmis en manipulant les requêtes.
*   L'utilisation d'API système ou de bibliothèques DNS influence le résultat.
*   La création et l'analyse personnalisées de paquets DNS offrent le plus de flexibilité.

**Vulnérabilités :**

Bien qu'aucune vulnérabilité spécifique avec un identifiant CVE ne soit explicitement mentionnée, l'article décrit un **abus de protocole**. La capacité à encoder des données arbitraires dans des requêtes DNS peut être exploitée pour :

*   **Communication C2 (Command and Control) de malwares :** Permet aux attaquants de communiquer avec des systèmes compromis de manière furtive.
*   **Exfiltration de données :** Les données sensibles peuvent être dissimulées dans les requêtes DNS sortantes.

**Recommandations :**

*   **Surveillance du trafic DNS :** Mettre en place des systèmes de détection capables d'identifier des modèles de trafic DNS anormaux, tels que des labels de domaine inhabituels ou des requêtes excessivement longues.
*   **Analyse approfondie des requêtes DNS :** Utiliser des outils d'analyse pour examiner le contenu des requêtes et identifier les tentatives de dissimulation de données.
*   **Contrôle des configurations DNS :** Bien que le contrôle sur les infrastructures tierces soit limité, une compréhension des limitations et des comportements de chaque fournisseur DNS peut aider à anticiper certains types d'attaques.
*   **Application des standards DNS :** Se fier aux implémentations conformes aux standards pour limiter les possibilités d'abus.

Il est possible de transmettre la plupart des caractères ASCII, et avec une ingénierie appropriée, même d'autres jeux de caractères, en fonction du fournisseur DNS utilisé et de la méthode de création des requêtes. L'utilisation de Google peut altérer la casse des lettres dans les requêtes, compliquant l'utilisation de formats comme le BASE64. L'envoi de valeurs d'octets supérieures à 0x7F (127) est souvent problématique en raison de conversions PUNICODE. La méthode la plus fiable pour transmettre tous les octets, y compris les caractères spéciaux comme le point (`.`), consiste à générer et analyser manuellement les paquets DNS, en particulier avec des services comme CloudFlare.

---
[Source](https://isc.sans.edu/diary/rss/32420){:target="_blank"}
