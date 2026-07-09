---
title: 'Microsoft Patches RoguePlanet Defender Flaw That Can Grant SYSTEM Privileges'
date: 2026-07-09
permalink: /posts/2026/07/09/microsoft-patches-rogueplanet-defender-flaw-that-can-grant-system-privileges/
tags:
- veille-cyber
- hackernews
---
### Correction de la faille RoguePlanet dans Microsoft Defender

Microsoft a déployé un correctif pour la vulnérabilité « RoguePlanet » au sein du moteur de protection contre les logiciels malveillants (*Microsoft Malware Protection Engine*), près d'un mois après sa divulgation publique par le chercheur Chaotic Eclipse.

**Points clés :**
*   **Nature de la faille :** Il s'agit d'une condition de concurrence (*race condition*) permettant une élévation de privilèges.
*   **Impact :** Un attaquant peut obtenir des privilèges au niveau **SYSTEM**, lui permettant d'exécuter du code arbitraire ou d'effectuer des actions non autorisées.
*   **Portée :** L'exploitation est possible même avec la protection en temps réel activée et sur des systèmes Windows entièrement mis à jour.
*   **Historique :** Il s'agit de la quatrième vulnérabilité Defender découverte par ce même chercheur, après BlueHammer, UnDefend et RedSun.

**Vulnérabilité identifiée :**
*   **CVE-2026-50656 :** Score CVSS de 7.8 (élévation de privilèges dans `mpengine.dll`).

**Recommandations :**
*   **Mise à jour automatique :** Le correctif est inclus dans la version **1.1.26060.3008** du moteur. Aucune action manuelle n'est théoriquement requise pour la plupart des utilisateurs, car le moteur se met à jour automatiquement et fréquemment.
*   **Vérification :** Pour les environnements critiques ou en cas de doute, les administrateurs et utilisateurs peuvent forcer une recherche manuelle de mises à jour des définitions et du moteur via l'interface de leur logiciel antivirus Microsoft pour garantir l'application du correctif.

---
[Source](https://thehackernews.com/2026/07/microsoft-patches-rogueplanet-defender.html){:target="_blank"}
