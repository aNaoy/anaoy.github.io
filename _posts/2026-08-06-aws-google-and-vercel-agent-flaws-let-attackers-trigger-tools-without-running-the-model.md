---
title: 'AWS, Google, and Vercel Agent Flaws Let Attackers Trigger Tools Without Running the Model'
date: 2026-08-06
permalink: /posts/2026/08/06/aws-google-and-vercel-agent-flaws-let-attackers-trigger-tools-without-running-the-model/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les infrastructures d'agents IA : La faille CoreBreak

Des vulnérabilités majeures ont été identifiées dans les infrastructures d'agents d'IA d'AWS, Google et Vercel. Le défaut principal, nommé **CoreBreak**, permet à des attaquants de déclencher l'exécution d'outils (API, accès aux données, exécutions de commandes) sans passer par le modèle de langage (LLM). En contournant le modèle, les attaquants neutralisent les mécanismes de sécurité, les filtres de contenu et les garde-fous intégrés, car le système traite des données malveillantes comme des ordres légitimes.

#### Points clés
*   **Contournement du LLM :** Les requêtes malveillantes sont directement injectées dans la boucle d'exécution (event loop) du SDK.
*   **Absence de preuve d'autorisation :** Le système d'exécution ne vérifie pas si l'instruction provient réellement du modèle après une analyse logique.
*   **Nature des vulnérabilités :** Bien que liées, les vecteurs diffèrent : requêtes distantes authentifiées (AWS), manipulation de sessions/événements (Google) ou code non fiable dans un environnement sandbox (Vercel).

#### Vulnérabilités identifiées
*   **AWS Bedrock AgentCore :** CVE-2026-18830 (Score 8.6) – Validation d'entrée insuffisante permettant d'injecter des blocs d'utilisation d'outils.
*   **Google ADK for Python :** CVE-2026-18236 (Score 9.3) – Falsification de confirmation et contournement du mode « résumable ».
*   **Vercel AI SDK :** CVE-2026-64650 et CVE-2026-64651 (Score 6.3) – Contournement de l'autorisation sandbox-vers-hôte via un chemin de processus approuvé.

#### Recommandations
*   **Mise à jour immédiate :**
    *   Google ADK for Python : Version **2.5.0** ou supérieure.
    *   Vercel `@ai-sdk/harness-codex` : Version **1.0.29** ou supérieure.
    *   Vercel `@ai-sdk/harness-opencode` : Version **1.0.28** ou supérieure.
*   **Sécurisation des entrées :** Traiter tout historique de conversation, événement de reprise ou bloc d'outil structuré provenant d'une source externe comme une donnée non fiable.
*   **Autorisation granulaire :** Lier chaque exécution d'outil à un événement spécifique généré par le modèle (nom de l'outil, arguments, session et état d'autorisation).
*   **Principe du moindre privilège :** Restreindre strictement les accès, rôles cloud et permissions accordés aux agents IA selon leurs besoins réels.

---
[Source](https://thehackernews.com/2026/08/aws-google-and-vercel-patch-agent-flaws.html){:target="_blank"}
