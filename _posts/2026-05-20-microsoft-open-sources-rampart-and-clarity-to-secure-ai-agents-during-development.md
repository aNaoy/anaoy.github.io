---
title: 'Microsoft Open-Sources RAMPART and Clarity to Secure AI Agents During Development'
date: 2026-05-20
permalink: /posts/2026/05/20/microsoft-open-sources-rampart-and-clarity-to-secure-ai-agents-during-development/
tags:
- veille-cyber
- hackernews
---
### Renforcer la sécurité des agents IA avec RAMPART et Clarity

Microsoft a rendu public deux outils open-source conçus pour intégrer la sécurité dès la phase de conception des agents d'intelligence artificielle :

*   **RAMPART (Risk Assessment and Measurement Platform for Agentic Red Teaming) :** Un framework natif Pytest permettant aux ingénieurs de tester la sécurité des agents pendant leur développement. Il automatise la création de tests pour détecter des comportements indésirables, des régressions ou des exfiltrations de données, en complément de l'outil PyRIT.
*   **Clarity :** Un outil de structuration de projet agissant comme un « partenaire de réflexion ». Il guide les développeurs dans l'analyse des risques et la justification des choix de conception avant même l'écriture du code, afin de prévenir les failles structurelles.

**Points clés :**
*   **Shift-left security :** Déplacer la sécurité en amont du cycle de vie du développement pour réduire les coûts de correction.
*   **Reproductibilité :** Transformer les enseignements des exercices de « Red Teaming » en tests automatisés réutilisables.
*   **Complémentarité :** Alors que PyRIT se concentre sur les tests « boîte noire » post-développement, RAMPART est conçu pour une intégration continue par les ingénieurs.

**Vulnérabilités adressées :**
L'article mentionne spécifiquement les risques liés aux **injections indirectes (cross-prompt injections)**, où des données non fiables provenant de sources externes (emails, fichiers, pages web) manipulent l'agent, ainsi que les problèmes d'accès non autorisés aux outils et les fuites de données. (Aucun identifiant CVE spécifique n'est associé, car il s'agit d'outils de prévention et de détection méthodologique).

**Recommandations :**
*   Utiliser **Clarity** en phase de planification pour valider les hypothèses de conception et documenter les décisions critiques.
*   Intégrer **RAMPART** dans les pipelines de développement pour transformer les scénarios de menace en tests automatisés (« living artifacts »).
*   Privilégier une approche de sécurité continue plutôt qu'une revue de sécurité ponctuelle en fin de cycle.

---
[Source](https://thehackernews.com/2026/05/microsoft-open-sources-rampart-and.html){:target="_blank"}
