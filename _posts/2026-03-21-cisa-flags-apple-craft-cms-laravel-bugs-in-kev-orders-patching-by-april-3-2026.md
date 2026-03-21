---
title: 'CISA Flags Apple, Craft CMS, Laravel Bugs in KEV, Orders Patching by April 3, 2026'
date: 2026-03-21
permalink: /posts/2026/03/21/cisa-flags-apple-craft-cms-laravel-bugs-in-kev-orders-patching-by-april-3-2026/
tags:
- veille-cyber
- hackernews
---
### Intégration de 5 vulnérabilités critiques au catalogue KEV de la CISA

La CISA a ajouté cinq vulnérabilités activement exploitées à son catalogue *Known Exploited Vulnerabilities* (KEV), imposant une correction aux agences fédérales d'ici le 3 avril 2026. Ces failles concernent les écosystèmes Apple, Craft CMS et Laravel Livewire, et sont utilisées par divers groupes de menace pour des campagnes d'espionnage, le déploiement de malwares ou des opérations de cryptominage.

**Points clés :**
* **Exploitation active :** Les vulnérabilités Apple font partie du kit d'exploitation iOS « DarkSword », utilisé pour le vol de données.
* **Acteurs étatiques :** Le groupe MuddyWater (lié au renseignement iranien) exploite activement la faille de Laravel pour ses campagnes d'espionnage contre les infrastructures critiques.
* **Évolution des menaces :** Les attaquants modernisent leurs outils (utilisation de Rust, IA, automatisation) pour assurer une persistance à long terme sur les systèmes compromis.

**Vulnérabilités identifiées :**

| CVE | Logiciel | Risque | Nature de la faille |
| :--- | :--- | :--- | :--- |
| **CVE-2025-31277** | Apple WebKit | 8.8 | Corruption de mémoire |
| **CVE-2025-43510** | Apple Kernel | 7.8 | Corruption de mémoire |
| **CVE-2025-43520** | Apple Kernel | 8.8 | Corruption de mémoire |
| **CVE-2025-32432** | Craft CMS | 10.0 | Injection de code (RCE) |
| **CVE-2025-54068** | Laravel Livewire| 9.8 | Injection de code (RCE) |

**Recommandations :**
* **Mise à jour immédiate :** Appliquer les correctifs de sécurité fournis par les éditeurs pour l'ensemble des systèmes impactés.
* **Vigilance accrue :** Surveiller les comportements anormaux sur les serveurs web (Craft CMS/Laravel) et les terminaux iOS.
* **Défense en profondeur :** Compte tenu des tactiques de phishing sophistiquées de groupes comme MuddyWater, renforcer la sensibilisation des utilisateurs et les systèmes de détection basés sur l'analyse comportementale plutôt que sur la simple réputation des expéditeurs.

---
[Source](https://thehackernews.com/2026/03/cisa-flags-apple-craft-cms-laravel-bugs.html){:target="_blank"}
