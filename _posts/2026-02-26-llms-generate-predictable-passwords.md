---
title: 'LLMs Generate Predictable Passwords'
date: 2026-02-26
permalink: /posts/2026/02/26/llms-generate-predictable-passwords/
tags:
- veille-cyber
- schneier
---
## Génération de Mots de Passe par LLM : Un Risque de Sécurité

L'utilisation de grands modèles de langage (LLM) pour générer des mots de passe pose un problème de sécurité significatif, car ils produisent des identifiants hautement prévisibles et non aléatoires.

**Points Clés :**

*   Les LLM ont du mal à créer des mots de passe véritablement aléatoires.
*   Les mots de passe générés présentent des modèles récurrents et des caractères utilisés de manière inégale.
*   La répétition de caractères est évitée, ce qui va à l'encontre d'une génération aléatoire.
*   Certains caractères spécifiques, comme l'astérisque (*), peuvent être évités par le LLM en raison de leur interprétation dans des formats comme Markdown.
*   Des mots de passe entiers peuvent se répéter fréquemment, compromettant leur caractère unique.

**Vulnérabilités Identifiées :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans cet article. Cependant, la vulnérabilité inhérente réside dans la **prévisibilité des mots de passe générés par LLM**, ce qui les rend susceptibles aux attaques par force brute et aux attaques par dictionnaire.

**Recommandations :**

*   Ne pas utiliser les LLM pour la génération de mots de passe dans des contextes de sécurité.
*   Des solutions dédiées et robustes pour la génération de mots de passe aléatoires doivent être privilégiées.
*   La question de l'authentification des agents autonomes, qui pourraient utiliser des LLM pour créer des comptes, nécessite une réflexion approfondie et des mécanismes de sécurité adaptés.

---
[Source](https://www.schneier.com/blog/archives/2026/02/llms-generate-predictable-passwords.html){:target="_blank"}
