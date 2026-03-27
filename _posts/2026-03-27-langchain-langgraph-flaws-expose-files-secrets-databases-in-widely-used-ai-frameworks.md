---
title: 'LangChain, LangGraph Flaws Expose Files, Secrets, Databases in Widely Used AI Frameworks'
date: 2026-03-27
permalink: /posts/2026/03/27/langchain-langgraph-flaws-expose-files-secrets-databases-in-widely-used-ai-frameworks/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les frameworks d'IA LangChain et LangGraph

Trois failles de sécurité majeures ont été identifiées dans les frameworks LangChain et LangGraph, permettant à des attaquants d'exfiltrer des fichiers système, des secrets d'environnement et des historiques de conversations. Ces vulnérabilités mettent en péril de nombreuses applications basées sur des modèles de langage (LLM) en raison de l'omniprésence de ces bibliothèques dans l'écosystème IA.

**Points clés :**
*   **Risque étendu :** La nature intégrée de ces frameworks signifie qu'une faille dans le cœur de LangChain se répercute sur toutes les bibliothèques et intégrations tierces dépendantes.
*   **Nature des attaques :** Les vecteurs d'attaque incluent le parcours de répertoires, la désérialisation de données non fiables et l'injection SQL.

**Vulnérabilités identifiées :**

*   **CVE-2026-34070 (CVSS 7.5) :** Vulnérabilité de type *Path Traversal* dans `langchain_core/prompts/loading.py`, permettant d'accéder à des fichiers arbitraires via une manipulation des modèles de prompts.
*   **CVE-2025-68664 (CVSS 9.3) :** Vulnérabilité de désérialisation de données non fiables (surnommée "LangGrinch"), permettant de récupérer des clés API et des secrets d'environnement.
*   **CVE-2025-67644 (CVSS 7.3) :** Vulnérabilité d'injection SQL dans l'implémentation SQLite de LangGraph, permettant l'exécution de requêtes SQL arbitraires via des filtres de métadonnées.

**Recommandations :**

La mise à jour immédiate des composants concernés est indispensable pour sécuriser les environnements :
*   **langchain-core :** Mettre à jour vers la version **1.2.22** (pour CVE-2026-34070) ou versions **0.3.81 / 1.2.5** (pour CVE-2025-68664).
*   **langgraph-checkpoint-sqlite :** Mettre à jour vers la version **3.0.1** (pour CVE-2025-67644).

---
[Source](https://thehackernews.com/2026/03/langchain-langgraph-flaws-expose-files.html){:target="_blank"}
