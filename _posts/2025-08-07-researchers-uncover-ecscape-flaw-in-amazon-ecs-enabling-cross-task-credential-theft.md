---
title: 'Researchers Uncover ECScape Flaw in Amazon ECS Enabling Cross-Task Credential Theft'
date: 2025-08-07
permalink: /posts/2025/08/07/researchers-uncover-ecscape-flaw-in-amazon-ecs-enabling-cross-task-credential-theft/
tags:
- veille-cyber
- hackernews
---
## ECScape : Un risque de vol de crédentiels sur Amazon ECS

Une faille de sécurité nommée ECScape a été découverte dans Amazon Elastic Container Service (ECS), permettant à un attaquant d'obtenir les privilèges d'autres tâches sur la même instance EC2. Cette vulnérabilité permet à un conteneur faiblement privilégié de voler les identifiants AWS d'un conteneur plus privilégié, ouvrant la voie à une escalade de privilèges et à l'accès à des données sensibles.

**Points Clés :**

*   **Principe de l'attaque :** Un conteneur malveillant exploite un protocole interne ECS non documenté et un service de métadonnées interne (accessible à 169.254.170.2) pour intercepter les identifiants temporaires des rôles IAM d'autres tâches sur la même machine hôte.
*   **Moyen d'exploitation :** L'attaquant usurpe l'identité de l'agent ECS en utilisant ses propres identifiants d'instance EC2. Ensuite, il utilise les informations d'identification collectées pour s'authentifier auprès du point de terminaison de métadonnées de la tâche et de l'API d'introspection ECS. Enfin, il forge et signe une requête WebSocket du protocole de communication de l'agent (ACS) avec le paramètre `sendCredentials` défini sur "true" pour récolter les identifiants de toutes les tâches en cours d'exécution.
*   **Conséquences :** L'attaque permet un mouvement latéral, l'exposition de secrets et l'exfiltration de métadonnées, particulièrement dangereuse dans les environnements ECS sur des hôtes EC2 partagés.

**Vulnérabilités :**

Aucune CVE spécifique n'est mentionnée pour ECScape dans l'article. La vulnérabilité réside dans l'abus d'un protocole interne ECS non documenté et dans la façon dont le service de métadonnées expose les identifiants des tâches sur les instances EC2 partagées.

**Recommandations :**

*   **Modèles d'isolation renforcés :** Amazon recommande aux clients d'adopter des modèles d'isolation plus robustes.
*   **AWS Fargate :** Utiliser AWS Fargate pour une isolation véritable entre les tâches.
*   **Restriction d'accès au service de métadonnées (IMDS) :** Désactiver ou restreindre l'accès au service de métadonnées des tâches.
*   **Éviter la cohabitation de tâches :** Ne pas déployer des tâches à privilèges élevés aux côtés de tâches non fiables ou à faibles privilèges sur la même instance.
*   **Limiter les permissions de l'agent ECS :** Réduire les autorisations accordées à l'agent ECS.
*   **Surveillance avec CloudTrail :** Configurer des alertes CloudTrail pour détecter une utilisation inhabituelle des rôles IAM.
*   **Principe du moindre privilège :** Appliquer rigoureusement le principe du moindre privilège à tous les comptes de service (SA) dans l'environnement cloud.
*   **Mises à jour :** Maintenir tous les services et dépendances cloud à jour avec les derniers correctifs de sécurité.
*   **Remplacement des comptes de service obsolètes :** Si des comptes de service obsolètes sont présents, les remplacer par des comptes de service appliquant le moindre privilège.

---
[Source](https://thehackernews.com/2025/08/researchers-uncover-ecscape-flaw-in.html){:target="_blank"}
