---
title: 'Salesloft breached to steal OAuth tokens for Salesforce data-theft attacks'
date: 2025-08-27
permalink: /posts/2025/08/27/salesloft-breached-to-steal-oauth-tokens-for-salesforce-data-theft-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Des données sensibles dérobées via une faille dans l'intégration Salesloft-Salesforce**

Une campagne d'attaques a ciblé la plateforme de vente Salesloft, exploitant une vulnérabilité dans son intégration avec Salesforce via l'agent de chat Drift. Les acteurs malveillants sont parvenus à dérober des jetons d'authentification OAuth et de rafraîchissement, leur permettant d'accéder aux instances Salesforce des clients et d'exfiltrer des données sensibles.

**Points clés et déroulement de l'attaque :**

*   **Cible :** Plateforme Salesloft, spécifiquement son intégration SalesDrift avec Salesforce.
*   **Méthode :** Vol de jetons OAuth et de rafraîchissement utilisés par l'intégration Drift pour accéder à Salesforce.
*   **Objectif :** Exfiltration de données sensibles depuis les instances Salesforce des clients.
*   **Données volées :** Outre l'accès à Salesforce, les attaquants ont recherché des informations critiques telles que des clés d'accès AWS (identifiées par le préfixe "AKIA"), des mots de passe et des jetons d'accès liés à Snowflake.
*   **Techniques d'obscurcissement :** Utilisation du réseau Tor et d'hébergeurs tels qu'AWS et DigitalOcean pour masquer leur infrastructure. Des chaînes User-Agent spécifiques, incluant "python-requests/2.32.4", "Python/3.11 aiohttp/3.12.15", "Salesforce-Multi-Org-Fetcher/1.0" et "Salesforce-CLI/1.0", ont été observées.
*   **Acteurs suspectés :** Google classe le groupe sous le nom de UNC6395. Le groupe ShinyHunters a initialement revendiqué l'activité, bien que Google n'ait pas trouvé de preuves concrètes de leur implication directe dans cette attaque spécifique.

**Vulnérabilités et Exploitations :**

*   **Détournement de jetons d'authentification :** Les jetons OAuth et de rafraîchissement de l'intégration Drift-Salesforce ont été compromis, permettant un accès non autorisé.
*   **Requêtes SOQL malveillantes :** Une fois dans Salesforce, les attaquants ont utilisé des requêtes SOQL pour extraire des informations sensibles intégrées dans les cas de support, notamment des jetons d'authentification, des mots de passe et des secrets.

**Recommandations :**

*   **Réinitialisation des jetons :** Salesloft a révoqué tous les jetons d'accès et de rafraîchissement pour l'application Drift. Les administrateurs doivent déconnecter puis reconnecter l'intégration Salesforce via les paramètres de Salesloft.
*   **Rotation des identifiants :** Les administrateurs des environnements concernés doivent immédiatement faire pivoter tous les identifiants compromis.
*   **Analyse des logs Salesforce :** Il est crucial de rechercher dans les journaux Salesforce des indicateurs de compromission et des preuves d'exposition de données. Google recommande de rechercher spécifiquement des chaînes telles que "AKIA", "Snowflake", "snowflakecomputing.com", "password", "secret", "key", ainsi que des URLs de connexion spécifiques à l'organisation (VPN, SSO).
*   **Vérification des cas de support :** Examiner les cas de support Salesforce pour toute information sensible potentiellement dérobée.

Cette attaque s'inscrit dans une série plus large de compromissions de données Salesforce, souvent attribuées à des campagnes d'ingénierie sociale impliquant du vishing (hameçonnage vocal) pour inciter les employés à connecter des applications OAuth malveillantes.

---
[Source](https://www.bleepingcomputer.com/news/security/salesloft-breached-to-steal-oauth-tokens-for-salesforce-data-theft-attacks/){:target="_blank"}
