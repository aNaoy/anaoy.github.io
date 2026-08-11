---
title: 'Wesco confirms security incident after ExfilSquad claims data theft'
date: 2026-08-11
permalink: /posts/2026/08/11/wesco-confirms-security-incident-after-exfilsquad-claims-data-theft/
tags:
- veille-cyber
- bleepingcomp
---
### Incident de sécurité chez Wesco : ExfilSquad revendique un vol de données

Le géant de la chaîne d'approvisionnement Wesco a confirmé faire l'objet d'une enquête après que le groupe de cybercriminels « ExfilSquad » a affirmé avoir exfiltré 2,6 millions d'enregistrements provenant de son environnement CRM cloud. Bien que le groupe de pirates ait publié des données en ligne, Wesco minimise l'incident, affirmant ne pas avoir constaté de perturbation opérationnelle et jugeant que les informations sensibles (paiements, données financières) ne sont pas compromises.

**Points clés :**
*   **Auteur de l'attaque :** ExfilSquad, un groupe spécialisé dans l'extorsion de données.
*   **Périmètre :** Environnement CRM cloud de l'entreprise.
*   **Revendication des attaquants :** Vol de 2,6 millions d'enregistrements incluant des informations personnelles (PII), des profils d'utilisateurs CRM et des métadonnées d'authentification.
*   **Position de l'entreprise :** Wesco conteste la gravité de la fuite et affirme qu'aucun rançongiciel ni logiciel malveillant n'a été détecté.

**Vulnérabilités :**
*   Aucune CVE spécifique n'a été attribuée à cet incident. Toutefois, des recherches externes suggèrent que le groupe ExfilSquad exploite fréquemment des **tables de données mal configurées** (notamment sur des portails Microsoft Power Pages), une méthode souvent utilisée pour accéder illégalement à des données exposées sur le cloud.

**Recommandations :**
*   **Audit des configurations cloud :** Examiner rigoureusement les autorisations et les paramètres de sécurité des tables de données dans les solutions CRM (ex: Microsoft Dynamics 365) et les portails web associés.
*   **Surveillance des accès :** Mettre en place une surveillance renforcée des accès aux données sensibles, particulièrement lorsque des identifiants valides sont utilisés, afin de détecter les comportements inhabituels après une authentification légitime.
*   **Gestion des identités :** Appliquer le principe du moindre privilège pour limiter l'exposition des métadonnées et des profils d'utilisateurs en cas de compromission d'un compte.

---
[Source](https://www.bleepingcomputer.com/news/security/wesco-confirms-security-incident-after-exfilsquad-claims-data-theft/){:target="_blank"}
