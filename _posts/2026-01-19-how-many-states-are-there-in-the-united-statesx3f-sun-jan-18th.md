---
title: '"How many states are there in the United States&#x3f;", (Sun, Jan 18th)'
date: 2026-01-19
permalink: /posts/2026/01/19/how-many-states-are-there-in-the-united-statesx3f-sun-jan-18th/
tags:
- veille-cyber
- sans-isc
---
### Reconnaissance des LLM ouverts par requêtes répétées

Les journaux de honeypot ont révélé de nombreuses requêtes API visant des modèles de langage (LLM), toutes axées sur la même question : "Combien y a-t-il d'États aux États-Unis ?". Cette répétition suggère une phase de reconnaissance afin d'identifier les LLM accessibles publiquement. L'intention n'est pas nécessairement d'exploiter directement ces modèles, mais plutôt de les utiliser.

Ce comportement fait écho à des signalements récents concernant des acteurs malveillants ciblant des proxys mal configurés pour accéder à des services LLM payants.

**Points Clés :**

*   Des requêtes API répétitives et identiques sont observées, visant à identifier des modèles de langage ouverts.
*   L'objectif est la découverte et l'utilisation potentielle de ces modèles.
*   Ce type de reconnaissance est aligné avec des attaques connues visant à exploiter des infrastructures d'accès aux LLM.

**Vulnérabilités :**

*   Exposition non authentifiée de modèles de langage (LLM) à Internet.
*   Proxys mal configurés permettant un accès non autorisé à des services.

**Recommandations :**

*   Assurer que les modèles de langage (LLM) ne sont pas exposés directement sur Internet sans mesures d'authentification appropriées.
*   Vérifier et sécuriser les configurations des proxys pour empêcher tout accès non autorisé.

---
[Source](https://isc.sans.edu/diary/rss/32618){:target="_blank"}
