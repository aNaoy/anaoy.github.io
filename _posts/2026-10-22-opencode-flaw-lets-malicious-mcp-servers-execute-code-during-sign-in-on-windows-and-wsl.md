---
title: 'OpenCode Flaw Lets Malicious MCP Servers Execute Code During Sign-In on Windows and WSL'
date: 2026-10-22
permalink: /posts/2026/10/22/opencode-flaw-lets-malicious-mcp-servers-execute-code-during-sign-in-on-windows-and-wsl/
tags:
- veille-cyber
- hackernews
---
### Exécution de code arbitraire dans l'agent OpenCode sur Windows

Une vulnérabilité critique a été identifiée dans l'agent de codage AI **OpenCode**, permettant à un serveur MCP (Model Context Protocol) malveillant ou compromis d'exécuter du code arbitraire sur les machines Windows et WSL des développeurs lors de la procédure de connexion (OAuth).

**Points clés :**
*   **Mécanisme d'attaque :** L'application utilise un utilitaire externe pour ouvrir l'URL d'authentification dans un navigateur. Sur Windows/WSL, cette URL n'est pas correctement échappée, permettant à un attaquant d'injecter des commandes PowerShell malveillantes via l'adresse fournie par le serveur MCP.
*   **Absence de CVE :** L'éditeur (Anomaly) a corrigé la faille silencieusement sans demander de CVE, ce qui empêche les outils de scan de vulnérabilités standards de détecter les versions obsolètes.
*   **Portée :** La faille concerne uniquement les systèmes Windows et WSL. Les environnements macOS et Linux ne sont pas affectés.

**Vulnérabilités :**
*   **Type :** Injection de commande (Command Injection).
*   **Versions affectées :** 1.0.137 à 1.18.32.
*   **CVE :** Aucune assignée (l'éditeur a refusé de traiter cela comme une vulnérabilité de sécurité, arguant que les serveurs MCP tiers sont hors de son périmètre de confiance).

**Recommandations :**
*   **Mise à jour :** Installer immédiatement la version **1.18.33** ou ultérieure.
*   **Audit de configuration :** Exécuter la commande `opencode mcp list` pour identifier et supprimer tout serveur MCP distant non approuvé ou inconnu.
*   **Atténuation :** Si la mise à jour est impossible, limiter strictement l'usage aux serveurs MCP de confiance, car tout serveur ajouté possède les permissions d'exécution sur la machine hôte.

---
[Source](https://thehackernews.com/2026/10/opencode-flaw-lets-malicious-mcp.html){:target="_blank"}
