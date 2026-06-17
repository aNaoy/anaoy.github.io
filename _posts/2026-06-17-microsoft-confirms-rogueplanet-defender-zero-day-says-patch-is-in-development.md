---
title: 'Microsoft Confirms RoguePlanet Defender Zero-Day, Says Patch is in Development'
date: 2026-06-17
permalink: /posts/2026/06/17/microsoft-confirms-rogueplanet-defender-zero-day-says-patch-is-in-development/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique "RoguePlanet" dans Microsoft Defender

Microsoft a confirmé l'existence d'une faille de sécurité zero-day, baptisée « RoguePlanet », affectant le moteur de protection contre les logiciels malveillants de Microsoft Defender. Un correctif est actuellement en cours de développement.

**Points clés :**
*   **Nature de la faille :** Il s'agit d'une condition de concurrence (race condition) permettant une élévation de privilèges.
*   **Impact :** Un attaquant peut obtenir un accès avec les privilèges de niveau "SYSTEM".
*   **Efficacité :** Le chercheur à l'origine de la découverte (Chaotic Eclipse) indique que l'exploit fonctionne indépendamment de l'activation de la protection en temps réel.
*   **Historique :** C'est la quatrième vulnérabilité signalée sur Defender par ce même chercheur au cours de la période récente.

**Vulnérabilité identifiée :**
*   **CVE-2026-50656**
*   **Score CVSS :** 7.8 (Élevé)

**Recommandations :**
*   Surveiller activement le portail de sécurité de Microsoft (MSRC) pour le déploiement immédiat du correctif officiel.
*   Appliquer les mises à jour de sécurité de Microsoft Defender dès leur publication.
*   Appliquer le principe du moindre privilège en limitant les droits des utilisateurs sur les systèmes sensibles en attendant le patch.

---
[Source](https://thehackernews.com/2026/06/microsoft-confirms-rogueplanet-defender_02022423645.html){:target="_blank"}
