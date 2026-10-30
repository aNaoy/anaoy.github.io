---
title: 'Filter generation in practice: from algorithms to LLMs'
date: 2026-10-30
permalink: /posts/2026/10/30/filter-generation-in-practice-from-algorithms-to-llms/
tags:
- veille-cyber
- securelist
---
### Automatisation de la génération de filtres pour les alertes de sécurité

L'automatisation de la création de règles de filtrage est cruciale pour réduire la charge de travail des analystes SOC face au volume massif de faux positifs. Les organisations doivent passer d'une gestion manuelle à une génération automatisée basée sur des algorithmes ou des modèles de langage (LLM).

#### Points clés
*   **Objectif :** Filtrer les alertes non pertinentes sans supprimer les incidents réels en isolant les critères de filtrage optimaux (exclure les champs utilisés dans la règle de détection pour éviter de la neutraliser).
*   **Approches comparées :**
    *   **Algorithmique (FP-Growth) :** Déterministe et interprétable, ne nécessite pas d'IA, mais dépend fortement du contexte historique.
    *   **LLM (Single-prompt) :** Flexible face aux cas atypiques et normalisation efficace des chaînes, performant mais nécessite un accès à un modèle.
    *   **Agents IA multiples :** Architecture modulaire avec validation croisée, mais plus lente et complexe à déployer.
*   **Résultats :** L'approche LLM simple permet une réduction des faux positifs de 99 %, une augmentation de 28 % de la génération de filtres et un gain d'efficacité de 17 % pour les analystes.

#### Défis techniques
*   **Volume de données :** Gestion de centaines de champs par événement (nécessite une sélection préalable des champs pertinents).
*   **Normalisation :** Nécessité de standardiser les chemins de fichiers et les variables d'environnement pour assurer la robustesse des filtres.
*   **Validation :** Risque de générer des filtres trop larges (suppression d'alertes légitimes) ou trop spécifiques (inutilisables).

#### Recommandations
*   **Prioriser une approche hybride :** Utiliser des algorithmes pour la sélection initiale des champs (rapide et fiable) combinés à un LLM pour la génération et l'explication des règles.
*   **Mise en place de métriques de succès :**
    *   *Taux d'approbation :* Proportion de filtres générés validés par les analystes.
    *   *Taux de réduction des faux positifs :* Comparaison du volume d'alertes avant et après déploiement.
*   **Flexibilité :** Choisir l'approche algorithmique pour les environnements isolés sans accès LLM, et le modèle LLM simple pour les environnements connectés afin d'équilibrer précision et performance.

*Note : Aucune vulnérabilité CVE n'est associée à cet article, car il traite d'une méthodologie opérationnelle et non de failles logicielles spécifiques.*

---
[Source](https://securelist.com/practical-filter-generation/121697/){:target="_blank"}
