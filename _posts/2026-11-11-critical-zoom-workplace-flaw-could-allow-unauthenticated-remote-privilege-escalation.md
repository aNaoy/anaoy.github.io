---
title: 'Critical Zoom Workplace Flaw Could Allow Unauthenticated Remote Privilege Escalation'
date: 2026-11-11
permalink: /posts/2026/11/11/critical-zoom-workplace-flaw-could-allow-unauthenticated-remote-privilege-escalation/
tags:
- veille-cyber
- hackernews
---
### Risques d'élévation de privilèges dans Zoom Workplace pour Windows

Zoom a publié des correctifs pour deux vulnérabilités critiques affectant son application Workplace sur Windows. Ces failles permettent à un attaquant non authentifié d'obtenir une élévation de privilèges sur le système cible via un accès réseau, sans nécessiter d'autorisations préalables.

**Vulnérabilités identifiées :**

*   **CVE-2026-108186 (Score CVSS : 9.6) :** Vulnérabilité liée à une validation incorrecte des entrées. Elle concerne les versions de Zoom Workplace pour Windows comprises entre 7.1.0 et 7.1.7.
*   **CVE-2026-108187 (Score CVSS : 8.1) :** Vulnérabilité liée à une validation d'origine défaillante. Elle impacte les versions antérieures à la 7.1.5.

**Points clés :**
*   Les deux failles permettent une élévation de privilèges à distance sans authentification.
*   Bien qu'aucune preuve d'exploitation active ("in the wild") n'ait été signalée, la criticité des scores CVSS impose une vigilance immédiate.
*   Ces correctifs s'inscrivent dans une série de mises à jour de sécurité récentes pour l'application.

**Recommandations :**
*   Mettre à jour immédiatement l'application Zoom Workplace vers la version la plus récente disponible sur le site officiel.
*   Vérifier systématiquement les journaux de mise à jour pour s'assurer que les correctifs de sécurité sont correctement appliqués sur tous les postes de travail Windows de l'organisation.

---
[Source](https://thehackernews.com/2026/11/critical-zoom-workplace-flaw-could.html){:target="_blank"}
