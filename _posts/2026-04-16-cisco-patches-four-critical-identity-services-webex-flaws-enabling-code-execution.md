---
title: 'Cisco Patches Four Critical Identity Services, Webex Flaws Enabling Code Execution'
date: 2026-04-16
permalink: /posts/2026/04/16/cisco-patches-four-critical-identity-services-webex-flaws-enabling-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques chez Cisco : correctifs pour ISE et Webex

Cisco a publié des correctifs pour quatre vulnérabilités critiques affectant ses solutions *Identity Services Engine* (ISE) et *Webex*. Ces failles exposent les systèmes à l'exécution de code arbitraire et à l'usurpation d'identité.

**Points clés :**
* Les vulnérabilités permettent aux attaquants d'exécuter des commandes à distance avec des privilèges élevés (root) ou d'usurper l'identité d'utilisateurs.
* Une exploitation réussie sur ISE peut entraîner un déni de service (DoS), rendant les nœuds inaccessibles pour l'authentification réseau.
* Aucune exploitation active n'a été signalée à ce jour.

**Vulnérabilités identifiées :**
* **CVE-2026-20184 (Score 9.8) :** Problème de validation de certificat SSO dans Webex Control Hub, permettant l'usurpation d'utilisateurs.
* **CVE-2026-20147 (Score 9.9) :** Validation insuffisante des entrées utilisateur dans ISE/ISE-PIC, permettant l'exécution de code à distance via des requêtes HTTP forgées.
* **CVE-2026-20180 & CVE-2026-20186 (Score 9.9) :** Vulnérabilités liées aux entrées utilisateur dans ISE permettant l'exécution de commandes système par un administrateur en lecture seule.

**Recommandations :**
* **Webex :** Aucune action directe sur les serveurs, mais les utilisateurs doivent impérativement mettre à jour leur certificat SAML d'identité (IdP) dans le Control Hub.
* **Cisco ISE/ISE-PIC :** Appliquer les correctifs (patchs) selon les versions spécifiées :
    * Pour **CVE-2026-20147** : Mettre à jour vers les versions 3.1 P11, 3.2 P10, 3.3 P11, 3.4 P6 ou 3.5 P3.
    * Pour **CVE-2026-20180 & CVE-2026-20186** : Mettre à jour vers les versions 3.2 P8, 3.3 P8 ou 3.4 P4 (la version 3.5 n'est pas concernée).

---
[Source](https://thehackernews.com/2026/04/cisco-patches-four-critical-identity.html){:target="_blank"}
