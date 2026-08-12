---
title: 'Prompt Injections for Defense'
date: 2026-08-12
permalink: /posts/2026/08/12/prompt-injections-for-defense/
tags:
- veille-cyber
- schneier
---
### Le « Context Bombing » : Retourner les injections de prompt contre les agents IA

Des chercheurs de Tracebit ont mis au point une technique défensive innovante baptisée « context bombing » pour neutraliser les agents IA malveillants. En dissimulant des injections de prompt spécifiques au sein de données sensibles (mots de passe, clés cryptographiques), il est possible de forcer une IA attaquante à outrepasser ses propres garde-fous.

**Points clés :**
*   **Mécanisme :** L'insertion de commandes interdites (ex: demandes de création de substances illégales ou sujets politiquement sensibles) dans des fichiers ciblés par une IA provoque un conflit interne dans le modèle.
*   **Réaction de l'IA :** Face à ces instructions proscrites par ses filtres de sécurité, l'agent IA se bloque, mettant fin à l'attaque.
*   **Efficacité :** Cette méthode permet de protéger les données stockées sur des plateformes comme AWS contre le siphonnage automatisé.

**Vulnérabilités :**
*   Aucun identifiant CVE n'est associé à cette technique, car il s'agit d'une vulnérabilité intrinsèque au fonctionnement des LLM (gestion du contexte et des politiques de sécurité).

**Recommandations et limites :**
*   **Limitation critique :** Cette défense ne fonctionne que contre les modèles dotés de garde-fous (guardrails).
*   **Risque émergent :** La montée en puissance des modèles d'IA exécutés localement, dépourvus de filtres de sécurité, rend cette stratégie défensive inopérante face aux attaquants utilisant des modèles personnalisés ou "jailbreakés".

---
[Source](https://www.schneier.com/blog/archives/2026/08/prompt-injections-for-defense.html){:target="_blank"}
