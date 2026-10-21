---
title: 'PHP warns admins of two critical flaws, emergency patches coming tomorrow'
date: 2026-10-21
permalink: /posts/2026/10/21/php-warns-admins-of-two-critical-flaws-emergency-patches-coming-tomorrow/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques "PHP2Shell" : Patchs d'urgence requis

L'équipe de sécurité de PHP a publié des correctifs d'urgence pour deux vulnérabilités critiques permettant l'exécution de code à distance (RCE), surnommées "PHP2Shell". Ces failles, dont les détails ont fuité prématurément, affectent un large éventail de versions de PHP (5, 6, 7 et 8).

**Points clés :**
* **Nature des failles :** Exécution de code à distance (RCE).
* **Impact :** Les vulnérabilités sont jugées critiques, avec des scores CVSS variant entre 9.2 et 10.0 selon les sources.
* **Situation :** Bien que des protections temporaires (WAF Cloudflare) aient été déployées pour bloquer les premières tentatives d'exploitation observées, les développeurs de PHP insistent sur le fait qu'aucun contournement logiciel n'est viable.

**Vulnérabilités identifiées :**
* **CVE-2026-109618**
* **CVE-2026-109619**

**Recommandations :**
* **Installation prioritaire :** La mise à jour vers les versions corrigées fournies par la PHP Foundation est la seule solution définitive pour sécuriser les serveurs.
* **Mesures temporaires (non exhaustives) :** Pour les systèmes ne pouvant pas être patchés immédiatement, certains chercheurs suggèrent de désactiver la fonctionnalité `session.upload_progress` dans le fichier `php.ini` (`session.upload_progress.enabled = Off`), bien que cette mesure ne garantisse pas une protection complète contre les exploits.
* **Vigilance WAF :** Si vous utilisez des solutions comme Cloudflare, assurez-vous que les règles de pare-feu applicatif (WAF) les plus récentes sont activées pour mitiger les tentatives d'attaques connues.

---
[Source](https://www.bleepingcomputer.com/news/security/php-warns-admins-of-two-critical-flaws-emergency-patches-coming-tomorrow/){:target="_blank"}
