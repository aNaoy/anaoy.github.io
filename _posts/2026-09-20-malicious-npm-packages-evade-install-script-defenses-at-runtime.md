---
title: 'Malicious npm packages evade install-script defenses at runtime'
date: 2026-09-20
permalink: /posts/2026/09/20/malicious-npm-packages-evade-install-script-defenses-at-runtime/
tags:
- veille-cyber
- bleepingcomp
---
### Contournement des défenses npm par exécution différée

Une campagne malveillante visant l'écosystème npm utilise le paquet `indexed-btree` (et neuf autres bibliothèques similaires) pour infiltrer les chaînes d'approvisionnement logicielles. Contrairement aux attaques classiques, ce malware contourne les mesures de sécurité récentes de npm — qui bloquent les scripts d'installation suspects — en dissimulant sa charge utile dans une méthode de bibliothèque légitime (`BTree.prototype.set()`). Le code malveillant ne s'exécute qu'au moment de l'utilisation de la bibliothèque par l'application, échappant ainsi aux outils d'analyse statique.

**Points clés :**
* **Méthode d'infection :** Le code malveillant est activé lors de l'appel à une fonction courante du paquet, évitant ainsi de déclencher les mécanismes d'approbation liés aux scripts d'installation (`preinstall`, `postinstall`).
* **Comportement malveillant :** Une fois actif, le malware exfiltre des données système via Slack/Telegram et interroge un contrat intelligent Ethereum sur le réseau Sepolia pour recevoir des commandes de contrôle (C2) et des charges utiles de second niveau.
* **Complexité :** Les attaquants ont créé des dépôts GitHub factices avec un historique de commits crédible pour paraître légitimes. 
* **Impact :** Des millions de téléchargements enregistrés pour la suite de paquets identifiée.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, car il s'agit d'un abus de logique applicative (l'exécution malveillante est masquée dans le comportement normal du programme). La vulnérabilité réside dans la confiance accordée au code importé et dans l'insuffisance de l'analyse statique seule.

**Recommandations :**
* **Analyse comportementale :** Ne pas se limiter au scan lors de l'installation ; mettre en place une surveillance de l'activité réseau et système lors de l'exécution (runtime).
* **Remédiation immédiate :** Si l'un des paquets listés (ex: `indexed-btree`, `btree-core`, `btree-leaderboard`) a été utilisé, il est impératif de réinitialiser tous les secrets (clés API, identifiants) et de restaurer l'environnement de développement à partir d'une sauvegarde propre.
* **Audit des dépendances :** Vérifier rigoureusement les nouvelles dépendances ajoutées aux projets, même celles ayant un historique de commits apparent.

---
[Source](https://www.bleepingcomputer.com/news/security/malicious-npm-packages-evade-install-script-defenses-at-runtime/){:target="_blank"}
