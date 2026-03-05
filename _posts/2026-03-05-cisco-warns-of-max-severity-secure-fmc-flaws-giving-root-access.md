---
title: 'Cisco warns of max severity Secure FMC flaws giving root access'
date: 2026-03-05
permalink: /posts/2026/03/05/cisco-warns-of-max-severity-secure-fmc-flaws-giving-root-access/
tags:
- veille-cyber
- bleepingcomp
---
**Sécurité des pare-feux Cisco : Vulnérabilités critiques corrigées**

Cisco a publié des mises à jour pour deux failles de sécurité d'une gravité maximale affectant son logiciel Secure Firewall Management Center (FMC). Ces vulnérabilités permettent à des attaquants non authentifiés d'obtenir un accès distant et de prendre le contrôle total des systèmes affectés.

**Points clés :**

*   Deux vulnérabilités critiques ont été découvertes dans Cisco Secure FMC.
*   Ces failles peuvent être exploitées à distance par des acteurs malveillants sans nécessiter d'authentification.
*   Aucune preuve d'exploitation active ou de code d'exploitation public n'a été détectée pour ces vulnérabilités spécifiques.

**Vulnérabilités :**

*   **CVE-2026-20079 :** Une faille de contournement d'authentification qui permet à un attaquant d'obtenir un accès "root" au système d'exploitation sous-jacent via des requêtes HTTP spécialement conçues.
*   **CVE-2026-20131 :** Une vulnérabilité d'exécution de code à distance (RCE) permettant à un attaquant d'exécuter du code Java arbitraire avec des privilèges "root" en envoyant un objet Java sérialisé à l'interface web de gestion. Cette vulnérabilité affecte également Cisco Security Cloud Control (SCC) Firewall Management.

**Recommandations :**

*   Appliquer immédiatement les mises à jour de sécurité publiées par Cisco pour le logiciel Secure Firewall Management Center (FMC).
*   Gérer attentivement les requêtes HTTP et les objets Java sérialisés envoyés aux interfaces de gestion des pare-feux.

---
[Source](https://www.bleepingcomputer.com/news/security/cisco-warns-of-max-severity-secure-fmc-flaws-giving-root-access/){:target="_blank"}
