---
title: 'McGraw-Hill confirms data breach following extortion threat'
date: 2026-04-14
permalink: /posts/2026/04/14/mcgraw-hill-confirms-data-breach-following-extortion-threat/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de données chez McGraw-Hill via une mauvaise configuration Salesforce

L'éditeur éducatif McGraw-Hill a confirmé une intrusion dans ses systèmes suite à l'exploitation d'une mauvaise configuration au sein de l'environnement Salesforce. Bien que le groupe de cybercriminels **ShinyHunters** affirme détenir 45 millions d'enregistrements contenant des données personnelles et menace de les divulguer, McGraw-Hill soutient que les données exposées sont limitées, non sensibles et qu'aucune base de données client ou information financière n'a été compromise.

**Points clés :**
* **Origine de l'attaque :** Une vulnérabilité de configuration dans l'écosystème Salesforce, touchant potentiellement plusieurs organisations utilisatrices.
* **Revendication contradictoire :** Le groupe ShinyHunters, connu pour de nombreuses attaques récentes, conteste la nature mineure de la brèche et prétend détenir un volume massif de données identifiables (PII).
* **Réponse de l'entreprise :** Sécurisation immédiate des pages web concernées et ouverture d'une enquête avec des experts en cybersécurité.

**Vulnérabilités :**
* Aucune CVE spécifique n'a été attribuée à cet incident, celui-ci découlant d'une **mauvaise configuration de sécurité (misconfiguration)** au sein de la plateforme Salesforce plutôt que d'une faille logicielle répertoriée.

**Recommandations :**
* **Audit de configuration :** Les entreprises utilisant des plateformes SaaS (comme Salesforce) doivent auditer régulièrement leurs paramètres de partage, d'accès aux pages publiques et de gestion des permissions.
* **Principe du moindre privilège :** Restreindre strictement l'exposition des données aux composants Salesforce nécessaires au bon fonctionnement des services.
* **Surveillance proactive :** Mettre en place des mécanismes de détection d'anomalies sur les accès aux données web pour identifier rapidement toute consultation inhabituelle.

---
[Source](https://www.bleepingcomputer.com/news/security/mcgraw-hill-confirms-data-breach-following-extortion-threat/){:target="_blank"}
