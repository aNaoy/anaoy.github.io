---
title: 'Salesforce Flags Unauthorized Data Access via Gainsight-Linked OAuth Activity'
date: 2025-11-21
permalink: /posts/2025/11/21/salesforce-flags-unauthorized-data-access-via-gainsight-linked-oauth-activity/
tags:
- veille-cyber
- hackernews
---
**Accès non autorisé aux données Salesforce via une application tierce**

Une activité inhabituelle a été détectée concernant des applications publiées par Gainsight et connectées à la plateforme Salesforce. Cette activité a potentiellement permis un accès non autorisé à certaines données de clients Salesforce via la connexion de ces applications.

L'enquête de Salesforce suggère que le problème ne provient pas d'une vulnérabilité de la plateforme Salesforce elle-même, mais plutôt de la connexion externe de l'application tierce. Salesforce a révoqué tous les jetons d'accès et de rafraîchissement actifs liés aux applications Gainsight et les a temporairement retirées de l'AppExchange pour les besoins de l'enquête. Des actions similaires ont été entreprises pour les intégrations HubSpot et Zendesk.

Cette campagne est attribuée au groupe ShinyHunters (également connu sous le nom d'UNC6240) et s'inscrit dans une tendance accrue de ciblage des jetons OAuth des intégrations SaaS tierces. Des attaques similaires ont précédemment affecté des applications comme Salesloft Drift. Il est confirmé que ShinyHunters est à l'origine de ces attaques, revendiquant le vol de données de près de 1000 organisations via les vagues d'attaques sur Salesloft et Gainsight.

**Points Clés :**

*   Accès non autorisé aux données Salesforce via une application tierce (Gainsight).
*   Cause identifiée : compromission des jetons OAuth de l'application tierce.
*   Impact : Potentiel accès aux données clients Salesforce.
*   Acteurs malveillants : ShinyHunters (UNC6240).
*   Tendance : Augmentation du ciblage des jetons OAuth des intégrations SaaS tierces.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique de Salesforce n'a été identifiée. Le problème réside dans la gestion ou la compromission de la connexion OAuth de l'application tierce.

**Recommandations :**

*   Examiner toutes les applications tierces connectées à Salesforce.
*   Révoquer les jetons pour les applications inutilisées ou suspectes.
*   Rotation des identifiants en cas d'anomalies détectées dans une intégration.

---
[Source](https://thehackernews.com/2025/11/salesforce-flags-unauthorized-data.html){:target="_blank"}
