---
title: 'LangGraph Flaw Chain Exposes Self-Hosted AI Agents to Remote Code Execution'
date: 2026-06-12
permalink: /posts/2026/06/12/langgraph-flaw-chain-exposes-self-hosted-ai-agents-to-remote-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans LangGraph : Risque d'exécution de code à distance

Trois vulnérabilités ont été identifiées dans le framework open-source LangGraph, utilisé pour le développement d'agents IA. Bien que les déploiements gérés par LangSmith ne soient pas affectés, les instances auto-hébergées sont vulnérables, notamment via une chaîne d'exploitation permettant l'exécution de code à distance (RCE).

#### Points clés
*   **Chaîne d'attaque :** La combinaison d'une injection SQL et d'une désérialisation non sécurisée permet à un attaquant de corrompre les points de contrôle (checkpoints) et de prendre le contrôle du serveur.
*   **Vecteur :** L'attaque cible principalement les déploiements utilisant SQLite ou Redis si l'entrée des filtres est contrôlée par l'utilisateur.

#### Vulnérabilités identifiées
*   **CVE-2025-67644 (Score 7.3) :** Injection SQL dans l'implémentation `langgraph-checkpoint-sqlite` via les clés de métadonnées.
*   **CVE-2026-28277 (Score 6.8) :** Désérialisation non sécurisée (msgpack) dans `langgraph`, permettant l'exécution de code lors du chargement de points de contrôle manipulés.
*   **CVE-2026-27022 (Score 6.5) :** Injection de requête RediSearch dans `@langchain/langgraph-checkpoint-redis` contournant les contrôles d'accès.

#### Recommandations
*   **Mise à jour immédiate :** Installer les correctifs les plus récents fournis par les mainteneurs de LangGraph.
*   **Sécurisation des accès :** Implémenter une authentification robuste pour tous les serveurs auto-hébergés.
*   **Principe du moindre privilège :** Restreindre strictement les accès des agents IA aux ressources critiques et aux secrets.
*   **Segmentation réseau :** Isoler les serveurs hébergeant les agents IA pour limiter les mouvements latéraux en cas de compromission.
*   **Gestion des secrets :** Éviter l'utilisation de secrets statiques à longue durée de vie.

---
[Source](https://thehackernews.com/2026/06/langgraph-flaw-chain-exposes-self.html){:target="_blank"}
