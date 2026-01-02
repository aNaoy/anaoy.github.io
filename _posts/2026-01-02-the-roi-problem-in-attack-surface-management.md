---
title: 'The ROI Problem in Attack Surface Management'
date: 2026-01-02
permalink: /posts/2026/01/02/the-roi-problem-in-attack-surface-management/
tags:
- veille-cyber
- hackernews
---
**La Mesure Réelle de la Gestion de la Surface d'Attaque**

Les outils de gestion de la surface d'attaque (ASM) promettent une réduction des risques, mais se concentrent souvent sur la quantité d'informations collectées plutôt que sur les résultats concrets. La difficulté à prouver le retour sur investissement (ROI) de l'ASM réside dans la mesure des progrès : l'augmentation du nombre d'actifs découverts et d'alertes générées ne se traduit pas nécessairement par une organisation plus sûre.

Les métriques courantes comme le nombre d'actifs ou de changements ne reflètent pas l'amélioration réelle. Le problème vient d'un décalage entre la visibilité et la réponse. Une efficacité accrue de l'ASM devrait se traduire par une réduction des risques, ce qui est difficile à quantifier avec les méthodes actuelles.

**Points Clés :**

*   L'ASM génère souvent plus d'informations (actifs, alertes) que de preuves de réduction des risques.
*   La mesure actuelle de l'ASM se concentre sur la couverture (combien d'actifs sont connus) plutôt que sur l'efficacité (comment le risque est géré).
*   Les métriques basées sur les entrées (nombre d'actifs) ne montrent pas les résultats (réduction des incidents).
*   La fatigue des alertes, les arriérés de traitement et la confusion sur la propriété des actifs sont des symptômes d'une ASM inefficace.

**Vulnérabilités (non spécifiées dans l'article, mais implicites dans les problèmes de gestion) :**

*   Actifs non répertoriés ou inconnus.
*   Actifs sans propriétaire clair, entraînant des retards de patching et de maintenance.
*   Exposition prolongée des risques.
*   Points d'entrée externes non authentifiés et modifiables.
*   Actifs abandonnés ou obsolètes qui persistent dans la surface d'attaque.

**Recommandations pour un ROI Significatif :**

Pour mesurer efficacement le ROI de l'ASM, il faut se concentrer sur les résultats tangibles de la gestion des risques plutôt que sur la simple visibilité des actifs. Les métriques clés à suivre incluent :

1.  **Temps Moyen pour l'Attribution de la Propriété (Mean Time to Asset Ownership) :** Mesurer la rapidité avec laquelle la propriété d'un actif est clairement identifiée. Un temps plus court indique une meilleure réactivité et une réduction de la fenêtre d'exposition sans responsabilité.
2.  **Réduction des Endpoints Exécutant des Actions d'État Sans Authentification :** Surveiller la diminution du nombre de points d'accès externes qui peuvent modifier l'état d'un système sans nécessiter d'authentification. Une réduction de ces points est un indicateur fort d'une surface d'attaque plus restreinte.
3.  **Délai de Mise Hors Service Après Perte de Propriété (Time to Decommission After Ownership Loss) :** Quantifier la rapidité avec laquelle les actifs sont retirés lorsque la propriété est perdue (par exemple, suite à des changements d'équipe, des dépréciations d'applications, etc.). Cela met en évidence l'hygiène à long terme et l'absence d'actifs oubliés.

En adoptant ces métriques orientées résultats, les organisations peuvent démontrer des progrès réels en matière de gestion de la surface d'attaque, rendant le programme plus défendable et axé sur la diminution effective des risques.

---
[Source](https://thehackernews.com/2026/01/the-roi-problem-in-attack-surface.html){:target="_blank"}
