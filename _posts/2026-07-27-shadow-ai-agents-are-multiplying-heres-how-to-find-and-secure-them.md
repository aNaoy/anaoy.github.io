---
title: 'Shadow AI agents are multiplying. Heres how to find and secure them.'
date: 2026-07-27
permalink: /posts/2026/07/27/shadow-ai-agents-are-multiplying-heres-how-to-find-and-secure-them/
tags:
- veille-cyber
- bleepingcomp
---
### Maîtriser le risque lié aux agents IA « fantômes »

L'utilisation d'agents IA autonomes au sein des entreprises, souvent déployés par les employés sans supervision informatique (Shadow AI), représente un vecteur d'attaque majeur. Contrairement aux simples chatbots, ces agents disposent de permissions persistantes et peuvent interagir directement avec des systèmes critiques, augmentant considérablement la surface d'exposition.

**Points clés :**
*   **Visibilité insuffisante :** La majorité des organisations manquent de programmes de gouvernance matures pour suivre la prolifération des agents.
*   **Limites des API :** De nombreuses plateformes d'agents ne fournissent pas de données via API, rendant les méthodes de découverte traditionnelles inefficaces.
*   **Approche hybride :** Une stratégie de détection complète doit combiner l'analyse des API (pour les plateformes exposées) et l'analyse via extension de navigateur (pour les outils sans API).

**Vulnérabilités associées :**
*   Accès excessifs ou destructeurs accordés aux agents.
*   Présence d'identifiants codés en dur ou de données personnelles (PII) dans les instructions des agents.
*   Connexions MCP (Model Context Protocol) non authentifiées.
*   Persistance d'agents dormants ou créés par d'anciens collaborateurs.
*   Agents accessibles publiquement à l'ensemble de l'organisation sans contrôle d'accès.
*(Note : Aucune CVE spécifique n'est mentionnée, le risque étant lié à la configuration et à la gouvernance plutôt qu'à une faille logicielle isolée).*

**Recommandations :**
*   **Inventaire automatisé :** Mettre en place un outil de découverte capable de détecter les agents dès leur création sur l'ensemble des plateformes utilisées.
*   **Évaluation des risques :** Analyser systématiquement les capacités réelles de chaque agent (permissions, accès aux données, type d'instructions).
*   **Gouvernance proactive :** Responsabiliser les créateurs d'agents en les impliquant directement dans la correction des configurations risquées.
*   **Gestion du cycle de vie :** Automatiser l'attribution de propriétaires pour chaque agent et définir des statuts d'approbation (approuvé, en cours d'examen, interdit) afin d'éviter le blocage de l'innovation tout en maintenant la sécurité.

---
[Source](https://www.bleepingcomputer.com/news/security/shadow-ai-agents-are-multiplying-heres-how-to-find-and-secure-them/){:target="_blank"}
