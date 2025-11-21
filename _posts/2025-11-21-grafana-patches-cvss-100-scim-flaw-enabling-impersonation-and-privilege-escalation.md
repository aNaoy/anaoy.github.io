---
title: 'Grafana Patches CVSS 10.0 SCIM Flaw Enabling Impersonation and Privilege Escalation'
date: 2025-11-21
permalink: /posts/2025/11/21/grafana-patches-cvss-100-scim-flaw-enabling-impersonation-and-privilege-escalation/
tags:
- veille-cyber
- hackernews
---
## Vulnérabilité Critique dans Grafana Enterprise

Une faille de sécurité d'une gravité maximale, notée **CVE-2025-41115** avec un score CVSS de 10.0, a été corrigée dans Grafana Enterprise. Cette vulnérabilité affecte le composant SCIM (System for Cross-domain Identity Management), utilisé pour l'approvisionnement et la gestion automatisés des utilisateurs.

### Points Clés

*   La faille permet potentiellement une **escalade de privilèges** ou **l'usurpation d'identité** d'utilisateur.
*   Elle est active uniquement lorsque la fonctionnalité SCIM est activée et configurée, et que le drapeau `enableSCIM` est à `true` ainsi que l'option `user_sync_enabled` à `true` dans le bloc `[auth.scim]`.
*   L'exploitation implique qu'un client SCIM compromis provisionne un utilisateur avec un `externalId` numérique.
*   Grafana interprète cet `externalId` numérique comme un identifiant d'utilisateur interne, pouvant mener à la substitution d'un compte existant, y compris le compte administrateur.

### Vulnérabilité

*   **CVE-2025-41115**: Affecte les versions de Grafana Enterprise 12.0.0 à 12.2.1.

### Recommandations

Les utilisateurs de Grafana Enterprise doivent appliquer les mises à jour de sécurité suivantes dans les plus brefs délais pour atténuer les risques :

*   Grafana Enterprise 12.0.6+security-01
*   Grafana Enterprise 12.1.3+security-01
*   Grafana Enterprise 12.2.1+security-01
*   Grafana Enterprise 12.3.0

---
[Source](https://thehackernews.com/2025/11/grafana-patches-cvss-100-scim-flaw.html){:target="_blank"}
