---
title: 'cPanel, WHM Release Fixes for Three New Vulnerabilities — Patch Now'
date: 2026-05-09
permalink: /posts/2026/05/09/cpanel-whm-release-fixes-for-three-new-vulnerabilities-patch-now/
tags:
- veille-cyber
- hackernews
---
### Correction critique : Vulnérabilités critiques dans cPanel et WHM

cPanel a publié des correctifs de sécurité pour trois vulnérabilités critiques affectant cPanel et WHM, permettant potentiellement l'exécution de code, l'escalade de privilèges et des attaques par déni de service. Bien qu'aucune exploitation active ne soit signalée à ce jour, la vigilance est de mise compte tenu de la récente utilisation malveillante d'autres failles dans ces produits.

**Vulnérabilités identifiées :**

*   **CVE-2026-29201 (Score CVSS 4.3) :** Défaut de validation des entrées dans l'appel `feature::LOADFEATUREFILE`, permettant une lecture arbitraire de fichiers.
*   **CVE-2026-29202 (Score CVSS 8.8) :** Mauvaise validation du paramètre « plugin » via l'API `create_user`, pouvant mener à une exécution de code Perl arbitraire.
*   **CVE-2026-29203 (Score CVSS 8.8) :** Gestion non sécurisée des liens symboliques, permettant de modifier les permissions de fichiers via `chmod`, risquant un déni de service ou une élévation de privilèges.

**Recommandations :**

*   **Mise à jour immédiate :** Appliquez sans délai les correctifs en passant aux versions corrigées (ex: 11.136.0.9, 11.134.0.25, 11.132.0.31, etc.).
*   **Systèmes obsolètes :** Les utilisateurs sous CentOS 6 ou CloudLinux 6 doivent impérativement migrer vers la version 110.0.114 pour bénéficier du correctif spécifique.
*   **Vérification de version :** Consultez la liste complète des versions supportées sur le portail officiel de cPanel pour garantir la compatibilité de votre instance.

---
[Source](https://thehackernews.com/2026/05/cpanel-whm-patch-3-new-vulnerabilities.html){:target="_blank"}
