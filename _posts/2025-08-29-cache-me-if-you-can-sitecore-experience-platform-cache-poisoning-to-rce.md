---
title: 'Cache Me If You Can (Sitecore Experience Platform Cache Poisoning to RCE)'
date: 2025-08-29
permalink: /posts/2025/08/29/cache-me-if-you-can-sitecore-experience-platform-cache-poisoning-to-rce/
tags:
- veille-cyber
- zerodaysfans
---
## Sitecore Experience Platform : Empoisonnement de Cache et Exécution de Code à Distance

Une recherche sur la plateforme Sitecore Experience Platform a révélé plusieurs vulnérabilités critiques permettant un compromis total du système. Ces failles permettent la combinaison d'un empoisonnement de cache HTML sans authentification avec une exécution de code à distance (RCE) après authentification.

### Points Clés

*   **Empoisonnement de Cache HTML (WT-2025-0023, CVE-2025-53693):** Une vulnérabilité permet à un attaquant de modifier le contenu du cache HTML de Sitecore sans authentification préalable. Cette attaque exploite une réflexion non sécurisée dans le composant `XamlPageHandlerFactory` et peut être utilisée pour injecter du contenu malveillant dans les pages mises en cache.
*   **Exécution de Code à Distance (RCE) Post-Authentification (WT-2025-0019, CVE-2025-53691):** Une vulnérabilité d'exécution de code à distance a été découverte via une désérialisation non sécurisée des données encodées en Base64 dans le pipeline `ConvertToRuntimeHtml`. Bien que certaines voies d'accès aient été corrigées, une autre voie via le contrôle `Sitecore.Shell.Applications.ContentEditor.Dialogs.FixHtml.aspx` subsiste et nécessite des droits d'accès au Content Editor.
*   **Énumération des Clés de Cache (WT-2025-0027, CVE-2025-53694):** L'API ItemService, si elle est exposée et mal configurée, permet à un attaquant d'énumérer les éléments cachables et leurs paramètres de configuration (comme `VaryByData`, `VaryByDevice`, etc.). Cela facilite la construction de clés de cache précises pour mener à bien l'empoisonnement de cache. Une faiblesse supplémentaire permet même à un utilisateur restreint de participer à cette énumération en exploitant un bug dans le comptage des résultats.
*   **Chaîne d'Exploitation:** L'empoisonnement du cache HTML peut être utilisé pour injecter du JavaScript malveillant, qui à son tour peut déclencher une vulnérabilité RCE post-authentification (ou d'autres failles RCE documentées précédemment), permettant un contrôle complet du système.

### Vulnérabilités et CVEs

*   **WT-2025-0023 (CVE-2025-53693):** Empoisonnement de Cache HTML via Réflexion Non Sécurisée.
*   **WT-2025-0019 (CVE-2025-53691):** Exécution de Code à Distance via Désérialisation Non Sécurisée (après authentification).
*   **WT-2025-0027 (CVE-2025-53694):** Divulgation d'Informations dans l'API ItemService permettant l'énumération de clés de cache.

D'autres vulnérabilités documentées dans la première partie de la recherche incluent WT-2025-0024 (CVE-2025-34509) pour les identifiants codés en dur et WT-2025-0032 (CVE-2025-34510) et WT-2025-0025 (CVE-2025-34511) pour des RCE post-authentification via Path Traversal et l'Extension PowerShell de Sitecore.

### Recommandations

*   **Appliquer les correctifs de sécurité :** Sitecore a publié des correctifs pour ces vulnérabilités en juin et juillet 2025. Il est crucial de les installer rapidement.
*   **Sécuriser l'API ItemService :** S'assurer que l'API ItemService n'est pas exposée à Internet et que l'accès anonyme est désactivé. Si elle doit être exposée dans des scénarios spécifiques, une authentification robuste doit être mise en place.
*   **Réviser la configuration du cache HTML :** Examiner et restreindre l'utilisation du cache HTML aux cas où cela est strictement nécessaire, en particulier pour les éléments dont les clés de cache incluent des informations sensibles ou variables difficiles à deviner.
*   **Surveiller l'activité du cache :** Mettre en place des mécanismes de surveillance pour détecter les modifications inhabituelles ou les accès fréquents aux ressources de cache.
*   **Mettre à jour les composants Sitecore :** Maintenir la plateforme Sitecore et ses extensions (comme Sitecore PowerShell Extension) à jour avec les derniers correctifs de sécurité.

---
[Source](https://labs.watchtowr.com/cache-me-if-you-can-sitecore-experience-platform-cache-poisoning-to-rce/){:target="_blank"}
