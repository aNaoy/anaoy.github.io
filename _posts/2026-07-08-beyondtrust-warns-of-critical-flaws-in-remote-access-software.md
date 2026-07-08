---
title: 'BeyondTrust warns of critical flaws in remote access software'
date: 2026-07-08
permalink: /posts/2026/07/08/beyondtrust-warns-of-critical-flaws-in-remote-access-software/
tags:
- veille-cyber
- bleepingcomp
---
### Alert de sécurité : Vulnérabilités critiques dans les logiciels BeyondTrust

BeyondTrust a émis un avertissement concernant plusieurs failles de sécurité critiques touchant ses solutions *Remote Support* (RS) et *Privileged Remote Access* (PRA). Ces vulnérabilités permettent à des attaquants non authentifiés de contourner les contrôles d'accès ou d'accéder indûment aux appliances ciblées.

**Points clés :**
*   **Risques :** Contournement de l'authentification, accès non autorisé aux systèmes, accès à des comptes à privilèges, déni de service et accès restreint aux ressources.
*   **Contexte :** Près de 2 000 instances RS et PRA restent exposées en ligne. Bien qu'aucune exploitation active n'ait été confirmée pour ces failles spécifiques, le passé a démontré que les produits BeyondTrust sont des cibles privilégiées pour des groupes de cyberespionnage (ex: Silk Typhoon).

**Vulnérabilités identifiées :**
*   **CVE-2026-40138 :** Erreur d'authentification dans le sous-système de RS et PRA (versions 25.3.2 et antérieures). Permet un contournement des contrôles d'accès.
*   **CVE-2026-40139 :** Mauvais traitement des requêtes d'authentification dans RS, permettant un accès distant non authentifié.
*   **CVE-2026-40140 & CVE-2026-40141 :** Vulnérabilités de haute sévérité pouvant mener à des attaques par déni de service (DoS) ou à un accès non autorisé à des ressources restreintes.

**Recommandations :**
*   **Clients Cloud :** Les correctifs ont été automatiquement appliqués par BeyondTrust le 21 avril 2026.
*   **Clients auto-hébergés :** 
    *   Appliquer immédiatement le correctif de sécurité du mois d'avril.
    *   Mettre à niveau vers la version **25.3.3 ou supérieure** pour les solutions RS et PRA.
    *   S'assurer que les instances ne sont pas exposées inutilement sur Internet.

---
[Source](https://www.bleepingcomputer.com/news/security/beyondtrust-warns-of-critical-flaws-in-remote-access-software/){:target="_blank"}
