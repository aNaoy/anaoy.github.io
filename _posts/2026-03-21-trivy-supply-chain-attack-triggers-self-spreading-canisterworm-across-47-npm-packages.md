---
title: 'Trivy Supply Chain Attack Triggers Self-Spreading CanisterWorm Across 47 npm Packages'
date: 2026-03-21
permalink: /posts/2026/03/21/trivy-supply-chain-attack-triggers-self-spreading-canisterworm-across-47-npm-packages/
tags:
- veille-cyber
- hackernews
---
### Propagation virale via CanisterWorm : Attaque de la supply chain npm

Une campagne d'attaque contre l'outil de scan Trivy a permis au groupe cybercriminel **TeamPCP** de compromettre plusieurs paquets npm et de déployer un ver auto-propagateur baptisé **CanisterWorm**.

**Points clés :**
*   **Mécanisme décentralisé :** Le malware utilise des *canisters* (smart contracts) de la blockchain Internet Computer (ICP) comme "dead drop" pour récupérer dynamiquement les adresses de serveurs C2 (Command & Control), rendant l'infrastructure très difficile à neutraliser.
*   **Propagation autonome :** Contrairement à la première phase nécessitant une intervention manuelle, les nouvelles itérations du ver scannent l'environnement de la victime pour exfiltrer des jetons (tokens) d'authentification npm, permettant au malware de publier automatiquement des versions infectées des paquets sur le registre.
*   **Persistance :** Le ver s'installe via une tâche `systemd` masquée sous le nom de service "pgmon" (simulant un outil PostgreSQL) pour garantir son exécution permanente.
*   **Cible :** 47 paquets npm ont été identifiés, incluant des composants sous les scopes `@EmilGroup` et `@opengov`, ainsi que des paquets spécifiques comme `@teale.io/eslint-config`.

**Vulnérabilités exploitées :**
*   **Abus de supply chain :** Vol de jetons d'authentification npm pour compromettre des comptes de développeurs ou des pipelines CI/CD.
*   **Scripts post-installation :** Exécution arbitraire de code malveillant lors de l'installation de paquets via `postinstall` hooks.
*   *Note : Aucune CVE spécifique n'est associée à cette campagne, car elle repose sur une utilisation malveillante de fonctionnalités légitimes (tokens npm, systemd, scripts npm).*

**Recommandations :**
*   **Audit des jetons :** Révoquer et renouveler immédiatement les jetons d'accès npm utilisés dans les environnements de développement et les pipelines CI/CD.
*   **Surveillance :** Inspecter les services `systemd` suspects (ex: "pgmon") et vérifier les journaux d'exécution des scripts `postinstall` dans les dépendances `package.json`.
*   **Principe du moindre privilège :** Restreindre les permissions des jetons npm aux seules actions nécessaires (lecture seule si possible) et éviter de stocker des jetons avec des droits de publication sur des machines non sécurisées.
*   **Mise à jour :** Auditer les dépendances npm listées comme compromises et forcer la mise à jour vers des versions saines après vérification.

---
[Source](https://thehackernews.com/2026/03/trivy-supply-chain-attack-triggers-self.html){:target="_blank"}
