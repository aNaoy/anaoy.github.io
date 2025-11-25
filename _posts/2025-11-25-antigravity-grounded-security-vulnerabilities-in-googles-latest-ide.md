---
title: 'Antigravity Grounded! Security Vulnerabilities in Googles Latest IDE'
date: 2025-11-25
permalink: /posts/2025/11/25/antigravity-grounded-security-vulnerabilities-in-googles-latest-ide/
tags:
- veille-cyber
- zerodaysfans
---
## Vulnérabilités dans l'IDE Antigravity de Google

De récentes analyses de sécurité ont mis en évidence plusieurs vulnérabilités dans l'Environnement de Développement Intégré (IDE) Antigravity de Google, dont certaines étaient déjà connues et signalées sur le projet Windsurf avant son acquisition par Google. Ces failles exposent potentiellement les utilisateurs à des risques de sécurité importants, allant de l'exécution de commandes à distance à l'exfiltration de données sensibles.

### Points Clés :

*   **Héritage de Vulnérabilités :** L'IDE Antigravity, basé sur Windsurf, a hérité de vulnérabilités déjà identifiées et signalées en mai 2025.
*   **Exécution de Commandes à Distance (RCE) :** La configuration par défaut de l'IDE permet à l'IA d'exécuter des commandes terminal sans validation humaine préalable. Des techniques d'injection indirecte de prompts, y compris via des caractères Unicode invisibles, peuvent inciter l'IA à télécharger et exécuter des scripts malveillants.
*   **Instructions Cachées :** Les modèles Gemini sont capables d'interpréter des instructions masquées par des caractères Unicode. Ces instructions invisibles peuvent être insérées dans le code source ou d'autres données, échappant ainsi aux revues de code manuelles et aux interfaces utilisateur, et menant à l'exécution de commandes arbitraires.
*   **Absence de Validation Humaine (Human-in-the-Loop - HITL) :** L'IDE manque de mécanismes de validation humaine pour l'invocation des outils via les serveurs MCP (Mechanism for Code Processing). Cela ouvre la porte à des attaques par injection de prompt qui peuvent activer n'importe quel outil, entraînant potentiellement l'exfiltration de données, l'exécution de code, ou la manipulation/suppression de données.
*   **Exfiltration de Données :** Deux méthodes principales d'exfiltration de données ont été identifiées :
    *   Via l'outil `read_url_content` : Permet à un attaquant de lire le contenu de fichiers sensibles (comme les fichiers `.env`) et de les transmettre à un serveur distant.
    *   Via le rendu d'images : L'IA peut être amenée à télécharger des images depuis des URL externes, permettant ainsi d'exfiltrer des informations sensibles via une requête HTTP masquée dans une balise image.
*   **Manque de Sécurité par Défaut :** L'IDE s'appuie trop sur la bonne conduite de l'IA, ce qui constitue une approche de sécurité inadéquate face à des attaques adversariales.

### Vulnérabilités Identifiées (avec CVE si applicable, bien qu'absentes de l'article) :

*   **Exécution de commandes arbitraires via indirect prompt injection (Auto-Execute Bypasses) :** Permet à un attaquant d'exécuter des commandes sur le système de l'utilisateur.
*   **Antigravity suit des instructions cachées (via Unicode Tag characters) :** Exploitation de l'interprétation d'instructions invisibles par les modèles Gemini pour contourner les mesures de sécurité.
*   **Manque de validation humaine pour les invocations d'outils MCP :** Permet l'exécution non autorisée d'outils potentiellement dangereux.
*   **Exfiltration de données via l'outil `read_url_content` :** Lecture et transmission de fichiers sensibles.
*   **Exfiltration de données via le rendu d'images :** Utilisation du rendu d'images pour envoyer des données à des serveurs externes.

### Recommandations et Mitigations :

*   **Prudence avec les Serveurs MCP :** Désactiver les outils potentiellement dangereux et configurer prudemment les serveurs MCP.
*   **Implémentation du Human-in-the-Loop (HITL) :** Les équipes de développement de l'IDE devraient intégrer des contrôles HITL par défaut pour l'invocation des outils, en particulier pour les actions considérées comme destructrices ou critiques.
*   **Détection des Caractères Unicode Cachés :** Développer des outils de CI/CD capables de détecter programmatiquement les caractères Unicode suspects dans le code. Les revues de code manuelles sont insuffisantes pour ces attaques.
*   **Désactiver l'Exécution Automatique :** Les développeurs devraient désactiver l'option "Auto-Execute" et privilégier l'approbation manuelle des commandes. L'utilisation d'une "Liste d'autorisation" pour les commandes terminal est recommandée.
*   **Évaluation du Risque :** Les organisations utilisant cet IDE devraient envisager des exercices d'équipe Rouge ou Pourpre pour identifier les opportunités de détection et de surveillance.
*   **Alternatives :** Les développeurs pourraient envisager d'autres IDE plus matures en matière de sécurité, comme Claude Code, GitHub Copilot, Cursor, Codex, ou le Gemini CLI de Google, jusqu'à ce que ces vulnérabilités soient résolues.
*   **Surveillance des Mises à Jour :** Il sera intéressant de suivre l'évolution de l'IDE Antigravity et la priorité accordée aux correctifs de sécurité.

---
[Source](https://embracethered.com/blog/posts/2025/security-keeps-google-antigravity-grounded/){:target="_blank"}
