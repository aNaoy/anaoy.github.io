---
title: 'Microsoft Defender RoguePlanet zero-day grants SYSTEM privileges'
date: 2026-06-10
permalink: /posts/2026/06/10/microsoft-defender-rogueplanet-zero-day-grants-system-privileges/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité zero-day "RoguePlanet" dans Microsoft Defender

Une nouvelle faille zero-day baptisée "RoguePlanet", découverte par le chercheur Nightmare Eclipse, permet d'obtenir des privilèges **SYSTEM** sur des systèmes Windows 10 et 11 entièrement mis à jour. Cette vulnérabilité, initialement conçue comme une exécution de code à distance (RCE), exploite une condition de course (*race condition*) dans la gestion des fichiers par Microsoft Defender.

**Points clés :**
* **Nature de la faille :** Condition de course dans Microsoft Defender, testée avec succès sur des versions de Windows 11 équipées du correctif KB5094126.
* **Impact :** Élévation de privilèges (LPE) permettant d'ouvrir une invite de commande avec les droits SYSTEM.
* **Historique :** Le chercheur, en conflit ouvert avec Microsoft concernant sa politique de divulgation, a publié ce PoC après la suppression de ses dépôts sur GitHub et GitLab.
* **État actuel :** Aucune CVE n'a encore été attribuée à cette vulnérabilité spécifique au moment de la publication.

**Recommandations :**
* **Mise en place d'une liste blanche d'applications :** Selon ThreatLocker, l'utilisation de politiques de contrôle des applications (*allowlisting*) constitue une mesure de défense efficace pour empêcher l'exécution de l'exploit.
* **Surveillance proactive :** Les équipes de sécurité doivent surveiller les comportements suspects liés à l'exécution de fichiers VHD/VHDX via des partages SMB distants.
* **Attente de correctif :** Dans l'attente d'une mise à jour officielle de Microsoft, limiter autant que possible l'exposition des systèmes aux partages SMB non sécurisés et appliquer les futures mises à jour de sécurité de Windows dès leur disponibilité.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-defender-rogueplanet-zero-day-grants-system-privileges/){:target="_blank"}
