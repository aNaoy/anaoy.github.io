---
title: 'The CLAIR Model: A Synthesized Conceptual Framework for Mapping Critical Infrastructure Interdependencies &#x5b;Guest Diary&#x5d;, (Wed, Feb 25th)'
date: 2026-02-26
permalink: /posts/2026/02/26/the-clair-model-a-synthesized-conceptual-framework-for-mapping-critical-infrastructure-interdependencies-x5bguest-diaryx5d-wed-feb-25th/
tags:
- veille-cyber
- sans-isc
---
**Modèle CLAIR : Cartographier les Interdépendances des Infrastructures Critiques**

Le modèle CLAIR (Comprehensive Linkage and Architectural Infrastructure Resiliency) est une nouvelle approche qui fusionne les modèles d'architecture d'entreprise traditionnels (comme le modèle Purdue pour l'industrie) avec les cadres d'architecture d'entreprise plus larges (comme le cadre Zachman). Il vise à mieux comprendre comment les différents systèmes interconnectés, des réseaux électriques aux centres de données et aux systèmes de sécurité, dépendent les uns des autres. L'objectif est d'identifier les points de défaillance potentiels et de prévoir les effets en cascade lors de perturbations.

**Points Clés :**

*   **Convergence IT/OT :** L'interconnexion croissante des technologies de l'information (IT) et des technologies opérationnelles (OT) a mis en évidence le besoin d'un cadre unifié pour analyser les risques.
*   **Cadre d'Analyse Amélioré :** CLAIR étend la hiérarchie du modèle Purdue de 5 à 10 niveaux, incluant les infrastructures externes (niveau -1 : réseau électrique, eau) et les systèmes de sécurité/cloud (niveaux 6 et 7).
*   **Visualisation des Dépendances :** Le modèle utilise une matrice combinant ses 10 niveaux avec les 6 questions du cadre Zachman ("Quoi", "Comment", "Où", "Qui", "Quand", "Pourquoi") pour cartographier les interdépendances sous différents angles.
*   **Types de Dépendances :** Il distingue les défaillances physiques, cybernétiques, géographiques et logiques.
*   **Impact des Pannes :** L'article utilise l'exemple des pannes du réseau électrique affectant les centres de données pour illustrer le mécanisme des défaillances en cascade.
*   **Intelligence Artificielle (IA) :** L'intégration de l'IA dans les systèmes opérationnels crée de nouvelles dépendances liées à la qualité des données, à la dérive des modèles et au manque d'explicabilité.
*   **Niveaux de Maturité :** Une échelle de maturité (MIL) est proposée pour évaluer la résilience des interdépendances, soulignant que la résilience globale est limitée par le maillon le plus faible.

**Vulnérabilités :**

Bien que l'article ne mentionne pas de CVE spécifiques, il décrit des vulnérabilités générales découlant des interdépendances :

*   **Défaillances en Cascade :** Un dysfonctionnement dans une partie du système (par exemple, le réseau électrique) peut déclencher une série de défaillances dans d'autres systèmes interconnectés (par exemple, les centres de données).
*   **Dépendances Externes Inhérentes :** Même les systèmes qui semblent sous contrôle direct peuvent dépendre de mises à jour logicielles ou de services externes, créant des vulnérabilités non gérées.
*   **Perte de Visibilité :** La défaillance des réseaux de surveillance (souvent basés sur le cloud) peut entraîner une perte de contrôle et des décisions incorrectes lors d'une crise.
*   **Risques liés à l'IA :**
    *   **Qualité des Données :** L'IA à des niveaux opérationnels peut prendre de mauvaises décisions si les données des capteurs sont compromises.
    *   **Dérive des Modèles :** Les modèles d'IA obsolètes peuvent nécessiter des mises à jour régulières via des liens cybernétiques, créant un risque.
    *   **Manque d'Explicabilité :** En cas de défaillance d'un système contrôlé par IA, le temps de récupération peut être allongé faute d'explications claires sur son comportement.

**Recommandations :**

*   **Adopter un Cadre Holistique :** Utiliser le modèle CLAIR ou un cadre similaire pour obtenir une vision complète des interdépendances plutôt que de se concentrer uniquement sur la sécurité interne.
*   **Cartographier les Liens :** Identifier et visualiser activement les relations entre les différents niveaux d'infrastructure, des utilités primaires aux systèmes cloud et de sécurité.
*   **Évaluer la Maturité des Dépendances :** Mesurer le niveau de résilience de chaque interdépendance et s'assurer que la résilience globale n'est pas compromise par des liens faibles.
*   **Comprendre les Effets en Cascade :** Analyser comment les défaillances d'un secteur peuvent se propager à travers le paysage des données et de la fabrication.
*   **Gérer les Risques de l'IA :** Mettre en place des stratégies pour garantir la qualité des données, la mise à jour des modèles d'IA et améliorer leur explicabilité dans les systèmes opérationnels.
*   **Visualisation des Flux :** Utiliser des outils comme les Sankey Flow Maps pour représenter clairement les dépendances entrantes et sortantes, en attribuant des "poids" de criticité.

---
[Source](https://isc.sans.edu/diary/rss/32748){:target="_blank"}
