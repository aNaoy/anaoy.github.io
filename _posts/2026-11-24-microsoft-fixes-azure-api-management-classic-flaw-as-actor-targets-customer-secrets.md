---
title: 'Microsoft Fixes Azure API Management Classic Flaw as Actor Targets Customer Secrets'
date: 2026-11-24
permalink: /posts/2026/11/24/microsoft-fixes-azure-api-management-classic-flaw-as-actor-targets-customer-secrets/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans Azure API Management Classic : Fuite de secrets

Une faille de sécurité identifiée dans les instances « Classic » d'Azure API Management (APIM) a permis à des acteurs malveillants d'accéder à des secrets et des jetons d'authentification. Bien que Microsoft ait corrigé la vulnérabilité le 19 novembre 2026, des entreprises, notamment dans le secteur énergétique norvégien, ont été ciblées par cette exploitation.

**Points clés :**
*   **Périmètre :** Seules les instances de niveau « Classic » sont concernées ; les versions v2 ne sont pas affectées.
*   **Risque :** Les attaquants pouvaient exfiltrer des informations sensibles si le service n'était pas configuré selon les meilleures pratiques de sécurité.
*   **Impact :** Accès potentiel aux clés d'abonnement, aux secrets clients (OpenID Connect, fournisseurs d'identité), aux « Named Values » et aux jetons d'API de gestion.

**Vulnérabilité :**
*   **CVE :** Aucune référence CVE spécifique n'a été publiée à ce jour dans l'avis officiel de Microsoft. La faille concerne un accès non autorisé à la fonctionnalité de gestion lié à une configuration par défaut vulnérable sur les instances legacy.

**Recommandations :**
*   **Rotation des secrets :** Il est impératif d'identifier et de renouveler tous les secrets, clés d'abonnement et identifiants configurés dans les instances APIM Classic.
*   **Audit de configuration :** Appliquer strictement les recommandations de sécurité de Microsoft pour le durcissement des services Azure.
*   **Surveillance :** Inspecter les journaux d'accès pour détecter toute utilisation inhabituelle des identifiants compromis.
*   **Migration :** Envisager le passage vers les versions v2 (ou supérieures) du service, qui ne sont pas exposées à ce vecteur d'attaque spécifique.

---
[Source](https://thehackernews.com/2026/11/microsoft-fixes-azure-api-management.html){:target="_blank"}
