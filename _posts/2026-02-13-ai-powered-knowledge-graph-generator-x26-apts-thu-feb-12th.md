---
title: 'AI-Powered Knowledge Graph Generator &#x26; APTs, (Thu, Feb 12th)'
date: 2026-02-13
permalink: /posts/2026/02/13/ai-powered-knowledge-graph-generator-x26-apts-thu-feb-12th/
tags:
- veille-cyber
- sans-isc
---
### Générateur de graphes de connaissances piloté par l'IA pour l'analyse de menaces

Cet article présente un outil novateur, le "AI Powered Knowledge Graph Generator" (AIKG), qui transforme le texte non structuré en un graphe de connaissances interactif. En utilisant des grands modèles linguistiques (LLM) et l'extraction de triplets Sujet-Prédicat-Objet (SPO), l'outil identifie et visualise les relations entre les entités. Le système gère efficacement les documents volumineux en les divisant en segments et assure une dénomination cohérente des entités pour découvrir des liens inédits.

L'outil est compatible avec n'importe quel point de terminaison d'API compatible avec OpenAI, et une démonstration a été réalisée avec Ollama et le modèle Gemma 3 de Google, capable de traiter texte et images et fonctionnant sur une seule carte graphique. L'installation et la configuration sont détaillées pour une mise en œuvre rapide sur des systèmes Linux.

L'application pratique de cet outil a été illustrée en l'utilisant pour analyser deux articles concernant des campagnes cybernétiques menées par des acteurs étatiques russes : un avis de cybersécurité de la CISA sur le GRU russe ciblant des entités logistiques et technologiques occidentales, et un article de SecurityWeek sur APT28 ciblant des entités de recherche énergétique et de collaboration de défense. Ces articles, convertis en fichiers texte, ont été traités par AIKG avec différentes versions du modèle Gemma 3 (12 milliards et 27 milliards de paramètres).

Les résultats démontrent la capacité de l'outil à extraire et visualiser des relations complexes, telles que les acteurs de la menace ciblant des personnes ou des industries spécifiques, les méthodes d'exploitation, et l'infrastructure utilisée. L'analyse des triplets SPO, bien que souvent associée à l'optimisation pour les moteurs de recherche (SEO), se révèle particulièrement puissante pour les applications d'intelligence de menace.

#### Points Clés :

*   **AIKG :** Outil transformant le texte non structuré en graphes de connaissances interactifs.
*   **Technologie :** Utilise des LLM et l'extraction de triplets Sujet-Prédicat-Objet (SPO).
*   **Fonctionnalités :** Gestion de documents volumineux, dénomination cohérente des entités, visualisation interactive des relations.
*   **Compatibilité :** Fonctionne avec les API compatibles OpenAI (ex: Ollama).
*   **Cas d'usage :** Analyse d'informations sur des groupes APT et des campagnes cybernétiques.
*   **Bénéfices :** Fournit des perspectives enrichies et contextuelles pour les analystes en cybersécurité, les chasseurs de menaces et les professionnels de la sécurité.

#### Vulnérabilités :

Aucune vulnérabilité spécifique n'est mentionnée dans l'article. L'article se concentre sur l'application d'un outil pour l'analyse de menaces et de groupes APT.

#### Recommandations :

*   **Adoption d'AIKG :** Envisager l'intégration des principes d'AIKG dans les pratiques de génération de contexte et d'enrichissement au sein des équipes ML.
*   **Exploration des sorties :** Télécharger les fichiers JSON et HTML générés par l'outil pour expérimenter directement avec les graphes interactifs.
*   **Utilisation des triplets SPO :** Reconnaître la puissance des triplets SPO combinés aux LLM pour les applications d'intelligence de menace.
*   **Visualisation des données :** Continuer à privilégier la visualisation et les cartographies des relations d'entités pour une compréhension approfondie des menaces.

---
[Source](https://isc.sans.edu/diary/rss/32712){:target="_blank"}
