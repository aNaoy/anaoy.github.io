---
title: 'Continuing Scans for swagger.json, (Wed, Jun 3rd)'
date: 2026-06-03
permalink: /posts/2026/06/03/continuing-scans-for-swaggerjson-wed-jun-3rd/
tags:
- veille-cyber
- sans-isc
---
### La menace des fichiers Swagger exposés

Les fichiers `swagger.json` (OpenAPI), essentiels pour le développement d'API REST, sont devenus une cible privilégiée pour les attaquants. Ces fichiers agissent comme une cartographie détaillée, exposant les fonctionnalités de l'API et facilitant l'identification de composants vulnérables au sein d'une infrastructure. Bien que nécessaires à l'interopérabilité, leur exposition publique sur Internet offre aux assaillants une reconnaissance automatisée très efficace.

**Points clés :**
*   **Reconnaissance automatisée :** Les attaquants scannent en permanence le Web à la recherche de fichiers `swagger.json` pour dresser un inventaire des API et de leurs métadonnées.
*   **Risque de divulgation :** L'accès non restreint à ces fichiers permet de comprendre la structure de l'application et d'identifier rapidement des surfaces d'attaque exploitables.
*   **Persistence :** Les campagnes de scan sont continues, avec des volumes de requêtes élevés et constants sur des chemins standards et des variantes plus récentes.

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, car il s'agit d'une problématique de **configuration par défaut ou d'exposition inappropriée** (proche du CWE-200 : *Exposure of Sensitive Information to an Unauthorized Actor*). Le risque réside dans le fait que l'outil de documentation devient un outil d'aide à l'exploitation.

**Recommandations :**
*   **Audit interne :** Scannez préventivement votre propre environnement pour identifier les fichiers `swagger.json` accessibles publiquement et non protégés.
*   **Contrôle d'accès :** Restreignez l'accès aux points de terminaison de documentation (Swagger UI/JSON) aux réseaux internes ou aux adresses IP authentifiées uniquement.
*   **Hygiène des API :** Ne laissez pas de fichiers de documentation en production si leur accès n'est pas strictement nécessaire pour des utilisateurs autorisés.

---
[Source](https://isc.sans.edu/diary/rss/33044){:target="_blank"}
