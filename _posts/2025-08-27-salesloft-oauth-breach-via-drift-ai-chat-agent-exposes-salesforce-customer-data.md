---
title: 'Salesloft OAuth Breach via Drift AI Chat Agent Exposes Salesforce Customer Data'
date: 2025-08-27
permalink: /posts/2025/08/27/salesloft-oauth-breach-via-drift-ai-chat-agent-exposes-salesforce-customer-data/
tags:
- veille-cyber
- hackernews
---
**Vol de Données via OAuth chez Salesloft Cible les Clients Salesforce**

Une campagne de vol de données a permis à des pirates d'accéder à la plateforme de ventes Salesloft, dérobant des jetons OAuth et de rafraîchissement liés à l'agent de chat IA de Drift. L'acteur de menace, identifié comme UNC6395, a ciblé des instances Salesforce de clients entre le 8 et le 18 août 2025. Les attaquants ont exporté d'importants volumes de données, y compris des clés d'accès AWS, des mots de passe et des jetons liés à Snowflake, probablement pour obtenir des identifiants compromettant davantage les environnements ciblés. UNC6395 a fait preuve d'une certaine rigueur en supprimant les tâches de requête après leur exécution.

Salesloft a révoqué les connexions entre Drift et Salesforce et a recommandé aux administrateurs de réauthentifier leurs connexions. Salesforce a confirmé qu'un "petit nombre de clients" a été touché par la compromission de la connexion de l'application, entraînant l'invalidation des jetons et la suppression de Drift de l'AppExchange.

**Points Clés :**

*   **Acteur de menace :** UNC6395
*   **Méthode d'attaque :** Exploitation de jetons OAuth volés liés à l'application tierce Drift dans Salesloft.
*   **Cible :** Instances Salesforce de clients de Salesloft.
*   **Données exfiltrées :** Clés d'accès AWS (AKIA), mots de passe, jetons liés à Snowflake, et informations des objets Salesforce (Cases, Accounts, Users, Opportunities).
*   **Impact :** Potentiel vol d'identifiants, compromission accrue des environnements victimes et possible début d'une attaque de chaîne d'approvisionnement.

**Vulnérabilités :**

*   Bien qu'aucun CVE spécifique ne soit mentionné, le vecteur d'attaque repose sur la compromission des jetons OAuth et le manque potentiel de contrôles d'accès granulaires ou de surveillance des connexions tierces.

**Recommandations :**

*   Examiner les journaux pertinents pour détecter les preuves d'exposition de données.
*   Révoquer les clés API compromises.
*   Rotation des identifiants et des jetons d'authentification.
*   Réauthentifier les connexions Salesforce aux applications tierces.
*   Surveiller activement les activités des applications tierces et leurs autorisations.
*   Évaluer la nécessité de chaque intégration et les autorisations accordées.

---
[Source](https://thehackernews.com/2025/08/salesloft-oauth-breach-via-drift-ai.html){:target="_blank"}
