---
title: 'Bugs that survive the heat of continuous fuzzing'
date: 2025-12-30
permalink: /posts/2025/12/30/bugs-that-survive-the-heat-of-continuous-fuzzing/
tags:
- veille-cyber
- zerodaysfans
---
## Les failles cachées malgré le fuzzing intensif

Même les projets open source les plus matures et les plus audités par des outils comme OSS-Fuzz peuvent encore receler des vulnérabilités critiques. L'article illustre ce fait à travers trois exemples concrets, démontrant que le "fuzzing" seul, bien qu'efficace, nécessite une supervision humaine et des approches plus sophistiquées pour une sécurité optimale.

**Points clés :**

*   **OSS-Fuzz** a trouvé des milliers de bugs, mais la continuité du fuzzing n'est pas une garantie absolue contre les vulnérabilités.
*   Les **statistiques de couverture** sont un indicateur important : des projets comme GStreamer, avec une faible couverture (environ 19%), sont plus susceptibles de cacher des failles malgré un long historique de fuzzing, contrairement à des projets comme OpenSSL ou bzip2.
*   Une **fausse confiance** peut s'installer chez les développeurs une fois qu'un projet est intégré à OSS-Fuzz, ignorant le besoin d'une expertise humaine continue.
*   Les **dépendances externes** sont une source majeure de vulnérabilités non détectées si elles ne sont pas correctement fuzées ou incluses dans le processus.
*   La **partie encodage** des formats de fichiers multimédias est souvent moins explorée par le fuzzing que la partie décodage, ce qui peut laisser des vulnérabilités passer inaperçues.
*   Le fuzzing traditionnel peut avoir du mal à détecter les bugs nécessitant de **très grandes entrées** ou des **temps d'exécution longs**.

**Vulnérabilités identifiées (avec CVE si mentionné) :**

*   **GStreamer :** 29 nouvelles vulnérabilités découvertes en décembre 2024, dont plusieurs à haut risque. (Pas de CVE spécifique mentionné dans cet extrait pour GStreamer).
*   **Poppler :** Une vulnérabilité "1-click RCE" (Remote Code Execution) affectant Evince, due à une dépendance externe non fuzée (DjVuLibre). (Pas de CVE spécifique mentionné pour cette vulnérabilité Poppler/DjVuLibre).
*   **Exiv2 :**
    *   CVE-2024-39695
    *   CVE-2024-24826
    *   CVE-2023-44398
    *   CVE-2025-26623
    *   CVE-2025-54080
    Ces vulnérabilités sont apparues malgré une inscription à OSS-Fuzz depuis plus de trois ans, souvent liées à la partie encodage.

**Recommandations et Approches Améliorées :**

L'article propose un "workflow de fuzzing en cinq étapes" pour aller au-delà des limites actuelles :

1.  **Préparation du code :** Optimiser le code cible pour le fuzzing (supprimer les checksums, réduire le hasard, etc.).
2.  **Amélioration de la couverture code :** Viser une couverture supérieure à 90%. Cela implique d'écrire de nouveaux "fuzzing harnesses" et de créer des cas d'entrée spécifiques. Il est crucial de fuzer aussi bien les vecteurs d'attaque évidents que ceux moins évidents (encodage, fonctions d'écriture). Les techniques avancées comme l'**injection de fautes** (simuler des erreurs comme des allocations mémoire échouées, des lectures/écritures interrompues) et le **snapshot fuzzing** (capturer l'état du programme pour des tests répétés) sont recommandées.
3.  **Amélioration de la couverture contextuelle :** Au-delà de la couverture par arêtes (edges), utiliser des approches comme la **couverture de branche sensible au contexte** ou la **couverture N-Gram de branche** qui prennent en compte l'ordre d'exécution des blocs de code. Une couverture de 60% peut être considérée comme bonne dans ce cas.
4.  **Amélioration de la couverture de valeurs :** Guider le fuzzing non seulement par les chemins d'exécution, mais aussi par les **plages de valeurs que les variables peuvent prendre**. Cela nécessite des mécanismes pour faire varier les valeurs des variables contrôlées par l'entrée et atteindre des états critiques (ex: division par zéro). Des méthodes comme le "bucketting" peuvent aider à gérer la complexité.
5.  **Tri (Triage) :** Analyser les résultats du fuzzing.

Pour les bugs difficiles à détecter (grands fichiers d'entrée, longs temps d'exécution), des méthodes alternatives comme l'analyse statique, les tests "concolic" (symbolique + concret) ou la revue manuelle de code sont nécessaires, car les fuzzers actuels ont du mal à les identifier. Le fuzzing n'est pas une solution autonome, mais un outil puissant nécessitant une expertise humaine continue.

---
[Source](https://github.blog/security/vulnerability-research/bugs-that-survive-the-heat-of-continuous-fuzzing/){:target="_blank"}
