---
title: 'Hijacked npm and Go Packages Use VS Code Tasks to Deploy Python Infostealer'
date: 2026-06-29
permalink: /posts/2026/06/29/hijacked-npm-and-go-packages-use-vs-code-tasks-to-deploy-python-infostealer/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement : Le malware "Fake Font" cible les développeurs via VS Code

Des chercheurs en cybersécurité ont identifié une campagne malveillante sophistiquée ciblant les développeurs via des paquets npm (`html-to-gutenberg`, `fetch-page-assets`) et 16 paquets Go corrompus. Cette attaque, attribuée à des acteurs liés à la Corée du Nord, s'inscrit dans la continuité de la campagne « Contagious Interview ».

**Points clés :**
*   **Vecteur d'exécution :** Le malware contourne les restrictions classiques de npm en utilisant une tâche VS Code (`.vscode/tasks.json`) configurée pour s'exécuter automatiquement (`runOn: 'folderOpen'`) lors de l'ouverture d'un projet.
*   **Dissimulation :** Le code malveillant est masqué dans un faux fichier de police (`fa-solid-400.woff2`) qui contient en réalité du JavaScript.
*   **Persistance et C2 :** L'attaque utilise la blockchain (TronGrid/Aptos) comme serveur de résolution pour récupérer les instructions de commande et de contrôle (C2).
*   **Charge utile finale :** Déploiement du malware « InvisibleFerret », un infostealer Python capable de collecter des portefeuilles crypto, des identifiants de navigateurs, des clés API, des données Git et des informations provenant de gestionnaires de mots de passe (Windows, macOS, Linux).
*   **Fonctionnalités :** Installation d'une backdoor via Socket.io permettant le contrôle à distance, l'exécution de commandes et le vol de fichiers.

**Vulnérabilités :**
*   **Exploitation de la fonctionnalité « Task Auto-Run » de VS Code :** L'activation automatique de tâches de confiance lors de l'ouverture d'un dossier permet l'exécution de code arbitraire sans interaction supplémentaire de l'utilisateur.

**Recommandations :**
*   **Suppression immédiate :** Désinstaller les paquets suspects identifiés.
*   **Audit de sécurité :** Rechercher la présence de tâches VS Code malveillantes dans les dossiers de projet.
*   **Réinitialisation des accès :** Procéder au renouvellement immédiat de tous les identifiants, tokens, clés API, clés SSH et mots de passe stockés dans les navigateurs, gestionnaires de secrets et portefeuilles de cryptomonnaies compromis.
*   **Prudence :** Ne pas marquer les dossiers de projets inconnus ou non vérifiés comme « dossiers de confiance » dans les IDE.

---
[Source](https://thehackernews.com/2026/06/hijacked-npm-and-go-packages-use-vs.html){:target="_blank"}
