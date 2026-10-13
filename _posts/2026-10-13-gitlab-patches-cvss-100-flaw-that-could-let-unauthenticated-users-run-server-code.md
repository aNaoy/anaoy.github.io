---
title: 'GitLab Patches CVSS 10.0 Flaw That Could Let Unauthenticated Users Run Server Code'
date: 2026-10-13
permalink: /posts/2026/10/13/gitlab-patches-cvss-100-flaw-that-could-let-unauthenticated-users-run-server-code/
tags:
- veille-cyber
- hackernews
---
### Correction critique : GitLab corrige une faille critique d'exécution de code

GitLab a publié des correctifs urgents pour ses éditions Community (CE) et Enterprise (EE) afin de remédier à plusieurs vulnérabilités majeures, dont une faille de criticité maximale permettant l'exécution de code arbitraire sans authentification.

**Points clés :**
*   La vulnérabilité principale repose sur une validation insuffisante des expressions régulières dans les configurations CI/CD, permettant à un attaquant non authentifié d'exécuter du code à distance.
*   En complément, trois autres vulnérabilités de haute sévérité ont été corrigées, touchant l'injection de scripts (XSS), des problèmes d'autorisation dans les pipelines et l'empoisonnement de cache.

**Vulnérabilités identifiées :**
*   **CVE-2026-97229 (CVSS 10.0) :** Dépassement d'entier et exécution de code arbitraire via des expressions régulières malveillantes.
*   **CVE-2026-92883 (CVSS 8.7) :** Vulnérabilité de Cross-Site Scripting (XSS) permettant l'exécution de JavaScript dans une session utilisateur.
*   **CVE-2026-16301 (CVSS 8.5) :** Problème d'autorisation permettant à un utilisateur doté du rôle "Developer" de lancer des pipelines sur des branches protégées.
*   **CVE-2026-14814 (CVSS 8.2) :** Vulnérabilité permettant d'empoisonner le cache des fichiers de dépôt et de compromettre les pipelines CI/CD des utilisateurs ciblés.

**Recommandations :**
Il est impératif de mettre à jour les instances GitLab vers les versions sécurisées suivantes :
*   **19.4.2**
*   **19.3.5**
*   **19.2.8**

---
[Source](https://thehackernews.com/2026/10/gitlab-patches-cvss-100-flaw-that-could.html){:target="_blank"}
