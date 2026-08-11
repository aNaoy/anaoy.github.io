---
title: 'Malicious MCP Servers Can Split Instructions to Make AI Coding Agents Exfiltrate Secrets'
date: 2026-08-11
permalink: /posts/2026/08/11/malicious-mcp-servers-can-split-instructions-to-make-ai-coding-agents-exfiltrate-secrets/
tags:
- veille-cyber
- hackernews
---
### GhostSplice : L’attaque par fragmentation contre les agents IA

La technique **GhostSplice** met en évidence une vulnérabilité critique affectant les agents de codage utilisant le protocole **Model Context Protocol (MCP)**. Cette méthode permet à un serveur MCP malveillant d'exfiltrer des données sensibles (clés SSH, variables d'environnement, code source) en contournant les filtres de sécurité des modèles d'IA par une décomposition de l'instruction malveillante en plusieurs fragments anodins.

**Points clés :**
*   **Fonctionnement :** L'attaquant fragmente une instruction d'exfiltration en plusieurs morceaux répartis dans des champs de formulaires ou des résultats d'outils différents.
*   **Efficacité :** En isolant les fragments, l'agent IA ne perçoit aucune intention malveillante globale. Une fois combinés dans le contexte de travail, l'IA exécute la séquence complète, augmentant drastiquement le taux de réussite de l'exfiltration.
*   **Dépendance au contexte :** La vulnérabilité dépend de la configuration de l'agent et des contrôles de sécurité du client, et non uniquement du modèle d'IA lui-même.
*   **Portée :** L'attaque suppose que l'utilisateur a préalablement connecté un serveur MCP malveillant et que l'agent possède les privilèges d'accès aux fichiers ciblés.

**Vulnérabilités :**
*   **CVE :** Aucune CVE n'est attribuée à ce jour. La technique repose sur une faille logique inhérente au traitement contextuel des interactions MCP par les agents, plutôt que sur un bug logiciel classique.

**Recommandations :**
*   **Vérification rigilouse :** Les organisations doivent impérativement inspecter et valider tous les serveurs MCP tiers ou personnalisés avant leur intégration.
*   **Traitement des données :** Les clients MCP doivent impérativement traiter les sorties des serveurs comme des données brutes et non comme des instructions exécutables.
*   **Isolation des flux :** Empêcher le transfert automatique et non vérifié de données provenant de la sortie d'un outil vers les arguments d'un autre outil.
*   **Supervision humaine :** Maintenir une validation humaine obligatoire pour toute invocation d'outil sensible.

---
[Source](https://thehackernews.com/2026/08/malicious-mcp-servers-can-split.html){:target="_blank"}
