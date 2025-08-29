---
title: 'Windsurf MCP Integration: Missing Security Controls Put Users at Risk'
date: 2025-08-29
permalink: /posts/2025/08/29/windsurf-mcp-integration-missing-security-controls-put-users-at-risk/
tags:
- veille-cyber
- zerodaysfans
---
### Sécurité des agents IA : L'intégration MCP de Windsurf présente des lacunes

L'intégration des agents IA avec des serveurs MCP (Model-Centric Processing) soulève des préoccupations importantes en matière de sécurité, particulièrement lorsqu'elle est utilisée localement. Un examen de l'intégration MCP de Windsurf révèle une absence de contrôles de sécurité fondamentaux, autorisant les invocations d'outils en mode automatique sans intervention humaine par défaut. Cette configuration, qualifiée de "YOLO mode", est jugée dangereuse compte tenu de la maturité encore limitée de l'écosystème MCP et de la tendance croissante à la surconfiance dans les sorties des grands modèles linguistiques (LLM).

L'article démontre qu'une simple manipulation des instructions par un adversaire, via un commentaire de code par exemple, peut détourner le comportement de l'agent. Ce dernier peut alors être amené à exécuter des actions sensibles, comme la publication d'un message d'un canal Slack privé vers un canal public, sans aucune confirmation de l'utilisateur. Ces instructions malveillantes peuvent être dissimulées dans du code, des fichiers ou sur des sites web visités, permettant ainsi le détournement de l'agent.

Face à l'impossibilité actuelle de solutionner le problème de l'injection de prompts, l'approbation humaine des actions critiques est présentée comme la meilleure stratégie d'atténuation. Bien que les dialogues d'approbation puissent être perçus comme ennuyeux, ils restent la méthode la plus efficace pour gérer les attaques et les hallucinations. Il est souligné que les utilisateurs doivent pouvoir définir des étapes où ils souhaitent conserver le contrôle, adaptées à leur tolérance au risque et aux politiques organisationnelles.

**Points clés :**

*   **Invocation automatique d'outils sans supervision :** L'intégration MCP de Windsurf permet aux agents d'exécuter des outils automatiquement, sans nécessiter de confirmation utilisateur par défaut.
*   **Vulnérabilité aux attaques par injection de prompts :** Des instructions malveillantes cachées dans des sources de données peuvent détourner le comportement de l'agent, entraînant des actions non désirées.
*   **Risque de fuite d'informations et d'actions non autorisées :** Des scénarios comme la publication de messages privés dans des canaux publics illustrent le potentiel de préjudice.
*   **Nécessité de contrôles configurables :** La possibilité de désactiver des outils individuels ou de définir un niveau de confirmation par outil est cruciale pour la gestion des risques.

**Vulnérabilités :**

*   Manque de contrôles par défaut pour l'invocation d'outils (pas de confirmation humaine obligatoire).
*   Absence d'options pour suggérer des appels d'outils à l'utilisateur pour revue avant exécution.
*   Désactivation d'outils individuels en tant que seule option de configuration de sécurité existante à l'origine.

**Recommandations :**

*   Permettre aux utilisateurs de configurer quels outils doivent être désactivés, approuvés automatiquement, ou nécessitent une intervention humaine lors de l'ajout d'un nouveau serveur MCP.
*   Offrir des options de configuration détaillées pour chaque outil individuel d'un serveur MCP, à l'instar de ce que proposent d'autres fournisseurs.
*   Favoriser une approche d'"humain au contrôle de l'IA" plutôt que l'inverse.

---
[Source](https://embracethered.com/blog/posts/2025/windsurf-dangers-lack-of-security-controls-for-mcp-server-tool-invocation/){:target="_blank"}
