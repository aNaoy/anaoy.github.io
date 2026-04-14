---
title: 'Stolen Rockstar Games analytics data leaked by extortion gang'
date: 2026-04-14
permalink: /posts/2026/04/14/stolen-rockstar-games-analytics-data-leaked-by-extortion-gang/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données chez Rockstar Games via une compromission tierce

Le groupe de cybercriminels ShinyHunters a publié plus de 78,6 millions d'enregistrements provenant de Rockstar Games. Cette violation de données fait suite à un incident de sécurité chez Anodot, un prestataire tiers spécialisé dans l'analyse de données, dont les jetons d'authentification ont été dérobés pour accéder aux environnements cloud connectés (notamment Snowflake, S3 et Amazon Kinesis).

**Points clés :**
* **Nature des données :** La fuite concerne principalement des métriques internes (revenus en jeu, comportements des joueurs, économie des jeux *GTA Online* et *Red Dead Online*), des tickets de support client (Zendesk) et des données liées aux systèmes de détection de fraude et anti-triche.
* **Impact :** Rockstar Games confirme une intrusion limitée « non matérielle » et assure qu'aucun impact n'affecte l'organisation ou les comptes des joueurs.
* **Mode opératoire :** Les attaquants ont exploité des jetons d'accès volés lors de la compromission d'Anodot pour infiltrer les instances Snowflake de ses clients.

**Vulnérabilités :**
* Bien qu'aucune CVE spécifique ne soit mentionnée, l'attaque repose sur une **vulnérabilité de gestion des identités et des accès (IAM)** au sein des intégrations tierces (utilisation de jetons d'authentification volés pour contourner les contrôles de sécurité des instances cloud).

**Recommandations :**
* **Audit des accès tiers :** Réviser strictement les autorisations accordées aux applications tierces connectées à des environnements cloud critiques (SaaS/IaaS).
* **Renforcement de l'authentification :** Implémenter l'authentification multifacteur (MFA) systématique et privilégier la rotation fréquente des jetons d'API.
* **Surveillance des journaux :** Analyser les accès aux instances cloud (Snowflake, AWS) pour détecter toute activité inhabituelle provenant d'intégrations ou d'adresses IP tierces.
* **Principe du moindre privilège :** Restreindre les droits d'accès des outils tiers au strict nécessaire pour leur fonctionnement, afin de limiter l'exposition en cas de compromission du fournisseur.

---
[Source](https://www.bleepingcomputer.com/news/security/stolen-rockstar-games-analytics-data-leaked-by-extortion-gang/){:target="_blank"}
