---
title: 'Keyv-Linked npm Worm Poisons Hundreds of Packages, Plants Claude Code and VS Code Hooks'
date: 2026-08-04
permalink: /posts/2026/08/04/keyv-linked-npm-worm-poisons-hundreds-of-packages-plants-claude-code-and-vs-code-hooks/
tags:
- veille-cyber
- hackernews
---
### Compromission massive de la chaîne d'approvisionnement npm par le ver « Shai-Hulud »

Une campagne malveillante sophistiquée a compromis des centaines de paquets npm (au moins 1 684 versions identifiées sur 420 noms de paquets) via une propagation automatisée. Le ver, identifié comme appartenant à la famille « Shai-Hulud », injecte des scripts malveillants dans le cycle de vie des dépendances pour dérober des identifiants et prendre le contrôle de nouveaux comptes de publication.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation du script `preinstall` (via le fichier `setup.mjs`) pour télécharger le runtime Bun et exécuter une charge utile lourde (environ 700 Ko).
*   **Capacités du malware :** Extraction d'identifiants (GitHub, npm, cloud, Kubernetes, bases de données, clés privées), lecture de la mémoire des runners GitHub Actions et installation d'un mécanisme de surveillance pour empêcher la révocation des jetons volés.
*   **Persistance IDE :** Intégration de hooks dans `.vscode/` et `.claude/` pour exécuter le code malveillant dès l'ouverture d'un projet dans VS Code ou Claude Code si l'utilisateur accorde sa confiance à l'espace de travail.
*   **Tromperie :** Le code malveillant bénéficiait de signatures GitHub valides (provenance SLSA) via le workflow de publication légitime du projet, rendant la détection difficile par les outils de vérification classiques.

**Vulnérabilités :**
*   L'exécution automatique de scripts de cycle de vie (`preinstall`) par le gestionnaire de paquets npm.
*   La confiance accordée aux espaces de travail dans les IDE (VS Code/Claude) permettant l'exécution de tâches locales malveillantes.
*   Aucune CVE spécifique n'est attribuée à cette attaque, car elle exploite des comportements attendus de la chaîne d'outils (scripts d'installation).

**Recommandations :**
*   **Audit immédiat :** Analyser les fichiers `package-lock.json` et les versions résolues sur les systèmes de développement et les environnements CI/CD pour détecter les paquets compromis.
*   **Sécurisation des environnements :** Désactiver les scripts d'installation automatique dans npm (`npm config set ignore-scripts true`) ou migrer vers npm 12+ qui bloque ces scripts par défaut.
*   **Gestion des accès :** Si un environnement a exécuté une version affectée, considérer tous les jetons, clés API et identifiants stockés sur cette machine comme compromis.
*   **Procédure de remédiation :** Avant de révoquer les jetons, supprimer impérativement le « watcher » de révocation installé par le malware, car ce dernier peut intercepter la procédure de révocation pour exécuter des commandes malveillantes locales.
*   **Hygiène de développement :** Se méfier des fichiers de configuration IDE (`.vscode/`, `.claude/`) contenus dans les dépendances tierces et ne pas accorder de confiance aveugle aux nouveaux projets.

---
[Source](https://thehackernews.com/2026/08/keyv-linked-npm-worm-poisons-hundreds.html){:target="_blank"}
