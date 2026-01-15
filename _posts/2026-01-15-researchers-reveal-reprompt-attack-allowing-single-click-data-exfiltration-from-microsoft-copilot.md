---
title: 'Researchers Reveal Reprompt Attack Allowing Single-Click Data Exfiltration From Microsoft Copilot'
date: 2026-01-15
permalink: /posts/2026/01/15/researchers-reveal-reprompt-attack-allowing-single-click-data-exfiltration-from-microsoft-copilot/
tags:
- veille-cyber
- hackernews
---
### Attaque Reprompt : Exfiltration de Données Facile via Microsoft Copilot

Une nouvelle technique d'attaque nommée Reprompt permet d'exfiltrer des données sensibles de chatbots IA comme Microsoft Copilot, potentiellement en un seul clic, tout en contournant les mesures de sécurité d'entreprise. Cette méthode exploite la manière dont les IA traitent les requêtes, en distinguant mal les instructions de l'utilisateur de celles injectées.

L'attaque repose sur l'utilisation du paramètre URL "q" pour injecter des instructions malveillantes. En demandant à l'IA de répéter ses actions, les protections contre les fuites de données, qui ne s'appliquent qu'à la requête initiale, sont contournées. Cela déclenche une chaîne de requêtes cachées entre Copilot et le serveur de l'attaquant, permettant une exfiltration continue et dynamique d'informations. Même après la fermeture de la fenêtre de discussion, l'attaquant peut maintenir le contrôle et continuer à extraire des données.

Il est important de noter que Microsoft a déjà corrigé cette vulnérabilité, et elle n'affecte pas les clients utilisant Microsoft 365 Copilot.

**Points Clés :**

*   **Méthode d'Attaque :** Reprompt
*   **Cible :** Chatbots IA, notamment Microsoft Copilot.
*   **Impact :** Exfiltration de données sensibles, contournement des contrôles de sécurité d'entreprise.
*   **Mode Opératoire :** Exploitation du paramètre "q" des URLs pour injecter des instructions, contournement des gardes-fous par répétition d'actions, exfiltration continue via échange serveur-IA.
*   **Vulnérabilité Fondamentale :** Incapacité de l'IA à distinguer clairement les instructions utilisateur des instructions injectées.

**Vulnérabilités Mentionnées (avec CVE si disponibles - Note : l'article ne liste pas de CVE spécifiques pour Reprompt) :**

*   **Reprompt :** Permet l'exfiltration de données en un clic en exploitant des paramètres URL et des boucles de requête.
*   **ZombieAgent :** Vulnérabilité exploitant les connexions de ChatGPT aux applications tierces pour transformer des injections indirectes de prompts en attaques zéro-clic et permettre la persistance via la mémoire de l'IA.
*   **Lies-in-the-Loop (LITL) / HITL Dialog Forging :** Exploite la confiance des utilisateurs dans les invites de confirmation pour exécuter du code malveillant, transformant une protection Human-in-the-Loop (HITL) en vecteur d'attaque (affecte Anthropic Claude Code et Microsoft Copilot Chat dans VS Code).
*   **GeminiJack :** Permet d'obtenir des données d'entreprise potentiellement sensibles en insérant des instructions cachées dans des documents partagés, des invitations de calendrier ou des e-mails (affecte Gemini Enterprise).
*   **Risques d'injection de prompt dans Perplexity Comet :** Contournement de BrowseSafe, une technologie conçue pour sécuriser les navigateurs IA contre les attaques par injection de prompt.
*   **GATEBLEED :** Vulnérabilité matérielle permettant de déterminer les données d'entraînement d'un système IA et de fuiter des informations privées en surveillant le temps d'exécution des fonctions logicielles sur les accélérateurs matériels.
*   **Vecteur d'attaque par injection de prompt sur Model Context Protocol (MCP) :** Exploite la fonction d'échantillonnage pour épuiser les quotas de calcul IA, permettre des invocations d'outils cachées, ou injecter des instructions persistantes et exfiltrer des données.
*   **CellShock :** Vulnérabilité affectant Anthropic Claude pour Excel, permettant l'exfiltration de données via des formules non sécurisées cachées dans des sources de données non fiables.
*   **Vulnérabilité d'injection de prompt dans Cursor et Amazon Bedrock :** Permet aux non-administrateurs de modifier les contrôles budgétaires et de fuiter des jetons API, ce qui peut conduire à une drainer les budgets d'entreprise.
*   **Diverses vulnérabilités d'exfiltration de données :** Mentionnées pour Claude Cowork, Superhuman AI, IBM Bob, Notion AI, Hugging Face Chat, Google Antigravity, et Slack AI.

**Recommandations :**

*   Adopter des défenses en couches pour contrer les risques persistants liés aux injections de prompts.
*   S'assurer que les outils sensibles ne s'exécutent pas avec des privilèges élevés.
*   Limiter l'accès des agents IA aux informations critiques de l'entreprise si nécessaire.
*   Évaluer attentivement les frontières de confiance des systèmes IA déployés.
*   Mettre en œuvre une surveillance robuste.
*   Rester informé des recherches émergentes en matière de sécurité de l'IA.

---
[Source](https://thehackernews.com/2026/01/researchers-reveal-reprompt-attack.html){:target="_blank"}
