---
title: 'North Korea-Linked npm Packages Mimic Rollup Polyfills to Steal Developer Secrets'
date: 2026-07-03
permalink: /posts/2026/07/03/north-korea-linked-npm-packages-mimic-rollup-polyfills-to-steal-developer-secrets/
tags:
- veille-cyber
- hackernews
---
### Campagne de cyber-espionnage via des paquets npm malveillants

Des acteurs liés à la Corée du Nord mènent une campagne de compromission de la chaîne d'approvisionnement logicielle en publiant des paquets **npm** malveillants imitant des outils légitimes de type « Rollup polyfill ». Ces paquets visent les environnements de développement pour exfiltrer des données sensibles et établir un accès distant.

**Points clés :**
* **Méthode d'infection :** Utilisation de noms de paquets proches des originaux (typosquatting) pour tromper les développeurs lors de l'installation.
* **Déroulement de l'attaque :** Installation en plusieurs étapes (téléchargement d'un second paquet, exécution d'un script JavaScript via JSONKeeper, puis déploiement d'une charge utile chiffrée).
* **Cibles :** Stations de travail des développeurs et serveurs CI/CD contenant des clés API, clés SSH, identifiants cloud, portefeuilles de cryptomonnaies et historiques de configuration (VS Code, AWS, Azure, etc.).
* **Capacités malveillantes :** Accès à distance interactif, capture d'écran, enregistrement des frappes clavier, contrôle de la souris et exfiltration massive de fichiers de configuration.
* **Contexte :** Cette vague s'inscrit dans une recrudescence d'attaques similaires sur les dépôts open source (PyPI et npm), incluant le détournement de forks populaires (comme *pyrogram*) et l'usage de contrats intelligents pour la résolution de serveurs C2.

**Vulnérabilités :**
* Aucune CVE n'est associée à ces attaques, car elles exploitent des vecteurs d'ingénierie sociale et la confiance accordée aux dépôts de paquets tiers plutôt qu'une faille logicielle spécifique.

**Recommandations :**
* **Suppression et rotation :** Si l'un des paquets est identifié (ex: `rollup-packages-polyfill-core`, `quirky-token`, `react-icon-svgs`), désinstallez-le immédiatement. Considérez tout environnement l'ayant utilisé comme compromis : effectuez une rotation complète des secrets (clés SSH, tokens, mots de passe).
* **Sécurisation des pipelines :** Intégrez des outils d'analyse de dépendances dans les processus CI/CD pour détecter les paquets suspects ou récemment publiés.
* **Surveillance réseau :** Bloquez les flux sortants vers les adresses IP suspectes identifiées (ex: `216.126.236.244`).
* **Vigilance accrue :** Examinez systématiquement les fichiers `package.json` et les dépendances avant toute installation, particulièrement pour les outils de configuration système.

---
[Source](https://thehackernews.com/2026/07/north-korea-linked-npm-packages-mimic.html){:target="_blank"}
