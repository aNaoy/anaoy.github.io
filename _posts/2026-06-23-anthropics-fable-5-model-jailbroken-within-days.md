---
title: 'Anthropic’s Fable 5 Model Jailbroken Within Days'
date: 2026-06-23
permalink: /posts/2026/06/23/anthropics-fable-5-model-jailbroken-within-days/
tags:
- veille-cyber
- schneier
---
### Vulnérabilité précoce du modèle Fable 5 d'Anthropic

Le modèle d'intelligence artificielle « Fable 5 » d'Anthropic a été victime d'un *jailbreak* (contournement des restrictions de sécurité) seulement quelques jours après sa mise en service. Cet incident illustre la fragilité des mesures de protection (« safety classifiers ») face à la détermination des chercheurs en sécurité et des utilisateurs malveillants.

**Points clés :**
*   **Échec des mesures de sécurité :** Malgré des processus de contrôle qualité approfondis, les garde-fous mis en place par Anthropic ont été rapidement neutralisés.
*   **Le rôle des "Red Teamers" :** L'incident souligne l'efficacité des méthodes de recherche en sécurité non conventionnelles pour trouver des failles imprévues par les développeurs.
*   **Limites de la confiance dans l'IA :** Le débat met en lumière l'illusion de sécurité inhérente aux affirmations selon lesquelles un modèle serait totalement « sûr et sécurisé ».

**Vulnérabilités :**
*   Aucun identifiant CVE n'est associé à cet événement, car il s'agit d'une vulnérabilité liée au **« prompt engineering » malveillant** et au contournement logique des filtres de sécurité, plutôt qu'à une faille logicielle traditionnelle ou une injection de code standard.

**Recommandations :**
*   **Abandonner le dogme du "zéro risque" :** Les concepteurs de modèles d'IA doivent éviter de communiquer sur une sécurité absolue, car celle-ci est techniquement impossible à garantir contre des attaques créatives.
*   **Renforcement itératif :** Intégrer des boucles de rétroaction plus rapides entre les tentatives de *jailbreak* réelles et les mises à jour des filtres de sécurité.
*   **Approche « Zero Trust » pour l'IA :** Traiter les réponses des modèles comme potentiellement non fiables, même après application de filtres, et concevoir des systèmes de surveillance capables de détecter les comportements déviants en temps réel.

---
[Source](https://www.schneier.com/blog/archives/2026/06/anthropics-fable-5-model-jailbroken-within-days.html){:target="_blank"}
