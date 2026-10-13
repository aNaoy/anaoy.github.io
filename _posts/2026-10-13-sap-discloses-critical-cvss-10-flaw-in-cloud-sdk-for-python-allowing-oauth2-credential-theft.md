---
title: 'SAP Discloses Critical CVSS 10 Flaw in Cloud SDK for Python Allowing OAuth2 Credential Theft'
date: 2026-10-13
permalink: /posts/2026/10/13/sap-discloses-critical-cvss-10-flaw-in-cloud-sdk-for-python-allowing-oauth2-credential-theft/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans le SDK SAP Cloud pour Python

Une vulnérabilité critique affectant le **SAP Cloud SDK pour Python** permet à un attaquant de détourner les identifiants OAuth2 (Client ID et Client Secret) d'une application en manipulant le sous-domaine du locataire (*tenant subdomain*). Lorsqu'il est malveillant, ce paramètre redirige la requête d'authentification vers un serveur contrôlé par l'attaquant.

**Points clés :**
*   **Nature du risque :** Cette vulnérabilité de type *Server-Side Request Forgery* (SSRF) survient lorsque le SDK construit dynamiquement l'URL de jeton d'accès sans valider correctement l'entrée utilisateur.
*   **Historique :** Bien qu'un correctif initial ait été publié en août (version 0.45.2), des régressions ont été observées dans certaines versions ultérieures (notamment de 0.53.0 à 0.55.0), où le contrôle de validation était absent pour le module de service "Destination".
*   **Impact :** Les applications multi-tenant sur la SAP Business Technology Platform (BTP) utilisant les versions vulnérables sont exposées au vol de leurs identifiants d'authentification.

**Vulnérabilité identifiée :**
*   **CVE-2026-89111** (Score CVSS : 10.0/10).

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version **0.58.4** ou supérieure, qui intègre les correctifs de validation nécessaires.
*   **Vérification de sécurité :** Éviter les versions 0.53.0 à 0.55.0 ainsi que la branche 0.36, qui manquent des contrôles de sécurité requis.
*   **Atténuation temporaire :** Pour les environnements ne pouvant pas être mis à jour immédiatement, SAP préconise de valider manuellement chaque sous-domaine du locataire par une liste blanche de locataires enregistrés avant de le transmettre au SDK.
*   **Renouvellement des secrets :** Bien que non explicitement exigé par SAP, il est fortement recommandé de renouveler les identifiants OAuth2 si une application a utilisé une version vulnérable du SDK.

---
[Source](https://thehackernews.com/2026/10/sap-discloses-critical-cvss-10-flaw-in.html){:target="_blank"}
