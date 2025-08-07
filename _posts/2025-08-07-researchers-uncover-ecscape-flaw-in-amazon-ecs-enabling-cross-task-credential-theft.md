---
title: 'Researchers Uncover ECScape Flaw in Amazon ECS Enabling Cross-Task Credential Theft'
date: 2025-08-07
permalink: /posts/2025/08/07/researchers-uncover-ecscape-flaw-in-amazon-ecs-enabling-cross-task-credential-theft/
tags:
- veille-cyber
- hackernews
---
**ECScape : Escalade de privilèges sur Amazon ECS**

Une faille découverte dans Amazon Elastic Container Service (ECS) permet à des conteneurs malveillants à faibles privilèges de voler les identifiants AWS de conteneurs plus privilégiés s'exécutant sur la même instance EC2. Cette technique, nommée ECScape, ouvre la voie à des mouvements latéraux, à l'accès à des données sensibles et à la prise de contrôle de l'environnement cloud. L'exploitation repose sur l'abus d'un protocole interne non documenté d'ECS et d'un service de métadonnées exposé.

**Points clés :**

*   Une chaîne d'escalade de privilèges de bout en bout a été identifiée dans Amazon ECS.
*   Un conteneur compromis peut usurper l'identité de l'agent ECS pour accéder aux identifiants de toutes les tâches sur la même instance.
*   L'attaque exploite le service de métadonnées de l'instance (IMDS) et le protocole de communication de l'agent ECS.
*   Les conséquences incluent l'exposition de secrets, l'exfiltration de données et la prise de contrôle de l'environnement.

**Vulnérabilités :**

*   La documentation AWS indique explicitement qu'il n'y a pas d'isolation des tâches sur EC2, et que les conteneurs peuvent potentiellement accéder aux identifiants d'autres tâches sur la même instance. L'article ne mentionne pas de CVE spécifique pour cette vulnérabilité, mais il s'agit d'une faiblesse inhérente au modèle d'isolation d'ECS sur EC2.

**Recommandations :**

*   Éviter de déployer des tâches à privilèges élevés aux côtés de tâches non fiables ou à faibles privilèges sur la même instance.
*   Utiliser AWS Fargate pour une isolation réelle des tâches.
*   Désactiver ou restreindre l'accès au service de métadonnées de l'instance (IMDS) pour les tâches.
*   Limiter les permissions de l'agent ECS.
*   Configurer des alertes CloudTrail pour détecter une utilisation inhabituelle des rôles IAM.
*   Appliquer le principe du moindre privilège à tous les comptes de service (SA) dans l'environnement cloud.
*   S'assurer que tous les services et dépendances cloud sont à jour avec les derniers correctifs de sécurité.

---
[Source](https://thehackernews.com/2025/08/researchers-uncover-ecscape-flaw-in.html){:target="_blank"}
