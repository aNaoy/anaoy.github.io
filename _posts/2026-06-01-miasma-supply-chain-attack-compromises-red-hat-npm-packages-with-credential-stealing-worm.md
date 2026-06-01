---
title: 'Miasma Supply Chain Attack Compromises Red Hat npm Packages with Credential-Stealing Worm'
date: 2026-06-01
permalink: /posts/2026/06/01/miasma-supply-chain-attack-compromises-red-hat-npm-packages-with-credential-stealing-worm/
tags:
- veille-cyber
- hackernews
---
### Miasma : Campagne de compromission de la chaîne d'approvisionnement npm chez Red Hat

La campagne « Miasma » exploite des paquets npm légitimes de `@redhat-cloud-services` pour déployer un ver auto-propageant visant le vol d'identifiants et l'empoisonnement de la chaîne d'approvisionnement logicielle. L'attaque initiale aurait été facilitée par la compromission du compte GitHub d'un employé de Red Hat, permettant d'injecter du code malveillant en contournant les revues de code.

**Points clés :**
* **Vecteur d'attaque :** Utilisation de hooks `preinstall` obfusqués pour exécuter le malware lors de l'installation des paquets.
* **Cibles de données :** Jetons npm, clés SSH, secrets GitHub Actions, identifiants cloud (GCP/Azure), Kubernetes, Vault et fichiers de configuration sensibles.
* **Persistance :** Le malware s'implante dans VS Code (`tasks.json`) et Anthropic Claude Code, garantissant une exécution à chaque session utilisateur.
* **Évasion :** Le logiciel malveillant détecte la présence de solutions EDR (CrowdStrike, SentinelOne, etc.) et évite l'exécution sur les systèmes configurés en russe.
* **Propagation :** Le malware utilise l'API GitHub pour commettre des modifications signées, transformant les machines infectées en vecteurs de propagation pour les futures versions des paquets.

**Vulnérabilités :**
Aucun identifiant CVE spécifique n'est attribué à cette campagne, car il s'agit d'une injection de code malveillant dans des paquets légitimes (Supply Chain Attack) plutôt qu'une faille logicielle traditionnelle.

**Recommandations :**
* **Nettoyage approfondi :** La simple suppression des `node_modules` est insuffisante. Il est impératif d'auditer et de supprimer les artefacts de persistance dans `~/.claude/settings.json`, `.vscode/tasks.json` et les workflows GitHub.
* **Gestion des accès :** Procéder à une rotation immédiate de tous les secrets et identifiants potentiellement exposés sur les machines infectées.
* **Sécurité CI/CD :** Suspendre les workflows suspects, invalider les artefacts de build générés durant la période d'exposition et examiner les déploiements récents pour détecter toute manipulation.
* **Isolation :** Isoler les hôtes ayant utilisé les paquets compromis et mener une analyse forensique pour identifier toute tentative d'élévation de privilèges ou d'accès cloud non autorisé.

---
[Source](https://thehackernews.com/2026/06/miasma-supply-chain-attack-compromises.html){:target="_blank"}
