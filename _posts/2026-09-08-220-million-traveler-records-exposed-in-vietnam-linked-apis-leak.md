---
title: '220 million traveler records exposed in Vietnam-linked APIS leak'
date: 2026-09-08
permalink: /posts/2026/09/08/220-million-traveler-records-exposed-in-vietnam-linked-apis-leak/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite massive de données du système APIS vietnamien

Une base de données Elasticsearch contenant plus de 220 millions d'enregistrements de passagers et de membres d'équipage a été exposée en ligne. Ces données, liées à un système de contrôle des informations préalables sur les voyageurs (APIS) au Vietnam, couvrent la période de janvier 2017 à avril 2026. Bien que la fuite ait été sécurisée le 8 juin 2024, la durée réelle de l'exposition demeure inconnue.

**Points clés :**
*   **Volume :** 220 783 700 entrées (107 Go de données).
*   **Contenu :** Noms, dates de naissance, nationalités, numéros de passeport, détails des vols, aéroports de transit et informations sur les bagages.
*   **Origine :** Le cluster était hébergé sur des infrastructures IP liées à l'opérateur Viettel à Hanoï.
*   **Impact :** Des voyageurs de nombreuses nationalités ayant transité par le Vietnam au cours des neuf dernières années sont potentiellement concernés.

**Vulnérabilités :**
*   **Chaînage de mauvaises configurations :** L'accès a été rendu possible par une combinaison de deux failles : une configuration réseau permettant de contourner une protection HTTP 401, suivie de l'utilisation d'identifiants par défaut sur le cluster Elasticsearch.
*   **Absence de CVE :** Aucun identifiant CVE spécifique n'est associé, car l'incident résulte d'erreurs de configuration plutôt que d'une vulnérabilité logicielle logicielle répertoriée.

**Recommandations :**
*   **Audit d'accès :** Sécuriser impérativement les services Elasticsearch en désactivant les identifiants par défaut et en implémentant des mécanismes d'authentification robustes.
*   **Segmentation réseau :** Ne jamais exposer directement des bases de données sur Internet, même derrière des couches de sécurité partielles.
*   **Surveillance des journaux :** Maintenir des logs serveurs détaillés pour détecter toute activité suspecte ou extraction de données non autorisée.
*   **Gestion des risques tiers :** Les organisations impliquées dans la gestion de données sensibles doivent auditer régulièrement les configurations de leurs clusters cloud pour éviter que des erreurs humaines n'exposent des informations critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/220-million-traveler-records-exposed-in-vietnam-linked-apis-leak/){:target="_blank"}
