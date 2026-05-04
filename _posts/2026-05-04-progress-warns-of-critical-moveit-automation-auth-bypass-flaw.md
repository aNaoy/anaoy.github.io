---
title: 'Progress warns of critical MOVEit Automation auth bypass flaw'
date: 2026-05-04
permalink: /posts/2026/05/04/progress-warns-of-critical-moveit-automation-auth-bypass-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques dans MOVEit Automation

Progress Software a émis une alerte de sécurité concernant son outil de transfert de fichiers (MFT) MOVEit Automation. Les failles identifiées permettent à des attaquants distants de compromettre les systèmes sans nécessiter d'interaction utilisateur ni de privilèges préalables. Plus de 1 400 instances, incluant certaines appartenant à des agences gouvernementales américaines, sont actuellement exposées en ligne.

**Points clés :**
*   **Risque élevé :** Bien qu'aucune exploitation active ne soit confirmée, les logiciels MFT sont des cibles privilégiées pour les groupes de ransomwares, comme l'a démontré la campagne massive du gang Clop en 2023.
*   **Impact :** La mise à jour nécessite une installation complète qui entraîne une interruption de service.

**Vulnérabilités :**
*   **CVE-2026-4670 :** Faille critique de contournement d'authentification (critique).
*   **CVE-2026-5174 :** Vulnérabilité d'élévation de privilèges causée par une mauvaise validation des entrées (sévérité élevée).

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs en passant aux versions 2025.1.5, 2025.0.9 ou 2024.1.8 (selon la branche utilisée).
*   **Installation :** Utiliser exclusivement le programme d'installation complet fourni par l'éditeur pour garantir la remédiation de la faille.

---
[Source](https://www.bleepingcomputer.com/news/security/moveit-automation-customers-warned-to-patch-critical-auth-bypass-flaw/){:target="_blank"}
