---
title: 'Compromised jscrambler 8.14.0 npm Release Drops Rust Infostealer During Install'
date: 2026-07-11
permalink: /posts/2026/07/11/compromised-jscrambler-8140-npm-release-drops-rust-infostealer-during-install/
tags:
- veille-cyber
- hackernews
---
### Compromission de la supply chain : Le paquet npm jscrambler injecte un infostealer

La version 8.14.0 du paquet npm `jscrambler` a été compromise, intégrant un script malveillant qui s'exécute automatiquement lors de l'installation via un hook `preinstall`. Ce paquet injecte un *infostealer* écrit en Rust, conçu pour dérober des données sensibles sur Windows, macOS et Linux.

**Points clés :**
* **Propagation :** Le code malveillant n'apparaît pas dans le dépôt GitHub officiel, suggérant une compromission directe du compte npm ou du pipeline de build.
* **Cibles :** L'outil exfiltre des identifiants cloud (AWS, Azure, GCP), des portefeuilles de cryptomonnaies, des mots de passe de gestionnaires (Bitwarden), des sessions (Discord, Slack, Telegram) et des clés API d'outils de développement IA (Cursor, VS Code, etc.).
* **Capacités avancées :** Le malware assure sa persistance via des tâches planifiées ou des *LaunchAgents* et, sous Linux, tente de charger un programme eBPF au niveau du noyau pour maintenir un accès privilégié.
* **Contexte :** Bien que npm 12 désactive désormais ces scripts par défaut, les clients plus anciens restent vulnérables.

**Vulnérabilités :**
* Il n'existe pas de CVE spécifique pour cette attaque, car elle repose sur une compromission de la chaîne d'approvisionnement (*supply chain attack*) et l'usage détourné des hooks d'installation natifs de npm.

**Recommandations :**
1. **Suppression immédiate :** Éliminez la version 8.14.0 des `lockfiles`, des caches npm et des environnements CI/CD. Mettez à jour vers la version 8.15.0 ou revenez à la 8.13.0.
2. **Audit de sécurité :** Si la version 8.14.0 a été installée, considérez que tous les secrets accessibles par la machine (clés API, tokens, sessions) sont compromis. Procédez à une rotation immédiate de ces accès.
3. **Analyse forensique :** Recherchez des processus suspects dans le répertoire temporaire système, vérifiez les tâches planifiées sur Windows et les `LaunchAgents` sur macOS créés depuis le 11 juillet 2026.
4. **Filtrage réseau :** Bloquez les adresses IP de commande et contrôle (C2) identifiées : `37.27.122.124` et `57.128.246.79`.

---
[Source](https://thehackernews.com/2026/07/compromised-jscrambler-8140-npm-release.html){:target="_blank"}
