---
title: 'High Frequency Trading and Lessons for Agentic AI'
date: 2026-05-02
permalink: /posts/2026/05/02/high-frequency-trading-and-lessons-for-agentic-ai/
tags:
- veille-cyber
- philvenables
---
### Sécuriser les agents IA : Leçons tirées du trading haute fréquence

L'essor des systèmes d'IA agentiques, capables d'actions autonomes et complexes, présente des risques systémiques similaires à ceux du trading haute fréquence (HFT). Pour éviter des défaillances en cascade ou des « flash crashs » numériques, l'architecture de sécurité doit passer d'un simple filtrage de sortie à des contrôles déterministes robustes.

**Points clés :**
*   **Risque de vélocité et d'agence :** Contrairement aux chatbots, les agents opèrent des workflows multi-étapes qui exigent une supervision en temps réel.
*   **Gouvernance :** Il est impératif d'adopter des cadres rigoureux (type AARM ou OWASP Top 10 pour les applications agentiques) pour isoler l'exécution des actions.
*   **Approche « Market Access » :** La sécurité doit être architecturale et immuable, et non basée sur le raisonnement probabiliste de l'IA elle-même.

**Vulnérabilités et risques associés :**
*   **Défaillance par rétroaction multi-agents :** Risque de boucles de rétroaction où la sortie d'un agent devient une entrée malveillante pour un autre, créant des spirales imprévisibles.
*   **Erreurs de déploiement (type Knight Capital) :** Désynchronisation entre serveurs distribuant des logiques ou des outils obsolètes.
*   **Dépendance au « Human-in-the-loop » (HITL) :** Risque de contournement des sécurités par un opérateur humain qui valide aveuglément des transactions bloquées sans comprendre le contexte de l'alerte.

**Recommandations de sécurité :**
*   **Passerelles pré-exécution :** Valider les actions critiques via des enveloppes de sécurité déterministes, sans se reposer sur une autre IA pour juger l'action.
*   **Disjoncteurs (Circuit Breakers) :** Imposer des limites codées en dur (dépenses maximales, privilèges temporels) qui contournent la logique interne de l'agent.
*   **Isolement total (« Kill Switch ») :** En cas d'anomalie, isoler le processus au niveau réseau et conteneur plutôt que de simplement révoquer des jetons d'authentification.
*   **Audit « Drop-Copy » :** Répliquer en temps réel toutes les actions dans un stockage immuable (WORM) inaccessible à l'agent.
*   **Infrastructure immuable :** Garantir la cohérence des versions et des prompts sur l'ensemble des nœuds de l'essaim d'agents pour éviter des comportements divergents.
*   **Contexte décisionnel :** Fournir aux opérateurs humains des bundles de contexte explicatifs lorsqu'un disjoncteur se déclenche, afin d'éviter une validation précipitée.

---
[Source](https://www.philvenables.com/post/high-frequency-trading-and-lessons-for-agentic-ai){:target="_blank"}
