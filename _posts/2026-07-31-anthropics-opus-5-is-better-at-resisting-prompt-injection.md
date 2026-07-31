---
title: 'Anthropic’s Opus 5 Is Better at Resisting Prompt Injection'
date: 2026-07-31
permalink: /posts/2026/07/31/anthropics-opus-5-is-better-at-resisting-prompt-injection/
tags:
- veille-cyber
- schneier
---
### Résistance accrue d'Anthropic Opus 5 face aux injections de prompts

Le modèle Claude Opus 5 d'Anthropic établit une nouvelle référence en matière de cybersécurité pour les grands modèles de langage (LLM), démontrant une résistance supérieure aux attaques par injection de prompts par rapport à ses concurrents.

**Points clés**
*   **Performance améliorée :** Opus 5 réduit considérablement le taux de réussite des injections de prompts, passant de 5,5 % à 2,0 % sur 15 tentatives par rapport à la version 4.8.
*   **Supériorité compétitive :** Opus 5 surpasse largement les modèles concurrents. À titre de comparaison, les modèles GPT 5.6 (variantes Sol, Terra, Luna) présentent des taux de réussite d'attaque allant de 20 % à près de 44 % sur 15 tentatives.
*   **Évolutivité de la menace :** Bien que la prévention absolue des injections de prompts reste théoriquement impossible à grande échelle, les avancées actuelles permettent une sécurisation nettement plus efficace dans des cas d'usage spécifiques.

**Vulnérabilités**
*   **Injection de prompts :** Il n'existe pas de CVE spécifique associée à ces modèles dans cet article, car il s'agit d'une vulnérabilité intrinsèque à l'architecture des LLM (problème d'interprétation des instructions système par rapport aux données utilisateur).

**Recommandations**
*   **Privilégier les modèles robustes :** Pour les déploiements critiques, privilégier des modèles ayant prouvé une résilience supérieure sur les benchmarks IPI (Iterative Prompt Injection).
*   **Defense in Depth :** Ne pas se reposer uniquement sur la robustesse du modèle. Continuer à mettre en œuvre des couches de filtrage en amont (input sanitization) et en aval (output validation) des interactions avec les LLM, car aucun modèle n'est totalement immunisé contre l'injection.

---
[Source](https://www.schneier.com/blog/archives/2026/07/anthropics-opus-5-is-better-at-resisting-prompt-injection.html){:target="_blank"}
