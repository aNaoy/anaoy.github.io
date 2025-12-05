---
title: 'RTCon: Context-Adaptive Function-Level Fuzzing for RTOS Kernels (to appear)'
date: 2025-12-05
permalink: /posts/2025/12/05/rtcon-context-adaptive-function-level-fuzzing-for-rtos-kernels-to-appear/
tags:
- veille-cyber
- zerodaysfans
---
**RTCon : Une approche d'analyse contextuelle pour la détection de vulnérabilités dans les noyaux RTOS**

Une nouvelle méthode d'analyse de sécurité, appelée RTCon, est proposée pour identifier les failles dans les noyaux des systèmes d'exploitation temps réel (RTOS). Cette technique adopte une approche d'analyse dynamique, où la recherche de vulnérabilités s'adapte au contexte d'exécution des fonctions analysées. Plutôt que d'appliquer des scénarios d'attaque génériques, RTCon utilise des informations contextuelles pour guider le processus de fuzzing, le rendant ainsi plus efficace.

**Points Clés :**

*   **Analyse Adaptative :** RTCon ajuste son approche d'analyse en fonction du contexte dans lequel les fonctions du RTOS sont appelées et exécutées.
*   **Fuzzing Contextuel :** La méthode exploite les informations sur l'état et les interactions des fonctions pour générer des entrées de test plus pertinentes.
*   **Efficacité Améliorée :** L'adaptation au contexte vise à découvrir des vulnérabilités qui pourraient échapper aux méthodes de fuzzing traditionnelles.

**Vulnérabilités Détectées (Exemples potentiels non spécifiques dans l'extrait) :**

L'article se concentre sur la méthodologie et sa capacité à découvrir des vulnérabilités. Bien que des CVE spécifiques ne soient pas mentionnés dans cet extrait, la méthode est conçue pour identifier des défauts tels que :

*   Dépassements de tampon (Buffer overflows)
*   Erreurs de gestion de mémoire (Use-after-free, double-free)
*   Conditions de course (Race conditions)
*   Problèmes de synchronisation

**Recommandations :**

*   **Adoption de RTCon :** Les développeurs de RTOS devraient considérer l'adoption de RTCon pour améliorer la sécurité de leurs noyaux.
*   **Tests de Sécurité Continus :** Intégrer RTCon dans les cycles de développement et de test pour une détection précoce des vulnérabilités.
*   **Analyse Approfondie :** Utiliser cette méthode pour sonder en profondeur les fonctions critiques et sensibles du RTOS.

---
[Source](https://kaist-hacking.github.io/publication/lee-rtcon/){:target="_blank"}
