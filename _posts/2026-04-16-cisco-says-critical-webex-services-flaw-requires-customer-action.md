---
title: 'Cisco says critical Webex Services flaw requires customer action'
date: 2026-04-16
permalink: /posts/2026/04/16/cisco-says-critical-webex-services-flaw-requires-customer-action/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques chez Cisco : actions requises pour Webex

Cisco a publié des correctifs pour plusieurs vulnérabilités critiques affectant ses solutions Webex Services et Identity Services Engine (ISE). Aucune preuve d'exploitation active n'a été signalée à ce jour.

**Points clés :**
* **Webex Services :** Une faille dans l'intégration de l'authentification unique (SSO) permettait à des attaquants distants non authentifiés d'usurper l'identité d'utilisateurs légitimes via des jetons contrefaits.
* **Identity Services Engine (ISE) :** Trois vulnérabilités critiques permettent l'exécution de commandes arbitraires sur le système d'exploitation, bien qu'elles nécessitent des privilèges d'administration pour être exploitées.
* **Autres correctifs :** 10 vulnérabilités de sévérité moyenne ont également été corrigées, couvrant des risques de contournement d'authentification, d'élévation de privilèges et de déni de service.

**Vulnérabilités identifiées :**
* **CVE-2026-20184 :** Faille critique de validation de certificat dans Webex Services (SSO/Control Hub).
* **CVE-2026-20147, CVE-2026-20180, CVE-2026-20186 :** Exécution de commandes à distance dans Cisco ISE.

**Recommandations :**
* **Pour les utilisateurs de Webex :** Le correctif étant appliqué côté cloud par Cisco, les administrateurs doivent impérativement télécharger et installer un nouveau certificat SAML pour leur fournisseur d'identité (IdP) dans le Control Hub afin d'éviter toute interruption de service.
* **Pour les utilisateurs d'ISE :** Procéder à la mise à jour immédiate vers les versions patchées pour neutraliser les vecteurs d'exécution de commandes.

---
[Source](https://www.bleepingcomputer.com/news/security/cisco-says-critical-webex-services-flaw-requires-customer-action/){:target="_blank"}
