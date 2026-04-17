---
title: 'Heres What Agentic AI Can Do With Have I Been Pwneds APIs'
date: 2026-04-17
permalink: /posts/2026/04/17/heres-what-agentic-ai-can-do-with-have-i-been-pwneds-apis/
tags:
- veille-cyber
- troyhunt
---
### L'IA agentique au service de l'analyse des fuites de données

L'intégration des APIs de *Have I Been Pwned* (HIBP) via le protocole MCP (Model Context Protocol) permet désormais aux agents d'IA d'interagir directement avec les données de violations de sécurité. Cette approche transforme radicalement l'analyse des menaces, rendant les informations complexes accessibles sans compétences techniques avancées.

**Points clés :**
*   **Protocol MCP :** HIBP propose un serveur MCP permettant à des outils comme Claude, ChatGPT ou GitHub Copilot d'interroger en temps réel les bases de données de fuites.
*   **Agents autonomes :** L'utilisation d'agents (ex: OpenClaw) permet d'automatiser le filtrage, l'analyse contextuelle et la corrélation de données complexes (ex: identifier quels employés sont touchés par une fuite spécifique).
*   **Visibilité sur les "Stealer Logs" :** L'analyse permet de détecter quels services tiers (sites personnels, jeux, plateformes tierces) sont utilisés avec des adresses professionnelles par les employés, exposant ainsi l'entreprise à des risques via des identifiants réutilisés.
*   **Automatisation :** Il est possible de configurer des tâches planifiées pour surveiller des domaines et recevoir des alertes automatisées ou générer des rapports exécutifs.

**Vulnérabilités associées :**
*   **Usage d'emails professionnels sur des plateformes tierces :** Augmente la surface d'attaque en cas de fuite sur un service non lié à l'entreprise.
*   **Risque lié aux infostealers :** L'infection d'appareils (personnels ou professionnels) utilisés pour se connecter aux ressources de l'entreprise constitue une menace majeure.
*   **Note sur les CVE :** L'article ne mentionne aucune vulnérabilité logicielle spécifique avec un identifiant CVE, se concentrant sur les risques liés aux comportements humains et à la gestion des fuites de données.

**Recommandations :**
*   **Surveillance proactive :** Utiliser les outils d'IA pour identifier les comptes professionnels compromis et restreindre l'usage de ces derniers sur des sites tiers.
*   **Sensibilisation :** Mener des actions de prévention auprès des employés utilisant leurs adresses de travail sur des services récréatifs (ex: Steam).
*   **Gestion des accès :** Appliquer une politique stricte de rotation des clés API HIBP et sécuriser les secrets utilisés par les agents d'IA pour interroger les services.
*   **Automatisation de la remédiation :** Mettre en place des flux de travail (via des agents) pour automatiser la détection des fuites et la génération de rapports d'impact.

---
[Source](https://www.troyhunt.com/heres-what-agentic-ai-can-do-with-have-i-been-pwneds-apis/){:target="_blank"}
