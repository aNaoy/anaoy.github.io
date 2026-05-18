---
title: 'MiniPlasma Windows 0-Day Enables SYSTEM Privilege Escalation on Fully Patched Systems'
date: 2026-05-18
permalink: /posts/2026/05/18/miniplasma-windows-0-day-enables-system-privilege-escalation-on-fully-patched-systems/
tags:
- veille-cyber
- hackernews
---
### MiniPlasma : Une faille d'élévation de privilèges non corrigée dans Windows

Une nouvelle vulnérabilité zero-day, baptisée **MiniPlasma**, permet d'obtenir des privilèges **SYSTEM** sur des systèmes Windows entièrement à jour. Cette faille réside dans le pilote « Windows Cloud Files Mini Filter » (`cldflt.sys`), spécifiquement au sein de la routine `HsmOsBlockPlaceholderAccess`.

**Points clés :**
*   **Historique :** Le problème avait été initialement signalé par Google Project Zero en 2020. Bien qu'il ait été censé être corrigé via CVE-2020-17103, la faille est toujours active et exploitable aujourd'hui.
*   **Exploitation :** Il s'agit d'une condition de course (*race condition*) qui permet d'ouvrir une invite de commande avec les droits SYSTEM.
*   **Portée :** Toutes les versions de Windows sont potentiellement affectées, y compris Windows 11 avec les mises à jour de mai 2026. Seules les versions « Insider Preview Canary » semblent résilientes pour le moment.

**Vulnérabilités :**
*   **CVE-2020-17103 :** Correctif incomplet ou régressif concernant le pilote `cldflt.sys`.
*   **CVE-2025-62221 :** Une autre vulnérabilité d'élévation de privilèges dans le même composant, corrigée en décembre 2025 mais exploitée par des acteurs malveillants.

**Recommandations :**
*   Il n'existe actuellement aucun correctif officiel pour MiniPlasma, car le problème semble persister malgré les tentatives de remédiation passées.
*   En attendant une mise à jour de sécurité de Microsoft, les administrateurs système doivent surveiller étroitement les accès aux journaux système et limiter les privilèges des utilisateurs locaux pour réduire la surface d'attaque.
*   Surveiller les prochaines communications de Microsoft concernant le pilote `cldflt.sys`.

---
[Source](https://thehackernews.com/2026/05/miniplasma-windows-0-day-enables-system.html){:target="_blank"}
