---
title: 'Massive Allianz Life data breach impacts 1.1 million people'
date: 2025-08-19
permalink: /posts/2025/08/19/massive-allianz-life-data-breach-impacts-11-million-people/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de Données Majeure chez Allianz Life

Plus d'un million de clients d'Allianz Life ont été affectés par une fuite de données massive résultant d'une attaque ciblée sur un système CRM basé sur le cloud de Salesforce. L'incident, survenu en juillet, a entraîné le vol d'informations personnelles sensibles. Ce groupe de pirates informatiques, lié au groupe d'extorsion ShinyHunters, a également ciblé de nombreuses autres entreprises de renom à l'échelle mondiale.

**Points Clés :**

*   **Victimes :** 1,1 million de clients d'Allianz Life aux États-Unis.
*   **Type de données volées :** Noms, adresses e-mail, genres, dates de naissance, numéros de téléphone et adresses physiques. Des identifiants fiscaux ont également été mentionnés dans des fuites confirmées.
*   **Système compromis :** Un système CRM cloud de Salesforce, utilisé par Allianz Life.
*   **Attaque :** Les pirates ont exploité une application OAuth malveillante, connectée à l'instance Salesforce de l'entreprise, pour télécharger et exfiltrer des bases de données.
*   **Acteurs de la menace :** Le groupe d'extorsion ShinyHunters, connu pour d'autres violations de données importantes, notamment celles liées à Snowflake, AT&T et PowerSchool.
*   **Conséquences :** Les données volées ont été divulguées publiquement par ShinyHunters et utilisées pour des tentatives d'extorsion. Allianz Life a également indiqué que certains employés ont été impactés.

**Vulnérabilités :**

Bien qu'aucun numéro CVE spécifique ne soit mentionné dans l'article, la vulnérabilité exploitée semble être liée à la mauvaise gestion ou à la compromission des applications OAuth connectées aux instances Salesforce. Cela permet aux attaquants d'obtenir un accès non autorisé aux données stockées dans ces systèmes.

**Recommandations :**

L'article ne détaille pas de recommandations spécifiques pour Allianz Life ou ses clients. Cependant, les actions typiques dans de tels cas incluent :

*   **Pour Allianz Life :** Mener une enquête approfondie, renforcer la sécurité des systèmes cloud et des autorisations d'accès, et réviser les politiques de gestion des applications tierces.
*   **Pour les clients affectés :** Être vigilant face aux tentatives de phishing ou d'usurpation d'identité, surveiller les comptes financiers et personnels, et modifier les mots de passe des services en ligne.

---
[Source](https://www.bleepingcomputer.com/news/security/massive-allianz-life-data-breach-impacts-11-million-people/){:target="_blank"}
