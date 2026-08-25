---
title: 'Attackers Target miniOrange SAML Flaws That Can Grant WordPress Admin Access'
date: 2026-08-25
permalink: /posts/2026/08/25/attackers-target-miniorange-saml-flaws-that-can-grant-wordpress-admin-access/
tags:
- veille-cyber
- hackernews
---
### Risque critique d'usurpation d'identité sur le plugin miniOrange SAML pour WordPress

Des attaquants exploitent actuellement deux vulnérabilités critiques dans le plugin **Xecurify miniOrange SAML 2.0 Single Sign On** pour WordPress. Ces failles permettent à des utilisateurs non authentifiés de contourner le mécanisme de connexion et de prendre le contrôle de n'importe quel compte, y compris celui d'un administrateur.

**Points clés :**
*   Les vulnérabilités sont activement exploitées par des scans opportunistes visant les sites équipés du plugin.
*   L'attaque repose sur l'envoi d'une réponse SAML manipulée avec une signature malformée, provoquant une erreur de traitement qui est interprétée à tort comme une validation réussie.
*   Le problème provient d'une vérification booléenne laxiste dans la fonction `mo_saml_validate_signature()`.

**Vulnérabilités :**
*   **CVE-2026-61979 (Score CVSS 8.1) :** Élévation de privilèges non authentifiée par confusion d'algorithme de signature.
*   **CVE-2026-15981 (Score CVSS 9.8) :** Contournement d'authentification lié à l'acceptation de signatures malformées (génère une erreur OpenSSL traitée comme valide).

**Recommandations :**
*   **Mise à jour immédiate :** Appliquez sans délai les correctifs disponibles. Les vulnérabilités ont été corrigées dans les versions **17.0.5** (pour CVE-2026-61979) et **17.0.6** (pour CVE-2026-15981) de l'édition Standard.
*   **Surveillance :** Inspectez les journaux d'accès WordPress à la recherche d'activités suspectes et surveillez les connexions administrateur inhabituelles.

---
[Source](https://thehackernews.com/2026/08/attackers-target-miniorange-saml-flaws.html){:target="_blank"}
