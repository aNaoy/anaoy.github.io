---
title: 'Google warns Salesloft breach impacted some Workspace accounts'
date: 2025-08-29
permalink: /posts/2025/08/29/google-warns-salesloft-breach-impacted-some-workspace-accounts/
tags:
- veille-cyber
- bleepingcomp
---
**Piratage de Salesloft : Impact Étendu sur les Comptes Google Workspace**

Une brèche de sécurité affectant la plateforme Salesloft Drift, initialement limitée à des instances Salesforce, s'est révélée plus étendue que prévu. Les attaquants ont exploité des jetons OAuth volés pour accéder non seulement aux données de Salesforce, mais également à un petit nombre de comptes Google Workspace.

**Points Clés :**

*   La campagne, identifiée comme UNC6395 par Google Threat Intelligence (Mandiant), a d'abord ciblé les intégrations entre Salesloft Drift et Salesforce.
*   Les attaquants ont accédé à des données sensibles dans Salesforce, incluant des clés d'accès AWS, des jetons Snowflake et des mots de passe, dans le but probable d'extorsion.
*   De nouvelles informations ont révélé que les jetons OAuth pour l'intégration "Drift Email" ont également été compromis.
*   Ces jetons ont permis aux acteurs de la menace d'accéder à des e-mails de comptes Google Workspace directement intégrés à Drift.
*   Aucun autre compte dans les domaines concernés n'a été touché, et Google Workspace ou Alphabet n'ont pas été compromis.

**Vulnérabilités :**

*   L'utilisation de jetons OAuth volés pour l'accès aux données via les intégrations Salesloft Drift. Aucun CVE spécifique n'est mentionné dans l'article pour cette brèche.

**Recommandations :**

*   Tous les clients de Salesloft Drift doivent considérer tout jeton d'authentification stocké ou connecté à la plateforme comme potentiellement compromis.
*   Révoquer et faire pivoter les identifiants des applications connectées à Drift.
*   Examiner tous les systèmes connectés pour détecter toute activité suspecte.
*   Vérifier toutes les intégrations tierces associées aux instances Drift et réinitialiser les identifiants potentiellement exposés.
*   Salesforce a désactivé les intégrations Drift avec Salesforce, Slack et Pardot jusqu'à la fin de l'enquête.

---
[Source](https://www.bleepingcomputer.com/news/security/google-warns-salesloft-breach-impacted-some-workspace-accounts/){:target="_blank"}
