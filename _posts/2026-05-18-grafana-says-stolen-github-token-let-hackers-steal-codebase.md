---
title: 'Grafana says stolen GitHub token let hackers steal codebase'
date: 2026-05-18
permalink: /posts/2026/05/18/grafana-says-stolen-github-token-let-hackers-steal-codebase/
tags:
- veille-cyber
- bleepingcomp
---
### Intrusion chez Grafana Labs : Vol de code source via GitHub

Grafana Labs a subi une cyberattaque menée par le groupe d'extorsion "CoinbaseCartel", ayant permis aux attaquants de dérober du code source après avoir compromis un jeton d'accès GitHub. Aucune donnée client ou personnelle n'a été exposée et les systèmes de production restent intacts. Refusant de céder au chantage, l'entreprise a choisi de ne pas payer la rançon, conformément aux recommandations du FBI.

**Points clés :**
* **Auteurs :** Le groupe "CoinbaseCartel", suspecté d'être composé d'affiliés de ShinyHunters et Lapsus$.
* **Impact :** Accès non autorisé au code source de la plateforme.
* **Réaction :** Grafana a invalidé les identifiants compromis et renforcé ses mesures de sécurité.
* **Modus Operandi :** Utilisation de jetons d'accès volés pour s'introduire dans les environnements GitHub.

**Vulnérabilités :**
* Compromission d'identifiants (jeton d'accès GitHub). Aucune CVE spécifique n'est associée à cet incident, l'attaque reposant sur l'exploitation d'accès légitimes détournés.

**Recommandations :**
* **Gestion des jetons :** Appliquer le principe du moindre privilège aux jetons d'accès API et mettre en place une rotation régulière.
* **Surveillance :** Renforcer la détection des activités inhabituelles sur les dépôts de code (GitHub/GitLab).
* **Authentification :** Généraliser l'authentification multifacteur (MFA) et surveiller les sessions actives pour détecter toute utilisation détournée de jetons.
* **Politique de réponse :** Établir une stratégie claire de gestion des incidents incluant le refus systématique de paiement des rançons pour limiter les incitations aux futures attaques.

---
[Source](https://www.bleepingcomputer.com/news/security/grafana-says-stolen-github-token-let-hackers-steal-codebase/){:target="_blank"}
