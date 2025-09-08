---
title: 'Salesloft: March GitHub repo breach led to Salesforce data theft attacks'
date: 2025-09-08
permalink: /posts/2025/09/08/salesloft-march-github-repo-breach-led-to-salesforce-data-theft-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Breach de la chaîne d'approvisionnement affectant Salesloft et Salesforce**

Une intrusion initiale dans le dépôt GitHub de Salesloft, survenue entre mars et juin, a permis aux attaquants de voler des jetons OAuth de Drift. Ces jetons ont ensuite été utilisés dans des attaques généralisées de vol de données Salesforce en août. Des groupes tels que ShinyHunters et Scattered Spider sont impliqués, ainsi que le groupe UNC6395 identifié par Google. Les attaquants ont principalement ciblé les tickets de support Salesforce pour dérober des identifiants, des clés d'accès AWS et des jetons d'accès Snowflake. Salesloft a résolu la vulnérabilité en réinitialisant les identifiants, en renforçant ses défenses et en isolant son infrastructure. L'intégration avec Salesforce a été rétablie.

**Points clés :**

*   L'attaque a débuté par une compromission du dépôt GitHub de Salesloft.
*   Des jetons OAuth volés ont été utilisés pour accéder aux données Salesforce.
*   Les informations dérobées visaient particulièrement les identifiants et clés d'accès.
*   De nombreuses entreprises clientes de Salesloft et utilisant Salesforce ont été affectées.

**Vulnérabilités :**

*   Accès non autorisé au dépôt GitHub de Salesloft.
*   Vol de jetons OAuth de la plateforme Drift.
*   Accès à l'environnement AWS de Drift.

**Recommandations :**

*   Réinitialisation des identifiants et authentifications compromises.
*   Renforcement des mesures de sécurité et segmentation des infrastructures.
*   Vérification de la présence d'indicateurs de compromission supplémentaires.
*   Restauration et synchronisation des données pour les utilisateurs affectés.

---
[Source](https://www.bleepingcomputer.com/news/security/salesloft-march-github-repo-breach-led-to-salesforce-data-theft-attacks/){:target="_blank"}
