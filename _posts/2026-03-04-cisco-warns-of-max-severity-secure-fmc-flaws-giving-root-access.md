---
title: 'Cisco warns of max severity Secure FMC flaws giving root access'
date: 2026-03-04
permalink: /posts/2026/03/04/cisco-warns-of-max-severity-secure-fmc-flaws-giving-root-access/
tags:
- veille-cyber
- bleepingcomp
---
**Alertes critiques sur la sécurité des équipements Cisco**

Des vulnérabilités d'une sévérité maximale ont été corrigées par Cisco dans son logiciel Secure Firewall Management Center (FMC). Ces failles, exploitables à distance par des attaquants non authentifiés, permettent d'obtenir un accès administrateur (root) au système d'exploitation sous-jacent ou d'exécuter du code arbitraire en tant que root.

**Points clés :**

*   Cisco a publié des mises à jour de sécurité pour le logiciel Secure FMC.
*   Deux vulnérabilités critiques ont été identifiées.
*   Ces failles peuvent être exploitées à distance sans authentification préalable.

**Vulnérabilités :**

*   **CVE-2026-20079** : Contournement d'authentification permettant un accès root au système d'exploitation. L'exploitation se fait via des requêtes HTTP spécialement conçues.
*   **CVE-2026-20131** : Exécution de code à distance (RCE). Permet d'exécuter du code Java arbitraire en tant que root via l'envoi d'un objet Java sérialisé à l'interface web. Cette vulnérabilité affecte également Cisco Security Cloud (SCC) Firewall Management.

Cisco indique ne disposer d'aucune preuve d'exploitation active de ces failles ni de publication de code d'exploitation.

**Recommandations :**

*   Appliquer immédiatement les mises à jour de sécurité publiées par Cisco pour Secure FMC.
*   Maintenir les systèmes à jour pour se prémunir contre les menaces connues.

---
[Source](https://www.bleepingcomputer.com/news/security/cisco-warns-of-max-severity-secure-fmc-flaws-giving-root-access/){:target="_blank"}
