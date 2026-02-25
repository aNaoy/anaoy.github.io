---
title: 'Poisoning AI Training Data'
date: 2026-02-25
permalink: /posts/2026/02/25/poisoning-ai-training-data/
tags:
- veille-cyber
- schneier
---
**L'Intoxication des Données d'Entraînement de l'IA : Une Vulnérabilité Exploitée**

Les modèles d'intelligence artificielle, malgré leur sophistication, sont sensibles à la manipulation de leurs données d'entraînement. Une expérimentation a démontré qu'il suffit de créer un site web contenant des informations erronées et trompeuses pour que les chatbots leaders, tels que Google Gemini et ChatGPT, les intègrent et les diffusent.

**Points Clés :**

*   **Facilité de Manipulation :** La création d'un simple article de blog sur un site personnel, avec des affirmations inventées et fausses, a suffi à influencer les réponses de grands modèles d'IA.
*   **Diffusion Rapide :** Les informations erronées publiées en ligne ont été rapidement ingérées par les IA, apparaissant dans leurs réponses moins de 24 heures plus tard.
*   **Absence de Fiabilité :** L'expérimentation souligne un manque de fiabilité intrinsèque dans la manière dont ces IA traitent et valident les informations issues de leurs données d'entraînement, même lorsqu'il s'agit de faits manifestement fantaisistes.
*   **Résilience Variable :** Tous les modèles ne sont pas également vulnérables, certains, comme Claude d'Anthropic, ayant démontré une plus grande résistance à cette forme de manipulation.

**Vulnérabilités :**

Bien que l'article ne détaille pas de CVE spécifiques, la vulnérabilité fondamentale réside dans la méthode d'acquisition et de traitement des données d'entraînement des IA, qui semble permettre l'ingestion d'informations non vérifiées ou malveillantes.

**Recommandations :**

L'article suggère implicitement la nécessité de développer des mécanismes plus robustes pour vérifier la fiabilité et l'exactitude des données utilisées pour entraîner les modèles d'IA, afin d'éviter la propagation d'informations erronées et potentiellement nuisibles.

---
[Source](https://www.schneier.com/blog/archives/2026/02/poisoning-ai-training-data.html){:target="_blank"}
