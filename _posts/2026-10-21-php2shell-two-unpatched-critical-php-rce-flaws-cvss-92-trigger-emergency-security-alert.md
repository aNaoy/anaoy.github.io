---
title: 'PHP2Shell: Two Unpatched Critical PHP RCE Flaws (CVSS 9.2) Trigger Emergency Security Alert'
date: 2026-10-21
permalink: /posts/2026/10/21/php2shell-two-unpatched-critical-php-rce-flaws-cvss-92-trigger-emergency-security-alert/
tags:
- veille-cyber
- hackernews
---
### Alerte de sécurité critique : Vulnérabilités RCE dans PHP

L'équipe de développement de PHP a annoncé une publication corrective d'urgence suite à la découverte de deux vulnérabilités critiques de type exécution de code à distance (RCE), surnommées « **php2shell** ». Ces failles, bien que non encore détaillées officiellement, ont été évaluées avec un score de sévérité de 9,2 sur l'échelle CVSS v4.0.

#### Points clés
*   **Fuite d'informations :** L'existence des failles a été révélée prématurément par une fuite non confirmée, forçant une publication corrective accélérée.
*   **Périmètre :** Seules les branches PHP actuellement supportées (8.2 à 8.5) bénéficieront d'un correctif officiel.
*   **Risque :** Aucune exploitation active n'a été signalée à ce jour, mais la criticité élevée impose une vigilance immédiate.

#### Vulnérabilités identifiées
*   **CVE-2026-109618**
*   **CVE-2026-109619**

#### Recommandations pour les administrateurs
1.  **Inventaire :** Recenser tous les environnements PHP en production, y compris ceux intégrés dans des appliances, logiciels tiers ou panneaux de contrôle (cPanel, Plesk).
2.  **Mise à jour prioritaire :** Appliquer les correctifs officiels dès leur disponibilité sur les systèmes exposés à Internet.
3.  **Gestion du cycle de vie (EOL) :** Les versions antérieures à 8.2 (8.1, 8.0, 7.x, 5.x) ne recevront aucun correctif. Il est impératif de mettre à jour ces versions, de les isoler du réseau public, ou de les placer derrière un pare-feu applicatif (WAF) strict.
4.  **Surveillance proactive :** Surveiller les comportements suspects des processus PHP (`php-fpm`, `php-cgi`) : toute tentative de lancement de shells, d'outils de téléchargement ou d'exécutables système doit être considérée comme une compromission.
5.  **Isolation :** En cas d'impossibilité de patching immédiat, le CERT-EU préconise l'isolation totale des applications web exposées jusqu'à l'application des correctifs.

---
[Source](https://thehackernews.com/2026/10/php2shell-two-unpatched-critical-php.html){:target="_blank"}
