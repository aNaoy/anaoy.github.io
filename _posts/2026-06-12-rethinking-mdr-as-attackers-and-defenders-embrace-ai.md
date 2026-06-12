---
title: 'Rethinking MDR as Attackers and Defenders Embrace AI'
date: 2026-06-12
permalink: /posts/2026/06/12/rethinking-mdr-as-attackers-and-defenders-embrace-ai/
tags:
- veille-cyber
- hackernews
---
### L'Obsolescence du Modèle MDR face à l'ère de l'IA

Le modèle traditionnel de gestion des détections et réponses (MDR) atteint ses limites face à des attaquants utilisant désormais l'IA pour automatiser leurs campagnes et exploiter les angles morts des équipes de sécurité.

**Points clés :**
*   **Saturation humaine :** Environ 60 % des alertes ne sont pas examinées par manque de ressources, créant des failles exploitables (1 % des menaces réelles se cachent dans les alertes de faible priorité).
*   **Incohérence opérationnelle :** La qualité des investigations varie selon l'heure, la charge de travail et l'expertise de l'analyste, rendant la détection des mouvements latéraux incertaine.
*   **Silos technologiques :** L'ingénierie de détection est déconnectée de l'investigation, empêchant une amélioration continue du posture de sécurité.
*   **Opacité et dépendance :** Le modèle MDR actuel fonctionne comme une "boîte noire" où les données, l'historique et les règles appartiennent au prestataire, empêchant le client de capitaliser sur ses propres incidents ou d'intégrer ses propres outils d'IA.

**Vulnérabilités mentionnées :**
Bien que l'article se concentre sur les failles structurelles du modèle MDR plutôt que sur des vulnérabilités logicielles spécifiques, il souligne la capacité des attaquants à contourner les outils EDR (souvent marqués à tort comme "atténués") et à exploiter des menaces furtives :
*   **Malwares "Fileless" :** S'exécutant uniquement en mémoire sans écriture sur le disque.
*   **Injection de code :** Dissimulée au sein de processus légitimes.
*   **Vol d'identifiants :** Mimant des comportements d'authentification normaux.

**Recommandations :**
*   **Transition vers un "AI SOC" :** Adopter un modèle où l'IA assure l'investigation forensique exhaustive (100 % des alertes) en quelques secondes, ne laissant aux humains que la prise de décision finale.
*   **Investigation avec profondeur forensique :** Exiger une analyse basée sur la mémoire, le binaire et la réutilisation de code plutôt qu'une simple synthèse contextuelle.
*   **Boucle de rétroaction fermée :** Intégrer les résultats des investigations directement dans l'ingénierie de détection pour corriger les règles bruyantes ou défectueuses en temps réel.
*   **Modèle économique prévisible :** Privilégier une tarification au nombre d'endpoints plutôt qu'au volume d'alertes pour éviter le tri sélectif des menaces (cherry-picking).
*   **Souveraineté des données :** S'assurer contractuellement de la propriété des règles de détection et de l'historique des investigations pour maintenir son indépendance et sa préparation à l'IA.

---
[Source](https://thehackernews.com/2026/06/rethinking-mdr-as-attackers-and.html){:target="_blank"}
