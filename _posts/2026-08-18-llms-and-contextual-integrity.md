---
title: 'LLMs and Contextual Integrity'
date: 2026-08-18
permalink: /posts/2026/08/18/llms-and-contextual-integrity/
tags:
- veille-cyber
- schneier
---
### Intégrité contextuelle et risques de fuite de données dans les LLM

L'utilisation de la mémoire persistante dans les grands modèles de langage (LLM) pose des défis critiques en matière de confidentialité. Ces modèles peinent à déterminer quelles informations personnelles sont appropriées selon le contexte de la tâche, entraînant des fuites involontaires de données sensibles.

**Points clés :**
* **Incohérence des modèles :** Les modèles de pointe présentent des taux de violation allant jusqu'à 69 % lors de l'utilisation de mémoires persistantes.
* **Instabilité temporelle :** Les violations augmentent avec le nombre de tâches effectuées (passant de 0,1 % à 9,6 % sur 40 tâches) et lors de répétitions de requêtes identiques, révélant un comportement imprévisible.
* **Échec du "prompting" :** Les techniques de prompt limitent souvent la capacité des modèles à faire des choix nuancés, les poussant à une généralisation excessive (partage total ou nul).
* **Nécessité de raisonnement :** La résolution du problème ne dépend pas du passage à l'échelle, mais de la capacité du modèle à raisonner explicitement sur le contexte de chaque interaction.

**Vulnérabilités :**
* **Fuite contextuelle de données :** Absence de mécanisme natif pour filtrer les attributs utilisateurs en fonction de la pertinence de la tâche.
* **Non-déterminisme des fuites :** Le comportement aléatoire des modèles face à des prompts identiques empêche toute sécurité prévisible.
* *Note : Aucune CVE spécifique n'est associée à ces recherches académiques, car il s'agit de vulnérabilités inhérentes à l'architecture des LLM actuels.*

**Recommandations :**
* **Intégration du raisonnement explicite :** Forcer les modèles à analyser le contexte avant toute divulgation d'information.
* **Apprentissage par renforcement (RL) :** Utiliser des frameworks de RL pour entraîner les modèles à respecter des normes de divulgation basées sur des ensembles de données diversifiés.
* **Évaluation par benchmarks dédiés :** Tester les systèmes d'IA avec des outils comme *CIMemories* ou *PrivacyLens* pour mesurer la gestion de l'intégrité contextuelle avant tout déploiement en environnement autonome.

---
[Source](https://www.schneier.com/blog/archives/2026/08/llms-and-contextual-integrity.html){:target="_blank"}
