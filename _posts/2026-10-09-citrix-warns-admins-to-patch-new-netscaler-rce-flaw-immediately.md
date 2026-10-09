---
title: 'Citrix warns admins to patch new NetScaler RCE flaw immediately'
date: 2026-10-09
permalink: /posts/2026/10/09/citrix-warns-admins-to-patch-new-netscaler-rce-flaw-immediately/
tags:
- veille-cyber
- bleepingcomp
---
### Alerte de sécurité critique pour les appliances Citrix NetScaler

Citrix a émis une mise en garde urgente concernant une vulnérabilité critique affectant les appliances NetScaler ADC et NetScaler Gateway. Bien qu'aucune exploitation active ne soit connue à ce jour, la sévérité du risque nécessite une intervention immédiate des administrateurs.

**Points clés :**
*   **Vulnérabilité :** Faille de dépassement de mémoire (memory overflow).
*   **Impact :** Exécution de code à distance (RCE) ou déni de service (DoS) provoquant des plantages.
*   **Condition d'exposition :** Les appliances doivent être configurées en tant que fournisseur d'identité (IdP) ou fournisseur de services (SP) SAML.
*   **Contexte :** Plus de 21 000 instances NetScaler exposées sur Internet ont été identifiées, augmentant significativement la surface d'attaque.

**Vulnérabilité identifiée :**
*   **CVE-2026-107406**

**Recommandations :**
Les administrateurs doivent mettre à jour leurs instances vers les versions corrigées dès que possible :
*   **NetScaler ADC / Gateway 14.1 :** Version 14.1-73.46 ou ultérieure.
*   **NetScaler ADC / Gateway 13.1 :** Version 13.1-64.29 ou ultérieure.
*   **NetScaler ADC 14.1-FIPS :** Version 14.1-73.46 FIPS ou ultérieure.
*   **NetScaler ADC 13.1-FIPS / 13.1-NDcPP :** Version 13.1.37.283 ou ultérieure.

---
[Source](https://www.bleepingcomputer.com/news/security/citrix-warns-admins-to-patch-new-netscaler-rce-flaw-immediately/){:target="_blank"}
