---
title: 'Microsoft Warns Poisoned MCP Tool Descriptions Can Make AI Agents Leak Data'
date: 2026-06-30
permalink: /posts/2026/06/30/microsoft-warns-poisoned-mcp-tool-descriptions-can-make-ai-agents-leak-data/
tags:
- veille-cyber
- hackernews
---
### Risques de sécurité : Empoisonnement des descriptions d'outils MCP pour les agents IA

Les agents IA capables d'exécuter des actions autonomes via le protocole MCP (*Model Context Protocol*) sont vulnérables à des attaques par "empoisonnement de description". En manipulant la description textuelle d'un outil connecté, un attaquant peut forcer l'IA à exfiltrer des données ou effectuer des actions malveillantes tout en conservant une apparence de fonctionnement légitime.

**Points clés :**
* **Vecteur d'attaque :** Le protocole MCP utilise des descriptions textuelles pour indiquer à l'IA comment utiliser un outil. Un attaquant insère des instructions malveillantes dans cette description, que l'agent interprète comme des commandes système.
* **Absence d'alerte :** Comme l'agent utilise les permissions légitimes de l'utilisateur et des outils approuvés, les actions malveillantes ne déclenchent généralement pas de mécanismes de sécurité classiques.
* **Surface d'exposition :** Le problème réside dans la confusion entre les données et les instructions au sein de la mémoire de l'agent.

**Vulnérabilités :**
Il n'existe pas de CVE unique, car il s'agit d'une faille conceptuelle liée à l'architecture des applications agents (référencée par l'OWASP sous le terme **Agentic Supply Chain Vulnerabilities**). Cette vulnérabilité est confirmée par le benchmark **MCPTox**, démontrant un taux de succès élevé (jusqu'à 72,8 %) pour ces injections.

**Recommandations :**
* **Gestion de la supply chain :** Restreindre l'utilisation des outils aux éditeurs approuvés et limiter les accès au strict nécessaire.
* **Contrôle des modifications :** Traiter chaque modification de description d'outil comme un changement de code source et soumettre ces descriptions à une revue de sécurité.
* **Human-in-the-loop :** Exiger une validation humaine systématique pour les actions critiques (transferts financiers, accès à des données sensibles, modification de paramètres de compte).
* **Surveillance proactive :** Établir une ligne de base du comportement normal de chaque agent et logger l'ensemble de ses actions pour détecter des appels anormaux ou des exfiltrations de données.
* **Principe du moindre pouvoir :** Appliquer le "moindre privilège" mais aussi la "moindre agence" : ne pas autoriser un agent à agir sans supervision constante, même avec des accès limités.

---
[Source](https://thehackernews.com/2026/06/microsoft-warns-poisoned-mcp-tool.html){:target="_blank"}
