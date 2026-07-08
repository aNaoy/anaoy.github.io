---
title: 'BeyondTrust Patches Critical Auth Bypass Flaws in Remote Support and PRA'
date: 2026-07-08
permalink: /posts/2026/07/08/beyondtrust-patches-critical-auth-bypass-flaws-in-remote-support-and-pra/
tags:
- veille-cyber
- hackernews
---
### Failles critiques de contournement d'authentification chez BeyondTrust

BeyondTrust a publié des correctifs pour quatre vulnérabilités critiques affectant ses solutions *Remote Support* (RS) et *Privileged Remote Access* (PRA). Ces failles, découvertes lors d'évaluations de sécurité internes assistées par IA, permettent à des attaquants distants non authentifiés de prendre le contrôle des appliances ou de provoquer des interruptions de service.

**Vulnérabilités identifiées :**

*   **CVE-2026-40138 (Score CVSS 9.2) :** Défaut de validation des données d'authentification permettant le contournement des contrôles d'accès et une prise de contrôle avec privilèges élevés.
*   **CVE-2026-40139 (Score CVSS 9.2) :** Mauvais traitement des requêtes d'authentification autorisant un attaquant distant à contourner les accès.
*   **CVE-2026-40140 (Score CVSS 8.7) :** Insuffisance de validation des entrées utilisateur pouvant entraîner un déni de service (DoS).
*   **CVE-2026-40141 (Score CVSS 8.5) :** Problème de validation des entrées permettant à un utilisateur authentifié de restreindre l'accès à des ressources non autorisées.

**Points clés :**
*   Les vulnérabilités 40138 et 40139 dépendent de configurations d'authentification spécifiques.
*   Bien qu'aucune exploitation active ne soit signalée, l'historique des produits BeyondTrust (fréquemment ciblés pour l'installation de web shells) impose une vigilance immédiate.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs en passant vers les versions **RS 25.3.3** ou **PRA 25.3.3** minimum.
*   **Audit de configuration :** Vérifier les paramètres d'authentification pour identifier si les instances sont exposées aux vecteurs d'attaque des CVE-2026-40138 et 40139.

---
[Source](https://thehackernews.com/2026/07/beyondtrust-patches-critical-auth.html){:target="_blank"}
