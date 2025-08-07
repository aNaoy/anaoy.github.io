---
title: 'Researchers Uncover ECScape Flaw in Amazon ECS Enabling Cross-Task Credential Theft'
date: 2025-08-07
permalink: /posts/2025/08/07/researchers-uncover-ecscape-flaw-in-amazon-ecs-enabling-cross-task-credential-theft/
tags:
- veille-cyber
- hackernews
---
### Escalade de privilèges dans Amazon ECS : ECScape

Une nouvelle faille baptisée "ECScape" a été découverte dans Amazon Elastic Container Service (ECS), permettant à un attaquant d'obtenir les identifiants de sécurité d'autres tâches fonctionnant sur la même instance EC2. Cela ouvre la voie à un mouvement latéral, à l'accès à des données sensibles et à la prise de contrôle de l'environnement cloud.

L'exploitation repose sur l'abus d'un protocole interne non documenté d'ECS. Un conteneur malveillant, même avec des privilèges IAM restreints, peut ainsi usurper les autorisations d'un conteneur plus privilégié sur le même hôte en volant ses identifiants. Ceci est rendu possible par le service de métadonnées qui expose des identifiants temporaires pour le rôle IAM de la tâche. En imitant le comportement de l'agent ECS et en abusant du canal de communication, un attaquant peut collecter passivement les identifiants de tous les autres conteneurs sur l'instance et agir avec leurs privilèges.

Les conséquences potentielles incluent l'escalade de privilèges inter-tâches, l'exposition de secrets et l'exfiltration de métadonnées, particulièrement critiques lorsque des tâches aux privilèges élevés et faibles coexistent sur des hôtes EC2 partagés.

**Points Clés :**

*   Une vulnérabilité dans Amazon ECS permet l'escalade de privilèges.
*   Un conteneur malveillant peut voler les identifiants IAM d'autres tâches sur la même instance EC2.
*   L'attaque est rendue possible par l'abus d'un protocole interne d'ECS et du service de métadonnées.
*   L'usurpation de l'agent ECS est au cœur de cette technique.

**Vulnérabilités :**

*   Aucune CVE spécifique n'est mentionnée pour cette vulnérabilité dans l'article.

**Recommandations :**

*   Adopter des modèles d'isolation plus robustes pour les tâches.
*   Éviter de déployer des tâches à hauts privilèges aux côtés de tâches non fiables ou à bas privilèges sur la même instance.
*   Utiliser AWS Fargate pour une isolation plus forte.
*   Désactiver ou restreindre l'accès au service de métadonnées de l'instance (IMDS) pour les tâches.
*   Limiter les permissions de l'agent ECS.
*   Mettre en place des alertes CloudTrail pour détecter une utilisation inhabituelle des rôles IAM.
*   Appliquer le principe du moindre privilège pour tous les rôles et comptes de service (SA) dans l'environnement cloud.
*   Maintenir à jour tous les services et dépendances cloud avec les derniers correctifs de sécurité.

---
[Source](https://thehackernews.com/2025/08/researchers-uncover-ecscape-flaw-in.html){:target="_blank"}
