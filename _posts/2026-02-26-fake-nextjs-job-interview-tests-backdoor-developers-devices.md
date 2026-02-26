---
title: 'Fake Next.js job interview tests backdoor developers devices'
date: 2026-02-26
permalink: /posts/2026/02/26/fake-nextjs-job-interview-tests-backdoor-developers-devices/
tags:
- veille-cyber
- bleepingcomp
---
**Campagne d'hameçonnage ciblant les développeurs Next.js par des tests de recrutement frauduleux**

Une campagne sophistiquée vise les développeurs en leur proposant de prétendus projets Next.js et des évaluations de codage dans le cadre de processus de recrutement. Ces dépôts malveillants sont conçus pour exécuter du code à distance sur les machines des développeurs, dérober des informations sensibles et installer d'autres charges utiles.

L'attaquant crée de faux projets web construits avec Next.js et les distribue via des plateformes d'hébergement de code comme Bitbucket. Lorsqu'un développeur clone le dépôt et lance le projet localement, des scripts JavaScript malveillants s'activent automatiquement. Ces scripts téléchargent et exécutent une porte dérobée JavaScript, permettant ainsi à l'attaquant de prendre le contrôle du système.

Plusieurs déclencheurs d'exécution sont intégrés pour maximiser les chances de succès de l'attaque :
*   **Déclencheur VS Code :** Un fichier `.vscode/tasks.json` configuré pour s'exécuter à l'ouverture du dossier.
*   **Déclencheur de serveur de développement :** Lors de l'exécution de `npm run dev`, une bibliothèque JavaScript modifiée décode une URL cachée, télécharge un chargeur et l'exécute en mémoire.
*   **Déclencheur de démarrage du backend :** Au démarrage du serveur, un module backend décode un point de terminaison Base64 depuis `.env`, envoie les variables d'environnement à l'attaquant et exécute le code JavaScript reçu.

Le processus d'infection installe une première charge utile qui enregistre le système auprès d'un serveur de commande et de contrôle (C2). Celle-ci peut ensuite évoluer vers un contrôleur de tâches qui communique avec un autre serveur C2, exécute des scripts JavaScript en mémoire, surveille les processus et permet l'énumération de fichiers, la navigation dans les répertoires et l'exfiltration de données.

Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article, mais les méthodes d'attaque exploitent les fonctionnalités standard de développement et l'exécution de code au sein de l'environnement de développement.

**Recommandations :**
*   Appliquer la fonction "Confiance dans l'espace de travail" (Workspace Trust) de VS Code ou utiliser le mode restreint.
*   Activer les règles de réduction de la surface d'attaque (Attack Surface Reduction - ASR).
*   Surveiller les connexions à risque avec la protection Entra ID.
*   Minimiser les secrets stockés sur les postes des développeurs.
*   Utiliser des jetons à courte durée de vie avec les privilèges minimum requis.

---
[Source](https://www.bleepingcomputer.com/news/security/fake-nextjs-job-interview-tests-backdoor-developers-devices/){:target="_blank"}
