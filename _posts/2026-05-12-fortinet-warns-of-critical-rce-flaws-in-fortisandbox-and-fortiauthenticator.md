---
title: 'Fortinet warns of critical RCE flaws in FortiSandbox and FortiAuthenticator'
date: 2026-05-12
permalink: /posts/2026/05/12/fortinet-warns-of-critical-rce-flaws-in-fortisandbox-and-fortiauthenticator/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques affectant les solutions Fortinet

Fortinet a publié des correctifs pour deux failles critiques permettant l'exécution de code à distance (RCE) sur ses plateformes FortiAuthenticator et FortiSandbox. Bien qu'aucune exploitation active ne soit signalée pour ces vulnérabilités spécifiques à ce jour, l'historique des produits Fortinet montre qu'ils sont des cibles fréquentes pour les campagnes de ransomware et d'espionnage.

**Points clés :**
*   **FortiAuthenticator :** Une vulnérabilité de contrôle d'accès permet à un attaquant non authentifié d'exécuter des commandes via des requêtes manipulées. La version Cloud n'est pas concernée.
*   **FortiSandbox :** Une faille d'autorisation manquante dans l'interface Web permet à un attaquant non authentifié d'exécuter du code à distance. Les déploiements sur site, Cloud et PaaS sont impactés.

**Vulnérabilités identifiées :**
*   **CVE-2026-44277 :** Problème de contrôle d'accès dans FortiAuthenticator (CWE-284).
*   **CVE-2026-26083 :** Défaut d'autorisation dans l'interface Web de FortiSandbox (CWE-862).

**Recommandations :**
*   **FortiAuthenticator :** Mettre à jour vers les versions 6.5.7, 6.6.9 ou 8.0.3 minimum.
*   **FortiSandbox :** Appliquer les correctifs de sécurité fournis par l'éditeur dès que possible pour protéger l'interface Web.
*   **Veille :** Surveiller les publications du PSIRT de Fortinet, compte tenu de la récurrence des vulnérabilités critiques exploitées activement dans cette gamme de produits.

---
[Source](https://www.bleepingcomputer.com/news/security/fortinet-warns-of-critical-rce-flaws-in-fortisandbox-and-fortiauthenticator/){:target="_blank"}
