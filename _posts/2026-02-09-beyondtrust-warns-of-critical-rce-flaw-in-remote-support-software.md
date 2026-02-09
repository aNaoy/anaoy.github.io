---
title: 'BeyondTrust warns of critical RCE flaw in remote support software'
date: 2026-02-09
permalink: /posts/2026/02/09/beyondtrust-warns-of-critical-rce-flaw-in-remote-support-software/
tags:
- veille-cyber
- bleepingcomp
---
### Alertes critiques pour les logiciels de support à distance de BeyondTrust

Une faille de sécurité critique a été découverte dans les logiciels Remote Support (RS) et Privileged Remote Access (PRA) de BeyondTrust, permettant à des attaquants non authentifiés d'exécuter du code arbitraire à distance.

**Points clés :**

*   La vulnérabilité, identifiée comme CVE-2026-1731, est une injection de commande système pré-authentification.
*   Les attaquants peuvent exploiter cette faille avec des requêtes client malveillantes, ne nécessitant aucune interaction utilisateur et présentant une faible complexité.
*   L'exploitation réussie pourrait permettre à un attaquant distant non authentifié d'exécuter des commandes système dans le contexte de l'utilisateur du site, entraînant potentiellement un compromis du système, un accès non autorisé, une exfiltration de données et une interruption de service.
*   Environ 11 000 instances sont exposées à Internet, dont environ 8 500 déploiements sur site qui restent potentiellement vulnérables si les correctifs ne sont pas appliqués.
*   BeyondTrust a indiqué qu'il n'y a actuellement aucune exploitation connue de cette vulnérabilité.

**Vulnérabilités :**

*   **CVE-2026-1731** : Injection de commande OS pré-authentification dans BeyondTrust Remote Support (versions 25.3.1 et antérieures) et Privileged Remote Access (versions 24.3.4 et antérieures).

**Recommandations :**

*   Les clients sur site doivent mettre à jour leurs systèmes manuellement en passant à Remote Support version 25.3.2 ou ultérieure, et Privileged Remote Access version 25.1.1 ou ultérieure, s'ils n'ont pas activé les mises à jour automatiques.
*   BeyondTrust a déjà sécurisé tous les systèmes cloud RS/PRA.

---
[Source](https://www.bleepingcomputer.com/news/security/beyondtrust-warns-of-critical-rce-flaw-in-remote-support-software/){:target="_blank"}
