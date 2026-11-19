---
title: 'PHP Fixes 7 Critical Flaws, Including Bugs That Could Allow Remote Code Execution'
date: 2026-11-19
permalink: /posts/2026/11/19/php-fixes-7-critical-flaws-including-bugs-that-could-allow-remote-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans PHP : correctifs et risques d'exécution de code à distance

La PHP Foundation a publié des mises à jour de sécurité corrigeant huit vulnérabilités critiques affectant plusieurs versions de PHP. Ces failles peuvent permettre, selon les configurations, une exécution de code à distance (RCE), une corruption de mémoire, un déni de service (DoS) ou une élévation de privilèges.

**Points clés :**
*   Les vulnérabilités touchent diverses versions de PHP et exploitent souvent des conditions spécifiques (configurations non par défaut ou serveurs utilisant des connexions persistantes).
*   La faille **CVE-2026-126714**, surnommée « phpAfterShell », est particulièrement notable : elle exploite une condition de compétition (TOCTOU) lors de l'écriture de sessions sur le disque pour déclencher une désérialisation malveillante.
*   La plupart des vulnérabilités affichent un score CVSS de 9.2, soulignant leur haute criticité.

**Vulnérabilités principales (CVSS 9.2) :**
*   **CVE-2026-115560 :** Validation d'entrée incorrecte.
*   **CVE-2026-129182 / 129474 / 129481 / 129496 :** Diverses vulnérabilités de type *use-after-free*.
*   **CVE-2026-126714 :** Faille TOCTOU (Time-of-check Time-of-use) dans la gestion des sessions.
*   **CVE-2026-129289 :** Interprétation incohérente des requêtes HTTP (impacte les environnements avec connexions persistantes comme Nginx, Apache ou HAProxy).

*Note : La CVE-2026-129291 (CVSS 8.8) concerne une élévation de privilèges locale.*

**Recommandations :**
*   **Mise à jour immédiate :** Appliquez les correctifs en migrant vers les versions **8.2.36, 8.3.37, 8.4.28, 8.5.13 ou 8.6.0**.
*   **Mesure palliative :** Si une mise à jour immédiate est impossible, il est fortement recommandé de désactiver la fonctionnalité de progression de téléversement de session (*session upload progress*) pour limiter les risques liés à la faille « phpAfterShell ».

---
[Source](https://thehackernews.com/2026/11/php-fixes-7-critical-flaws-including.html){:target="_blank"}
