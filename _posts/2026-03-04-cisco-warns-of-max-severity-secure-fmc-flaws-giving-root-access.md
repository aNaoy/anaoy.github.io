---
title: 'Cisco warns of max severity Secure FMC flaws giving root access'
date: 2026-03-04
permalink: /posts/2026/03/04/cisco-warns-of-max-severity-secure-fmc-flaws-giving-root-access/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilités critiques dans Cisco Secure FMC : accès root compromis**

Cisco a publié des mises à jour de sécurité pour corriger deux vulnérabilités d'une gravité maximale dans son logiciel Secure Firewall Management Center (FMC). Ces failles permettent à des attaquants non authentifiés d'obtenir un accès root au système d'exploitation sous-jacent, leur conférant ainsi des privilèges élevés.

**Points clés :**

*   **Impact :** Accès root à distance et exécution de code arbitraire.
*   **Cibles :** Cisco Secure Firewall Management Center (FMC) et Cisco Security Cloud Control (SCC) Firewall Management.
*   **Activité des attaquants :** Aucune preuve actuelle d'exploitation active ou de publication de code d'exploitation n'est disponible.

**Vulnérabilités :**

*   **CVE-2026-20079 :** Contournement d'authentification permettant l'obtention de l'accès root au système d'exploitation. Un attaquant peut exploiter cette faille en envoyant des requêtes HTTP malveillantes.
*   **CVE-2026-20131 :** Exécution de code à distance (RCE). Un attaquant peut exploiter cette faille en envoyant un objet Java sérialisé malveillant à l'interface de gestion web, permettant l'exécution de code arbitraire en tant que root.

**Recommandations :**

Il est fortement recommandé d'appliquer les mises à jour de sécurité fournies par Cisco pour les logiciels Cisco Secure FMC et Cisco Security Cloud Control (SCC) Firewall Management afin de corriger ces vulnérabilités critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/cisco-warns-of-max-severity-secure-fmc-flaws-giving-root-access/){:target="_blank"}
