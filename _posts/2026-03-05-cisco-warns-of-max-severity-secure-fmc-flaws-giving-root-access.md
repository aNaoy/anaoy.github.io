---
title: 'Cisco warns of max severity Secure FMC flaws giving root access'
date: 2026-03-05
permalink: /posts/2026/03/05/cisco-warns-of-max-severity-secure-fmc-flaws-giving-root-access/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilités Critiques dans Cisco Secure FMC**

Cisco a publié des mises à jour pour corriger deux vulnérabilités de sévérité maximale dans son logiciel Secure Firewall Management Center (FMC). Ces failles permettent à des attaquants non authentifiés, à distance, d'obtenir un accès root au système sous-jacent.

**Points Clés :**

*   Le logiciel Cisco Secure FMC est utilisé pour gérer les pare-feux Cisco et configurer diverses fonctions de sécurité.
*   Deux vulnérabilités critiques permettent une exploitation à distance sans authentification.
*   Bien qu'aucune exploitation active ou code de démonstration de faisabilité n'ait été signalée pour ces deux failles spécifiques, Cisco a récemment corrigé plusieurs autres vulnérabilités graves dans ses produits.

**Vulnérabilités :**

*   **CVE-2026-20079** (Bypass d'authentification) : Permet à un attaquant d'obtenir un accès root au système d'exploitation. L'exploitation se fait via des requêtes HTTP spécialement conçues.
*   **CVE-2026-20131** (Exécution de code à distance) : Permet à un attaquant d'exécuter du code Java arbitraire en tant que root. L'exploitation se fait en envoyant un objet Java sérialisé spécialement conçu à l'interface de gestion Web.

Cette dernière vulnérabilité affecte également Cisco Security Cloud Control (SCC) Firewall Management.

**Recommandations :**

*   Appliquer immédiatement les mises à jour de sécurité publiées par Cisco pour le logiciel Secure FMC.
*   Maintenir les systèmes à jour pour se prémunir contre les menaces connues.

---
[Source](https://www.bleepingcomputer.com/news/security/cisco-warns-of-max-severity-secure-fmc-flaws-giving-root-access/){:target="_blank"}
