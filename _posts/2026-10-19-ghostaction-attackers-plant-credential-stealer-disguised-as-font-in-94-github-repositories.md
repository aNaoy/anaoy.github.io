---
title: 'GhostAction Attackers Plant Credential Stealer Disguised as Font in 94 GitHub Repositories'
date: 2026-10-19
permalink: /posts/2026/10/19/ghostaction-attackers-plant-credential-stealer-disguised-as-font-in-94-github-repositories/
tags:
- veille-cyber
- hackernews
---
### Évolution de la campagne GhostAction : du vol de workflow au dérobeur de données persistantes

La campagne GhostAction a évolué en combinant hameçonnage sophistiqué et injection de logiciels malveillants persistants sur les postes de travail des développeurs. Les attaquants utilisent désormais des domaines trompeurs pour capturer les jetons d'authentification GitHub (via des flux OAuth) et implanter des charges utiles dissimulées dans de faux fichiers de police de caractères.

**Points clés :**
* **Infection persistante :** L'attaque ne se limite plus aux environnements CI/CD. Elle utilise une configuration VS Code (`tasks.json`) pour exécuter automatiquement un script malveillant lors de l'ouverture d'un projet.
* **Extraction massive de données :** Le malware cible des informations critiques : clés AWS, jetons PyPI/npm, identifiants Git, clés SSH, secrets Kubernetes et identifiants pour des services d'IA (Claude, Gemini).
* **Portée :** 94 dépôts GitHub compromis ont été identifiés. La stratégie inclut un recours à des workflows de secours (ex: `lint.yml`, `audit.yml`) en cas d'échec de la charge principale.
* **Technique de contournement :** En ciblant les machines locales des développeurs via VS Code, les attaquants s'affranchissent des mécanismes de défense de GitHub sur ses serveurs de build.

**Vulnérabilités exploitées :**
* **Phishing OAuth :** Utilisation d'un reverse proxy pour intercepter les sessions et autoriser silencieusement des applications OAuth malveillantes (Device Code Flow).
* **Exécution automatique :** Abus de la fonctionnalité `runOn: folderOpen` de VS Code pour l'exécution arbitraire de code local.
* *Note : Aucune CVE spécifique n'est associée à ces détournements de fonctionnalités légitimes.*

**Recommandations :**
* **Réinitialisation immédiate :** Révoquer tous les jetons GitHub, changer les mots de passe et faire pivoter l'ensemble des clés d'accès (AWS, Kubernetes, clés API) potentiellement exposées.
* **Audit des configurations :** Examiner les dossiers `.github/workflows/` pour détecter tout fichier suspect et vérifier les fichiers `tasks.json` dans les projets VS Code.
* **Assainissement :** Effectuer ces opérations de nettoyage et de révocation depuis une machine propre et sécurisée.
* **Veille sur les dépôts :** Alerter les utilisateurs ayant cloné les dépôts compromis, car la charge malveillante réside désormais sur le code source lui-même.

---
[Source](https://thehackernews.com/2026/10/ghostaction-attackers-plant-credential.html){:target="_blank"}
