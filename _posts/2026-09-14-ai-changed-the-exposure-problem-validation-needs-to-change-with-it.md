---
title: 'AI Changed the Exposure Problem. Validation Needs to Change With It.'
date: 2026-09-14
permalink: /posts/2026/09/14/ai-changed-the-exposure-problem-validation-needs-to-change-with-it/
tags:
- veille-cyber
- hackernews
---
### L'évolution de la validation des expositions face à l'IA

L'explosion du nombre de vulnérabilités (CVE) publiées et l'automatisation de leur découverte par l'IA rendent le modèle de gestion des risques basé uniquement sur le score CVSS obsolète. La priorité des équipes de sécurité doit désormais passer d'une approche réactive systématique à une validation contextuelle des expositions.

**Points clés :**
*   **Volume vs Réalité :** Bien que le nombre de CVE augmente drastiquement, seule une infime fraction est exploitée dans la nature. Traiter toutes les vulnérabilités "Critiques" comme des urgences est inefficace.
*   **Limites du CVSS :** Ce score offre une base de sévérité, mais ne prend pas en compte l'impact réel, la portée ou la configuration spécifique de l'environnement de l'entreprise.
*   **Complémentarité nécessaire :** Le pentesting automatisé est puissant mais limité par des contraintes de sécurité sur les actifs critiques et par l'absence fréquente d'exploits publics lors de la découverte.

**Recommandations pour une stratégie de validation unifiée :**
Pour gérer efficacement ces risques, il est recommandé d'intégrer trois piliers complémentaires dans une plateforme unique :
1.  **Validation de l'exploitabilité :** Déterminer si une vulnérabilité est réellement exploitable dans l'environnement, même en l'absence d'exploit public ou sur des systèmes critiques isolés.
2.  **Validation des contrôles de sécurité :** Vérifier systématiquement si les outils de prévention et de détection en place bloquent ou identifient réellement les tentatives d'exploitation.
3.  **Pentesting agentique :** Utiliser des outils autonomes pour simuler des chaînes d'attaques complexes et évaluer la progression réelle d'un attaquant au sein du réseau.

L'objectif est d'unifier ces preuves au sein d'un flux de travail opérationnel pour prioriser les remédiations sur la base de données concrètes, et non sur des scores théoriques.

---
[Source](https://thehackernews.com/2026/09/ai-changed-exposure-problem-validation.html){:target="_blank"}
