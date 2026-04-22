---
title: 'Microsoft releases emergency patches for critical ASP.NET flaw'
date: 2026-04-22
permalink: /posts/2026/04/22/microsoft-releases-emergency-patches-for-critical-aspnet-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Urgence : Correction d'une faille critique d'élévation de privilèges dans ASP.NET Core

Microsoft a publié une mise à jour corrective hors cycle pour pallier une vulnérabilité critique affectant les API de protection des données d'ASP.NET Core. Cette faille, introduite par une régression dans les versions récentes du framework, permet à des attaquants non authentifiés de manipuler des jetons d'authentification et d'obtenir des privilèges système.

**Vulnérabilité**
*   **CVE-2026-40372** : Une erreur de validation HMAC dans le package `Microsoft.AspNetCore.DataProtection` (versions 10.0.0 à 10.0.6) permet de falsifier des charges utiles (payloads). Un attaquant peut ainsi contourner les contrôles d'authenticité, déchiffrer des cookies, accéder à des fichiers et modifier des données.

**Points clés**
*   **Origine du problème** : Une régression logicielle lors de la mise à jour de mars (.NET 10.0.6) a corrompu la routine de validation cryptographique.
*   **Risque de persistance** : Les jetons légitimes générés par l'attaquant durant la période d'exposition restent valides même après l'application du correctif, sauf si les clés de protection sont renouvelées.
*   **Impact** : Élévation de privilèges (SYSTEM), accès non autorisé à des données sensibles (tokens, mots de passe), mais aucun impact direct sur la disponibilité (Déni de service).

**Recommandations**
1.  **Mise à jour immédiate** : Mettre à jour le package `Microsoft.AspNetCore.DataProtection` vers la version **10.0.7**.
2.  **Redéploiement** : Redéployer les applications concernées pour assurer la prise en compte de la correction.
3.  **Rotation des clés** : Il est fortement conseillé d'effectuer une rotation du trousseau de clés (*DataProtection key ring*) pour invalider tout jeton qui aurait pu être généré frauduleusement avant la mise à jour.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-emergency-security-updates-for-critical-aspnet-flaw/){:target="_blank"}
