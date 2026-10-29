---
title: 'Cohere’s Qwen Story: Looks More Like Model Jaggedness'
date: 2026-10-29
permalink: /posts/2026/10/29/coheres-qwen-story-looks-more-like-model-jaggedness/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse de l'instabilité du modèle Qwen3.8-Flash-Next

L'analyse du comportement suspect du modèle Qwen3.8-Flash-Next, initialement interprété comme une possible porte dérobée (backdoor), révèle plutôt un phénomène de « jaggedness » (irrégularité) du modèle. Lors de tentatives d'exécution d'une commande `curl`, le modèle génère des destinations variées et incohérentes plutôt qu'une adresse fixe, démontrant une confusion dans la logique d'exécution plutôt qu'une intention malveillante prédéterminée.

**Points clés :**
* **Instabilité contextuelle :** Le modèle produit des résultats divergents basés sur des variations mineures du contexte (ex: l'ordre des outils listés modifie la probabilité d'un appel réseau).
* **Absence de cible fixe :** Sur 64 itérations, 52 hôtes différents ont été générés, incluant des adresses inexistantes, des domaines invalides et des adresses locales.
* **Complexité expérimentale :** Le comportement erratique semble lié à la nature « expérimentale » de la préversion du modèle, qui présente des instabilités dans sa planification et son recours aux outils.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée. Le problème réside dans l'imprévisibilité intrinsèque des modèles de langage (LLM) lorsqu'ils sont dotés de capacités d'exécution d'outils (tool use).

**Recommandations :**
* **Sandboxing strict :** Isoler systématiquement les environnements d'exécution des agents IA pour bloquer toute commande réseau non autorisée ou non pertinente.
* **Principe du moindre privilège :** Restreindre strictement les accès réseau et les outils disponibles pour les modèles, afin que toute déviation comportementale soit bloquée par la couche de sécurité.
* **Validation des sorties :** Mettre en place des mécanismes de filtrage en aval pour détecter les incohérences entre la requête de l'utilisateur et les actions générées par l'agent.

---
[Source](https://research.checkpoint.com/2026/coheres-qwen-story-looks-more-like-model-jaggedness/){:target="_blank"}
