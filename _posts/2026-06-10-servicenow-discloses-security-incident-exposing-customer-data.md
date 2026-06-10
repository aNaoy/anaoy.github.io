---
title: 'ServiceNow discloses security incident exposing customer data'
date: 2026-06-10
permalink: /posts/2026/06/10/servicenow-discloses-security-incident-exposing-customer-data/
tags:
- veille-cyber
- bleepingcomp
---
### Incident de sécurité chez ServiceNow : fuite de données via une API vulnérable

ServiceNow a identifié et corrigé une faille de sécurité critique permettant à des attaquants non authentifiés d'accéder à des données sensibles sur des instances clients. L'exploitation a été détectée suite à une activité anormale sur un point de terminaison API.

**Points clés :**
*   **Cause :** Une mauvaise configuration de l'API (`/api/now/related_list_edit/create`) permettait des requêtes sans authentification (`requires_authentication=false`).
*   **Impact :** Les attaquants ont pu interroger des tables de données clients, potentiellement contenant des tickets de support, des identifiants, des jetons API, des documents internes et des rapports d'incidents.
*   **Cible :** Principalement les clients utilisant la version « Australia » ou des versions antérieures avec des configurations spécifiques.
*   **Vulnérabilité :** Aucune CVE n'a été attribuée pour le moment par l'éditeur.

**Recommandations pour les administrateurs :**
*   **Audit des logs :** Rechercher toute requête suspecte ciblant le point de terminaison `/api/now/related_list_edit`, particulièrement celles provenant de l'adresse IP `51.159.98.241`.
*   **Analyse des données exposées :** Vérifier les tickets et enregistrements potentiellement consultés pour identifier d'éventuelles compromissions d'informations sensibles.
*   **Mesures correctives :** Procéder à une rotation immédiate des identifiants, mots de passe et jetons API ayant pu transiter dans les flux de support.
*   **Sécurisation :** S'assurer que le journalisation (logging) des API est active et surveiller les configurations d'accès pour garantir que seuls les utilisateurs authentifiés ont des droits de consultation.

---
[Source](https://www.bleepingcomputer.com/news/security/servicenow-discloses-security-incident-exposing-customer-data/){:target="_blank"}
