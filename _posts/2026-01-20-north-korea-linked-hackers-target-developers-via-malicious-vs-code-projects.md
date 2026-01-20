---
title: 'North Korea-Linked Hackers Target Developers via Malicious VS Code Projects'
date: 2026-01-20
permalink: /posts/2026/01/20/north-korea-linked-hackers-target-developers-via-malicious-vs-code-projects/
tags:
- veille-cyber
- hackernews
---
### Pirates Nord-Coréens Ciblent les Développeurs via des Projets VS Code Malveillants

Des acteurs malveillants liés à la Corée du Nord, déjà connus pour la campagne "Contagious Interview", utilisent désormais des projets Visual Studio Code (VS Code) piégés pour déployer des portes dérobées (backdoors) sur les machines des développeurs. Cette tactique évoluée vise à exploiter les configurations de tâches de VS Code pour exécuter du code arbitraire lors de l'ouverture de projets malveillants, souvent présentés comme des évaluations professionnelles sur des plateformes comme GitHub, GitLab ou Bitbucket.

Les malwares, nommés BeaverTail (Node.js) et InvisibleFerret (Python), peuvent voler des informations sensibles, miner des cryptomonnaies, enregistrer les frappes clavier et établir un accès à distance. Des mécanismes de secours, comme des dépendances npm malveillantes ou l'exécution déguisée de code via des configurations de tâches, sont également utilisés pour garantir la réussite de l'infection. Ces acteurs ciblent spécifiquement les développeurs dans les secteurs de la cryptomonnaie, de la blockchain et de la fintech, afin d'accéder à des actifs financiers et à de la propriété intellectuelle.

**Points Clés :**

*   **Technique d'Attaque :** Exploitation des fichiers de configuration de tâches (`tasks.json`) de Visual Studio Code pour exécuter des commandes malveillantes.
*   **Mécanisme :** Encourager les développeurs à cloner et ouvrir des dépôts Git malveillants dans VS Code sous prétexte d'une évaluation d'emploi. L'option "runOn: folderOpen" déclenche l'exécution du code malveillant.
*   **Charge Utile :** Implantation de portes dérobées comme BeaverTail et InvisibleFerret, ainsi que potentiellement des mineurs de cryptomonnaies (XMRig) et des outils d'accès à distance (AnyDesk).
*   **Ciblage :** Développeurs travaillant dans la cryptomonnaie, la blockchain et la fintech, en raison de leur accès privilégié aux actifs numériques et aux infrastructures techniques.
*   **Objectif :** Espionnage, vol d'actifs numériques et financement du régime nord-coréen.

**Vulnérabilités :**

Bien qu'aucune CVE spécifique ne soit explicitement mentionnée dans l'article, l'attaque exploite une fonctionnalité légitime de VS Code (la configuration des tâches) pour exécuter du code. La vulnérabilité réside dans la confiance accordée par l'utilisateur lors de l'ouverture d'un projet, qui déclenche l'exécution de commandes potentiellement dangereuses sans consentement explicite après l'approbation initiale de la confiance dans l'auteur du dépôt.

**Recommandations :**

*   **Prudence avec les Dépôts Inconnus :** Faire preuve d'une extrême prudence lors du clonage et de l'ouverture de projets provenant de sources non fiables ou inconnues, même s'ils sont présentés dans un contexte professionnel.
*   **Gestion de la Confiance VS Code :** Être attentif aux invites de VS Code concernant la confiance dans les auteurs de dépôts. Examiner attentivement les fichiers de configuration de tâches (`tasks.json`) avant d'accorder la confiance.
*   **Sécurité des Environnements de Développement :** Maintenir les IDE (comme VS Code) et les systèmes d'exploitation à jour avec les derniers correctifs de sécurité.
*   **Surveillance des Activités Suspectes :** Surveiller les activités réseau inhabituelles et les processus suspects sur les postes de travail des développeurs.
*   **Utilisation de Solutions de Sécurité :** Déployer des solutions de sécuritéEndpoint Detection and Response (EDR) et des antivirus pour détecter et bloquer les malwares.

---
[Source](https://thehackernews.com/2026/01/north-korea-linked-hackers-target.html){:target="_blank"}
