---
title: 'New Microsoft Defender ShieldCrash zero-day grants SYSTEM access'
date: 2026-09-09
permalink: /posts/2026/09/09/new-microsoft-defender-shieldcrash-zero-day-grants-system-access/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité zero-day « ShieldCrash » dans Microsoft Defender

Le chercheur en sécurité « Nightmare Eclipse » a dévoilé « ShieldCrash », une faille zero-day permettant d'obtenir des privilèges **SYSTEM** sur les systèmes Windows (10, 11 et Server) entièrement mis à jour. Cette vulnérabilité constitue un contournement incomplet du correctif apporté au défaut « ShieldBreak » (CVE-2026-69414).

**Points clés :**
*   **Nature de la faille :** Il s'agit d'une élévation de privilèges exploitant une erreur résiduelle dans le patch précédent de Microsoft.
*   **Impact :** Permet une lecture arbitraire de fichiers avec des droits SYSTEM. Bien que l'accès en écriture ne soit pas actuellement possible, le risque reste critique.
*   **Contexte :** Cette publication s'inscrit dans un conflit persistant entre le chercheur et Microsoft concernant la gestion des programmes de « bug bounty » et la divulgation des vulnérabilités.
*   **Historique :** Le chercheur est à l'origine d'une série de divulgations zero-day (LegacyHive, RoguePlanet, BlueHammer, etc.) ciblant divers composants Windows et Defender au cours de l'année 2026.

**Vulnérabilité identifiée :**
*   **CVE-2026-69414 (ShieldBreak) :** Le correctif déployé lors du Patch Tuesday de septembre 2026 est jugé insuffisant, permettant la persistance de l'exploitation via « ShieldCrash ».

**Recommandations :**
*   **Veille active :** Surveiller les annonces du MSRC (Microsoft Security Response Center) pour la publication d'un nouveau correctif spécifique traitant ce contournement.
*   **Surveillance des logs :** Être vigilant face à toute activité suspecte tentant d'accéder à des fichiers système critiques, particulièrement dans les environnements où Defender est le principal outil de sécurité.
*   **Réduction de la surface d'attaque :** Appliquer le principe du moindre privilège pour limiter l'impact en cas d'exploitation réussie.

---
[Source](https://www.bleepingcomputer.com/news/security/new-microsoft-defender-shieldcrash-zero-day-grants-system-access/){:target="_blank"}
