---
title: 'Salesforce investigates customer data theft via Gainsight breach'
date: 2025-11-20
permalink: /posts/2025/11/20/salesforce-investigates-customer-data-theft-via-gainsight-breach/
tags:
- veille-cyber
- bleepingcomp
---
**Incident de sécurité chez Salesforce lié à des applications tierces**

Salesforce enquête actuellement sur des tentatives de vol de données clients survenues via des applications tierces liées à sa plateforme. L'entreprise a constaté une activité suspecte impliquant des applications publiées par Gainsight, qui se connectent à Salesforce et sont gérées par les clients.

L'incident ne provient pas d'une faille de sécurité au sein de la plateforme CRM de Salesforce elle-même, mais plutôt d'une exploitation de la connexion entre ces applications externes et Salesforce. En réponse, Salesforce a révoqué tous les jetons d'accès et de rafraîchissement actifs associés aux applications Gainsight concernées et les a temporairement retirées de l'AppExchange. Les clients affectés ont été informés.

Ce mode opératoire rappelle la brèche de sécurité de Salesloft en août 2025, où des jetons OAuth volés avaient permis à des acteurs malveillants d'accéder à des données sensibles dans des instances Salesforce. Le groupe d'extorsion ShinyHunters a revendiqué la responsabilité de ces attaques, affirmant avoir accédé à un grand nombre d'instances Salesforce en exploitant des secrets volés lors de la brèche de Salesloft, puis en accédant à Gainsight.

**Points Clés :**

*   **Cible :** Données clients hébergées sur Salesforce.
*   **Vecteur d'attaque :** Exploitation de la connexion entre des applications tierces (Gainsight) et la plateforme Salesforce.
*   **Méthode :** Accès non autorisé à des données clients via la connexion d'applications tierces.
*   **Contexte :** Incident similaire à la brèche de Salesloft, où des jetons OAuth volés ont été utilisés.
*   **Acteurs présumés :** ShinyHunters.

**Vulnérabilités / Failles exploitées :**

*   Il n'y a pas de CVE spécifique mentionné dans l'article. La vulnérabilité réside dans l'exploitation des mécanismes de connexion (jetons OAuth volés suite à une compromission précédente de Salesloft) permettant un accès non autorisé aux données via des applications tierces connectées. L'article suggère que les secrets volés lors de la brèche de Salesloft ont permis d'accéder à Gainsight, qui a ensuite été utilisé pour accéder aux instances Salesforce.

**Recommandations :**

*   **Pour Salesforce (mesures prises) :**
    *   Révocation des jetons d'accès et de rafraîchissement liés aux applications Gainsight.
    *   Retrait temporaire des applications concernées de l'AppExchange.
    *   Notification des clients impactés.
*   **Pour les clients Salesforce :**
    *   Être vigilant quant aux applications tierces connectées à leur instance Salesforce.
    *   Contacter le support Salesforce pour toute assistance supplémentaire.
    *   Surveiller les activités suspectes dans leurs instances.
*   **Implicitement pour les éditeurs d'applications tierces et les clients :**
    *   Sécuriser rigoureusement les jetons d'authentification et les secrets.
    *   Mettre en place des contrôles d'accès stricts et une surveillance continue des connexions entre applications.
    *   Répondre rapidement et de manière transparente aux incidents de sécurité touchant leurs produits.

---
[Source](https://www.bleepingcomputer.com/news/security/salesforce-investigates-customer-data-theft-via-gainsight-breach/){:target="_blank"}
