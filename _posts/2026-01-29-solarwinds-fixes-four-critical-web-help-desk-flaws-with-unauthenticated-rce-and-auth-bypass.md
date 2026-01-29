---
title: 'SolarWinds Fixes Four Critical Web Help Desk Flaws With Unauthenticated RCE and Auth Bypass'
date: 2026-01-29
permalink: /posts/2026/01/29/solarwinds-fixes-four-critical-web-help-desk-flaws-with-unauthenticated-rce-and-auth-bypass/
tags:
- veille-cyber
- hackernews
---
### Multiples Vulnérabilités Critiques dans SolarWinds Web Help Desk Corrigées

SolarWinds a publié des mises à jour pour corriger plusieurs failles de sécurité affectant son logiciel Web Help Desk. Parmi celles-ci, quatre vulnérabilités critiques permettent le contournement de l'authentification et l'exécution de code à distance (RCE). Ces failles représentent un risque significatif car elles sont exploitables par des attaquants non authentifiés.

**Points Clés :**

*   **Nature des Failles :** Les vulnérabilités incluent le contournement de contrôles de sécurité, l'utilisation d'identifiants codés en dur, la désérialisation de données non fiables et le contournement d'authentification.
*   **Impact :** L'exploitation peut mener à l'accès à des fonctionnalités restreintes, à des fonctions administratives et, de manière critique, à l'exécution de commandes arbitraires sur le système hôte.
*   **Récent Historique :** Ces correctifs font suite à la découverte et au traitement de plusieurs autres vulnérabilités dans le même produit au cours des dernières années, dont certaines ont été activement exploitées.

**Vulnérabilités (avec CVE) :**

*   **CVE-2025-40536** (CVSS 8.1) : Contournement de contrôle de sécurité, permettant l'accès à des fonctionnalités restreintes sans authentification.
*   **CVE-2025-40537** (CVSS 7.5) : Identifiants codés en dur, permettant l'accès aux fonctions administratives avec le compte "client".
*   **CVE-2025-40551** (CVSS 9.8) : Désérialisation de données non fiables, permettant une exécution de code à distance par un attaquant non authentifié.
*   **CVE-2025-40552** (CVSS 9.8) : Contournement d'authentification, permettant à un attaquant non authentifié d'exécuter des actions. Peut potentiellement mener à RCE.
*   **CVE-2025-40553** (CVSS 9.8) : Désérialisation de données non fiables, permettant une exécution de code à distance par un attaquant non authentifié.
*   **CVE-2025-40554** (CVSS 9.8) : Contournement d'authentification, permettant à un attaquant d'invoquer des actions spécifiques. Peut potentiellement mener à RCE.

**Recommandations :**

*   Mettre à jour SolarWinds Web Help Desk vers la version **WHD 2026.1** ou une version ultérieure dès que possible. Compte tenu du risque élevé et de l'historique d'exploitation, une action rapide est essentielle.

---
[Source](https://thehackernews.com/2026/01/solarwinds-fixes-four-critical-web-help.html){:target="_blank"}
