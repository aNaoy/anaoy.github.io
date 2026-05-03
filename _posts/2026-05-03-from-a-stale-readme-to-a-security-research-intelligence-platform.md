---
title: 'From a stale README to a security research intelligence platform'
date: 2026-05-03
permalink: /posts/2026/05/03/from-a-stale-readme-to-a-security-research-intelligence-platform/
tags:
- veille-cyber
- zerodaysfans
---
### Architecture d'une plateforme d'intelligence pour la recherche en cybersécurité

Cet article décrit la transformation d'un simple fichier `README` GitHub en un système expert automatisé capable d'ingérer, de structurer et d'analyser un corpus de 819 publications en cybersécurité. Contrairement aux outils RAG (Retrieval-Augmented Generation) classiques qui se concentrent sur la recherche textuelle, ce projet privilégie l'extraction de données structurées pour comparer les recherches de manière rigoureuse.

#### Points clés
*   **Records vs Réponses :** Le système privilégie l'extraction de champs typés (stance, modèle de menace, type de contribution) plutôt que la génération de résumés fluides mais imprécis.
*   **Auditabilité :** Chaque champ extrait est accompagné d'un extrait verbatim du texte original (*evidence snippet*) pour permettre une vérification humaine.
*   **Gestion des identités :** Utilisation d'un graphe de fusion pour traiter les multiples identifiants d'une même recherche (versions arXiv, DOI, prépublications).
*   **Interface comparative :** Le mode "Compare" permet d'aligner les champs de deux papiers pour identifier des tensions logiques ou des divergences de résultats avant même une lecture approfondie.
*   **Économie du système :** Passage d'un modèle de coût par "question" à un modèle de coût par "extraction" lors de l'ingestion, rendant la navigation gratuite et fluide.

#### Vulnérabilités de l'approche RAG classique
Le passage en revue des échecs des outils de recherche automatique a mis en évidence des failles critiques :
*   **Hallucinations techniques :** Le modèle invente des numéros de CVE ou des versions de noyau erronées mais plausibles.
*   **Effacement des nuances (Stance) :** Le découpage en "chunks" rend impossible la distinction entre la menace identifiée et la défense proposée par les auteurs.
*   **Incapacité comparative :** Le RAG ne saisit pas les contradictions entre deux papiers travaillant sur la même surface.

#### Recommandations techniques
1.  **Schémas typés :** Définir des structures strictes (en Rust dans ce projet) pour classifier les types de recherche (attaque, défense, formalisation).
2.  **Validation en deux temps :** Utiliser une désérialisation "bienveillante" au niveau de l'LLM, suivie d'une validation stricte via le typage du code.
3.  **Gestion de l'incertitude :** Intégrer un système de versionnage des schémas (`schema_version`) pour identifier automatiquement les enregistrements obsolètes lors de l'évolution de la méthodologie de recherche.
4.  **Maîtrise des coûts :**
    *   Prioriser la qualité du parsing PDF (réduction des tokens inutiles).
    *   Utiliser une barrière de dispatch pour bloquer les nouveaux lancements d'extractions si le budget prédéfini est atteint.
5.  **Traitement des données hostiles :** Envelopper les contenus des papiers dans des balises de délimitation (`<paper>`) pour éviter les injections de prompt présentes dans les recherches sur les attaques LLM.

---
[Source](https://0x434b.dev/from-a-stale-readme-to-a-security-research-intelligence-platform/){:target="_blank"}
