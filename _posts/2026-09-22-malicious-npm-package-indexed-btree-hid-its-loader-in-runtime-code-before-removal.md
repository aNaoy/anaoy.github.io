---
title: 'Malicious npm Package indexed-btree Hid Its Loader in Runtime Code Before Removal'
date: 2026-09-22
permalink: /posts/2026/09/22/malicious-npm-package-indexed-btree-hid-its-loader-in-runtime-code-before-removal/
tags:
- veille-cyber
- hackernews
---
### Évolution des menaces sur la supply chain : le passage à l'exécution au runtime

Des attaquants ont récemment détourné le package npm `indexed-btree` (et plusieurs autres) pour contourner les nouvelles restrictions de sécurité de npm v12. Plutôt que d'utiliser des scripts d'installation (lifecycle scripts) désormais bloqués, le code malveillant est directement intégré dans les fonctionnalités légitimes de la bibliothèque pour s'exécuter au moment de l'utilisation (runtime).

**Points clés :**
*   **Technique d'exécution :** Le code malveillant est dissimulé dans une méthode (`BTree.prototype.set()`) qui déclenche un script (`sharedLoad.min.js`) lors de l'appel de la fonction par l'application.
*   **Technique "EtherHiding" :** Le malware utilise la blockchain (smart contract sur le testnet Sepolia) pour récupérer des charges utiles chiffrées en plusieurs étapes, rendant la détection plus complexe.
*   **Persistance et évasion :** Une fois le code déployé, le malware s'autonettoie pour effacer ses traces, tout en exfiltrant des informations via Telegram et Slack.
*   **Campagne PolinRider :** Parallèlement, des acteurs (liés à la Corée du Nord) compromettent des comptes de développeurs pour injecter du code malveillant dans des dépôts légitimes, utilisant des déclencheurs variés (tâches VS Code, clones de dépôts, ou exécution via `shell_exec` dans PHP).

**Vulnérabilités :**
*   Il n'y a pas de CVE spécifique citée, car il s'agit d'une exploitation de la logique applicative et non d'une faille logicielle traditionnelle. Le risque réside dans l'injection de code dans des dépendances open-source légitimes, contournant les politiques de restriction des scripts d'installation.

**Recommandations :**
*   **Dépasser le blocage des scripts :** Ne pas se reposer uniquement sur les contrôles lors de l'installation.
*   **Analyse comportementale au runtime :** Mettre en œuvre des solutions capables de surveiller le comportement des dépendances pendant l'exécution de l'application.
*   **Sécurisation des workflows :** Pour les développeurs, renforcer la protection des comptes GitHub/Git, surveiller l'historique des commits et auditer les changements dans les fichiers de configuration ou les tâches d'automatisation (ex: VS Code).
*   **Stratégie de défense en profondeur :** Adopter des mesures de détection à chaque étape : pré-installation, exécution et post-déploiement.

---
[Source](https://thehackernews.com/2026/09/malicious-npm-package-indexed-btree-hid.html){:target="_blank"}
