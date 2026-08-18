---
title: 'One Attacker Has Scraped Both Salesforce and ServiceNow Portals Since 2025'
date: 2026-08-18
permalink: /posts/2026/08/18/one-attacker-has-scraped-both-salesforce-and-servicenow-portals-since-2025/
tags:
- veille-cyber
- hackernews
---
### Campagne "City Forum" : Exploitation persistante des accès invités Salesforce et ServiceNow

Une infrastructure unique, identifiée via l'adresse IP `158.220.87.79`, mène depuis début 2025 une campagne de scraping de données à grande échelle ciblant les portails Salesforce et ServiceNow de diverses organisations (télécoms, banques, secteur public). L'attaquant utilise un programme personnalisé (identifiable par l'agent utilisateur `Go-http-client`) pour extraire des enregistrements via des accès invités mal configurés.

**Points clés :**
*   **Technique avancée :** Contrairement aux méthodes classiques exploitant le framework Aura de Salesforce, cette campagne cible également le *Lightning Web Runtime* (via l'UI-API) et l'endpoint de recherche native `POST /api/now/sp/search` de ServiceNow.
*   **Volume important :** Certains portails ont enregistré plus de 560 000 requêtes provenant de cette même source.
*   **Vulnérabilité sous-jacente :** Il ne s'agit pas d'une faille logicielle classique (CVE), mais d'un problème de **privilèges excessifs accordés au profil "invité"**. Si un profil invité peut accéder à un enregistrement, celui-ci est exposé publiquement, indépendamment de la configuration de connexion.

**Recommandations pour la sécurisation :**

**Pour Salesforce :**
*   **Audit :** Examiner les règles de partage des invités (Guest Sharing Rules).
*   **Restriction :** Supprimer les accès inutiles aux objets et champs pour les profils invités.
*   **Configuration :** Désactiver l'auto-enregistrement (`/SiteRegister`) s'il n'est pas requis et limiter l'accès des invités aux API publiques via l' *Experience Builder*.
*   **Détection :** Surveiller les journaux `AuraRequest` et les accès suspects vers `/webruntime/api/services/data`.

**Pour ServiceNow :**
*   **Audit :** Cartographier les sources de recherche exposées sur les portails publics.
*   **Restriction :** Revoir les critères de lecture de la base de connaissances (*Knowledge Base*) pour restreindre strictement ce qui est retourné aux recherches anonymes.
*   **Détection :** Filtrer les journaux de transaction (`syslog_transaction`) à la recherche de requêtes vers `/api/now/sp/search` présentant une longueur de sortie inhabituelle.

---
[Source](https://thehackernews.com/2026/08/one-attacker-has-scraped-both.html){:target="_blank"}
