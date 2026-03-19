---
title: 'ConnectWise patches new flaw allowing ScreenConnect hijacking'
date: 2026-03-19
permalink: /posts/2026/03/19/connectwise-patches-new-flaw-allowing-screenconnect-hijacking/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique dans ConnectWise ScreenConnect : Risque d'accès non autorisé

ConnectWise a corrigé une faille critique affectant sa plateforme d'accès distant ScreenConnect, permettant à des attaquants de contourner l'authentification et d'élever leurs privilèges.

**Points clés :**
*   La vulnérabilité permet l'extraction et l'utilisation des clés machine ASP.NET pour générer ou modifier des jetons d'authentification valides.
*   Le risque est jugé tangible, bien que ConnectWise n'ait pas encore confirmé d'exploitation active généralisée au moment de la publication.
*   Les utilisateurs Cloud ont été mis à jour automatiquement, mais les déploiements sur site (on-premise) restent exposés jusqu'à une intervention manuelle.

**Vulnérabilité identifiée :**
*   **CVE-2026-3564** : Faille de vérification de signature cryptographique (gravité critique). Affecte les versions antérieures à la **26.1**.

**Recommandations :**
*   **Mise à jour immédiate :** Passer impérativement à la version **26.1** pour tous les serveurs ScreenConnect auto-hébergés.
*   **Renforcement de la sécurité :** Sécuriser strictement l'accès aux fichiers de configuration et aux clés secrètes.
*   **Surveillance :** Auditer les journaux (logs) à la recherche d'activités d'authentification inhabituelles.
*   **Maintenance :** Protéger les sauvegardes, les instantanés de données anciens et maintenir toutes les extensions à jour.

---
[Source](https://www.bleepingcomputer.com/news/security/connectwise-patches-new-flaw-allowing-screenconnect-hijacking/){:target="_blank"}
