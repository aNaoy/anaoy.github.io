---
title: 'Why More Analysts Won’t Solve Your SOC’s Alert Problem'
date: 2026-05-08
permalink: /posts/2026/05/08/why-more-analysts-wont-solve-your-socs-alert-problem/
tags:
- veille-cyber
- bleepingcomp
---
### Repenser le SOC : l'automatisation plutôt que l'augmentation des effectifs

Le modèle opérationnel actuel des SOC, fondé sur l'intervention humaine pour le tri des alertes, est devenu inefficace face à l'explosion du volume de données et à la rapidité des attaques modernes. Recruter davantage d'analystes ne résout pas le problème structurel du « goulot d'étranglement » de la file d'attente.

**Points clés**
*   **Déséquilibre opérationnel :** Le temps de « breakout » (temps entre l'accès initial et l'exfiltration) a chuté drastiquement (moyenne de 29 minutes), rendant le tri humain manuel obsolète.
*   **Dette opérationnelle :** La suppression de règles de détection jugées trop bruyantes sans remplacement technique crée des angles morts sécuritaires.
*   **Modèle basé sur l'IA :** Les SOC performants délèguent désormais les tâches répétitives et les investigations complexes à des agents d'IA, permettant une réduction drastique du temps d'investigation (quelques minutes au lieu de plusieurs heures).
*   **Économies indirectes :** L'utilisation de l'IA pour traiter les données directement à la source réduit les besoins de stockage et d'ingestion coûteux dans les SIEM.

**Diagnostic du SOC (4 questions essentielles)**
1. Quel pourcentage des alertes a été réellement investigué le trimestre dernier ? (Si < 90 %, il y a un risque caché).
2. Combien de règles ont été supprimées sans remplacement technique ?
3. Quel est le taux de rotation des analystes seniors (la perte de savoir-faire est un point de rupture critique) ?
4. Quelle activité serait abandonnée en priorité si le volume d'alertes doublait ? (Cette tâche est le point faible actuel).

**Recommandations et limites**
*   **Changement d'architecture :** Prioriser l'implémentation d'une IA capable d'investigation autonome plutôt que d'accroître le nombre d'analystes.
*   **Cas où l'humain reste indispensable :**
    *   **Menaces internes :** Lorsque le contexte humain (ressources humaines, historique relationnel) est plus crucial que les logs.
    *   **Attaques inédites (TTPs) :** Les menaces sans antécédents nécessitent l'expertise de chasseurs de menaces humains.
    *   **Conformité :** Environnements restreints par des règles strictes de souveraineté des données.
*   **Financement :** Exploiter les économies générées par la réduction de l'ingestion SIEM ou réaffecter les budgets de recrutement non pourvus.
*   **Gestion des risques fournisseurs :** Lors de l'adoption d'outils d'IA, exiger la portabilité des données, l'indépendance des scénarios de réponse (runbooks) et des clauses de continuité de service en cas de rachat ou de défaillance du prestataire.

---
[Source](https://www.bleepingcomputer.com/news/security/why-more-analysts-wont-solve-your-socs-alert-problem/){:target="_blank"}
