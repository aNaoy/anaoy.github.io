---
title: 'Over 8,300 Gitea servers vulnerable to code execution attacks'
date: 2026-08-28
permalink: /posts/2026/08/28/over-8300-gitea-servers-vulnerable-to-code-execution-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Menace critique sur les serveurs Gitea : vulnérabilité d'exécution de code à distance

Plus de 8 300 instances Gitea exposées sur Internet restent vulnérables à une faille critique activement exploitée par des attaquants pour déployer des malwares, notamment des mineurs de cryptomonnaies. La dangerosité de cette vulnérabilité réside dans la possibilité pour un utilisateur non authentifié d'obtenir un accès en écriture via la fonctionnalité d'auto-inscription par défaut, facilitant ainsi l'exécution de commandes arbitraires sur le serveur hôte.

**Points clés :**
*   **Risque élevé :** La faille permet une exécution de code à distance (RCE) avec les privilèges du compte de service Gitea.
*   **Exploitation active :** La CISA a intégré cette vulnérabilité à son catalogue des failles exploitées (Known Exploited Vulnerabilities) et exige une mise à jour immédiate des agences fédérales américaines.
*   **Vecteur d'attaque :** L'abus du point de terminaison `diffpatch` permet d'installer et d'exécuter des hooks Git malveillants.

**Vulnérabilités identifiées :**
*   **CVE-2026-60004 :** Vulnérabilité critique d'injection de code permettant l'exécution de commandes système arbitraires.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer sans délai le correctif en passant à la version **Gitea 1.27.1** ou supérieure.
*   **Durcissement de la configuration :** Désactiver l'auto-inscription des utilisateurs sur les instances exposées publiquement pour limiter les vecteurs d'entrée.
*   **Surveillance :** Auditer les logs des serveurs pour détecter toute activité suspecte liée à des modifications de dépôts ou à l'exécution de commandes inhabituelles.

---
[Source](https://www.bleepingcomputer.com/news/security/over-8-300-gitea-servers-vulnerable-to-code-execution-attacks/){:target="_blank"}
