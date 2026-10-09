---
title: 'Citrix Patches Critical NetScaler Flaw That Could Enable RCE in SAML Deployments'
date: 2026-10-09
permalink: /posts/2026/10/09/citrix-patches-critical-netscaler-flaw-that-could-enable-rce-in-saml-deployments/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans Citrix NetScaler : Risque d'exécution de code à distance

Citrix a publié des correctifs pour une faille de sécurité critique affectant ses appliances NetScaler ADC et NetScaler Gateway. Cette vulnérabilité, classée avec un score CVSS de 9,5, peut permettre l'exécution de code à distance (RCE) ou un déni de service (DoS) si les instances sont configurées en tant que fournisseur d'identité (IdP) ou fournisseur de services (SP) SAML.

**Points clés :**
*   **Impact :** La vulnérabilité touche spécifiquement les déploiements utilisant les configurations SAML.
*   **État de la menace :** Aucune exploitation active n'a été signalée pour cette faille spécifique, bien que d'autres vulnérabilités NetScaler fassent actuellement l'objet d'attaques actives.
*   **Détection :** Les administrateurs peuvent vérifier si leur instance est vulnérable en recherchant les commandes `add authentication samlAction` ou `add authentication samlIdPProfile` dans leur configuration.

**Vulnérabilité identifiée :**
*   **CVE-2026-107406 :** Vulnérabilité de dépassement de mémoire (memory overflow).

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les versions corrigées fournies par Citrix dès que possible :
    *   NetScaler ADC/Gateway 14.1-73.46 ou version ultérieure.
    *   NetScaler ADC/Gateway 13.1-64.29 ou version ultérieure.
    *   NetScaler ADC 14.1-FIPS 14.1-73.46 FIPS ou version ultérieure.
    *   NetScaler ADC 13.1-FIPS / 13.1-NDcPP 13.1.37.283 ou version ultérieure.
*   **Environnements hybrides :** Les déploiements "Secure Private Access" utilisant NetScaler sont également concernés et doivent être mis à jour.

---
[Source](https://thehackernews.com/2026/10/citrix-patches-critical-netscaler-flaw.html){:target="_blank"}
