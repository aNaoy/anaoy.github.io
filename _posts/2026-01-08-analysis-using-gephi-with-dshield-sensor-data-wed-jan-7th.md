---
title: 'Analysis using Gephi with DShield Sensor Data, (Wed, Jan 7th)'
date: 2026-01-08
permalink: /posts/2026/01/08/analysis-using-gephi-with-dshield-sensor-data-wed-jan-7th/
tags:
- veille-cyber
- sans-isc
---
**Visualisation des Interactions de Menaces avec Gephi**

Une analyse a été menée en utilisant les données collectées par les capteurs DShield et traitées avec l'outil de visualisation de graphes Gephi. L'objectif était de visualiser les relations entre les adresses IP sources, les noms de fichiers et les capteurs ayant reçu des copies de ces fichiers. Les données, couvrant 30 jours, ont été extraites de la base de données ELK via des requêtes ES|QL dans Kibana.

**Points Clés :**

*   Utilisation de Gephi et Graphviz pour explorer les relations dans les données de cybersécurité.
*   Exportation de données depuis Kibana via ES|QL pour l'analyse.
*   Filtrage des données pour exclure les chercheurs connus (via `event.reference == "no match"`).
*   Visualisation des groupes d'activités malveillantes et de leurs caractéristiques.
*   Identification spécifique d'une famille de logiciels malveillants, le "redtail malware", et de ses interactions.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec des identifiants CVE n'est mentionnée dans l'article. L'analyse porte sur l'exploitation de données existantes issues d'un honeypot pour identifier des activités malveillantes.

**Recommandations :**

L'article ne propose pas de recommandations directes, mais l'approche suggère :

*   L'exploitation d'outils de visualisation comme Gephi pour mieux comprendre les flux de données malveillantes.
*   L'utilisation d'outils de requête avancés comme ES|QL pour extraire des informations pertinentes des bases de données de logs.
*   L'importance du marquage et du filtrage des données pour isoler les activités d'intérêt.

---
[Source](https://isc.sans.edu/diary/rss/32608){:target="_blank"}
