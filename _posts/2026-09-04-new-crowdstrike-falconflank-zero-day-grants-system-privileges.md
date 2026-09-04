---
title: 'New CrowdStrike FalconFlank zero-day grants SYSTEM privileges'
date: 2026-09-04
permalink: /posts/2026/09/04/new-crowdstrike-falconflank-zero-day-grants-system-privileges/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité "FalconFlank" : Élévation de privilèges dans CrowdStrike Falcon

Une nouvelle vulnérabilité zero-day, baptisée **FalconFlank**, a été révélée par le chercheur en sécurité "Nightmare Eclipse". Elle permet à un attaquant disposant d'un accès initial d'élever ses privilèges au niveau **SYSTEM** sur des systèmes Windows 11 et Windows Server parfaitement à jour.

**Points clés :**
*   **Cible :** La faille exploite une fonctionnalité de la plateforme CrowdStrike Falcon, spécifiquement le mécanisme de remédiation des macros malveillantes Office.
*   **Contexte :** Le chercheur a rendu public un PoC (preuve de concept) fonctionnel. Bien que CrowdStrike travaille sur des détections, la vulnérabilité reste active.
*   **Série d'attaques :** Le même chercheur a récemment publié plusieurs autres exploits zero-day visant Kaspersky, Avast, Nvidia et divers composants Windows.

**Vulnérabilités :**
*   **CVE :** Aucune identification CVE n'a encore été attribuée à FalconFlank.
*   **Impact :** Élévation de privilèges locale permettant d'exécuter des commandes avec les droits les plus élevés (SYSTEM).

**Recommandations :**
*   **Action immédiate :** CrowdStrike conseille aux entreprises de désactiver la stratégie Windows nommée "File Suspicious Macro Removal" (Suppression des macros suspectes dans les fichiers Office) au sein des paramètres Microsoft Office.
*   **Protection maintenue :** La sécurité reste assurée par les paramètres "Cloud Anti-malware for Microsoft Office Files".
*   **Veille :** Les clients sont invités à consulter l'alerte technique spécifique disponible via le portail de support CrowdStrike pour des instructions détaillées.

---
[Source](https://www.bleepingcomputer.com/news/security/new-crowdstrike-falconflank-zero-day-grants-system-privileges/){:target="_blank"}
