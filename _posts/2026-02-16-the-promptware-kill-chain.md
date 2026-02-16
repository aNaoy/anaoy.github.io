---
title: 'The Promptware Kill Chain'
date: 2026-02-16
permalink: /posts/2026/02/16/the-promptware-kill-chain/
tags:
- veille-cyber
- schneier
---
### Chaîne d'Attaque "Promptware" : Une Nouvelle Menace pour l'IA

Les modèles linguistiques de grande taille (LLM) sont désormais la cible d'attaques sophistiquées, formant une nouvelle catégorie de logiciels malveillants baptisée "promptware". Contrairement à l'idée reçue d'une simple "injection de prompt", ces attaques s'articulent selon une chaîne en sept étapes, mimant les campagnes de logiciels malveillants traditionnels.

**Points Clés :**

*   **Nature des LLM :** Les LLM traitent indistintement données et instructions, créant une faille architecturale où un contenu malveillant peut être exécuté avec la même autorité qu'une commande système.
*   **Multimodalité :** L'évolution vers des LLM multimodaux élargit la surface d'attaque, permettant de dissimuler des instructions malveillantes dans des images ou des fichiers audio.
*   **Cadre d'Analyse :** Une "chaîne d'attaque promptware" en sept étapes a été proposée pour mieux comprendre et contrer ces menaces.
*   **Stratégie de Défense :** Plutôt que de tenter de corriger l'injection de prompt, il est crucial de se concentrer sur la prévention des étapes ultérieures de la chaîne d'attaque.

**La Chaîne d'Attaque Promptware :**

1.  **Accès Initial :** Le code malveillant pénètre le système. Cela peut être direct (prompt de l'attaquant) ou indirect (instructions malveillantes intégrées dans des données récupérées par le LLM, comme des pages web, emails, ou documents, voire des images/audios pour les modèles multimodaux).
2.  **Escalade de Privilèges (Jailbreaking) :** L'attaquant contourne les garde-fous de sécurité du modèle pour lui faire exécuter des actions normalement interdites, similaire à l'obtention de droits d'administrateur.
3.  **Reconnaissance :** L'attaquant manipule le LLM pour qu'il révèle des informations sur ses capacités et les systèmes connectés. Cette phase a lieu *après* l'accès initial.
4.  **Persistance :** Le promptware s'ancre dans la mémoire à long terme de l'agent IA ou corrompt ses bases de données pour assurer sa pérennité.
5.  **Commande et Contrôle (C2) :** Permet à l'attaquant de modifier le comportement du promptware dynamiquement, le transformant en un cheval de Troie contrôlable.
6.  **Mouvement Latéral :** L'attaque se propage à d'autres utilisateurs, appareils ou systèmes, exploitant l'interconnexion des agents IA pour une diffusion en cascade.
7.  **Action sur l'Objectif :** Réalisation des objectifs malveillants tels que l'exfiltration de données, la fraude financière, ou même l'impact dans le monde physique (ex: exécution de code arbitraire, manipulation d'agents pour transférer des fonds ou vendre des biens à bas prix).

**Vulnérabilités (Exemples Illustrés dans l'Article) :**

*   **"Invitation Is All You Need" :**
    *   **Accès Initial :** Prompt malveillant dans le titre d'une invitation Google Calendar.
    *   **Persistance :** Le prompt était intégré dans un artefact Google Calendar, se conservant dans la mémoire à long terme de l'espace de travail de l'utilisateur.
    *   **Mouvement Latéral :** Le prompt a incité l'Assistant Google à lancer l'application Zoom.
    *   **Action sur l'Objectif :** Diffusion en direct vidéo de l'utilisateur à son insu.
    *   *Note : C2 et reconnaissance non démontrés.*
*   **"Here Comes the AI Worm" :**
    *   **Accès Initial :** Prompt injecté dans un email.
    *   **Persistance :** Le prompt était intégré dans un email, se conservant dans la mémoire à long terme de l'espace de travail de l'utilisateur.
    *   **Mouvement Latéral :** L'assistant IA, une fois compromis, a été incité à exfiltrer des données sensibles lors de la rédaction de nouveaux emails, propageant ainsi l'attaque à de nouveaux clients.
    *   *Note : C2 et reconnaissance non démontrés.*

**Recommandations :**

*   Développer une stratégie de défense approfondie qui anticipe l'accès initial.
*   Se concentrer sur la rupture de la chaîne aux étapes suivantes :
    *   Limiter l'escalade de privilèges.
    *   Restreindre la reconnaissance.
    *   Prévenir la persistance.
    *   Perturber le C2.
    *   Limiter les actions autorisées des agents IA.
*   Adopter une approche de gestion des risques systématique plutôt que de simples corrections réactives.

---
[Source](https://www.schneier.com/blog/archives/2026/02/the-promptware-kill-chain.html){:target="_blank"}
