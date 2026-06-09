---
title: 'XBOW tests Anthropics Mythos Preview for offensive security'
date: 2026-06-09
permalink: /posts/2026/06/09/xbow-tests-anthropics-mythos-preview-for-offensive-security/
tags:
- veille-cyber
- bleepingcomp
---
# Évaluation de la sécurité offensive par Anthropic Mythos Preview

XBOW a testé le nouveau modèle d'IA d'Anthropic, **Mythos Preview**, afin d'évaluer ses capacités en cybersécurité offensive. Les tests ont porté sur l'analyse de code source, les tests d'intrusion sur des sites réels, le reverse engineering et la sécurité native.

### Points clés
*   **Performance exceptionnelle en analyse de code :** Le modèle excelle dans la lecture et la compréhension du code source pour identifier des vulnérabilités, surpassant nettement les versions précédentes (Opus 4.6).
*   **Besoin d'interactions réelles :** Bien que puissant en statique, le modèle gagne en efficacité lorsqu'il peut interagir avec des systèmes vivants pour valider si une vulnérabilité théorique est réellement exploitable.
*   **Capacités polyvalentes :** Le modèle démontre une grande pertinence en ingénierie inverse et dans l'analyse de code natif (ex: projet Chromium/V8).
*   **Limites de jugement :** Le modèle adopte une approche parfois trop littérale ou conservatrice, manquant de discernement sur les nuances de sécurité.
*   **Coût élevé :** Avec un coût estimé 5 fois supérieur aux modèles Opus, Mythos Preview n'est pas toujours l'option la plus rentable par rapport à une utilisation prolongée de modèles moins onéreux.

### Vulnérabilités ciblées
Bien qu'aucun identifiant CVE spécifique ne soit cité, les tests ont permis de découvrir de nombreuses vulnérabilités dans des logiciels open source, notamment dans les domaines suivants :
*   Vulnérabilités web exploitables.
*   Bugs de sécurité dans le code natif (ex: V8 sandbox).
*   Problèmes de configuration et de dépendances complexes non détectables par une simple lecture du code.

### Recommandations pour une utilisation efficace
*   **Orchestration hybride :** Ne pas utiliser le modèle isolément. Il doit être intégré à un cadre ("harness") de validation capable de tester les résultats sur des sites réels pour confirmer l'exploitabilité.
*   **Approche multi-modèles :** Ne pas se limiter à un seul modèle. Selon la complexité, il est parfois préférable d'utiliser des modèles moins coûteux sur plusieurs itérations plutôt qu'un seul passage coûteux de Mythos.
*   **Infrastructure de validation :** Puisque le modèle peut être trop rigide, il nécessite des prompts précis et une infrastructure de validation externe pour transformer ses pistes d'analyse en résultats fiables et exploitables.
*   **Focus sur le flux de travail :** Utiliser la puissance de lecture de code de Mythos pour identifier des pistes, puis utiliser des outils d'automatisation pour valider les vulnérabilités dans le déploiement réel.

---
[Source](https://www.bleepingcomputer.com/news/security/xbow-tests-anthropics-mythos-preview-for-offensive-security/){:target="_blank"}
