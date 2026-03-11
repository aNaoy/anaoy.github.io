---
title: 'Microsoft Patch Tuesday, March 2026 Edition'
date: 2026-03-11
permalink: /posts/2026/03/11/microsoft-patch-tuesday-march-2026-edition/
tags:
- veille-cyber
- krebs
---
### Mise à jour de sécurité Microsoft : Mars 2026

Le Patch Tuesday de mars 2026 corrige au moins 77 vulnérabilités dans l'écosystème Windows. Bien qu'aucune faille "zero-day" ne soit recensée ce mois-ci, plusieurs vulnérabilités critiques nécessitent une attention immédiate. Un fait marquant est l'identification de la faille **CVE-2026-21536** par **XBOW**, un agent d'intelligence artificielle autonome, soulignant l'évolution des capacités de découverte de vulnérabilités.

**Points clés :**
*   **Prédominance des privilèges :** 55 % des vulnérabilités corrigées concernent l'élévation de privilèges.
*   **Risques critiques :** Des failles d'exécution de code à distance (RCE) touchent Microsoft Office, exploitables via le volet de prévisualisation.
*   **Écosystème étendu :** Adobe a publié des correctifs pour 80 vulnérabilités, et Mozilla a mis à jour Firefox pour corriger trois failles de haute sévérité.

**Vulnérabilités notables :**
*   **CVE-2026-21262 :** Élévation de privilèges (sysadmin) sur SQL Server 2016 et versions ultérieures (Score CVSS : 8.8).
*   **CVE-2026-26113 & CVE-2026-26110 :** RCE dans Microsoft Office via le volet de prévisualisation.
*   **CVE-2026-24291 :** Élévation de privilèges via l'infrastructure d'accessibilité Windows (Score CVSS : 7.8).
*   **CVE-2026-24294 :** Authentification inappropriée dans SMB (Score CVSS : 7.8).
*   **CVE-2026-24289 :** Corruption mémoire et condition de concurrence (Score CVSS : 7.8).
*   **CVE-2026-25187 :** Vulnérabilité dans le processus Winlogon (Score CVSS : 7.8).
*   **CVE-2026-26127 :** Risque de déni de service dans les applications .NET.

**Recommandations :**
*   **Prioriser les correctifs :** Appliquer en priorité les correctifs pour SQL Server et les failles RCE touchant Microsoft Office, identifiées comme particulièrement dangereuses.
*   **Surveillance :** Les administrateurs système doivent suivre les correctifs via les ressources de référence (SANS Internet Storm Center ou AskWoody.com) pour anticiper d'éventuels problèmes liés au déploiement des mises à jour.
*   **Mise à jour Adobe/Mozilla :** Ne pas négliger les correctifs tiers essentiels pour Acrobat, Adobe Commerce et Firefox, publiés simultanément.

---
[Source](https://krebsonsecurity.com/2026/03/microsoft-patch-tuesday-march-2026-edition/){:target="_blank"}
