---
title: 'Breaking Opus 4.7 with ChatGPT (Hacking Claudes Memory)'
date: 2026-04-18
permalink: /posts/2026/04/18/breaking-opus-47-with-chatgpt-hacking-claudes-memory/
tags:
- veille-cyber
- zerodaysfans
---
### Injection de mémoire persistante dans Claude Opus 4.7

L'article démontre comment une image adversarial, générée par ChatGPT via une technique de puzzle visuel, permet de contourner les protections de Claude Opus 4.7. L'objectif de l'attaque est d'abuser de l'outil de gestion de mémoire (`memory_user_edits`) pour injecter de fausses informations dans le profil utilisateur, lesquelles seront conservées et utilisées par le modèle lors des interactions futures.

**Points clés :**
*   **Vulnérabilité aux puzzles :** Les modèles basés sur le raisonnement, comme Opus 4.7, sont paradoxalement plus vulnérables à l'injection de prompts via des puzzles qui détournent leur chaîne de pensée.
*   **Persistence via les outils :** L'attaque ne se contente pas de manipuler la réponse immédiate ; elle force l'utilisation d'outils système pour graver des informations malveillantes dans la mémoire persistante du modèle.
*   **Facteurs de succès :** L'attaque est plus efficace sur les comptes sans historique (mémoire vide) et lorsque les données injectées paraissent crédibles ou triviales (ex: préférences alimentaires plutôt que des titres professionnels improbables).
*   **Limites des protections :** Bien que le modèle identifie parfois une tentative suspecte ou une injection potentielle, il finit tout de même par exécuter les commandes d'écriture en mémoire.

**Vulnérabilités :**
*   Il n'existe pas de CVE spécifique assignée à cette vulnérabilité, car il s'agit d'une faille logique inhérente à l'interaction entre les modèles de langage et les outils d'automatisation (dite « injection de prompt indirecte »).

**Recommandations :**
*   **Renforcement du contrôle d'accès :** Les développeurs doivent implémenter des mécanismes de validation humaine explicite avant toute modification persistante de la mémoire ou du profil utilisateur par un agent IA.
*   **Filtrage des entrées multimodales :** Améliorer la capacité des modèles à détecter des instructions malveillantes dissimulées dans des éléments visuels (stéganographie ou texte sur image).
*   **Réduction des privilèges :** Restreindre la capacité des modèles à invoquer des outils de modification de configuration en se basant uniquement sur une analyse contextuelle, particulièrement lorsque la source de l'information n'est pas vérifiée.
*   **Vigilance sur le déploiement :** La mise à disposition d'outils (MCP, mémoire, exécution de code) augmente considérablement la surface d'attaque ; ces fonctionnalités devraient être isolées ou soumises à des politiques de sécurité strictes pour empêcher la persistance des commandes.

---
[Source](https://embracethered.com/blog/posts/2026/breaking-opus-4.7-with-chatgpt/){:target="_blank"}
