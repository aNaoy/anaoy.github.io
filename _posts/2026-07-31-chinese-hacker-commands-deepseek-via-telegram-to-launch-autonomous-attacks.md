---
title: 'Chinese Hacker Commands DeepSeek via Telegram to Launch Autonomous Attacks'
date: 2026-07-31
permalink: /posts/2026/07/31/chinese-hacker-commands-deepseek-via-telegram-to-launch-autonomous-attacks/
tags:
- veille-cyber
- hackernews
---
### Attaques cybernétiques autonomes orchestrées par IA via Telegram

Des chercheurs de l'unité Unit 42 de Palo Alto Networks ont identifié un acteur malveillant utilisant le framework open-source **Hermes Agent** et le modèle d'IA **DeepSeek** pour mener des attaques cybernétiques autonomes. Après une instruction initiale via Telegram, l'agent est capable de scanner Internet, d'identifier des systèmes vulnérables et d'exécuter des exploits sans intervention humaine. Bien que l'outil ait ciblé plus de 460 systèmes, le taux de réussite a été limité par des configurations de sécurité empêchant l'exploitation automatique.

**Points clés :**
*   **Mode opératoire :** Utilisation d'un agent IA capable d'effectuer des recherches sur FOFA, de tester des exploits et de pivoter en cas d'échec.
*   **Fuite de données :** L'opérateur a compromis sa propre opération en exposant par erreur, via un serveur HTTP local, des fichiers sensibles incluant des clés API, des listes de cibles et des logs de session.
*   **Infrastructure :** Le framework Hermes Agent permet une exécution autonome, planifiée et contrôlée à distance via Telegram.

**Vulnérabilités exploitées ou ciblées :**
*   **Langflow :** CVE-2026-33017 (Injection de code).
*   **n8n :** CVE-2026-21858 (Accès fichiers non authentifié) couplée à CVE-2025-68613 (Injection d'expression).
*   **Marimo :** CVE-2026-39987 (Exécution de code à distance).
*   **Citrix NetScaler :** CVE-2026-3055 (Fuite de mémoire).

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs pour Langflow (v1.9.0+), n8n (v1.121.1+), Marimo (v0.23.0+) et les versions corrigées pour NetScaler ADC/Gateway.
*   **Gestion des accès :** Restreindre strictement l'accès public aux interfaces de flux de travail, aux notebooks et aux endpoints d'API.
*   **Sécurisation des outils IA :** Auditer les configurations des agents autonomes et des environnements de développement pour éviter l'exposition accidentelle de données sensibles ou d'outils d'exploitation via des serveurs HTTP mal configurés.

---
[Source](https://thehackernews.com/2026/07/chinese-hacker-commands-deepseek-via.html){:target="_blank"}
