---
title: 'Salesforce Disables Klue App Integration After OAuth Token Abuse Exposes Customer Data'
date: 2026-06-19
permalink: /posts/2026/06/19/salesforce-disables-klue-app-integration-after-oauth-token-abuse-exposes-customer-data/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement SaaS : L'affaire Klue et Salesforce

L'entreprise de renseignement compétitif Klue a subi une intrusion majeure ayant permis au groupe cybercriminel « Icarus » d'accéder aux environnements Salesforce de plusieurs clients, dont Huntress, Jamf, Recorded Future et Tanium. L'incident ne provient pas d'une faille de sécurité de la plateforme Salesforce elle-même, mais d'une compromission de l'infrastructure d'intégration de Klue.

**Points clés :**
* **Vecteur d'attaque :** Utilisation d'identifiants obsolètes pour accéder à un service d'intégration, permettant ensuite l'injection de code malveillant.
* **Méthode :** Vol de jetons OAuth de clients tiers pour interroger directement l'API REST de Salesforce et exfiltrer massivement des données CRM (contacts, devis, opportunités commerciales).
* **Impact :** Les attaquants ont pu automatiser des requêtes massives pendant plus de 24 heures sans déclencher d'alertes, en se faisant passer pour une application de confiance.
* **Attribution :** Le groupe Icarus, actif depuis avril 2026, est responsable de l'exfiltration et tente désormais d'extorquer les entreprises victimes.

**Vulnérabilités :**
* **Abus de jetons OAuth :** Les jetons permettent un accès persistant et privilégié sans nécessiter de mot de passe ou de double authentification (MFA).
* **Gestion des identités non humaines :** Absence de surveillance étroite des comptes de service, souvent moins protégés que les comptes utilisateurs finaux.
* **Hygiène des identifiants :** Présence d'identifiants hérités (legacy) longtemps oubliés mais toujours actifs au sein des infrastructures.

**Recommandations :**
* **Audit des intégrations :** Révoquer et réinitialiser les jetons OAuth des applications tierces ayant des accès aux données sensibles.
* **Surveillance accrue :** Mettre en place un monitoring spécifique sur les activités des comptes de service (API) pour détecter des volumes de requêtes anormalement élevés (ex: scripts Python automatisés).
* **Gestion du cycle de vie des identités :** Désactiver immédiatement tout identifiant ou service obsolète ou inutilisé.
* **Principe du moindre privilège :** Restreindre les scopes (autorisations) accordés aux jetons OAuth au strict nécessaire pour limiter l'impact en cas de compromission.

---
[Source](https://thehackernews.com/2026/06/salesforce-disables-klue-app.html){:target="_blank"}
