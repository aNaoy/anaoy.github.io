---
title: 'Learning from the Vercel breach: Shadow AI & OAuth sprawl'
date: 2026-04-29
permalink: /posts/2026/04/29/learning-from-the-vercel-breach-shadow-ai-oauth-sprawl/
tags:
- veille-cyber
- bleepingcomp
---
### La prolifération des intégrations OAuth : un risque critique pour la sécurité d'entreprise

La montée en puissance des outils d'intelligence artificielle a accéléré le phénomène de « Shadow IT » (informatique fantôme), multipliant les ponts persistants entre les environnements d'entreprise et des services tiers via des jetons OAuth. Le cas récent de la compromission de Vercel illustre parfaitement ce danger : un employé a connecté une application tierce (Context.ai) à son compte Google Workspace. Lorsque Context.ai a été piraté, les attaquants ont utilisé ces accès persistants pour infiltrer Vercel.

**Points clés :**
* **Shadow Integrations :** L'ajout incontrôlé d'applications tierces crée des dépendances de sécurité invisibles et durables.
* **Le rôle des infostealers :** Les brèches chez des tiers (comme Context.ai, Salesloft ou Gainsight) sont souvent le point de départ, permettant aux attaquants d'exploiter des jetons d'authentification volés.
* **L'explosion du phishing par code d'appareil :** Une augmentation de 37x des attaques par « device code phishing » a été observée cette année, facilitant l'exfiltration massive de données via OAuth.
* **Surface d'attaque étendue :** Le risque ne se limite pas aux plateformes principales (Google/Microsoft) mais s'étend à tout l'écosystème SaaS interconnecté.

**Vulnérabilités :**
* **Abus de jetons OAuth :** Utilisation de jetons légitimes par des attaquants pour accéder à des données sensibles (API keys, identifiants, documents).
* **Phishing de type "Device Code" :** Manipulation des utilisateurs pour qu'ils accordent des accès API complets à des applications malveillantes.
* **Faiblesse de gestion des permissions :** Manque de contrôle centralisé sur les applications tierces ajoutées par les utilisateurs.
* *Note : Bien que l'article mentionne des campagnes massives de vol de données, il n'identifie pas de CVE spécifique, les attaques reposant sur le détournement de fonctionnalités légitimes (OAuth) plutôt que sur l'exploitation de failles logicielles documentées.*

**Recommandations :**
* **Appliquer une politique "Default-Deny" :** Restreindre la possibilité pour les utilisateurs de consentir à de nouvelles intégrations OAuth sans approbation préalable de l'administration.
* **Audits réguliers :** Inventorier et supprimer systématiquement les intégrations OAuth obsolètes ou inutilisées dans l'ensemble de l'environnement SaaS.
* **Visibilité au-delà du Cloud principal :** Étendre la surveillance des accès OAuth à toutes les applications SaaS utilisées, et pas uniquement à Google Workspace ou Microsoft 365.
* **Gestion des extensions de navigateur :** Contrôler et limiter les extensions tierces, souvent vecteurs d'entrée pour les attaquants.

---
[Source](https://www.bleepingcomputer.com/news/security/learning-from-the-vercel-breach-shadow-ai-and-oauth-sprawl/){:target="_blank"}
