---
title: 'New Agent Data Injection Attack Can Make AI Agents Misclick or Run Attacker Commands'
date: 2026-07-16
permalink: /posts/2026/07/16/new-agent-data-injection-attack-can-make-ai-agents-misclick-or-run-attacker-commands/
tags:
- veille-cyber
- hackernews
---
### La menace « Agent Data Injection » (ADI) : quand les IA sont manipulées par leurs propres données

Une nouvelle classe d'attaques, baptisée **Agent Data Injection (ADI)**, permet de détourner le comportement des agents IA en corrompant les données de confiance qu'ils traitent. Contrairement à l'injection de prompts classique, qui tente de forcer l'IA à ignorer ses instructions, l'ADI manipule les faits (identifiants, noms d'expéditeurs, résultats d'outils) pour que l'IA exécute des actions malveillantes en croyant suivre une procédure normale.

#### Points clés
*   **Fonctionnement par délimitation probabiliste :** Les modèles de langage utilisent des caractères de ponctuation (guillemets, crochets) pour structurer leurs données. L'attaquant insère des caractères similaires dans des champs non sécurisés, induisant l'IA en erreur sur la structure réelle des informations.
*   **Invisibilité pour les défenses actuelles :** Les mécanismes de défense contre l'injection de prompts (qui filtrent les ordres malveillants) sont inefficaces contre l'ADI, car l'attaque ne contient aucune instruction explicite, mais uniquement des données falsifiées.
*   **Récupération de formats :** Les chercheurs ont démontré qu'il est possible de découvrir le format de structuration des données d'un agent via du "jailbreaking" ou par rétro-ingénierie, rendant l'attaque réalisable même sur des services cloud fermés.

#### Vecteurs d'attaque observés
*   **Agents web :** Falsification d'identifiants de boutons sur une page web pour inciter l'IA à effectuer un achat non désiré au lieu d'une action anodine (ex: « Lire la suite »).
*   **Assistants de code :** Usurpation de l'identité d'un mainteneur dans un thread GitHub pour injecter des commandes malveillantes qu'un développeur validera par réflexe.
*   **Historique d'outils :** Fabrication de résultats de tests fictifs pour pousser l'IA à fusionner (merge) du code compromis.

#### Vulnérabilités identifiées
Bien qu'aucune CVE spécifique ne soit encore attribuée à cette méthode, les chercheurs ont confirmé sa faisabilité sur les modèles les plus récents :
*   **Modèles impactés :** GPT-5.2/mini, Claude Opus/Sonnet 4.5, Gemini 3 Pro/Flash.
*   **Vulnérabilité sous-jacente :** Absence de séparation stricte entre les données de confiance (système) et les données non fiables (provenant de l'utilisateur ou d'internet) au sein de la mémoire de l'agent.

#### Recommandations
*   **Utiliser des identifiants imprévisibles :** Remplacer les compteurs séquentiels (ID simples) par des jetons aléatoires (ex: tokens uniques pour chaque élément d'interface) pour empêcher la forge de correspondances.
*   **Isolation des données :** Implémenter une séparation stricte entre les métadonnées système et les contenus générés par des tiers.
*   **Traçabilité stricte :** Privilégier des systèmes qui conservent l'origine (provenance) de chaque donnée, bien que cette approche puisse réduire les performances et la fluidité des agents.
*   **Validation humaine renforcée :** Ne pas se contenter d'une validation globale, mais afficher explicitement à l'utilisateur le contexte et l'origine de l'action demandée par l'IA.

---
[Source](https://thehackernews.com/2026/07/new-agent-data-injection-attack-can.html){:target="_blank"}
