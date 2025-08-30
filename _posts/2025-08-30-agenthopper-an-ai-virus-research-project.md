---
title: 'AgentHopper: An AI Virus Research Project'
date: 2025-08-30
permalink: /posts/2025/08/30/agenthopper-an-ai-virus-research-project/
tags:
- veille-cyber
- zerodaysfans
---
AgentHopper : Une arme virale pour les agents IA

Cette recherche présente AgentHopper, un projet démontrant la création d'un "virus IA" capable de se propager en exploitant des vulnérabilités de prompt injection dans divers agents de codage. L'objectif est de mettre en garde les éditeurs de produits IA contre les conséquences potentielles de ces failles.

Points Clés :
*   **Concept de Virus IA** : AgentHopper a été conçu pour utiliser un unique payload de prompt injection capable d'exploiter plusieurs agents de codage simultanément.
*   **Modèle d'Infection** : Un agent compromis initialement télécharge et exécute AgentHopper. Celui-ci infecte ensuite des dépôts Git avec le payload, qui se propage lorsqu'un autre agent interagit avec le code compromis.
*   **Propagation par Prompt Injection Conditionnelle** : La technique exploite des informations du système pour adapter les actions du payload à des agents spécifiques, permettant ainsi une propagation ciblée.

Vulnérabilités Exploitées (et corrigées par les éditeurs) :
*   **GitHub Copilot** : Exécution de code à distance via prompt injection (CVE-2025-53773). Permet de modifier `settings.json` pour activer le mode "YOLO", puis de télécharger et exécuter AgentHopper.
*   **Amp Code** : Exécution de commandes arbitraires via prompt injection. Permet de modifier le fichier de configuration pour y ajouter un faux serveur MCP qui télécharge et exécute AgentHopper.
*   **Amazon Q Developer** : Exécution de code à distance avec prompt injection. Permet d'exécuter une commande `find` avec l'argument `-exec` pour télécharger et lancer AgentHopper.
*   **AWS Kiro** : Exécution de commandes arbitraires via prompt injection indirecte. Permet de modifier le fichier de configuration pour autoriser toutes les commandes bash, puis de télécharger et exécuter AgentHopper.

Recommandations :
*   **Pour les Utilisateurs/Développeurs** :
    *   Sécuriser les clés SSH et de signature avec des phrases secrètes.
    *   Activer la protection des branches pour les dépôts Git.
    *   Appliquer le principe de moindre privilège lors de la configuration des agents.
    *   Utiliser les capacités de sandbox des agents si disponibles.
    *   Les éditeurs EDR et GitHub devraient détecter et atténuer ces menaces rapidement.
*   **Pour les Éditeurs d'Agents IA** :
    *   Assurer des configurations par défaut sécurisées pour limiter les dommages en cas de compromission d'un agent.
    *   Réaliser des analyses approfondies de menaces pour identifier les problèmes de conception, comme l'isolement des paramètres de configuration.
    *   Partager publiquement les résultats des analyses de menaces pour montrer les mesures d'atténuation des risques liés aux prompt injections.

En conclusion, AgentHopper sert de rappel que les malwares pilotés par l'IA et les payloads de prompt injection sont susceptibles de se généraliser, soulignant l'importance des mesures de sécurité de base pour se protéger contre ces menaces.

---
[Source](https://embracethered.com/blog/posts/2025/agenthopper-a-poc-ai-virus/){:target="_blank"}
