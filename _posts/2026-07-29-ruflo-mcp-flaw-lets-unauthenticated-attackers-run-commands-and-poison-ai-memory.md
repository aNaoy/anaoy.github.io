---
title: 'Ruflo MCP Flaw Lets Unauthenticated Attackers Run Commands and Poison AI Memory'
date: 2026-07-29
permalink: /posts/2026/07/29/ruflo-mcp-flaw-lets-unauthenticated-attackers-run-commands-and-poison-ai-memory/
tags:
- veille-cyber
- hackernews
---
### RufRoot : Une faille critique dans la plateforme Ruflo permet l'exécution de code à distance

Une vulnérabilité majeure a été découverte dans **Ruflo**, une plateforme d'orchestration d'agents IA, permettant à des attaquants non authentifiés de prendre le contrôle total des instances exposées.

#### Points clés
* **Nature de la faille :** Exposition non sécurisée du pont « Model Context Protocol » (MCP).
* **Impact :** Exécution de code à distance (RCE), vol de clés API LLM, espionnage des conversations et empoisonnement de la mémoire persistante de l'IA (AgentDB).
* **Vecteur d'attaque :** Une simple requête HTTP POST sur le port 3001 permet d'exécuter des commandes système arbitraires.

#### Vulnérabilité
* **CVE-2026-59726** (Score CVSS : 10.0 - Sévérité maximale).
* Concerne toutes les versions antérieures à la **3.16.3**.
* La configuration par défaut (`docker-compose.yml`) liait le pont MCP et la base de données MongoDB à toutes les interfaces réseau (0.0.0.0) sans authentification.

#### Recommandations
* **Mise à jour immédiate :** Passer à la version **3.16.3** ou supérieure.
* **Sécurisation réseau :** Fermer les ports 3001 et 27017 s'ils sont accessibles depuis l'extérieur.
* **Rotation des secrets :** Considérer toutes les clés API LLM utilisées par la plateforme comme compromises et les révoquer/régénérer.
* **Audit et nettoyage :**
    * Vérifier l'intégrité de la base MongoDB et de la base de connaissances (AgentDB) pour détecter des entrées malveillantes ou des motifs « empoisonnés ».
    * Reconstruire les conteneurs à partir d'images propres.
    * Rechercher des signes de persistance (backdoors) dans le répertoire `/app`.

---
[Source](https://thehackernews.com/2026/07/ruflo-mcp-flaw-lets-unauthenticated.html){:target="_blank"}
