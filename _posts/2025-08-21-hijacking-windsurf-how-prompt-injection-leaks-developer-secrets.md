---
title: 'Hijacking Windsurf: How Prompt Injection Leaks Developer Secrets'
date: 2025-08-21
permalink: /posts/2025/08/21/hijacking-windsurf-how-prompt-injection-leaks-developer-secrets/
tags:
- veille-cyber
- zerodaysfans
---
**Fuite de Secrets Développeurs via Injection de Prompts dans Windsurf**

Des vulnérabilités critiques ont été découvertes dans Windsurf Cascade, un agent de codage basé sur VS Code, permettant l'exfiltration de données sensibles depuis les postes de travail des développeurs via des attaques d'injection de prompts indirectes. Ces failles exploitent la capacité de l'agent à interagir avec des ressources externes sans validation préalable par l'utilisateur. Face à l'inaction de Windsurf suite à une divulgation responsable, ces informations sont rendues publiques pour sensibiliser.

**Points Clés :**

*   **Injection de Prompts Indirecte :** Des instructions malveillantes intégrées dans des fichiers ou du contenu web peuvent être exécutées par Windsurf Cascade lors de son analyse.
*   **"Confused Deputy" :** L'agent est amené à agir sur la base d'instructions injectées, le faisant passer pour un tiers non fiable.
*   **Infoxication de Données :** Des informations sensibles comme le contenu des fichiers `.env` peuvent être dérobées.
*   **Manque de Réponse de Windsurf :** Malgré une divulgation responsable en mai 2025, Windsurf n'a pas répondu aux sollicitations concernant les correctifs.

**Vulnérabilités :**

*   **Utilisation du Tool `read_url_content` :** La capacité de lire le contenu d'une URL sans validation utilisateur permet l'exfiltration de données via des requêtes HTTP sortantes.
*   **Rendu d'Images à partir de Domaines Non Fiables :** Similaire à une faille précédemment corrigée dans GitHub Copilot, le rendu d'images issues de sources non sécurisées peut déclencher l'exfiltration de données.

**Recommandations :**

*   **Validation Humaine :** Implémenter une étape de validation par l'utilisateur avant l'invocation du tool `read_url_content` avec des serveurs non fiables.
*   **Liste Blanche de Domaines :** Utiliser une liste de domaines de confiance autorisés pour l'accès aux données sans approbation utilisateur.
*   **Sécurité du Rendu d'Images :** Éviter de rendre des images ou des hyperliens provenant de domaines non fiables, potentiellement en s'intégrant à des listes blanches existantes (comme celle de VS Code).
*   **Navigation Sécurisée :** Ne pas naviguer automatiquement vers des hyperliens cliquables pour prévenir les attaques de phishing.
*   **Demandes Clients :** Les clients de Windsurf sont encouragés à contacter leurs gestionnaires de compte pour demander des éclaircissements et des correctifs pour ces vulnérabilités.

---
[Source](https://embracethered.com/blog/posts/2025/windsurf-data-exfiltration-vulnerabilities/){:target="_blank"}
