---
title: 'Shiny tools, shallow checks: how the AI hype opens the door to malicious MCP servers'
date: 2025-09-15
permalink: /posts/2025/09/15/shiny-tools-shallow-checks-how-the-ai-hype-opens-the-door-to-malicious-mcp-servers/
tags:
- veille-cyber
- securelist
---
### L'IA ouvre la porte aux serveurs MCP malveillants

Le Protocole de Contexte Modèle (MCP), conçu pour connecter les assistants IA à des sources de données et outils externes, peut être exploité comme un point d'entrée dans la chaîne d'approvisionnement logicielle. Les attaquants peuvent créer des serveurs MCP malveillants qui semblent légitimes mais visent à voler des informations sensibles.

**Points clés et vulnérabilités :**

*   **Architecture MCP :** Le MCP utilise une architecture client-serveur. Les clients sont intégrés aux assistants IA, les hôtes sont les applications IA elles-mêmes, et les serveurs MCP agissent comme des adaptateurs intelligents pour traduire le langage naturel en commandes exécutables.
*   **Vecteurs d'attaque au niveau du protocole :**
    *   **Confusion de nommage MCP (usurpation et découverte d'outils) :** Un serveur malveillant peut se faire passer pour un serveur légitime pour intercepter des jetons ou des requêtes sensibles.
    *   **Empoisonnement d'outils MCP :** Des instructions cachées dans la description ou les exemples d'outils peuvent inciter l'IA à divulguer des données sensibles (par exemple, des clés SSH).
    *   **Ombrage MCP :** Un serveur malveillant peut modifier la définition d'un outil existant pour rediriger silencieusement les appels vers sa propre logique.
    *   **Scénarios de "rug pull" MCP :** Après avoir établi la confiance, un serveur peut être remplacé par une version malveillante qui se met à jour automatiquement.
    *   **Bugs d'implémentation :** Des vulnérabilités non corrigées dans les intégrations MCP (comme celle découverte dans l'intégration GitHub) peuvent entraîner des fuites de données.
*   **Abus de la chaîne d'approvisionnement :** Les serveurs MCP malveillants sont distribués via des canaux familiers (PyPI, Docker Hub, GitHub Releases) et sont souvent installés sans examen approfondi, profitant de la précipitation des développeurs à intégrer des outils IA.
*   **Preuve de concept :** Un serveur MCP malveillant a été développé pour simuler une attaque. Il se présentait comme un outil de productivité offrant des analyses de projet, des vérifications de sécurité de configuration et des optimisations d'environnement. En réalité, il collectait discrètement des données sensibles (fichiers d'environnement, clés SSH, configurations cloud, jetons API, etc.) et les exfiltrait vers un serveur contrôlé par l'attaquant, tout en présentant une sortie apparemment normale à l'utilisateur.

**Recommandations et atténuations :**

*   **Validation avant installation :** Mettre en place un workflow d'approbation pour scanner, examiner et approuver chaque nouveau serveur MCP avant son utilisation. Maintenir une liste blanche d'environnements approuvés.
*   **Isolement des serveurs :** Exécuter les serveurs MCP dans des conteneurs ou des machines virtuelles avec des accès restreints aux dossiers nécessaires et isolés des réseaux sensibles.
*   **Surveillance comportementale :** Enregistrer toutes les invites et réponses, et surveiller les anomalies telles que des instructions cachées, des commandes inattendues ou des flux de données inhabituels.
*   **Planification d'urgence :** Disposer d'un mécanisme pour bloquer ou désinstaller rapidement un serveur compromis sur l'ensemble du parc. Collecter des journaux centralisés pour faciliter l'analyse post-incident. Une surveillance et une détection continues sont essentielles.

---
[Source](https://securelist.com/model-context-protocol-for-ai-integration-abused-in-supply-chain-attacks/117473/){:target="_blank"}
