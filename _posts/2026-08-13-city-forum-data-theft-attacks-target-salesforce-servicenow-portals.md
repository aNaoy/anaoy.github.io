---
title: '"City-Forum" data-theft attacks target Salesforce, ServiceNow portals'
date: 2026-08-13
permalink: /posts/2026/08/13/city-forum-data-theft-attacks-target-salesforce-servicenow-portals/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de vol de données « City-Forum » : cibles Salesforce et ServiceNow

Une campagne de cyberespionnage active, baptisée « City-Forum », exploite des erreurs de configuration pour exfiltrer des données depuis des portails Salesforce Experience Cloud et ServiceNow. L'attaquant utilise une infrastructure centralisée (IP `158.220.87.79`) pour scanner les entreprises, incluant des institutions financières, des télécoms et des entités du secteur public.

**Points clés :**
* **Méthode :** Les attaques ne reposent pas sur l'exploitation d'une vulnérabilité logicielle (CVE), mais sur l'abus de comptes « invités » (guest users) disposant de droits trop permissifs.
* **Techniques Salesforce :**
    * Sur l'ancien framework *Aura* : énumération des objets via les contrôleurs `HostConfigController` et `SelectableListDataProviderController`.
    * Sur le framework *LWR* : utilisation de l'API GraphQL pour extraire des données publiques.
    * Vérification des fonctions d'auto-enregistrement (`/SiteRegister`) pour tenter une élévation de privilèges.
* **Techniques ServiceNow :** Exploitation du point de terminaison de recherche public (`/api/now/sp/search`) pour énumérer des données sensibles via des requêtes anonymes.
* **Indicateurs de compromission (IOC) :**
    * Adresse IP : `158.220.87.79` (hébergée chez Contabo).
    * User-Agent : `Go-http-client/1.1`.

**Vulnérabilités :**
Aucune CVE n'est associée à cette campagne. Il s'agit de **failles de configuration** liées à des règles de partage de données et des permissions excessives accordées aux utilisateurs non authentifiés (invités).

**Recommandations :**
* **Salesforce :**
    * Auditer strictement les règles de partage, les permissions d'objets/champs et les accès aux fichiers pour les comptes invités.
    * Désactiver l'option « Accès aux API publiques » dans l'Experience Builder pour les sites LWR si elle n'est pas nécessaire.
    * Désactiver l'auto-enregistrement si l'entreprise ne le requiert pas.
* **ServiceNow :**
    * Examiner les sources de recherche exposées sur les portails de services.
    * Restreindre l'accès aux sources de données sensibles via une authentification obligatoire, en limitant les requêtes anonymes sur l'API de recherche.

---
[Source](https://www.bleepingcomputer.com/news/security/city-forum-data-theft-attacks-target-salesforce-servicenow-portals/){:target="_blank"}
