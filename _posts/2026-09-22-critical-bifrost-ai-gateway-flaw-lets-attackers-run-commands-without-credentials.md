---
title: 'Critical Bifrost AI Gateway Flaw Lets Attackers Run Commands Without Credentials'
date: 2026-09-22
permalink: /posts/2026/09/22/critical-bifrost-ai-gateway-flaw-lets-attackers-run-commands-without-credentials/
tags:
- veille-cyber
- hackernews
---
### Exécution de code à distance critique sur la passerelle IA Bifrost

La passerelle IA open-source Bifrost présente des vulnérabilités critiques permettant à un attaquant non authentifié d'exécuter des commandes arbitraires sur le serveur. Ces failles découlent principalement d'une configuration par défaut où l'authentification de l'API de gestion est désactivée.

**Points clés :**
* Les attaquants peuvent détourner le processus de la passerelle pour accéder à des clés API sensibles stockées pour les fournisseurs LLM.
* L'image Docker officielle est particulièrement exposée car elle expose l'API de gestion sur toutes les interfaces (0.0.0.0).
* Les instances ayant fonctionné avec l'authentification désactivée et une API exposée doivent être considérées comme compromises.

**Vulnérabilités identifiées :**
* **CVE-2026-90898 (Score CVSS 9.8) :** Injection de commande via l'enregistrement d'un client MCP (stdio). L'exécution se produit immédiatement lors de l'envoi d'une requête POST non authentifiée sur `/api/mcp/client`.
* **CVE-2026-86242 (Score CVSS 8.1) :** Permet l'enregistrement d'un plugin personnalisé via une URL HTTP. Sur les builds liés dynamiquement, cela entraîne l'exécution de code distant.

**Recommandations :**
* **Mise à jour immédiate :** Passer à la version `transports/v2.1.0` pour corriger la faille MCP.
* **Sécurisation de la configuration :** Si la mise à jour est impossible, activer impérativement l'authentification (`governance.auth_config.is_enabled = true`) et utiliser des identifiants robustes.
* **Isolation réseau :** Restreindre l'accès à l'API de gestion aux réseaux de confiance uniquement.
* **Réponse aux incidents :** Procéder à une rotation immédiate de toutes les clés d'API et identifiants stockés si l'instance a été exposée.

---
[Source](https://thehackernews.com/2026/09/critical-bifrost-ai-gateway-flaw-lets.html){:target="_blank"}
