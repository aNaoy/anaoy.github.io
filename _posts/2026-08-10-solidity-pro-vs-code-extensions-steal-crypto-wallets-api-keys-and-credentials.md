---
title: 'Solidity Pro VS Code Extensions Steal Crypto Wallets, API Keys, and Credentials'
date: 2026-08-10
permalink: /posts/2026/08/10/solidity-pro-vs-code-extensions-steal-crypto-wallets-api-keys-and-credentials/
tags:
- veille-cyber
- hackernews
---
### Menace sur les extensions VS Code : L'affaire « Solidity Pro »

Des extensions malveillantes pour Visual Studio Code, identifiées sous les noms **`helper-beeps.solidity-pro`** et **`web3devtoolsx.solidity-pro`**, ont été découvertes diffusant un logiciel espion capable de dérober des données sensibles. Bien qu'elles aient été retirées des plateformes officielles, leur capacité à contourner les mesures de sécurité classiques souligne une menace persistante pour les développeurs.

**Points clés :**
*   **Mode opératoire :** Les extensions utilisent une activation différée (plusieurs heures ou jours après l'installation) et une forte obfuscation pour échapper aux scanners automatisés et aux sandboxes.
*   **Objectifs :** Vol massif de portefeuilles de cryptomonnaies, clés API (AWS, OpenAI, GitHub, GitLab), jetons 1Password, clés SSH et profils de navigation.
*   **Exfiltration :** Les données collectées sont transmises via des bots Telegram.
*   **Techniques d'évasion :** Utilisation de versions « propres » initiales pour bâtir une réputation, découpage des chaînes de caractères en mémoire et recours à des API natives (comme `vscode.env.clipboard`) pour éviter les alertes liées aux accès réseau ou fichiers.

**Vulnérabilités :**
*   Aucun identifiant CVE n'est associé, car il s'agit d'une **supply chain attack** exploitant la confiance accordée aux extensions tierces et l'absence d'analyse comportementale dynamique approfondie sur les places de marché.

**Recommandations :**
*   **Désinstallation immédiate :** Supprimer les extensions suspectes et vérifier les graphes de dépendances de vos projets.
*   **Rotation des secrets :** Considérer comme compromis tous les jetons, clés API, clés SSH et phrases de récupération (seed phrases) présents sur les machines où ces extensions ont été installées.
*   **Surveillance système :** Mettre en place des alertes sur l'exécution inhabituelle de processus tels que `cscript`, `mshta`, `cmd`, `curl` ou `powershell` au sein de l'environnement de développement.
*   **Vigilance accrue :** Limiter l'installation d'extensions provenant de sources non vérifiées et privilégier des outils audités.

---
[Source](https://thehackernews.com/2026/08/solidity-pro-vs-code-extensions-steal.html){:target="_blank"}
