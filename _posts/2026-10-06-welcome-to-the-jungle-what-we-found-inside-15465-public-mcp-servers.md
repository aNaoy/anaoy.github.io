---
title: 'Welcome to the Jungle: What We Found Inside 15,465 Public MCP Servers'
date: 2026-10-06
permalink: /posts/2026/10/06/welcome-to-the-jungle-what-we-found-inside-15465-public-mcp-servers/
tags:
- veille-cyber
- hackernews
---
### Risques de sécurité et absence de gouvernance dans l'écosystème MCP

Le protocole MCP (*Model Context Protocol*), conçu pour unifier la connexion des outils d'IA aux données, souffre d'un manque critique de mécanismes de sécurité et de gouvernance. Une analyse de 15 465 serveurs MCP publics a révélé une absence totale de contrôle, exposant les entreprises à des risques majeurs via des agents d'IA connectés.

**Points clés :**
*   **Absence de filtrage :** Aucune plateforme de référence MCP ne propose de vérification (type *bouncer*), permettant à quiconque de publier des serveurs sans validation.
*   **Divergence code/exécution :** Le code publié sur un dépôt public ne garantit pas ce qui est réellement exécuté sur le serveur distant.
*   **Risques de souveraineté et confidentialité :** 15,6 % des serveurs sont hébergés hors des États-Unis (notamment en Chine et en Russie), entraînant une fuite potentielle de données vers des juridictions non approuvées.
*   **Infrastructures précaires :** 0,45 % des serveurs utilisent des tunnels grand public (ex: ngrok) depuis des machines personnelles, et 2,3 % utilisent des domaines expirés, facilement détournables par des attaquants pour intercepter des requêtes.

**Vulnérabilités :**
*   **Injection de prompts :** Le rapport souligne le risque d'attaques par injection de commandes permettant de manipuler les agents.
*   **Détournement de domaines :** L'utilisation de domaines expirés permet à un tiers de prendre le contrôle d'identités de serveurs existantes et de récupérer les flux de données associés.

**Recommandations :**
*   **Vérification rigoureuse :** En l'absence de certification par les places de marché, les entreprises doivent effectuer elles-mêmes un audit approfondi de tout serveur MCP avant intégration.
*   **Application de politiques de sécurité :** Intégrer les connexions MCP aux politiques de gouvernance existantes (Zero Trust, IAM granulaire, audit de la chaîne d'approvisionnement).
*   **Contrôle de l'origine :** Exiger la signature du code et la vérification de l'origine des serveurs, car le protocole seul ne protège pas contre les serveurs malveillants ou compromise.

---
[Source](https://thehackernews.com/2026/10/welcome-to-jungle-what-we-found-inside.html){:target="_blank"}
