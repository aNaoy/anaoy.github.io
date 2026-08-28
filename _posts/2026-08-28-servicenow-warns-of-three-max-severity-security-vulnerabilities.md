---
title: 'ServiceNow warns of three max severity security vulnerabilities'
date: 2026-08-28
permalink: /posts/2026/08/28/servicenow-warns-of-three-max-severity-security-vulnerabilities/
tags:
- veille-cyber
- bleepingcomp
---
### Alert critique sur la plateforme ServiceNow AI

ServiceNow a déployé des correctifs de sécurité pour trois vulnérabilités de gravité maximale affectant sa plateforme d'IA, ainsi qu'une faille de haute sévérité. Ces vulnérabilités permettent à des attaquants non authentifiés d'exécuter du code arbitraire, d'élever leurs privilèges ou d'accéder aux données via des injections SQL, sans nécessiter d'interaction utilisateur.

**Points clés :**
*   **Surface d'exposition :** Les vulnérabilités concernent les environnements cloud et les instances auto-hébergées.
*   **Complexité :** Les attaques sont classées comme étant de faible complexité, rendant l'exploitation techniquement accessible à un large éventail d'acteurs malveillants.
*   **Historique :** Bien qu'aucune exploitation active ne soit signalée pour ces failles spécifiques, la plateforme a été la cible de campagnes d'exploitation répétées ces dernières années.

**Vulnérabilités identifiées :**
*   **CVE-2026-18885 :** Injection de code (exécution de code arbitraire).
*   **CVE-2026-18886 :** Injection de code (élévation de privilèges).
*   **CVE-2026-74820 :** Injection SQL (accès ou modification des données).
*   **CVE-2026-6876 :** Évasion de bac à sable (*sandbox escape*) permettant l'exécution de code à distance (gravité élevée).

**Recommandations :**
*   Appliquer immédiatement les correctifs fournis par ServiceNow via les mises à jour des versions Xanadu, Yokohama, Zurich et Australia.
*   Vérifier les versions installées sur les instances auto-hébergées et procéder à la mise à niveau vers les versions corrigées (ex: Yokohama Patch 13 Hot Fix 4 ou Zurich Patch 12).
*   Surveiller les journaux d'accès pour détecter d'éventuelles activités anormales sur les API et les terminaux de la plateforme.

---
[Source](https://www.bleepingcomputer.com/news/security/servicenow-warns-of-three-max-severity-security-vulnerabilities/){:target="_blank"}
