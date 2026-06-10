---
title: 'Microsoft Defender RoguePlanet Zero-Day Grants SYSTEM Access on Updated Windows'
date: 2026-06-10
permalink: /posts/2026/06/10/microsoft-defender-rogueplanet-zero-day-grants-system-access-on-updated-windows/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité "RoguePlanet" : Escalade de privilèges via Microsoft Defender

Un chercheur en sécurité nommé « Chaotic Eclipse » a publié une preuve de concept (PoC) pour **RoguePlanet**, une nouvelle vulnérabilité zero-day affectant Microsoft Defender. Malgré les récentes mises à jour de juin 2026, cette faille permet à un attaquant d'obtenir des privilèges **SYSTEM** sur Windows 10 et 11.

**Points clés :**
*   **Nature de la faille :** Il s'agit d'une condition de course (*race condition*) permettant une escalade de privilèges.
*   **Impact :** L'exploitation réussie offre un accès total au système avec des droits élevés (SYSTEM), permettant l'exécution de code arbitraire.
*   **Portée :** La faille est confirmée sur les versions à jour de Windows 10 et 11. Bien que non fonctionnel sur Windows Server dans sa forme actuelle, le chercheur précise que le système reste vulnérable sous réserve d'une adaptation de l'exploit.
*   **Contexte conflictuel :** Cette divulgation s'inscrit dans un différend prolongé entre le chercheur et Microsoft, suite à la suspension de son compte de signalement de vulnérabilités (MSRC) et à des accusations de mauvaise gestion des recherches par l'éditeur.

**Vulnérabilités mentionnées :**
*   **RoguePlanet :** Zero-day (pas encore de CVE assigné à ce jour).
*   **Précédentes failles Defender divulguées par le même chercheur :** BlueHammer (CVE-2026-33825), UnDefend (CVE-2026-45498) et RedSun (CVE-2026-41091).

**Recommandations :**
*   **Surveillance :** Étant donné qu'aucun correctif n'est disponible pour "RoguePlanet", les administrateurs système doivent surveiller les comportements anormaux liés au processus Microsoft Defender.
*   **Veille :** Appliquer systématiquement les correctifs du *Patch Tuesday* dès leur publication, bien que cette vulnérabilité spécifique ne soit pas encore corrigée.
*   **Principe du moindre privilège :** Restreindre les droits des utilisateurs locaux pour limiter la surface d'attaque, bien que l'exploit cible le service Defender lui-même.

---
[Source](https://thehackernews.com/2026/06/microsoft-defender-rogueplanet-zero-day.html){:target="_blank"}
