---
title: 'Researchers Uncover Prompt Adware Hidden in OpenAI Codex Jailbreak Toolkit'
date: 2026-11-04
permalink: /posts/2026/11/04/researchers-uncover-prompt-adware-hidden-in-openai-codex-jailbreak-toolkit/
tags:
- veille-cyber
- hackernews
---
### Menace émergente : Le « Prompt Adware » au cœur des agents IA

Des chercheurs ont identifié une nouvelle forme de menace baptisée « prompt adware » au sein d'un kit de jailbreak pour OpenAI Codex, nommé **Haiou**. Ce logiciel malveillant détourne les instructions de confiance d'un agent IA pour insérer de la publicité non sollicitée, illustrant une nouvelle vecteur d'attaque via la chaîne d'approvisionnement des composants d'IA.

**Points clés :**
*   **Mécanisme d'infection :** Haiou modifie les instructions globales de l'agent via le langage naturel pour forcer la réponse de l'IA à inclure la promotion d'une passerelle LLM tierce (zz.aiapi2025[.]top).
*   **Techniques de jailbreak :** Le kit utilise le jeu de rôle et des scénarios de type "Capture The Flag" (CTF) pour contourner les garde-fous de sécurité et installer des outils de test d'intrusion.
*   **Propagation :** Le code malveillant est diffusé via des dépôts GitHub (notamment `haiou-codex` et `Codex-X`), se présentant faussement comme une amélioration de configuration ou un outil de visualisation.
*   **Objectif :** Utiliser les utilisateurs comme canal d'acquisition pour un service payant opaque, tout en exposant potentiellement les entreprises à des comportements indésirables injectés dans leurs agents IA.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle classique (type CVE), mais d'une **vulnérabilité par injection de prompt et manipulation de configuration**. Le danger réside dans la confiance accordée aux instructions système qui, une fois compromises, dictent durablement le comportement de l'agent.

**Recommandations :**
*   **Vigilance sur les composants tiers :** Éviter l'utilisation de configurations, "skills" ou outils d'optimisation IA provenant de sources non vérifiées ou douteuses sur GitHub.
*   **Audit des instructions :** Examiner régulièrement les fichiers de configuration et les instructions globales des agents IA déployés pour détecter l'injection de commandes suspectes.
*   **Approche « Zero Trust » pour l'IA :** Considérer les prompts et les configurations comme des éléments critiques de la chaîne de confiance au même titre que le code exécutable, et soumettre les intégrations d'IA à des contrôles de sécurité rigoureux.

---
[Source](https://thehackernews.com/2026/11/researchers-uncover-prompt-adware.html){:target="_blank"}
