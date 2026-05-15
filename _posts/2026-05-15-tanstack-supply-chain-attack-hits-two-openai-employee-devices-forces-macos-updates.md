---
title: 'TanStack Supply Chain Attack Hits Two OpenAI Employee Devices, Forces macOS Updates'
date: 2026-05-15
permalink: /posts/2026/05/15/tanstack-supply-chain-attack-hits-two-openai-employee-devices-forces-macos-updates/
tags:
- veille-cyber
- hackernews
---
### Attaque de la chaîne d'approvisionnement TanStack : Impact sur OpenAI et risques persistants

OpenAI a récemment subi une attaque par compromission de la chaîne d'approvisionnement via le package **TanStack**, infectant deux appareils d'employés. Bien qu'aucune donnée utilisateur ou propriété intellectuelle majeure n'ait été altérée, l'incident a permis l'exfiltration limitée d'identifiants à partir de dépôts de code internes.

**Points clés :**
* **Propagation de l'attaque :** Le groupe "TeamPCP" utilise le ver *Mini Shai-Hulud* pour compromettre des dépendances open source largement utilisées (TanStack, Mistral AI, UiPath, etc.).
* **Risque de signature :** Des certificats de signature de code pour macOS ayant été exposés, OpenAI a dû révoquer et renouveler ces certificats pour éviter la distribution d'applications frauduleuses.
* **Techniques avancées :** Le malware utilise un mécanisme de commande et contrôle (C2) résilient appelé **FIRESCALE**, capable de récupérer des adresses de serveurs alternatives via des commits GitHub.
* **Comportement destructeur :** Le logiciel malveillant intègre une fonction "kamikaze" ciblant spécifiquement des régions géographiques (Israël, Iran) pour effacer les données des systèmes infectés.

**Vulnérabilités :**
* L'attaque exploite une faille dans le pipeline d'intégration continue (CI) de TanStack, permettant aux attaquants de dérober des jetons de publication au moment même de leur création. Aucune CVE spécifique n'est mentionnée pour le framework, car l'attaque repose sur une compromission logique du pipeline et non sur une faille de code dans la bibliothèque elle-même.

**Recommandations :**
* **Mise à jour immédiate :** Les utilisateurs de ChatGPT Desktop, Codex App, Codex CLI et Atlas sur macOS doivent mettre à jour leurs applications vers la dernière version avant le 12 juin 2026, date de révocation des anciens certificats.
* **Sécurisation des pipelines CI/CD :** Les organisations doivent auditer la confiance accordée aux caches de leurs outils de CI et restreindre strictement l'accès aux jetons de publication.
* **Surveillance accrue :** Il est conseillé de surveiller les comportements suspects liés aux variables d'environnement, aux clés SSH et aux accès aux conteneurs Docker, qui constituent des cibles prioritaires pour ce toolkit.

---
[Source](https://thehackernews.com/2026/05/tanstack-supply-chain-attack-hits-two.html){:target="_blank"}
