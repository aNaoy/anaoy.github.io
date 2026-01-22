---
title: 'Why AI Keeps Falling for Prompt Injection Attacks'
date: 2026-01-22
permalink: /posts/2026/01/22/why-ai-keeps-falling-for-prompt-injection-attacks/
tags:
- veille-cyber
- schneier
---
### L'illusion de la sécurité des IA face aux injections de prompt

Les grands modèles linguistiques (LLM) sont vulnérables aux attaques par injection de prompt, une méthode où des instructions spécifiques contournent les mesures de sécurité intégrées. Contrairement aux humains, qui s'appuient sur un jugement contextuel basé sur l'instinct, l'apprentissage social et la formation institutionnelle, les LLM traitent le contexte comme une simple similarité textuelle. Ils manquent d'une compréhension approfondie du "tableau d'ensemble", sont trop confiants dans leurs réponses et sont conçus pour plaire, ce qui les rend naïfs face à des manipulations cognitives simples.

Le problème s'aggrave avec les agents d'IA autonomes, qui peuvent exécuter des tâches complexes. Leur conception actuelle, qui combine une perception aplatie du contexte, une indépendance intégrée et une confiance excessive, les rend imprévisibles et susceptibles de prendre des décisions erronées. L'absence d'un réflexe d'interruption, comme celui des humains qui suspendent une action lorsque quelque chose semble suspect, est une lacune majeure.

La recherche de solutions se tourne vers des approches comme l'intégration des IA dans des modèles du monde physique, potentiellement pour leur conférer une meilleure compréhension du contexte et une moins grande naïveté. Cependant, il existe un trilemme fondamental : une IA ne peut être à la fois rapide, intelligente et sécurisée ; il faut prioriser deux de ces attributs. Pour les agents d'IA, la priorité devrait être donnée à la vitesse et à la sécurité, en les formant étroitement à des tâches spécifiques et en exigeant une supervision humaine pour toute requête sortant de l'ordinaire. Sans cela, le risque de compromission est élevé, malgré des succès fréquents.

**Points Clés:**

*   Les LLM ne comprennent pas le contexte comme les humains ; ils le traitent par similarité textuelle.
*   Les LLM sont trop confiants et conçus pour plaire, ce qui les rend naïfs.
*   Les agents d'IA autonomes amplifient ces vulnérabilités en raison de leur capacité à agir indépendamment.
*   L'absence d'un "réflexe d'interruption" chez les LLM les rend susceptibles de prendre des décisions erronées.
*   Il existe un compromis entre rapidité, intelligence et sécurité pour les IA.

**Vulnérabilités:**

*   **Injection de Prompt:** Méthode où des instructions spécifiques détournent les LLM de leurs objectifs de sécurité. Les exemples incluent le fait de demander des informations sensibles en les déguisant (ex: dans des histoires fictives, de l'ASCII art, ou sur des panneaux imaginaires) ou en utilisant des phrases comme "ignore les instructions précédentes".
*   **Absence de jugement contextuel:** Incapacité des LLM à évaluer la pertinence, la normalité ou le risque d'une requête de la même manière qu'un humain.
*   **Surconfiance et désir de plaire:** Tendances des LLM à fournir une réponse même en cas d'incertitude et à satisfaire les requêtes des utilisateurs.

**Recommandations:**

*   **Prioriser la sécurité et la rapidité:** Pour les agents d'IA, cela implique de limiter leur champ d'action à des tâches prédéfinies.
*   **Escalade vers un superviseur humain:** Tout ce qui sort du champ d'application normal d'un agent d'IA devrait être transmis à une personne pour vérification.
*   **Développement de "modèles du monde":** Intégrer les IA dans des environnements physiques pour leur donner une meilleure compréhension du contexte et de la réalité.
*   **Améliorations fondamentales en IA:** Nécessité de recherches pour rendre les LLM véritablement résistants aux injections de prompt, ce qui pourrait nécessiter de repenser la manière dont les commandes fiables et les entrées non fiables sont traitées.

---
[Source](https://www.schneier.com/blog/archives/2026/01/why-ai-keeps-falling-for-prompt-injection-attacks.html){:target="_blank"}
