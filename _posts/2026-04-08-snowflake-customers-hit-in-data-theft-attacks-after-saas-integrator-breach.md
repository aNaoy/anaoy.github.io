---
title: 'Snowflake customers hit in data theft attacks after SaaS integrator breach'
date: 2026-04-08
permalink: /posts/2026/04/08/snowflake-customers-hit-in-data-theft-attacks-after-saas-integrator-breach/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement : Fuites de données via Anodot

Une série de vols de données a touché plusieurs entreprises utilisant la plateforme Snowflake, à la suite d'une compromission chez le fournisseur d'intégration SaaS **Anodot**. Le groupe de cybercriminels **ShinyHunters** est à l'origine de l'attaque et tente actuellement d'extorquer les victimes pour empêcher la publication de données dérobées.

**Points clés :**
* **Vecteur d'attaque :** Des jetons d'authentification appartenant à Anodot ont été dérobés, permettant aux attaquants d'accéder aux comptes Snowflake de ses clients.
* **Impact :** Un nombre restreint de clients Snowflake a été touché. Les attaquants ont également tenté de cibler Salesforce, mais ont été bloqués par les systèmes de détection.
* **Réaction :** Snowflake a verrouillé les comptes potentiellement compromis par précaution. Anodot a suspendu l'ensemble de ses connecteurs.
* **Origine :** L'incident ne provient pas d'une vulnérabilité interne de Snowflake, mais d'une compromission de la chaîne d'approvisionnement (fournisseur tiers).

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée à cet incident. Il s'agit d'une compromission par **vol de jetons d'authentification (Token Theft)** et abus de droits d'accès légitimes via un tiers.

**Recommandations :**
* **Audit des accès tiers :** Révoquer et renouveler les jetons d'authentification utilisés par des services tiers pour accéder aux plateformes de données.
* **Gestion des privilèges :** Appliquer le principe du moindre privilège aux intégrations SaaS, en limitant strictement les permissions accordées aux connecteurs tiers.
* **Surveillance active :** Renforcer la surveillance des journaux d'activité pour détecter toute anomalie de connexion liée à des services d'intégration.
* **Authentification renforcée :** Favoriser l'usage d'identités à durée de vie limitée et, lorsque cela est possible, exiger une authentification forte pour toute connexion via API.

---
[Source](https://www.bleepingcomputer.com/news/security/snowflake-customers-hit-in-data-theft-attacks-after-saas-integrator-breach/){:target="_blank"}
