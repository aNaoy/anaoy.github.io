---
title: 'Researchers Uncover ECScape Flaw in Amazon ECS Enabling Cross-Task Credential Theft'
date: 2025-08-07
permalink: /posts/2025/08/07/researchers-uncover-ecscape-flaw-in-amazon-ecs-enabling-cross-task-credential-theft/
tags:
- veille-cyber
- hackernews
---
ECScape : Risque de vol d'identifiants dans Amazon ECS

Une faille de sécurité, nommée ECScape, a été découverte dans Amazon Elastic Container Service (ECS). Elle permet à un conteneur malveillant disposant de privilèges limités de voler les identifiants AWS d'autres conteneurs sur la même instance EC2. Un attaquant peut ainsi usurper l'identité de conteneurs plus privilégiés, menant à une escalade de privilèges, à l'accès à des données sensibles et à la prise de contrôle de l'environnement cloud. L'attaque exploite un protocole interne non documenté de l'ECS et le service de métadonnées exposant les identifiants temporaires des tâches.

**Points clés :**

*   Un conteneur peu privilégié peut obtenir les permissions d'un conteneur plus privilégié sur la même instance EC2.
*   L'exploitation d'un service de métadonnées interne à l'ECS (169.254.170.2) est au cœur de la vulnérabilité.
*   L'attaquant peut usurper l'identité de l'agent ECS pour accéder aux identifiants de toutes les tâches sur l'instance.
*   La technique reste furtive en mimant le comportement attendu de l'agent ECS.
*   Les conséquences incluent l'escalade de privilèges inter-tâches, l'exposition de secrets et l'exfiltration de métadonnées.

**Vulnérabilités :**

*   Aucune CVE spécifique n'est mentionnée dans l'article. La vulnérabilité réside dans l'abus d'un protocole interne et du service de métadonnées ECS lorsque plusieurs tâches partagent une instance EC2.

**Recommandations :**

*   Adopter des modèles d'isolation plus stricts pour les tâches dans ECS.
*   Éviter de déployer des tâches à privilèges élevés sur les mêmes instances EC2 que des tâches non fiables ou à faibles privilèges.
*   Utiliser AWS Fargate pour une isolation complète.
*   Désactiver ou restreindre l'accès au service de métadonnées de l'instance (IMDS) pour les tâches.
*   Limiter les permissions de l'agent ECS.
*   Configurer des alertes CloudTrail pour détecter une utilisation anormale des rôles IAM.
*   Appliquer le principe du moindre privilège pour tous les comptes de service (SA) dans l'environnement cloud.
*   Maintenir à jour tous les services cloud et dépendances avec les derniers correctifs de sécurité.

---
[Source](https://thehackernews.com/2025/08/researchers-uncover-ecscape-flaw-in.html){:target="_blank"}
