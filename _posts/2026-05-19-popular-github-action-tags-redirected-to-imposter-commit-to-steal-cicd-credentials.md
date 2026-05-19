---
title: 'Popular GitHub Action Tags Redirected to Imposter Commit to Steal CI/CD Credentials'
date: 2026-05-19
permalink: /posts/2026/05/19/popular-github-action-tags-redirected-to-imposter-commit-to-steal-cicd-credentials/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement : détournement de GitHub Actions

Une attaque de type « imposter commit » a permis de compromettre les workflows populaires `actions-cool/issues-helper` et `actions-cool/maintain-one-comment`. En déplaçant les tags vers des commits malveillants, les attaquants ont pu injecter du code arbitraire dans les pipelines CI/CD des utilisateurs, sans passer par les processus de revue habituels.

**Points clés :**
*   **Méthodologie :** Les attaquants ont fait pointer les tags existants vers des commits externes contenant du code malveillant, contournant ainsi la confiance accordée aux versions taguées.
*   **Mode opératoire :** Le code injecté installe le runtime Bun, extrait des secrets en mémoire depuis le processus `Runner.Worker`, et exfiltre ces données vers un serveur distant (`t.m-kosche[.]com`).
*   **Attribution :** Cette campagne est liée au groupe « Mini Shai-Hulud », également impliqué dans des attaques contre l'écosystème npm (`@antv`).

**Vulnérabilités :**
*   Pas de CVE spécifique attribuée (il s'agit d'une vulnérabilité logique liée à l'utilisation de tags mutables dans les workflows GitHub Actions).

**Recommandations :**
*   **Utiliser les hashs de commit (SHA) :** Pour garantir l'intégrité, ne référencez jamais une action par son numéro de tag (ex: `v1`), mais utilisez systématiquement le hash complet du commit (ex: `actions/checkout@b4ffde65f46336ab88ed53be65821814739de1a9`).
*   **Auditer les workflows :** Vérifiez régulièrement les dépendances de vos pipelines CI/CD et restreignez les accès réseau sortants des runners pour bloquer les exfiltrations vers des domaines inconnus.
*   **Surveillance :** Surveillez les logs de vos exécutions CI/CD pour détecter des téléchargements de binaires inattendus ou des connexions réseau suspectes.

---
[Source](https://thehackernews.com/2026/05/github-actions-supply-chain-attack.html){:target="_blank"}
