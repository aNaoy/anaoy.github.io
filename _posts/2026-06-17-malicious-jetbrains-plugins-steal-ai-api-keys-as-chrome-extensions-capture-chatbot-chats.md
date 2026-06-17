---
title: 'Malicious JetBrains Plugins Steal AI API Keys as Chrome Extensions Capture Chatbot Chats'
date: 2026-06-17
permalink: /posts/2026/06/17/malicious-jetbrains-plugins-steal-ai-api-keys-as-chrome-extensions-capture-chatbot-chats/
tags:
- veille-cyber
- hackernews
---
### Campagne de vol de données via des plugins JetBrains et des extensions Chrome

Une double menace ciblant les développeurs et les utilisateurs d'outils d'IA a été identifiée. D'une part, 15 plugins malveillants sur le JetBrains Marketplace usurpent l'identité d'assistants de codage basés sur DeepSeek pour dérober des clés API. D'autre part, deux extensions de blocage de publicité sur Chrome capturent secrètement l'historique des conversations avec les principales plateformes d'IA (ChatGPT, Claude, Gemini, etc.).

**Points clés :**
*   **Plugins JetBrains :** Les outils fonctionnent comme promis, mais exfiltrent les clés API saisies par l'utilisateur vers un serveur distant (`39.107.60.51`) via des requêtes HTTP en clair. Ils utilisent également un système de "dons" pour fournir des clés piratées à d'autres clients, créant un service illicite.
*   **Extensions Chrome (PromptSnatcher) :** Les extensions *Smart Adblocker* et *Adblock for Browser* utilisent des listes de filtrage légitimes pour masquer une fonction de télémétrie malveillante qui intercepte les conversations privées, l'usage des modèles et les métadonnées de compte.
*   **Vulnérabilités :** Aucune CVE spécifique n'est associée, car il s'agit d'une exploitation malveillante de fonctionnalités légitimes et d'abus de confiance dans les écosystèmes d'extensions.
*   **Risque :** "LLMjacking" (utilisation des ressources IA d'autrui aux frais de la victime) et exposition de données sensibles (code source, conversations privées).

**Recommandations :**
*   **Audit des extensions :** Désinstaller immédiatement *Smart Adblocker* et *Adblock for Browser* sur Google Chrome.
*   **Vigilance sur les plugins :** Avant d'installer un plugin IDE, vérifier sa réputation et limiter l'octroi de privilèges élevés.
*   **Gestion des secrets :** Ne jamais intégrer de clés API "longue durée" dans des outils tiers non vérifiés. Préférer l'utilisation de variables d'environnement ou d'outils de gestion de secrets sécurisés.
*   **Révocation :** Si vous avez utilisé l'un des plugins listés, révoquez immédiatement les clés API concernées sur les plateformes d'IA (OpenAI, DeepSeek, etc.).

---
[Source](https://thehackernews.com/2026/06/malicious-jetbrains-plugins-steal-ai.html){:target="_blank"}
