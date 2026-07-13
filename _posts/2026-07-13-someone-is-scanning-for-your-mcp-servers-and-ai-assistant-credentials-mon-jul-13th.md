---
title: 'Someone Is Scanning for Your MCP Servers and AI Assistant Credentials, (Mon, Jul 13th)'
date: 2026-07-13
permalink: /posts/2026/07/13/someone-is-scanning-for-your-mcp-servers-and-ai-assistant-credentials-mon-jul-13th/
tags:
- veille-cyber
- sans-isc
---
### Recrudescence des scans automatisés visant les infrastructures d'IA

Des analyses récentes révèlent une campagne de scan internet à grande échelle visant spécifiquement les composants liés aux agents d'IA. Les attaquants ne cherchent plus seulement des vulnérabilités classiques, mais ciblent activement les serveurs **Model Context Protocol (MCP)**, les fichiers de configuration d'assistants de codage et les endpoints de modèles de langage (LLM) mal sécurisés.

#### Points clés
*   **Automatisation ciblée :** Les scanners effectuent des handshakes réels (via JSON-RPC 2.0 pour MCP) pour vérifier si un serveur répond, permettant ainsi d'énumérer les outils et accès connectés à l'IA.
*   **Extraction de secrets :** Les attaquants recherchent des fichiers de configuration (`.claude/mcp.json`, `.cursor/mcp.json`, `.credentials.json`) exposés par erreur dans les répertoires web des serveurs.
*   **Recherche d'endpoints LLM :** Les endpoints comme `/v1/models` (OpenAI-compatible) ou `/api/tags` (Ollama) sont sondés pour identifier des instances de modèles accessibles sans authentification, offrant des vecteurs de pivot ou des ressources de calcul gratuites.
*   **Vecteur SSRF associé :** Les scanners combinent ces recherches avec des tentatives de SSRF (Server-Side Request Forgery) pour interroger les services de métadonnées cloud (GCP, AWS) afin de dérober des jetons de service.

#### Vulnérabilités
Bien qu'il s'agisse de campagnes d'exploitation plutôt que de vulnérabilités logicielles spécifiques avec CVE, les risques critiques sont les suivants :
*   **Exposition non intentionnelle :** Déploiement de fichiers de configuration sensibles dans des répertoires accessibles au public.
*   **Défaut d'authentification :** Serveurs MCP et endpoints LLM exposés directement sur Internet sans contrôle d'accès.
*   **SSRF (Server-Side Request Forgery) :** Les outils d'IA dotés de fonctionnalités "fetch" (récupération d'URL) peuvent être détournés pour accéder aux métadonnées internes des instances cloud (ex: `169.254.169.254`).

#### Recommandations de sécurité
*   **Audit des logs :** Rechercher dans les journaux d'accès les requêtes `POST /mcp`, `GET /sse`, `/v1/models` ou `/api/tags`.
*   **Protection des fichiers sensibles :** S'assurer qu'aucun répertoire ou fichier lié aux assistants (type `.claude/`, `.cursor/`, `.vscode/`) n'est accessible via le serveur web.
*   **Cloisonnement réseau :** Restreindre l'accès aux serveurs MCP et aux endpoints LLM pour qu'ils ne soient jamais exposés sur des interfaces publiques.
*   **Durcissement cloud :** Implémenter l'imposition d'en-têtes pour les services de métadonnées (ex: **IMDSv2** sur AWS) et configurer les politiques de pare-feu pour bloquer les requêtes sortantes vers les adresses de métadonnées cloud depuis les outils d'IA.
*   **Validation des entrées :** Désactiver ou restreindre les fonctionnalités de "fetch" d'URL dans les outils d'agent d'IA pour prévenir les attaques SSRF.

---
[Source](https://isc.sans.edu/diary/rss/33150){:target="_blank"}
