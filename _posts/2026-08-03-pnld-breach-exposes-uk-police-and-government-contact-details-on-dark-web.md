---
title: 'PNLD Breach Exposes U.K. Police and Government Contact Details on Dark Web'
date: 2026-08-03
permalink: /posts/2026/08/03/pnld-breach-exposes-uk-police-and-government-contact-details-on-dark-web/
tags:
- veille-cyber
- hackernews
---
### Fuite de données critiques au sein du PNLD : une alerte sur la sécurité des portails Microsoft Power Pages

La *Police National Legal Database* (PNLD) au Royaume-Uni a confirmé une fuite de données exposant des informations de contact de policiers, de membres du gouvernement et de citoyens ayant utilisé le service « Ask the Police ». Les données compromises incluent les noms et adresses e-mail professionnelles. Bien qu'aucun mot de passe n'ait été dérobé, cette exposition augmente significativement les risques d'attaques par hameçonnage ciblé.

**Points clés :**
*   **Incident :** Publication d'informations sur le dark web identifiée le 26 juillet 2026.
*   **Impact :** Personnel de police, partenaires gouvernementaux et utilisateurs publics. Aucune donnée confidentielle relative à des enquêtes criminelles ou des victimes n'est concernée.
*   **Auteurs présumés :** Le groupe *ExfilSquad*, bien que le PNLD n'ait pas formellement attribué l'incident.
*   **Méthode suspectée :** L'analyse d'experts pointe vers une mauvaise configuration des portails Microsoft Power Pages (accès anonyme activé sur des tables de base de données Dataverse), permettant une exfiltration sans authentification. 
*   **Vulnérabilité :** Aucune CVE n'est associée à cet incident. Il s'agit d'un problème de **configuration de sécurité** (mauvaise gestion des permissions de table « Anonymous Users ») plutôt que d'une faille logicielle.

**Recommandations de sécurité :**
*   **Contrôle de gouvernance :** Activer les paramètres de niveau locataire (tenant-level) pour bloquer la lecture des données Dataverse par des utilisateurs non authentifiés.
*   **Audit des permissions :** Réviser strictement les permissions des tables « Anonymous Users » et désactiver les interfaces API Web ou les flux OData hérités si ceux-ci ne sont pas indispensables.
*   **Validation proactive :** Tester régulièrement l'accès aux données du portail depuis une session de navigateur non authentifiée pour s'assurer qu'aucune information sensible n'est exposée.
*   **Veille :** En cas d'utilisation de solutions de type Power Apps/Pages, suivre les directives de sécurisation de Microsoft pour le contrôle des accès aux données.

---
[Source](https://thehackernews.com/2026/08/pnld-breach-exposes-uk-police-and.html){:target="_blank"}
