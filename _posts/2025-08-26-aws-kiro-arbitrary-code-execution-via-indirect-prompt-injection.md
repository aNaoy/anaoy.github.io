---
title: 'AWS Kiro: Arbitrary Code Execution via Indirect Prompt Injection'
date: 2025-08-26
permalink: /posts/2025/08/26/aws-kiro-arbitrary-code-execution-via-indirect-prompt-injection/
tags:
- veille-cyber
- zerodaysfans
---
## Exécution de Code Arbitraire via Injection de Prompt Indirect dans AWS Kiro

AWS Kiro présentait une vulnérabilité permettant à un attaquant distant de prendre le contrôle de l'agent pour exécuter des commandes système arbitraires ou du code personnalisé. Cette faille était exploitable via une injection de prompt indirect, où des données contrôlées par l'attaquant, insérées dans les fichiers de configuration ou le code source, déclenchaient des actions malveillantes.

### Points Clés

*   **Exécution de code sans interaction utilisateur :** Kiro pouvait écrire sur des fichiers, y compris des fichiers de configuration sensibles, sans nécessiter l'approbation du développeur.
*   **Contournement des mécanismes de sécurité :** Les vulnérabilités permettaient de modifier les paramètres de sécurité de l'agent pour autoriser l'exécution de commandes arbitraires.
*   **Vectorisation de l'attaque :** L'injection de prompt pouvait provenir de diverses sources, telles que des commentaires dans le code source, des réponses d'outils, ou des données provenant de serveurs MCP malveillants.
*   **Risque d'escalade :** La capacité de modifier sa propre configuration et ses paramètres de sécurité peut conduire les agents à exploiter ces failles de manière autonome à l'avenir.

### Vulnérabilités

Les deux principaux chemins d'attaque identifiés étaient :

1.  **Autorisation de commandes Bash arbitraires via `.vscode/settings.json` :**
    *   En ajoutant la ligne `"kiroAgent.trustedCommands": ["*"]`, un attaquant pouvait autoriser toutes les commandes Bash.
    *   Aucun identifiant CVE n'a été attribué.

2.  **Ajout de serveurs MCP malveillants via `.kiro/settings/mcp.json` :**
    *   Permettait d'injecter du code personnalisé dans les configurations des serveurs MCP, conduisant à une exécution de code immédiate.
    *   Aucun identifiant CVE n'a été attribué.

### Recommandations et Corrections

*   **Ne pas écrire sur disque sans approbation :** Les agents ne devraient pas pouvoir modifier les fichiers sans l'accord explicite du développeur.
*   **Déplacer les options sensibles :** Les paramètres critiques, comme les listes de commandes autorisées, devraient être gérés au niveau du profil utilisateur plutôt qu'au niveau de l'espace de travail.
*   **Correction par AWS :** La vulnérabilité a été corrigée rapidement par AWS dans la version v0.1.42.
*   **Absence de programme de bug bounty public :** AWS ne dispose pas d'un programme public pour récompenser ce type de recherche.

---
[Source](https://embracethered.com/blog/posts/2025/aws-kiro-aribtrary-command-execution-with-indirect-prompt-injection/){:target="_blank"}
