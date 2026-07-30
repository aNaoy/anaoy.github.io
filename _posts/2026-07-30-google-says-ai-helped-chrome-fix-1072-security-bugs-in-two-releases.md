---
title: 'Google says AI helped Chrome fix 1,072 security bugs in two releases'
date: 2026-07-30
permalink: /posts/2026/07/30/google-says-ai-helped-chrome-fix-1072-security-bugs-in-two-releases/
tags:
- veille-cyber
- bleepingcomp
---
### L'IA au service de la sécurisation accélérée de Google Chrome

Google a radicalement transformé la gestion des vulnérabilités de Chrome grâce à l'intégration massive de modèles de langage (LLM) et d'agents IA, permettant la correction de 1 072 failles dans les versions 149 et 150. Ce déploiement dépasse le nombre total de correctifs cumulés sur les 23 versions précédentes.

**Points clés :**
*   **Automatisation du cycle de vie :** L'IA intervient désormais sur l'ensemble du processus : découverte, reproduction des preuves de concept, évaluation de la criticité, routage vers les développeurs et génération de patchs.
*   **Efficacité prouvée :** Le système "Big Sleep" et les agents Gemini ont notamment permis de découvrir une faille d'évasion de sandbox présente dans le code depuis 13 ans, capable de permettre la lecture de fichiers locaux.
*   **Réduction du délai d'exposition :** Google raccourcit son cycle de publication (mises à jour hebdomadaires) pour contrer la rétro-ingénierie des correctifs par les attaquants.
*   **Innovations en déploiement :** Expérimentation du « patch dynamique » visant à appliquer les correctifs sans redémarrage du navigateur et automatisation des redémarrages en arrière-plan (sur macOS).

**Vulnérabilités :**
*   L'article mentionne une faille majeure d'évasion de sandbox (sandbox escape) vieille de 13 ans découverte par l'IA. Aucune référence CVE spécifique n'est fournie dans le texte, les failles étant traitées en masse dans les rapports de version.

**Recommandations :**
*   **Accélération des mises à jour :** Les utilisateurs sont incités à adopter le rythme de publication plus soutenu (cycle hebdomadaire) pour limiter le "patch gap" exploitable.
*   **Standardisation du code :** Pour les développeurs, l'adoption de fichiers `SECURITY.md` décrivant précisément les limites de confiance et les modèles de menace est essentielle pour permettre aux outils d'IA de mieux identifier les zones critiques du code.
*   **Maintien des tests hybrides :** L'automatisation par IA ne remplace pas le fuzzing traditionnel ; les deux approches doivent rester complémentaires pour maximiser la détection de vulnérabilités complexes.

---
[Source](https://www.bleepingcomputer.com/news/google/google-says-ai-helped-chrome-fix-1-072-security-bugs-in-two-releases/){:target="_blank"}
