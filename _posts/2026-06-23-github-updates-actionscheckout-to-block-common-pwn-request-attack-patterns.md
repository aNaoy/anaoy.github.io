---
title: 'GitHub Updates actions/checkout to Block Common Pwn Request Attack Patterns'
date: 2026-06-23
permalink: /posts/2026/06/23/github-updates-actionscheckout-to-block-common-pwn-request-attack-patterns/
tags:
- veille-cyber
- hackernews
---
### Sécurisation de la chaîne d'approvisionnement : GitHub bloque les attaques « Pwn Request »

GitHub a mis à jour l'action `actions/checkout` (version 7) pour empêcher par défaut l'exécution de code malveillant provenant de dépôts forkeurs lors de l'utilisation du déclencheur `pull_request_target`. Cette mesure vise à contrer les attaques de type « pwn request » qui exploitent les privilèges élevés associés aux workflows GitHub Actions.

**Points clés :**
*   **Vulnérabilité contextuelle :** Le déclencheur `pull_request_target` s'exécute avec les secrets et les permissions en écriture du dépôt de base. Lorsqu'il est combiné avec `actions/checkout` pour extraire le code d'un fork non fiable, un attaquant peut exécuter du code arbitraire avec les privilèges du workflow.
*   **Mesure de protection :** Depuis le 18 juin 2026, `actions/checkout` refuse automatiquement de récupérer le code source des pull requests issues de forks si certaines conditions de référence (références `refs/pull/...` ou SHA de commit) sont remplies.
*   **Portée limitée :** Cette protection est un garde-fou spécifique à `actions/checkout`. Elle ne couvre pas les autres méthodes d'extraction de code (via Git ou CLI) ni les autres déclencheurs d'événements.

**CVE associée :**
*   Aucune CVE spécifique n'est mentionnée ; le problème réside dans une mauvaise configuration logique des privilèges GitHub Actions.

**Recommandations :**
*   **Utilisation restreinte :** Privilégier le déclencheur `pull_request` standard plutôt que `pull_request_target` dès que l'accès aux secrets ou aux droits d'écriture n'est pas strictement nécessaire.
*   **Principe du moindre privilège :** Restreindre explicitement les permissions accordées aux workflows (`GITHUB_TOKEN` avec des droits en lecture seule si possible).
*   **Audit de code :** Ne jamais exécuter de code provenant d'une source non fiable au sein d'un workflow disposant de privilèges élevés.
*   **Option de dérogation :** Pour les cas d'usage légitimes nécessitant cette fonctionnalité, l'utilisation du flag `allow-unsafe-pr-checkout: true` est requise, tout en étant conscient des risques de sécurité accrus.

---
[Source](https://thehackernews.com/2026/06/github-updates-actionscheckout-to-block.html){:target="_blank"}
