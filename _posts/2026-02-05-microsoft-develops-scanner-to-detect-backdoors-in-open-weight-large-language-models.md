---
title: 'Microsoft Develops Scanner to Detect Backdoors in Open-Weight Large Language Models'
date: 2026-02-05
permalink: /posts/2026/02/05/microsoft-develops-scanner-to-detect-backdoors-in-open-weight-large-language-models/
tags:
- veille-cyber
- hackernews
---
**Détection des portes dérobées dans les grands modèles linguistiques à poids ouverts**

Microsoft a mis au point un analyseur léger capable de détecter les portes dérobées (backdoors) intégrées dans les grands modèles linguistiques (LLM) à poids ouverts. Cette technologie vise à renforcer la confiance dans les systèmes d'intelligence artificielle en identifiant les comportements malveillants cachés.

**Points Clés :**

*   Les LLM peuvent être compromis via leurs poids (paramètres apprenants) ou leur code.
*   L'empoisonnement de modèles consiste à introduire des comportements indésirables lors de l'entraînement, activés par des déclencheurs spécifiques. Ces modèles agissent comme des agents dormants.
*   L'outil de Microsoft analyse trois signaux observables pour repérer ces portes dérobées avec un faible taux de faux positifs, sans nécessiter de réentraînement ou de connaissance préalable des failles.
*   La méthode repose sur l'extraction et l'analyse de contenu mémorisé par le modèle, ainsi que sur l'examen des schémas d'attention et des distributions de sortie.
*   Cette approche est compatible avec les modèles de type GPT et s'intègre dans le cycle de développement sécurisé de Microsoft, qui est étendu pour aborder les menaces spécifiques à l'IA.

**Vulnérabilités :**

*   **Empoisonnement de modèles (Model Poisoning):** Insertion de comportements cachés dans les poids du modèle pendant l'entraînement.
    *   *CVE :* Aucune CVE spécifique n'est mentionnée dans l'article, car il s'agit d'une catégorie de vulnérabilité plutôt que d'une instance précise.

**Recommandations :**

*   Utiliser l'analyseur développé par Microsoft pour détecter les portes dérobées dans les LLM à poids ouverts.
*   Intégrer la détection des portes dérobées dans les cycles de développement et de déploiement des systèmes d'IA.
*   Collaborer au sein de la communauté de la sécurité de l'IA pour partager les apprentissages et améliorer les méthodes de détection.
*   Adapter les pratiques de développement sécurisé (SDL) pour tenir compte des nouveaux points d'entrée des menaces dans les systèmes d'IA (prompts, plugins, données récupérées, etc.).

**Limitations de l'outil :**

*   Ne fonctionne pas sur les modèles propriétaires nécessitant un accès aux fichiers.
*   Efficace principalement pour les portes dérobées basées sur des déclencheurs produisant des sorties déterministes.
*   Ne constitue pas une solution universelle pour détecter tous types de comportements de portes dérobées.

---
[Source](https://thehackernews.com/2026/02/microsoft-develops-scanner-to-detect.html){:target="_blank"}
