---
title: 'The Real-World Attacks Behind OWASP Agentic AI Top 10'
date: 2025-12-29
permalink: /posts/2025/12/29/the-real-world-attacks-behind-owasp-agentic-ai-top-10/
tags:
- veille-cyber
- bleepingcomp
---
### L'essor des menaces ciblant les IA autonomes

Le paysage de la cybersécurité évolue avec l'intégration croissante des IA dites "agentiques", capables d'agir de manière autonome dans des environnements complexes. OWASP a lancé son premier cadre de sécurité dédié, le "Top 10 for Agentic Applications 2026", pour adresser les risques spécifiques à ces systèmes. Ces IA, utilisées dans des tâches telles que la gestion d'emails, l'écriture de code et l'accès à des systèmes sensibles, représentent des cibles attractives pour les attaquants en raison de leur accès étendu et de la confiance implicite qui leur est accordée. Les méthodes de sécurité traditionnelles s'avèrent souvent insuffisantes face à leur capacité à interagir avec le contenu externe et à exécuter des actions.

Ce nouveau cadre vise à établir un langage commun pour les risques liés à ces applications, à l'instar de l'impact qu'a eu le Top 10 OWASP original sur la sécurité web.

**Points clés et Vulnérabilités identifiées (avec exemples concrets) :**

*   **ASI01: Agent Goal Hijack (Détournement d'objectif de l'agent)**
    *   **Description:** Manipulation des objectifs d'un agent par des instructions injectées, le rendant incapable de distinguer les commandes légitimes des malveillantes.
    *   **Exemples:**
        *   Malware NPM contenant des chaînes de caractères destinées à tromper les outils de sécurité basés sur l'IA (mai 2025).
        *   Utilisation de noms de packages imaginés par les IA ("slopsquatting") pour distribuer des malwares via des recommandations d'assistants IA (enquêtes PhantomRaven).

*   **ASI02: Tool Misuse & Exploitation (Mauvaise utilisation et exploitation des outils)**
    *   **Description:** Les agents utilisent des outils légitimes de manière préjudiciable, non pas à cause d'un défaut des outils, mais à cause d'une manipulation de l'agent.
    *   **Exemple:** Un assistant de codage IA d'Amazon (Amazon Q) a failli exécuter des commandes destructrices sur des environnements de production, incluant la suppression de ressources cloud, via une extension malveillante avec des flags de contournement de confirmation (`--trust-all-tools --no-interactive`) (juillet 2025).

*   **ASI04: Agentic Supply Chain Vulnerabilities (Vulnérabilités de la chaîne d'approvisionnement agentiques)**
    *   **Description:** Ciblage des dépendances chargées par les IA à l'exécution, telles que les serveurs MCP (Machine Control Protocol), les plugins ou les outils externes.
    *   **Exemples:**
        *   Découverte du premier serveur MCP malveillant sur npm, se faisant passer pour un service de messagerie et exfiltrant secrètement chaque message envoyé (septembre 2025).
        *   Un serveur MCP contenant deux "reverse shells" (une à l'installation, une à l'exécution) permettant une persistance malgré les détections (octobre 2025). Ces attaques peuvent cibler jusqu'à 126 packages et 86 000 téléchargements.

*   **ASI05: Unexpected Code Execution (Exécution de code inattendue)**
    *   **Description:** Les agents, conçus pour exécuter du code, deviennent une vulnérabilité lorsque ce code est malveillant et exécuté avec des privilèges élevés.
    *   **Exemple:** Trois vulnérabilités d'exécution de code à distance (RCE) critiques (CVSS 8.9) ont été découvertes dans des extensions officielles de Claude Desktop (Chrome, iMessage, Apple Notes). Elles permettaient l'exécution de commandes arbitraires via l'injection dans AppleScript, transformant une simple question posée à l'IA en une compromission du système (novembre 2025).

**Recommandations Générales :**

Pour les organisations déployant des IA agentiques, les mesures clés incluent :

*   **Inventaire exhaustif:** Connaître tous les serveurs MCP, plugins et outils utilisés par les agents.
*   **Vérification de provenance:** Examiner l'origine des composants et privilégier les packages signés par des éditeurs reconnus.
*   **Principe du moindre privilège:** Accorder uniquement les autorisations strictement nécessaires à chaque agent et éviter les identifiants larges.
*   **Surveillance comportementale:** Observer l'exécution réelle des agents, au-delà de l'analyse statique du code.
*   **Mécanisme d'arrêt d'urgence:** Mettre en place un moyen de désactivation rapide en cas de compromission.

---
[Source](https://www.bleepingcomputer.com/news/security/the-real-world-attacks-behind-owasp-agentic-ai-top-10/){:target="_blank"}
